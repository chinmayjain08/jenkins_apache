pipeline{
    agent any
    stages{
        stage('checkout'){
            steps{
                git url='github.com/chinmayjain08/jenkins_apache' branch='main'
            }
        }
        stage('deploy'){
            steps{
                sh '''
                  rm -rf /var/www/html
                  cp -r website/* var/www/html
                '''
            }
        }
    }
    post{
        success{
            echo "Success"
        }
        failure{
            echo "Failed"
        }
    }
}
