pipeline {
    agent any

    parameters
    {
        string(name: 'reason', description: 'Reason to run the job')
    }

    stages
    {
        stage('Print parameters') {
            steps {
                script {
                    def reason = "${params.reason}"

                    println("Reason: $reason")
                    if (reason.contains("test")) {
                        println("Test mode")
                    } else {
                        println("Production mode")
                    }
                }
            }
        }

        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}