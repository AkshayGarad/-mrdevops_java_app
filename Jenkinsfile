@Library('my-shared-library') _

pipeline{
    agent any

    stages{
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

        stage('Unit Test Maven'){
            steps{
                script{
                    mvnTest(
                        branch: "main",
                        url: "https://github.com/AkshayGarad/mrdevops_java_app.git"
                    )
                }
            }
        }


    }
}