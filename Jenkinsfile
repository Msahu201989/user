pipeline {

 agent {
    node { label 'Workstation' }
 }

 stages {

  stage ('code quality') {
    steps {
     echo 'code quality'
    }
  }

    stage ('Style checks') {

        when { tag "*" }

          steps {
       echo 'style checks'
      }
    }

      stage ('unit Tests') {
           when {
              branch 'demo'
              }
        steps {
         echo 'Unit Test'
        }
      }

      stage ('Download dependencies') {
        when {
            branch 'demo'
            }
        steps {
         echo 'Download Dependencies'
        }
      }

       stage ('Prepare Artifact') {
        when { tag "*" }
         steps {
          echo 'Prepare Artifact'
         }
       }

         stage ('Publish Artifact') {
           when { tag "*" }
           steps {
            echo 'Publish Artifact'
           }
         }
 }
 }


