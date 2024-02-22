// primer paso crear el token para configurarme contra AWS
ubuntu@LinuxDocker:~/html$ aws configure
AWS Access Key ID [None]:  
AWS Secret Access Key [None]:  
Default region name [None]:  
Default output format [None]:  

//insertar el aws_session_token en el fichero   ~/.aws/credentials
sudo nano ~/.aws/credentials
aws_access_key_id = ASIA6GBM333DL7UDRAGT
aws_secret_access_key = MI1nngODHxKmtfebY0eHPxSxo3333zHdfZpsrfB
aws_session_token=FwoGZXIvYXdzEIr//////////wEaDN+NMartm/a524SrEd1zgYOvWbPLOOdS5cP0ry3444q/hO7IY5733uteh+9NSc/BVi4NB444dur4TMA3Ra4uPCnI9qdyxl8EYCXIjI7tOGk>

// realizar la autenficación

ubuntu@LinuxDocker:~/html$ aws configure
AWS Access Key ID [****************]: 
AWS Secret Access Key [****************srfB]: 
Default region name [us-east-1]: 
Default output format [json]: 



