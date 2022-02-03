pipeline    {
            agent any
            stages {
             stage('BUILD'){
                steps {
                        git branch: 'main', url: 'https://github.com/sharath030/java-project.git'
                            sh 'mvn clean install'
                    }
                  }
            }
}
