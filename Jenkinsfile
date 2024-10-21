@Library('my-first-shared-library') _

pipeline{
    agent any

    stages{
        stage('Git Checkout'){
            steps{          
                gitCheckout(
                branch: "main", 
                url: "https://github.com/Shubhre97/mrdevops_java_devsecops_project.git"
                )               
            }
        }
        stage('Unit Tests Maven'){
            steps{
                script{
                    mvnTest()
                }    
            }
        }
    }
}