In order to run this file, you need to install docker:
https://docs.docker.com/installation/#installation

1. Build the image using the following command:
sudo docker build -t your_images_sshd_name

2. Run the container as a daemon using:
sudo docker run -d -p --name your_container_sshd_name your_images_sshd_name

3. Check the host port the container's port 22 map to:
sudo docker port your_container_sshd_name 22

=> 0.0.0.0:sshd_port

Or check the container's ip by using:
sudo docker inspect your_container_sshd_name

4. Now you can login to sshd on docker using:
ssh root@ip_of_container -p sshd_port
