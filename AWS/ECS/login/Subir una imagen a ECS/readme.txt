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



// realizar la autenficación en el repositorio
Recupere un token de autenticación y autentique su cliente de Docker en el registro.
Utilice AWS CLI:

aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 975050370694.dkr.ecr.us-east-1.amazonaws.com
Nota: Si recibe un error al utilizar AWS CLI, asegúrese de tener instaladas las últimas versiones de AWS CLI y Docker.
Cree una imagen de Docker con el siguiente comando. Para obtener información sobre cómo crear un archivo de Docker desde cero, consulte las instrucciones aquí . Puede omitir este paso si ya se creó la imagen:

docker build -t frodriguezmoron .
Cuando se complete la creación, etiquete la imagen para poder enviarla a este repositorio:

docker tag frodriguezmoron:latest 975050370694.dkr.ecr.us-east-1.amazonaws.com/frodriguezmoron:latest
Ejecute el siguiente comando para enviar esta imagen al repositorio de AWS recién creado:

docker push 975050370694.dkr.ecr.us-east-1.amazonaws.com/frodriguezmoron:latest
