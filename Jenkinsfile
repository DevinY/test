pipeline {
    agent any 

    stages {
        stage('組態') { 
            steps { 
                sh 'ssh web "cp /var/www/html/test3/.env.example /var/www/html/test3/.env"'
                sh 'ssh web "cd /var/www/html/test3;composer install"'
                sh 'ssh web "cd /var/www/html/test3/;php artisan key:generate"'
            }
        }
    }
}
