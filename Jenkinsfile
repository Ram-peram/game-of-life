node{
    stage('scm') {
    
    git 'https://github.com/wakaleo/game-of-life.git'
    
    }
    stage('build & package')
    {
        bat 'mvn package'
    }
   stage('results')
{
   archiveArtifacts 'gameoflife-web\\target\\gameoflife.war'
   junit 'gameoflife-web\\target\\surefire-reports\\*.xml'
}
}