Jenkinsfile (Declarative Pipeline)
pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') {
            steps {
               checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'Prashanthi', url: 'https://github.com/prashanthiazuredevops/Java_Code.git']])
            }
        stage('Build') {
            steps {
                build 'Java'
            }
        }
        stage('Test') {
            steps {
                warnError('Warn Errors') {
                // some block
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
}
