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
