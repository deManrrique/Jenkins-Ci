pipeline {
    agent any

    stages {
        stage('Crear Carpeta') {
            steps {
                script {
                    sh 'mkdir -p ~/mi_carpeta_kokito'
                }
            }
        }

        stage('Crear Archivo') {
            steps {
                script {
                    sh 'echo "Te amo kokito te amo chipita, tu sabes que te amo" > ~/mi_carpeta_kokito/archivo.txt'
                }
            }
        }

        stage('Asignar y Mostrar Hora') {
            steps {
                script {
                    def variable = sh(script: 'date +"%H:%M"', returnStdout: true).trim()
                    sh "echo 'La hora actual es: $variable' >> ~/mi_carpeta_kokito/archivo.txt"
                }
            }
        }
    }
}
