pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Installing Dependencies'
                sh 'npm install'
		echo 'Building NextJS App'
		sh 'node_modules/next/dist/bin/next build'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
