node {
    checkout(scm).each { k,v -> env.setProperty(k, v) }
    sh 'printenv'
    stage('Example') {
    if (env.GIT_BRANCH == 'master') {
        echo "Image tag is ${env.GIT_BRANCH}-${env.GIT_COMMIT}"
    } else {
        echo "Image tag is ${env.GIT_BRANCH}"
    }
    when { tag "*" }
    echo 'Test message'
    }
}


