1) Install your Ubuntu OS
2) Open a terminal and type:

  sudo apt update
  sudo apt install -y git
  git config --global user.name "Your Name"
  git config --global user.email "you@example.com"
  git clone https://github.com/yourusername/network-automation-labs.git
  cd network-automation-labs
  git config --global credential.helper cache
  Jenkins Setup on jenkins-server

3) Update Java:
  sudo apt update
  sudo apt install -y openjdk-17-jdk git

4)Install Jenkins after adding APT repo:
  wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key |   sudo tee /usr/share/keyrings/jenkins-keyring.asc > /dev/null
  echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]   https://pkg.jenkins.io/debian-stable binary/ |   sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
  sudo apt update
  sudo apt install -y jenkins

5) Start and Enable Jenkins:
   sudo systemctl enable jenkins
   sudo systemctl start jenkins

6) Open http://10.10.21.10:8080 in your browser and finish setup using the password derived from executing the command below on the jenkins-server terminal:
   sudo cat /var/lib/jenkins/secrets/initialAdminPassword
