# ssh to server

Navigate to instance page and select instance recently launched and click on connect button top 

![Screenshot 2024-11-07 150759](https://github.com/user-attachments/assets/34d6ea4a-c8d3-4562-9637-b21e2603d24c)


Scroll down and click connect button 

![Screenshot 2024-11-06 150908](https://github.com/user-attachments/assets/5fc966e5-ab42-43a1-8716-f46bac8da6d0)



# Install docker 

```
yum install docker -y

docker --version

```
![Screenshot 2024-11-07 124141](https://github.com/user-attachments/assets/9b27040c-9e7f-497f-86bc-7dbafda6dbf9)

![Screenshot 2024-11-07 124211](https://github.com/user-attachments/assets/4ba075a8-6135-4842-96af-0c0344346271)

# Start the service

```

systemctl start docker
systemctl status docker

```
![Screenshot 2024-11-07 124301](https://github.com/user-attachments/assets/74b6685c-596c-40c2-a7d0-cdca88c5019b)



# Clone the repo

![Screenshot 2024-11-07 130740](https://github.com/user-attachments/assets/ee6fe5cf-037f-452e-a745-7bbd00e1d228)

# Docker file 

![Screenshot 2024-11-07 144019](https://github.com/user-attachments/assets/d6136034-a36d-47bd-be84-6606d58e9299)

# Build the Docker Image

```
docker build -t todo-img:v1 .

```
![Screenshot 2024-11-07 144336](https://github.com/user-attachments/assets/d0d9407b-9d2a-45d0-a5c9-e40fe6b3a318)



# Run the Docker Container

```

docker run -d --name todo-server -p 8000:8000 todo-img:v1
```

![Screenshot 2024-11-07 151329](https://github.com/user-attachments/assets/581bdf39-7588-4de6-811f-2f68fd0838e4)


# Open port in security group

Go to the AWS Management Console -> Navigate to EC2 Instances and select your instance -> Under Security edit the Security Group for your instance click on inbound rule -> open 8000 port 

![Screenshot 2024-11-07 144925](https://github.com/user-attachments/assets/638c103b-ede9-47c9-ae03-ffa1fab133f8)


# Access the application

select server and copy the public ip address and paste in browser with the specified port number (eg.107.23.243.219:8000) If we can see the website in fully functional mode, it means we have properly set up and configured 


![Screenshot 2024-11-07 145641](https://github.com/user-attachments/assets/705f12b6-98a7-4466-8194-43a1c4d55ca0)


# Push to github

![Screenshot 2024-11-07 145828](https://github.com/user-attachments/assets/46143f3e-28dd-4813-ba1d-4f89f0060e41)

![Screenshot 2024-11-07 150008](https://github.com/user-attachments/assets/533bfed5-02d1-4864-9dfb-7ae5be1e0712)

