node {
   stage('Checkout') {
            steps {
                sh 'printenv'
                checkout scm: [$class: 'GitSCM', branches: [[[name: '*/development']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [url: 'https://github.com/s-lavr/pipeline-jenkins.git']]]
                sh 'git submodule foreach --recursive \'git submodule sync\''
                sh 'git submodule update --init --recursive'
                sh 'printenv'

            }
        }
}
