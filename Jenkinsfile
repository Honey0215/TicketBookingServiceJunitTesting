pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
               // bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                bat "git clone https://github.com/kishancs2020/TicketBookingServiceJunitTesting.git"
                bat "mvn clean -f TicketBookingServiceJunitTesting"
                
              // ssh "rmdir  -rf TicketBookingServiceJunitTesting"
              // ssh  "git clone https://github.com/Honey0215/TicketBookingServiceJunitTesting.git"
               //ssh "mvn clean -f TicketBookingServiceJunitTesting"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f TicketBookingServiceJunitTesting"
               // ssh "mvn install -f TicketBookingServiceJunitTesting"
            }
        }
        stage('test') {
            steps {
              bat "mvn test -f TicketBookingServiceJunitTesting"
                //ssh "mvn test -f TicketBookingServiceJunitTesting"
            }
        }
        stage('package') {
            steps {
                bat "mvn package -f TicketBookingServiceJunitTesting"
              //  ssh "mvn package -f TicketBookingServiceJunitTesting"
                
            }
        }
    }
}
