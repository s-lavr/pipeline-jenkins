node {
    checkout(scm).each { k,v -> env.setProperty(k, v) }
    sh 'printenv'
    stage('Example') {
    if (env.GIT_BRANCH == 'master') {
        echo "Image tag is ${env.GIT_BRANCH}-${env.GIT_COMMIT}"
    } else {
        echo "Image tag is ${env.GIT_BRANCH}"
    }
    sh "git tag"
    if (env.TAG_NAME!=Null){
    echo "Hello, Tag exists"
    }
    echo 'Test message 123'
    }
}


