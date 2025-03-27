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