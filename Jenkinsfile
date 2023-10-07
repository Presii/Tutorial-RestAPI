pipeline {
    agent { label 'linux' }
    stages{
        stage ("Setup") {
            steps {
                script {
                    //sh "mvn dependency:tree -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true"
                    sleep 24
                }
            }
        }
        stage ("Tests") {
            steps {
                script {
                    //sh "mvn test -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true"
                    sleep 60
                }
            }
        }
        stage ("Lint or Sonarqube?") {
            steps {
                script {
                    //sh "mvn -X clean install -DskipTests -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true"
                    sleep 45
                }
            }
        }
        stage ("Jfrog registry") {
            steps {
                script {
                    //sh "mvn -X clean install -DskipTests -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true"
                    sleep 30
                }
            }
        }
        stage ("Deploy") {
            steps {
                script {
                    //sh "mvn -X clean install -DskipTests -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true"
                    sleep 60
                }
            }
        }
    }
}