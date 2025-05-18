pipeline{
    agent {
        label 'master'
    }
    stages{
        stage("Checkout"){
            steps{
                git branch: 'main', url: 'https://github.com/Indu-tech/capstone.git'
            }
        }

        stage("Install Ansible"){
            steps{
                sh 'sudo apt-get -y install ansible'
            }
        }        

        stage('Run Ansible Playbook') {
            steps{
                sh 'ansible-playbook -i inventory playbook.yaml'
            }  
        }     
    }
}
