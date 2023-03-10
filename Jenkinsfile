pipeline {
    agent any
    stages {
        stage('readjson') {
            steps {
                script {
                    def jstring = '{"one":1, "two":2}'
                    def jobj = readJSON text: jstring
                    echo jobj.toString()
                }
            }
        }
    }
} 
