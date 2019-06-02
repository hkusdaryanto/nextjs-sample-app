pipeline {
    agent {
		docker {
			image: 'alpine:6-alpine'
			args: '-p 3000:3000'
	}

    } 

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
