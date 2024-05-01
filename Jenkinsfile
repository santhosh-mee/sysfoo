pipeline {
    agent any
    stages {
        stage('Step 1 Packaging') {
            steps {
		echo "Packaging"
              sh "mvn clean package"
            }
        }
		stage('Step 2 archive artifacts') {
            steps {
             archiveArtifacts artifacts: '**/*.war', fingerprint: true
            }
        }
}
}
