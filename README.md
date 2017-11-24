# CS-445-Final-Project

# Configuration instructions
You'll need jdk 8 & tomcat to run this project

To install jdk 8 and tomcat, please open a terminal, then type in these commands

JDK:

sudo apt-get install oracle-java8-set-default

Then use this command to verify your installation:

java -version

Tomcat:

cd Downloads

wget http://mirrors.ibiblio.org/apache/tomcat/tomcat-8/v8.0.47/bin/apache-tomcat-8.0.47.tar.gz

tar -zxf apache-tomcat-8.0.47.tar.gz

sudo mv apache-tomcat-8.0.47 /opt/tomcat

cd /opt/tomcat/bin

chmod 744 *sh


Then, verify tomcat is properly installed by typing these 2 commands, after the first line, you're supposed to see the "Tomcat started" message, then type in the second line of command to shut it down:

./startup.sh

./shutdown.sh

# Build and deploy instructions
Open a new terminal:

git clone https://github.com/newlifepop/CS-445-Final-Project

cd CS-445-Final-Project

mv thalia.tar.gz ../Downloads

cd ../Downloads

tar -zxf thalia.tar.gz

mv thalia.war /opt/tomcat/webapps

cd /opt/tomcat/bin

./startup.sh

# Build and run test program
Open a new terminal

cd Downloads/thalia/WebContent/WEB-INF/lib

javac -cp .:* ../../../src/edu/iit/hawk/cwu49/*.java

cd ../../../src

java -cp ../WebContent/WEB-INF/lib/junit.jar:../WebContent/WEB-INF/lib/org.hamcrest.core_1.3.0.v201303031735.jar:. edu.iit.hawk.cwu49.TestRunner

You should see the output of the test program now

# Known Bugs
Did not implement the last 2 parts of the project, which are Reports and Search

# Credits and Asknowledgement
For testing, I used a software called "Postman". Also, since I didn't have any prior experience with Java & Tomcat, this project to me was a little hard at first. But the sample project had made it clear for me to follow & did the project. Thanks to the person who wrote the project as well

# Licence
MIT License
