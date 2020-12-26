pipeline {
    agent any

    stages {
        stage('Verfify Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }   
        stage('Docker build') {
            steps {
                sh(script:  'sudo docker images -a')
				sh(script: """
				cd voting-app/
				sudo docker iamges -a
				sudo docker built -t jenkins-pipeline .
				sudo docker images -a 
				cd ..
				""")
            }
        }    
    }
}
