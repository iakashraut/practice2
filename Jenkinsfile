pipeline{
    agent{
        label{label'slave'
        customWorkspace'/mnt/test3'
             }
          }
        stages{
            stage(checkout){
                steps{
                    sh'rm -rf index.html'
                    git'https://github.com/iakashraut/docker-assign.git'
                    sh'chmod 755 index.html'
                    sh'docker run -itdp 12000:80 bhide httpd'
                    sh'docker cp /mnt/test3/index.html bhide: /usr/local/apache2/htdocs/
                    
                    
                }
            }
        }
        
    }
