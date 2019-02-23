pipeline {
  agent any
  stages {
    stage('Initiation') {
      steps {
        echo 'Start to Destroy Deployment on AWS'
      }
    }
    stage('Destroy') {
      steps {
        sh '''cd "/Users/artwang2/Documents/My Jar/terraform-provider-aws/examples/two-tier"
touch ./yes
echo "yes" > ./yes
terraform destroy -input=false < yes > destroy.log'''
      }
    }
    stage('Done') {
      steps {
        sh '''cd "/Users/artwang2/Documents/My Jar/terraform-provider-aws/examples/two-tier"
terraform show'''
        echo 'Destroy done!'
      }
    }
  }
}