node{
   stage('SCM Checkout'){
     git 'https://github.com/vishnu2198/airflow-jenkins-integration.git'
     }
   stage('Deploy to airflow'){
    sshagent(['jenkinstom']) {
     sh  "ssh -v ec2-user@3.85.1.101 'ls' "
    sh 'whoami'
    sh 'scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/airflow_final/*.py  ec2-user@3.85.1.101:/home/ec2-user/airflow/dags/'
    
    //sh 'scp /home/ec2-user/jenkins.pem ec2-user@ip-172-31-39-88.ec2.internal:/home/ec2-user/'
    sh'pwd'
    sh 'whoami'
    sh 'ls'
     sh  "ssh -v ec2-user@3.85.1.101 'cd /home/ec2-user/airflow/' "
     sh  "ssh -v ec2-user@3.85.1.101 'pwd' "
     sh "ssh -v ec2-user@3.85.1.101  'ls' "
      sh  "ssh -v ec2-user@3.85.1.101 'airflow webserver -p 8080 & airflow scheduler && fg' "  
    //dir("/home/ec2-user/airflow/dags") {
    //sh "pwd"
    //sh 'ls'
   
    }  
   
    
     
    
    }
} 
