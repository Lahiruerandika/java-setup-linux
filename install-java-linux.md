# Installing Java on Linux

## Method 1: Manual Installation (Tarball)

This method allows you to install a specific version of Java manually.

### **Step 1: Create a Directory for Java**
```bash
sudo mkdir -p /usr/java

```

### **Step 2: Extract the Java Tarball**
```bash
tar xvf jdk1.8.0_241.tgz -C /usr/java
```

### **Step 3: Set Up Environment Variables**
```bash
echo "export JAVA_HOME=/usr/java/jdk1.8.0_241" | sudo tee -a /etc/profile
```

### **Step 4: Configure Java with Alternatives**
```bash
sudo alternatives --install /usr/bin/java java /usr/java/jdk1.8.0_241/bin/java 2
sudo alternatives --config java
```

### **Step 5: Configure Javac and Jar**
```bash
sudo alternatives --install /usr/bin/javac javac /usr/java/jdk1.8.0_241/bin/javac 2
sudo alternatives --config javac

sudo alternatives --install /usr/bin/jar jar /usr/java/jdk1.8.0_241/bin/jar 2
sudo alternatives --config jar
```

### **Step 6: Verify Java Installation**
```bash
java -version
javac -version
echo $JAVA_HOME
```