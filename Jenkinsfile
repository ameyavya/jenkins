node{
    stage 'Download-SCM'
    git 'https://github.com/ameyavya/mavenrepo.git'
    stage 'maven-compile'
    tool name: 'MAVEN-3.5.2', type: 'maven'
    sh 'mvn clean compile package deploy'
}
