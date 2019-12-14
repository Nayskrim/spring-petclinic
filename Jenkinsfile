stage('Build') {
    node {
        git url: 'https://github.com/Nayskrim/spring-petclinic.git'
        env.PATH = "${tool 'MAVEN3.3.9'}/bin:${env.PATH}"
        sh 'mvn clean package'
        archiveArtifacts artifacts: '**/target/*.war', fingerprint: true
    }
}
