pipeline    {
            agent any
            stages {
             stage('BUILD'){
                steps {
                        git branch: 'main', url: 'https://github.com/sharath030/java-project.git'
                            sh 'mvn clean install'
                    }
                  }
                        stage('DEPLOY'){
                                    agent { label label1 }
                                    steps {
                                                sh 'scp -r /var/lib/jenkins/workspace/newpipleline/target/hello-world-war-1.0.0.war ec2-user@172.31.25.229:/home/ec2-user/apache-tomcat-9.0.58/webapps'
                                                echo 'Deploy success'
                                    }
                        }
            
}
}
