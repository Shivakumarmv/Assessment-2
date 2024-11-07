# ssh to server

Navigate to instance page and select instance recently launched and click on connect button top 

![Screenshot 2024-11-07 150759](https://github.com/user-attachments/assets/34d6ea4a-c8d3-4562-9637-b21e2603d24c)


Scroll down and click connect button 

![Screenshot 2024-11-06 150908](https://github.com/user-attachments/assets/504d7daa-c15f-41d6-b554-744a2ee103fb)


# Install docker 

```
yum install docker -y

docker --version

```
![Screenshot 2024-11-07 124141](https://github.com/user-attachments/assets/22bb00ab-2310-48d4-9a58-808cc1310c38)

![Screenshot 2024-11-07 124211](https://github.com/user-attachments/assets/e9fe070a-a825-4c3a-8ee0-db59f6220f1b)

# Start the service

```

systemctl start docker
systemctl status docker

```

![Screenshot 2024-11-07 124301](https://github.com/user-attachments/assets/669ea7ca-f926-4ad1-8c89-8472f157aa86)

# Clone the repo

![Screenshot 2024-11-07 130740](https://github.com/user-attachments/assets/0f261753-f74e-4faf-aa87-22e9e47821df)

# Docker file 

![Screenshot 2024-11-07 144019](https://github.com/user-attachments/assets/c5df5724-a19f-4540-a389-3f8326838e69)

# Build the Docker Image

```
docker build -t todo-img:v1 .

```

![Screenshot 2024-11-07 144336](https://github.com/user-attachments/assets/f242ef59-75fb-4970-ac09-6b7d2540fac6)

# Run the Docker Container

```

docker run -d --name todo-server -p 8000:8000 todo-img:v1
```

![Screenshot 2024-11-07 151329](https://github.com/user-attachments/assets/b041b105-f252-4c6f-b939-f95ca15ff723)



# Open port in security group

Go to the AWS Management Console -> Navigate to EC2 Instances and select your instance -> Under Security edit the Security Group for your instance click on inbound rule -> open 8000 port 

![Screenshot 2024-11-07 144925](https://github.com/user-attachments/assets/0475029c-22ed-4889-a290-3f5b3d1ed8e0)


# Access the application

select server and copy the public ip address and paste in browser with the specified port number (eg.107.23.243.219:8000) If we can see the website in fully functional mode, it means we have properly set up and configured 


![Screenshot 2024-11-07 145641](https://github.com/user-attachments/assets/8ab5289c-e3fb-4083-9243-641570a837b4)

# Push to github

![Screenshot 2024-11-07 145828](https://github.com/user-attachments/assets/33d6c15e-2907-495e-9690-498d156429e4)


![Screenshot 2024-11-07 150008](https://github.com/user-attachments/assets/c06886f4-ebf5-42dd-9791-65bdd1114251)



