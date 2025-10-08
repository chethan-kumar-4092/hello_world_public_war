pipeline{
    agent any
    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "maven_3.9.9"
    }
    stages{
        stage('checkout'){
           steps{
               git branch: 'main', url: 'https://github.com/chethan-kumar-4092/hello_world_public_war.git'
           } 
        }
        
        stage('create binaries'){
            steps{
                 sh "mvn clean install"
                }
        }
        // stage('create docker image'){
        //     steps{
        //         sh "docker build -t chethanarjun/devopsapp:latest ."
        //         sh "docker tag chethanarjun/devopsapp:latest chethanarjun/devopsapp:test-deploy_${BUILD_NUMBER}"
        //         sh "docker push chethanarjun/devopsapp:test-deploy_${BUILD_NUMBER}"
        //     }
        // }
    }
}
