
    pipeline{
    agent any

    stages{
        stage('zip the file'){
            steps{
                sh 'zip ansible-${BUILD_ID}.zip * --exclude Jenkinsfile'
            }
        }
        stage('upload artifacts to jfrog'){
            steps{
                sh 'curl -uadmin:AP5RB9x5AQha5vBcX7VG1sxdMDb -T  \
                 *ansible-${BUILD_ID}.zip "http://100.25.180.250:8081/artifactory/ansible-repo/ansible-${BUILD_ID}.zip"'
            }
        }
    }
}