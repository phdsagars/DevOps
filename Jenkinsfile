node {

checkout([$class: 'GitSCM', branches: [[name: '*/master']], 
doGenerateSubmoduleConfigurations: false, 
extensions: [], 
submoduleCfg: [], 
userRemoteConfigs: [[url: 'https://github.com/phdsagars/DevOps.git']]])


sh 'mvn clean package'

archiveArtifacts 'target/Helloworldwebapp_ChangedFromBASH.war'

sh '''sudo cp target/Helloworldwebapp_ChangedFromBASH.war /usr/share/tomcat7-root
sudo service tomcat7 stop
sudo service tomcat7 start'''

}
