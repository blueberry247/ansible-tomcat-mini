pipeline {
    agent any

    stages {
        stage('Deploy with Ansible') {
            steps {
                sh '''
                  ansible-playbook -i inventory.yml site.yml
                '''
            }
        }
    }
}

