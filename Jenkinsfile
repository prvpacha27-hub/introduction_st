pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Checkout jenkins file') {
            steps {
                checkout scm
            }
        }
        stage('Checkout java code') {
          steps {
            deleteDir()
            git branch: 'master',
                //    credentialsId: 'github-creds',
                url: 'https://github.com/Prashanthv10/javaparser-maven-sample.git'
            }
        }

        stage('Build') {
            steps {
                sh 'echo Build step here'
            }
        }
    }
}
