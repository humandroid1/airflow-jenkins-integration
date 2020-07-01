node{
   stage('SCM Checkout'){
     git 'https://github.com/vishnu2198/airflow-jenkins-integration.git'
     }
   stage('Deploy to airflow'){
    sshagent(['jenkinstom']) {
    sh 'whoami'
    sh 'scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/airflow_integration_5/*.py  ec2-user@34.207.99.204:/home/ec2-user/airflow/dags/'
    sh 'pwd'
    }
    sh 'scp -i /home/ec2-user/jenkins.pem ec2-user@ec2-34-207-99-204.compute-1.amazonaws.com:/home/ec2-user/'
    sh 'whoami'
    dir("/home/ec2-user/airflow/") {
    sh "pwd"
   
    
   
    }
     
    
    }
} 
