pipeline{
    agent any
    
    stages{
        stage("code"){
            steps{
                git url: "https://github.com/VedThavkar/node-todo-cicd.git"
                echo "Code cloned"
            }
        }
        stage("build and test"){
            steps{
                sh "docker build -t node-app ."
                echo "code builded and tested"
            }
        }
        stage("scan image"){
            steps{
                echo "image scanning ho gayi"
            }
        }
        stage("push"){
            steps{
                echo "deployment ho gayi"
            }
        }
        stage("deploy"){
            steps{
                sh "docker-compose down && docker-compose up -d"
                echo "deployment ho gayi"
            }
        }
    }
}
