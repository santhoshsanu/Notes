# Installing Java 11 on Ubuntu and Setting Up JAVA_HOME

## Step 1: Update Package List
```sh
sudo apt update
```

## Step 2: Install OpenJDK 11
```sh
sudo apt install -y openjdk-11-jdk
```

## Step 3: Verify Java Installation
```sh
java -version
```

## Step 4: Find Java Installation Path
```sh
sudo update-java-alternatives --list
```
Example output:
```
java-1.11.0-openjdk-amd64  1111  /usr/lib/jvm/java-11-openjdk-amd64
```

## Step 5: Set Up JAVA_HOME and Update Path
Edit the `/etc/profile` file:
```sh
sudo nano /etc/profile
```
Add the following lines at the end:
```sh
export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64
export PATH=$JAVA_HOME/bin:$PATH
```

## Step 6: Apply Changes
```sh
source /etc/profile
```

## Step 7: Verify JAVA_HOME
```sh
echo $JAVA_HOME
```

Now, Java 11 is installed and the `JAVA_HOME` environment variable is set.

