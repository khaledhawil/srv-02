# This Project to run a server code on ec2 
Steps:
## 1- create Your Own repo and push two files  main.cs and srv02.csproj
## 2- create a Launch Templates  and configure the template:
-    chose ubuntu os,
-    t3.micro,
-    add tags U want,
-    Add your Key pair 
-    chose VPC and security group,  
-    In Advanced details add the content of script file 
## 3-   Launch instants from  template 
-    add 2 ec2 and create them  
##  Now  You can Access the Server code from LoadBalancer:8002
```markdown
To watch the traffics of this server , follow these steps:

1. Run the following command:
   ```bash
    journalctl -f -u srv-02

##

![The diagram of projcts](https://github.com/khaledhawil/srv-02/blob/master/Untitled%20Diagram.drawio.png)
