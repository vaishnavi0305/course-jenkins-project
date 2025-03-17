pipeline {

    agent any

    stages {
	stage('Install Dependencies') {
            steps {
                sh '''
		    apt install python3.12-venv
                    python3 -m venv venv  # Create virtual environment
                    source venv/bin/activate  # Activate it
                    pip install --upgrade pip  # Upgrade pip inside venv
                    pip install -r requirements.txt  # Install dependencies
                '''
            }
        }
        stage('Test') {
            steps {
                sh "pytest"
                
            }
        }    
                    
    }
}
