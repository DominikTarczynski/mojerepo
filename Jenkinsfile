pipeline {
    agent any
    environment {
       python3 = '"C:\\Users\\Student\\AppData\\Local\\Programs\\Python\\Python313\\python.exe"' 
    }

    stages {
        stage('Build') {
            steps {
                echo "Starting building python script"
                bat "${python3} code.py"
                echo "Finishing building python script"
            }
        }
        stage('Test') {
            steps {
                echo "testing from SCM..."
            }
        }
        stage('ParallelScript') {
            steps {
               parallel (
                    "TaskOne" : {
                        echo 'task one stuff part 1'
                        echo 'task one stuff part 2'
                        echo 'task one stuff part 3'
                    },
                    "TaskTwo" : {
                        echo 'tasl two stuff part 1'
                        echo 'tasl two stuff part 2'
                    }
                    )

            }
        }
    }
}
