pipeline {
    agent {                     
        docker { 
            image 'gcc:9.4.0'
            label 'ubuntu22'
        }
    }
    stages {
        stage('build') {
            steps {
                echo "building"
                sh """
                gcc --version
                """
            }
            steps {
                echo "building"
                sh """
                gcc -o dist/main src/main.c
                """
            }
            steps {
                echo "building"
                sh """
                dist/main
                """
            }
        }      
    }
}
