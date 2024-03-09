pipeline 
{ 
  agent any 
  stages 
  { 
 
    stage('Build') 
    { 
      steps 
      { 
        build 'PES2UG21CS015-1'  
        sh 'g++ test.cpp -o output' 
      } 
    } 
 
    stage('Test') 
    { 
      steps 
      {
         sh './output' 
      } 
    } 
    stage('Deploy') 
    { 
      steps 
      { 
        echo 'deploy' 
      } 
    } 
  } 
 
  post 
  { 
    failure 
    { 
      echo 'Pipeline failed' 
    } 
  } 
} 
