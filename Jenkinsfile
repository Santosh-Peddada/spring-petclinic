node('MAVEN'){
 
  stage('SCM'){
    // cloning code
    git 'https://github.com/Santosh-Peddada/spring-petclinic.git'

 }
  stage('Build the package'){
      // Build Step
      sh 'mvn package'
  }

   stage('Archival'){
   // This step should not normally be used in your script. Consult the inline help for details.
    archive 'targer/*.jar'
  }
   stage('Test-results'){
   // This step should not normally be used in your script. Consult the inline help for details.
   junit 'target/surefire-reports/*.xml'
  }
}