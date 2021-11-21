pipeline { 
agent any
    stages {
        stage('clone the repository') {
            steps {
                git 'https://github.com/masterchief01/init-jenkins'
            }
        }
        stage('exec main') {
            steps {
		sh "chmod u+x main.py"
                sh "python3 main.py"
            }
        }
     stage('run tests') {
            steps {
		sh "chmod u+x spec.py"
                sh "python3 spec.py"
            }
        }
    } 
}
