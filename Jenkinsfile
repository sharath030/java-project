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
                                    steps {
                                                sh 'scp -r /home/ec2-user/.m2/repository/com/efsavage/hello-world-war/1.0.0/hello-world-war-1.0.0.war ec2-user@172.31.25.229:/home/ec2-user/apache-tomcat-9.0.58/webapps'
                                                echo 'Deploy success'
                                    }
                        }
            
}
}
