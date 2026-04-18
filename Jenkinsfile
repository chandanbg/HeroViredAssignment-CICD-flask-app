pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo "Installing dependencies........."
                sh 'python3 -m venv venv'
                sh '. venv/bin/activate && pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests...1"
                sh '. venv/bin/activate && pytest'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying to staging..."
		echo "auto-deploy working"
                sh 'nohup python3 app.py &'
            }
        }
    }
    
    post {
        success {
            mail to: 'chandan.bgc@gmail.com',
                 subject: 'Jenkins Build SUCCESS',
                 body: 'Build completed successfully!'
        }
        failure {
            mail to: 'chandan.bgc@gmail.com',
                 subject: 'Jenkins Build FAILED',
                 body: 'Build failed. Check Jenkins logs.'
        }
    }
}
