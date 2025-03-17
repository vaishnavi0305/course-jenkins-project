pipeline {

    agent any

    stages {
	stage('Install Dependencies') {
            steps {
                sh '''
		    sudo apt install python3.12-venv -y
                    python3 -m venv .venv # Create virtual environment
                    bash -c "source .venv/bin/activate && pip install --upgrade pip && pip install -r requirements.txt"
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''
			bash -c "source .venv/bin/activate && pytest"
		'''
                
            }
        }    
                    
    }
}
