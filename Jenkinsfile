node {
    checkout(scm).each { k,v -> env.setProperty(k, v) }
    sh 'printenv'
    echo $GIT_COMMIT
}


