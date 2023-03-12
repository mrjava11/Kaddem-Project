pipeline {
    agent {
        label 'vagrant'
    }

    stages {
        stage('SonarQube analysis') {
            steps {
                // Run SonarQube analysis ozdozjdozjdozjdo
                withSonarQubeEnv('sonarqube') {
                    sh 'mvn sonar:sonar -Dsonar.projectKey=tn.esprit:KaddemProject -Dsonar.host.url=http://localhost:9000 -Dsonar.login=50373cb03e7e7ad7fda38f55f5fa7fbe74a049a4'
                }
            }
        }
       
        stage("Build") {
            steps {
                sh "mvn -version"
                sh "mvn clean package -DskipTests"
            }
        }

        // stage("Sonar") {
        //     steps {
        //         bat "mvn sonar:sonar"
        //     }
        // }
        
        // stage("SRC Analysis Testing") {
        //     steps {
        //         bat "mvn sonar:sonar"
        //     }
        // }
        
        // stage("Build Docker image") {
        //     steps {
        //         sh "sudo docker build -t app-devops ."
        //     }
        // }
        
        // stage("down Docker compose") {
        //     steps {
        //         sh "sudo docker compose down"
        //     }
        // }
        
        // stage("run Docker compose") {
        //     steps {
        //         sh "sudo docker compose up -d"
        //     }
        // }
        
        // stage('Spin Up Receiver') {
        //     agent any
        //     steps {
        //         script { 
        //             def receiver = docker.build("receiver",  "--rm receiver_docker")
        //             receiver_container = receiver.run("-d -u 0:0 -v /var/lib/jenkins/workspace/RsyncRealtime/jenkins_rt:/DSK1/SSN/LOG5_F/17191 --network='rsync_test' --name='test_receiver'")
        //         }
        //     }
        // }

        // stage("Deploy Artifact to private registry") {
        //     steps {
        //         sh "..............."
        //     }
        // }

        // stage("Deploy Dokcer Image to private registry") {
        //     steps {
        //         sh "..............."
        //     }
        // }
    }
   
    post {
        always {
            cleanWs()
        }
    }
    
}