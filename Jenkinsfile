pipeline {
    agent any

    stages {
        stage('code clone') {
            steps {
               git credentialsId: '7a209082-6d25-48ff-ac02-12895a741803', url: 'https://github.com/saikumarbaddapuri10/car-prediction.git'
            }
        }
       
        stage('build image') {
            steps {
               script{
                   sh "pip3 install -r requirements.txt"
               }
            }
        }
        stage('build container') {
            steps {
               script{
                   sh "screen -m -d python3 app.py"
               }
            }
        }
    }
}
