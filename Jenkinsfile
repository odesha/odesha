node
{
    stage "1. install docker"
    sh "yum install docker -y"
    
    stage "2. Start the service"
    sh "service docker start"
    
    stage "3. Build the image"
    sh "docker build -t jenkinsfile_image_scm1 /home/ec2-user"
    
    stage "4. Run the container"
    sh "docker run -dit --name jenkinsfile_container_scm1 jenkinsfile_image_scm1"
    
    stage "5. Push the image"
    sh "docker login --username odesha --password Welcome@9"
    
    sh "docker tag jenkinsfile_image_scm1 odesha/jenkinsfile_image_scm1"
    
    sh "docker push odesha/jenkinsfile_image_scm1"
}
