pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master',
                    url: 'git@github.com:blueberry247/ansible-tomcat-mini.git'
            }
        }

        stage('Deploy with Ansible') {
            steps {
                sh '''
                  ansible-playbook -i inventory.yml site.yml
                '''
            }
        }
    }
}

