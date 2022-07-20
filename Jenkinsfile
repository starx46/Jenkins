def remote = [:]
remote.name = "node"
remote.host = "172.31.88.95"
remote.allowAnyHosts = true

node {
    withCredentials([usernamePassword(credentialsId: 'sshUserAcct', passwordVariable: 'password', usernameVariable: 'userName')]) {
        remote.user = root
        remote.password = root@123

        stage("SSH Steps Rocks!") {
            sshCommand remote: remote, command: 'for i in {1..5}; do echo -n \"Loop \$i \"; date ; sleep 1; done'
           
        }
    }
}
