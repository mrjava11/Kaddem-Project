pipeline {
    agent {
        label 'vagrant'
    }

    stages {
        
       
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