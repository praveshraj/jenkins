pipeline {
    agent any
    parameters{
        choice(name:'VERSION', choices:['1','2','3'], description:'Version to run')
    }


    stages {
        stage('Build') {
            when{
                expression{params.VERSION =='1'}
            }
            steps {
                input ('Do you want to proceed')
                echo 'This is build step'
            }
        }
        stage('Test') {
            steps {
                input ('Do you want to proceed?')
                echo 'This is test step'
            }
        }
        stage('Deploy') {
            steps {
                input ('Do you want to proceed?')
                echo 'This is deploy step'
            }
        }        
    }
    post {
        success{
            echo 'The job ran successfully'
        }
    }
}
