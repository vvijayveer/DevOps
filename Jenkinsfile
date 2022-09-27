node {
    stage('Gitclone') {
	    git credentialsId: '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', url: 'https://github.com/vvijayveer/Jenkins.git'
	     
    }
    stage('Maven version') {
	  sh 'mvn --version'
      
    }
	stage('Java version') {
	   sh 'java -version'
      
    }
	stage('Maven Validate') {
	  sh 'mvn validate'
      
    }
	
	stage('Sonar Scan')
	{
	sh 'mvn sonar:sonar \
       -Dsonar.host.url=http://192.168.29.29:9000 \
       -Dsonar.login=6c12d406ec033100d2c3ef47f78660ae0daa3b87'	
	}
	
	stage('Maven Compile') {
	   sh 'mvn compile'
      
    }
	stage('Maven Test') {
	  sh 'mvn test'
      
    }
	stage('Maven Package') {
	   sh 'mvn package'
      
    }
	stage('Maven Deploy') {
	   sh 'mvn deploy'
    }
	
}
