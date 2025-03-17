pipeline {

    agent any

    stages {
	stage('Install Dependencies') {
            steps {
                sh '''
		    sudo apt install python3.12-venv -y
                    python3 -m venv venv -y # Create virtual environment
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
