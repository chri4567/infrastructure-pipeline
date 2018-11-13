properties([pipelineTriggers([githubPush()])])
node('linux') {
    git url: 'https://github.com/chri4567/infrastructure-pipeline.git', branch: 'master'
    stage('Test') {
        sh "env"    }
}
