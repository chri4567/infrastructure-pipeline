properties([pipelineTriggers([githubPush()])])
node('linux') {
    git url: 'https://github.com/chri4567/infrastructure-pipeline.git', branch: 'master'
    stage('Test') {
        sh "env"    }
    stage ("GetInstances") {

    sh "aws ec2 describe-instances --region us-east-1"
}

stage ("CreateInstance") {
    sh "aws ec2 run-instances --image-id ami-013be31976ca2c322 --count 1 --instance-type t2.micro --key-name seis665_devops --security-group-ids sg-fdefd0b1 --subnet-id subnet-41a22f6f --region us-east-1"

}
}
