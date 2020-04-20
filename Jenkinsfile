peline {
    agent any
   
   stages {
       stage ('Start') {
      steps {         
          slackSend channel: 'infra-amine', color: 'warning', message: 'started', teamDomain: 'alanies', tokenCredentialId: 'salck-demo'
        }
       }
       stage('clone') {
           steps {
               //sh "rm -rf *"
               //sh "git clone https://github.com/aminespankes/exemple-jenkins.git"
               echo"CLONE DONE!"
           }
       }
       stage('build') {
           steps {
               //sh "cd /var/lib/jenkins/workspace/pipelinexemple2/exemple-jenkins/src/"
               echo "BUILD DONE!"
           }
       }
       stage('run') {
           steps {
                //sh "cd /var/lib/jenkins/workspace/pipelinexemple2/exemple-jenkins/src/"
                echo "ARE YOU READY!"
           }
       }
       
}
post {
    success {        
        slackSend channel: '#infra-amine', color: 'good', message: 'done ', teamDomain: 'alanies', tokenCredentialId: 'salck-demo'
    }

    failure {   
        slackSend channel: 'infra-amine', color: 'danger', failOnError: true, message: 'error', teamDomain: 'alanies', tokenCredentialId: 'salck-demo'
    }
  }
}
