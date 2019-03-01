pipeline {
    agent any 

    stages {
        stage('組態') { 
            steps { 
                sh 'ssh web "cp /var/www/html/test3_master/.env.example /var/www/html/test3_master/.env"'
                sh 'ssh web "cd /var/www/html/test3_master;composer install"'
                sh 'ssh web "cd /var/www/html/test3_master/;php artisan key:generate"'
            }
        }
    }
}
