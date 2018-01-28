node{
    stage 'Download-SCM'
    git 'https://github.com/ameyavya/mavenrepo.git'
    stage 'maven-compile'
    tool name: 'MAVEN-3.5.2', type: 'maven'
    sh 'mvn clean compile package deploy'
    stage 'Env Dev Deployment'
    sh '''
    cd /var/lib/jenkins/ansible
    ansible-playbook -i DEVAPP -u ec2-user --private-key ec2-user.pem STUDENT-DEV-APP-DEPLOY.yml
    '''
}
