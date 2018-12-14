1. Unzip sonar installation
2. cd sonar installation
3. change the conf/sonar.properties from
3a.
# TCP port for incoming HTTP connections. Default value is 9000.
#sonar.web.port=9000

TO

# TCP port for incoming HTTP connections. Default value is 9000.
sonar.web.port=9011
3b.
# As a security precaution, should be blocked by a firewall and not exposed to the Internet.
#sonar.search.port=

TO

# As a security precaution, should be blocked by a firewall and not exposed to the Internet.
sonar.search.port=9012

4.  Start Sonarqube locally:
For Windows:

cd bin\windows-x86-64
InstallNTService.bat
StartNTService.bat

For MAC:

cd bin/macosx-universal-64
./sonar.sh start

5. Browse sonarqube:

http://localhost:9001

