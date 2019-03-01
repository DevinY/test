pipeline {
    agent any 

    stages {
        stage('組態') { 
            steps { 
                sh 'ssh web "cp /var/www/html/test/.env.example /var/www/html/test/.env"'
                sh 'ssh web "ssh web "cd /var/www/html/test;composer install"'
                sh 'ssh web "cd /var/www/html/test/;php artisan key:generate"'
            }
        }
    }
}
