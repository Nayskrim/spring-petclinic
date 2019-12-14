stage('Build') {
    node {
        git url: 'https://github.com/Nayskrim/spring-petclinic.git'
        env.PATH = "${tool 'Maven-3.6.1'}/bin:${env.PATH}"
        sh 'mvn clean package'
        archiveArtifacts artifacts: '**/target/*.war', fingerprint: true
    }
}
