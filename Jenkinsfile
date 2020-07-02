node{
   stage('SCM Checkout'){
     git 'https://github.com/vishnu2198/airflow-jenkins-integration.git'
     }
   stage('Deploy to airflow'){
    sshagent(['jenkinstom']) {
     sh  "sudo  ssh ec2-user@18.215.229.222 'ls' "
    //sh 'whoami'
    //sh 'scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/airflow_integration_5/*.py  ec2-user@34.207.99.204:/home/ec2-user/airflow/dags/'
    sh 'pwd'
    //sh 'scp /home/ec2-user/jenkins.pem ec2-user@ip-172-31-39-88.ec2.internal:/home/ec2-user/'
    //sh'pwd'
    //sh 'whoami'
    //sh 'ls'
    //ssh ec2-user 18.215.229.222 'ls'
   
    //dir("/home/ec2-user/airflow/dags") {
    //sh "pwd"
    //sh 'ls'
   
    }  
   
    
     
    
    }
} 
