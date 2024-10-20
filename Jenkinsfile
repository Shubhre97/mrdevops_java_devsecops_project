@Library('my-first-shared-library') _

pipeline{
    agent any

    stages{
        stage('Git Checkout'){
            steps{
                script{
                    gitCheckout{
                    branch: 'main', 
                    url: 'https://github.com/Shubhre97/mrdevops_java_devsecops_project.git'
                    }               
                }
            }
        }
    }
}