# This Project to run a server code on ec2 using  LoadBalancer
Steps:

## 1- create Your Own repo but with name i  (srv-020) 

###  push two files  main.cs and srv02.csproj
-  git add .
-  git commit -m ""
-  git push origin master
## 2- Go To ec2 from AWS console create a Launch Templates  and configure the template:
-    chose ubuntu os,
-    t3.micro,
-    add tags U want,
-    Add your Key pair 
-    chose VPC and security group,  
-    In Advanced details add the content of script.sh file  but replace  the repo url with your repoURL in script.sh file
## 3-   Launch instants from  template 
-    add 2 ec2 and create them  
## 4- Create the Target Group and LoadBalancer:
- create target group and add the two ec2 to it 
- create LoadBalancer , attach with target group add 8002 to port 

###  Now  You can Access the Server code from LoadBalancer:8002
```markdown
To watch the traffics of this server , follow these steps:

1. Run the following command:
  
    journalctl -f -u srv-02
``` 

### - This is a diagram of Project 

![The diagram of projcts](https://github.com/khaledhawil/srv-02/blob/master/Untitled%20Diagram.drawio.png)
