node {
    // Clean workspace before doing anything
    deleteDir()

    try {
        stage ('job1') {
            checkout scm
        }
        stage ('job2') {
            sh "echo 'hello.sh'"
        }
       
        stage ('job3') {
            sh "echo 'hello.sh'"
        }
    } catch (err) {
        currentBuild.result = 'FAILED'
        throw err
    }
}
