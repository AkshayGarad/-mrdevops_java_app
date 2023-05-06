@Library('my-shared-library') _

pipeline{
    agent any

    parameters{
        choice(name: 'action', choice: 'create\ndelete', description: create/destroy)
    }

    stages{

        when { expression {param.action == 'create'}}
        stage('Git Checkout'){
            steps{
                script{
                    gitCheckout(
                        branch: "main",
                        url: "https://github.com/AkshayGarad/mrdevops_java_app.git"
                    )
                }
            }
        }

        stage('Unit Test maven'){

            when { expression {param.action == 'create'}}
            steps{
                script{
                    mvnTest()
                }     
            }
        }

        stage('Integration Test maven'){

            when { expression {param.action == 'create'}}
            steps{
                script{
                    mvnintergrationTest()
                }     
            }
        }

    }
}