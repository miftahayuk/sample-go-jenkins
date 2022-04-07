pipeline{
    agent any

    environment{
        root ="go"
        branch="master"
        scmUrl ="https://github.com/miftahayuk/sample-go-jenkins.git"
    }

    stages{
        stage("Go Version"){
            steps{
                sh "${root} version"
            }
        }
        stage("Git Clone"){
            steps{
                git branch: "${branch}", url:"${scmUrl}"
            }
        }
        stage("Go Test"){
            steps{
                sh "${root} test ./... -cover"
            }
        }
        stage("Go Build"){
            steps{
                sh "${root} build ./..."
            }
        }
    }
    
}


