pipeline {
    agent { label 'linux' }
    stages{
        stage ("Setup") {
            steps {
                script {
                    sh "mvn dependency:tree -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true"
                }
            }
        }
        stage ("Tests") {
            steps {
                script {
                    sh "mvn test -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true"
                }
            }
        }
        stage ("Build") {
            steps {
                script {
                    sh "mvn -X clean install -DskipTests -Dmaven.wagon.http.ssl.insecure=true -Dmaven.wagon.http.ssl.allowall=true"
                }
            }
        }
    }
}