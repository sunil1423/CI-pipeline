pipeline {
    agent any
 
    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building application...'
                
            }
        }
        stage('Run Tests') {
            steps {
                echo 'Running tests...'
                
            }
        }
        stage('Publish Artifacts') {
            steps {
                echo 'Publishing artifacts...'
                
            }
        }
    }
 
    pipeline {
    agent any
 
    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building application...'
                // Add build commands here (e.g., Maven, Gradle, NPM)
            }
        }
        stage('Run Tests') {
            steps {
                echo 'Running tests...'
                // Add test commands (e.g., unit tests)
            }
        }
        stage('Publish Artifacts') {
            steps {
                echo 'Publishing artifacts...'
                // Push artifacts to Docker, Nexus, JFrog, or S3
            }
        }
    }
 
    post {
            success {
                echo "CI Pipeline executed successfully for ${BRANCH_NAME} branch"
		build job: "MultiBranch-CD-Pipeline(SL)/${BRANCH_NAME}", wait: true
            }
 
            failure {
                echo "CI Pipeline execution failed for ${BRANCH_NAME} branch"
            }
        }
    }
}
