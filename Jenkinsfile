pipeline {
	
	agent any
	environment {
		branch = 'master'
		scmUrl = 'https://github.com/hkusdaryanto/nextjs-sample-app.git'
		developmentServer = 'www-dev.giggedin.com'
		stagingServer = 'www-staging.giddedin.com'
		productionServer = 'www-prod.giggedin.com'
	}	
	
    stages {
        stage('build') {
            steps {
                echo 'Installing Dependencies'
                sh 'npm install'
				echo 'Building NextJS App'
				sh 'node_modules/next/dist/bin/next build'
            }
        }
        stage('deploy development') {
            steps {
                echo 'Deploy Development'
            }
        }
        stage('deploy staging') {
            steps {
                echo 'Deploy Staging'
            }
        }
		stage('deploy production') {
			steps {
				echo 'Deploy Production'
			}
		}
    }
	post {
		failure {
			mail to: 'henry.kusdaryanto@gmail.com', subject: 'Pipeline failed', body: "${env.BUILD_URL}"
		}
	}
}
