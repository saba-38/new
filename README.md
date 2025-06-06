prgm-5
Step 1: Install JDK 17/21 on GNU/Linux - Ubuntu

sudo apt update
sudo apt install openjdk-17-jdk -y

Step 2: Add Jenkins repository and key

curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null


Step 3: Add Jenkins repo to sources list

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null


Step 4: Update package list
sudo apt update

Step 5: Install Jenkins

sudo apt install jenkins -y

Step 6: Start and Enable Jenkins
sudo systemctl start jenkins
sudo systemctl enable jenkins
sudo systemctl status jenkins



to Reset Jenkins Admin Password (Manually)

. STOP IT - sudo systemctl stop jenkins
. sudo mv /var/lib/jenkins/users /var/lib/jenkins/users_backup
. sudo rm /var/lib/jenkins/config.xml
. repeat step 6
. http://localhost:8080

tO  GET ADMINITRATIVE PASSOWRD: (to continue normal process)
sudo cat /var/lib/jenkins/secrets/initialAdminPassword

---------------------------------------------------------------------
---------------------------------------------------------------------
to update the version of gradle to 7(pgm-4) for migration


1. Remove old Gradle (if installed via apt) - sudo apt remove gradle
2.  Download Gradle 7 - wget https://services.gradle.org/distributions/gradle-7.6.4-bin.zip -P /tmp
sudo unzip -d /opt/gradle /tmp/gradle-7.6.4-bin.zip
3.  update to gradle home
export GRADLE_HOME=/opt/gradle/gradle-7.6.4
export PATH=$GRADLE_HOME/bin:$PATH
4.
source ~/.bashrc
gradle -v

------------------------------------------------------------------------------

pgm-2 : to install eclispse
sudo apt install snapd
sudo snap install eclipse --classic











