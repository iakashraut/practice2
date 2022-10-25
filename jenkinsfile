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
                    
                    sh'docker run -itdp 12000:80 --name xyz4 httpd'
                    sh'chmod 755 index.html'
                    sh'docker cp /mnt/test/index.html xyz4:/usr/local/apache2/htdocs'
                    
                    
                }
            }
        }
        
    }
