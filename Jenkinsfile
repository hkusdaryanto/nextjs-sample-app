pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
		echo 'Cloning the repositories'
		sh 'git clone https://github.com/hkusdaryanto/nextjs-sample-app.git'
                echo 'Installing Dependencies'
                sh 'npm install'
		echo 'Building NextJS App'
		sh './node_modules/next/bin/next build'
		echo 'Running App with Production ENV'
		sh './node_modules/next/bin/next start'
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
