node {
    checkout(scm).each { k,v -> env.setProperty(k, v) }
    sh 'printenv'
    stage('Example') {
    if (env.GIT_BRANCH == 'master') {
        echo "Image tag is ${env.GIT_BRANCH}-${env.GIT_COMMIT}"
    } else if (env.TAG_NAME) {
        echo "Hello, Tag exists, it's ${env.TAG_NAME}"
    } else if (env.CHANGE_ID) {
        echo "This is Pull Request"
    } else {
        echo "Image tag is ${env.GIT_BRANCH}"
    }
}

}
