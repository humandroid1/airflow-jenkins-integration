node{
   stage('SCM Checkout'){
     git 'https://github.com/vishnu2198/airflow-jenkins-integration.git'
     }
   stage('Deploy to airflow'){
    sshagent(['jenkinstom']) {
    sh 'whoami'
    sh 'scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/airflow_integration_2/*.py  ec2-user@54.224.100.175:/usr/local/airflow/dags/'
    sh 'pwd'
    sh 'whoami'
    dir("/usr/local/airflow/") {
    sh "pwd"
    sh 'cd /usr/local/airflow'
    sh 'airflow webserver -p 8080 & airflow scheduler && fg'
}
    
   
    
     }
    
    }
} 
