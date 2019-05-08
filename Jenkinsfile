pipeline{
    agent any 
    stages {
        stage('CheckOut')
        {
            steps{
                sh 'rm -rf cloudproduct'
                sh 'git clone https://github.com/codebrainsvps/cloudproduct.git'
            }
        }
    }
    post {
        success
        {
          build 'JenkinsJobs_Vasanth/SampleJob' 
          build job: 'JenkinsJobs_Vasanth/paramater', parameters: [string(name: 'JobNumber', value: '125')]
        }
    }
    
}
