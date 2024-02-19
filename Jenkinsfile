pipeline {
    agent any

    stages {
        stage('Create Remote File') {
            steps {
                script {
                    // SSH configuration
                    def remoteServer = '172.16.185.130'  // IP address or hostname of your remote server
                    def remoteUser = 'ali123'      // Username for SSH login
                    def remotePwd = 'ali123'     // Password for SSH login (or use SSH key)

                    // SSH command to create a file on the remote server
                    sh "sshpass -p '${remotePwd}' ssh ${remoteUser}@${remoteServer} 'echo \"This is a test file created by Jenkins\" > //home/ali123/new_ssh/newfile.txt'"
                }
            }
        }
    }
}
