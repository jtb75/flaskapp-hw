node {
        stage('Clone') {
            echo 'Cloning Repo..'
            sh """
            git clone https://github.com/jtb75/flaskapp-hw.git
            cd flaskapp-hw
            """
        }
        stage ('Cleanup') {
            echo 'Cleaning up Image..'
            sh """
            docker rmi webapps/flaskapp-hw:$BUILD_NUMBER
            docker rmi webapps/flaskapp-hw:latest
            """
        }
}
