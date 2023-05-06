pipeline{
    agent any

    stages{
        stage('Git Checkout'){
            steps{
                script{
                    git branch: 'main', url: 'https://github.com/AkshayGarad/mrdevops_java_app.git'
                }
            }
        }
    }
}