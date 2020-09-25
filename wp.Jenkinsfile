pipeline {
  agent  any
  }
  stages {
    stage ("Git-Checkout-wordpress"){
        steps {
            git clone "repo_url"
        }
    }
    stage('Build wordpress') {
      steps {
        sh " php build"
      }
    } 
    stage('test-wordpress-app') {
      steps {
        sh "php test"
      }
    }
    stage('deploy to DEV/UAT servers') {
      steps {
       
        sh "ansible-plyabook -i inventory_name <pb_name>"
      }
    } 
    // approvals requreid to deploy on Prod Server
    stage('deploy to Prod servers') {
      steps {
        sh "ansible-plyabook -i inventory_name <pb_name>"
      }
    } 
        }
      }
    }
  }
}