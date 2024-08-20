pipeline {
    agent {                     
        docker { 
            image 'gcc:9.4.0'
            label 'ubuntu-22.04'
        }
    }
    stages {
        stage('build') {
            steps {
                echo "building"
                sh """
                gcc --version
                """
                sh """
                gcc -o main src/main.c
                """
                sh """
                ./main
                """
            }
        }      
    }
}

