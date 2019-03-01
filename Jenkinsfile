pipeline {
    agent any 

    stages {
        stage('下載') { 
            steps { 
                git 'https://github.com/DevinY/test.git' 
            }
        }
        stage('組態') { 
            steps { 
                sh 'ssh web "cp /var/www/html/test/.env.example /var/www/html/test/.env"'
                sh 'ssh web "cd /var/www/html/test;composer install"'
                sh 'ssh web "cd /var/www/html/test/;php artisan key:generate"'
            }
        }
    }
}
