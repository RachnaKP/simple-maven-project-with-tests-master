node {
   
def mvnHome
   
	stage('Preparation') { // for display purposes
      
		// Get some code from a GitHub repository
 
      
		// Get the Maven tool.
      
		// ** NOTE: This 'M3' Maven tool must be configured
     
                                // **       in the global configuration.           
      
		mvnHome = tool 'M3'
   
	}
  
 	stage('Build') {
      // Run the maven build
     
		 if (isUnix()) {
         sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
      }
		 else {
         bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
      }
  
	 }
   

	stage('Results') 
	{
      junit '**/target/surefire-reports/TEST-*.xml'
      archive 'target/*.jar'
   
	}
	
	stage('test_date') 
	{
         sh "date"
   
	}
	
	stage('test_date2') 
	{
         sh "date"
   
	}
	
	stage('test_date3') 
	{
         sh "date"
   
	}

}
