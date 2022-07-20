pipeline {
    agent any
    stages {
        stage('SSH remote') {
            steps {
                 script {
                     def remote = [name: 'test', host: '172.31.88.95', user: 'root', password: "root@123', allowAnyHosts: true]
                     sshCommand remote: remote, command: "for i in {1..5}; do echo -n \"Loop \$i \"; date ; sleep 1; done"
                 }
            }
        }
    }
}
