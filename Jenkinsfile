pipeline{
    agent{
        label{label'built-in'
        customWorkspace'/mnt/test'
             }
          }
        stages{
            stage(checkout){
                steps{
                    sh'rm -rf index.html'
                    git'https://github.com/iakashraut/practice2.git'
                    
                    sh'docker run -itdp 15000:80 --name xyz7 httpd'
                    sh'chmod 755 index.html'
                    sh'docker cp /mnt/test/index.html xyz7:/usr/local/apache2/htdocs'
                    
                    
                }
            }
        }
        
    }
