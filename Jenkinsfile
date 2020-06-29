node{
   stage('SCM Checkout'){
     git 'https://github.com/vishnu2198/airflow-jenkins-integration.git'
     }
   stage('Deploy to airflow'){
    sshagent(['jenkinstom']) {
    sh 'scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/airflow_jenkins_integration/*.py  ec2-user@174.129.230.154:/home/ec2-user/airflow/dags/'
    
    
     }
    
    }
} 
