pipeline{
    agent any
    stages{
        stage("Checkout"){
            steps{
                git branch: 'main', url: 'https://github.com/Indu-tech/capstone.git'
            }
        }      

        stage('Run Ansible Playbook') {
            steps{
                sh 'ansible-playbook -i inventory playbook.yaml'
            }  
        }     
    }
}
