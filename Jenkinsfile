node {
    def scmVars = checkout scm
    echo 'scm : the commit id is ' +scmVars.GIT_COMMIT
    stage('Example') {

        //git "https://github.com/s-lavr/pipeline-jenkins.git"
        if (env.BRANCH_NAME == 'master') {
            echo 'I only execute on the master branch'
        } else {
            echo 'I execute elsewhere'
        }

        echo "Test message for Jenkins"
        sh 'printenv'
        echo "${env.GIT_COMMIT}"
        // echo "${GIT_PREVIOUS_COMMIT}"
        // echo "${env.GIT_BRANCH}"
        // echo "${GIT_URL}"

    }
}
