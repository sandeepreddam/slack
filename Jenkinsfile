pipeline
{
  agent any
   stages
  {
     stage('1')
           {
             steps:
             {
               sh 'mkdir sab'
             }
           }
  }
          post
           {
               always
               {
                    slackSend channel: 'cloud',
                     message: "Find Status of Pipeline:- ${currentBuild.currentResult} ${env.JOB_NAME} ${env.BUILD_NUMBER} ${BUILD_URL}"
               }
           }
}
