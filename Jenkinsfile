def remote = [:]
remote.name = "worker-1"
remote.host = "172.31.24.178"
remote.allowAnyHosts = true

node {
    withCredentials([sshUserPrivateKey(credentialsId: 'docker-build', keyFileVariable: 'identity', passphraseVariable: '', usernameVariable: 'userName')]) {
        remote.user = userName
        remote.identityFile = identity
        stage("SSH Steps Rocks!") {
            writeFile file: '/root/abc.sh', text: 'date'
            sshCommand remote: remote, command: 'hostname -i'
            sshPut remote: remote, from: '/root/abc.sh', into: '.'
            sshGet remote: remote, from: '/root/abc.sh', into: 'bac.sh', override: true
            sshScript remote: remote, script: '/rootabc.sh'
            sshRemove remote: remote, path: 'abc.sh'
        }
    }
}
