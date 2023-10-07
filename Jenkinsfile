pipeline {
    agent { label 'linux' }
    stages{
        stage ("Setup") {
            steps {
                script {
                    //sh "mvn dependency:tree -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true"
                    sleep 24s
                }
            }
        }
        stage ("Tests") {
            steps {
                script {
                    //sh "mvn test -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true"
                    sleep 60s
                }
            }
        }
        stage ("Lint or Sonarqube?") {
            steps {
                script {
                    //sh "mvn -X clean install -DskipTests -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true"
                    sleep 45s
                }
            }
        }
        stage ("Jfrog registry") {
            steps {
                script {
                    //sh "mvn -X clean install -DskipTests -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true"
                    sleep 30s
                }
            }
        }
        stage ("Deploy") {
            steps {
                script {
                    //sh "mvn -X clean install -DskipTests -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true"
                    sleep 60s
                }
            }
        }
    }
}