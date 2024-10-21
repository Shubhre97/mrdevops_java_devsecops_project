@Library('my-first-shared-library') _

pipeline{
    agent any
    parameters{

        choice(name: 'action', choices: 'create\ndelete', description: 'Choose create/Destroy')
    }

    stages{
        stage('Git Checkout'){
            when { expression {  params.action == 'create' } }
            steps{          
                gitCheckout(
                branch: "main", 
                url: "https://github.com/Shubhre97/mrdevops_java_devsecops_project.git"
                )               
            }
        }
        stage('Unit Tests Maven'){
            when { expression {  params.action == 'create' } }
            steps{
                script{
                    mvnTest()
                }    
            }
        }
        stage('Integration Tests Maven'){
            when { expression {  params.action == 'create' } }
            steps{
                script{
                    mvnIntegrationTest()
                }    
            }
        }
    }
}