pipeline {
   agent any
   stages {
       stage('Build Code') {
           steps {
               sh "mvn clean package"
               echo "Building Artifact for project samplewebapp"
               
           }
       }
       stage('Reading branch wise')
       {
       when
       {
       branch "feature*"
       }
       steps
       {
       echo " It is only for Feature branch"
       }
       }

       stage('Deploy Code') {
	   when
       {
       branch "stage"
	       }
          steps {
               sh "mvn tomcat7:deploy"
               echo "Deploying Code"
               
          }
      }
      }
      }
i
