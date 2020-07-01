node{
   stage('SCM Checkout'){
     git 'https://github.com/vishnu2198/airflow-jenkins-integration.git'
     }
   stage('Deploy to airflow'){
    sshagent(['jenkinstom']) {
    sh 'whoami'
    sh 'scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/airflow_integration_5/*.py  ec2-user@54.205.198.48:/home/ec2-user/airflow/dags/'
    sh 'pwd'
    sh 'whoami'
    dir("/home/ec2-user/airflow/") {
    sh "pwd"
    sh 'airflow webserver -p 8080 & airflow scheduler && fg'
}
    
   
    
     }
    
    }
} 
