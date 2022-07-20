pipeline {
    agent any
    stages {
        parameters {
                 choice choices: ['production'], name: 'branch'
                        }
        stage('Example Build') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Example Deploy') {
            when {
                branch 'production'
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}
