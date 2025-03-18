pipeline{
    agent any
    stages{
        stage("Check code"){
            steps{
            git branch: 'main',url:"https://github.com/gowtham123K/test.git"
            }
        }
        stage("Install dependencies"){
            steps{
                bat '''
                python -m venv venv
                call venv\\Scripts\\activate
                python -m pip install --upgrade pip
                pip install -r requirements.txt

                '''
            }
        }
        stage("deploy"){
            steps{
                bat '''
                call venv\\Script\\activate
                python helloworld.py
                '''
            }
        }
    }
}
