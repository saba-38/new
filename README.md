Step 1: Install JDK 17/21 on GNU/Linux - Ubuntu
sudo apt update
sudo apt install openjdk-17-jdk -y

Step 2: Add Jenkins repository and key
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-
2023.key | sudo tee \
/usr/share/keyrings/jenkins-keyring.asc > /dev/null

Step 3: Add Jenkins repo to sources list
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
/etc/apt/sources.list.d/jenkins.list > /dev/null

Step 4: Update package list
sudo apt update

Step 5: Install Jenkins
sudo apt install jenkins -yStep 6: Start and Enable Jenkins
sudo systemctl start jenkins
sudo systemctl enable Jenkins
