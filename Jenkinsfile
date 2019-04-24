node {
    stage('Example') {
        if (env.BRANCH_NAME == 'master') {
            echo 'I only execute on the master branch'
        } else {
            echo 'I execute elsewhere'
        }
        echo "Test message"
        echo "${GIT_COMMIT}"
        echo "${GIT_PREVIOUS_COMMIT}"
        echo "${GIT_BRANCH}"
        echo "${GIT_URL}"

    }
}
