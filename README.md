# jenkinsc
```

# Update package index
sudo apt update

# Install Java and fontconfig
sudo apt install fontconfig openjdk-21-jdk -y

# Create Jenkins keyring directory
sudo mkdir -p /etc/apt/keyrings

# Download Jenkins key
sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc https://pkg.jenkins.io/debian-stable/jenkins.io-2026.key

# Add Jenkins repository
echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/" | sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null

# Update package index
sudo apt update

# Install Jenkins
sudo apt-get install jenkins -y

# Configure Java version
sudo update-alternatives --config java

# Start Jenkins
sudo systemctl start jenkins

# Enable Jenkins
sudo systemctl enable jenkins

# Check Jenkins status
sudo systemctl status jenkins

# Get initial Jenkins administrator password
sudo cat /var/lib/jenkins/secrets/initialAdminPassword

```

After installation, open `http://localhost:8080` and complete the Jenkins initial setup.
