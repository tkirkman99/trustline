System Requirements:
JDK 1.8 with JAVA_HOME set
Tomcat 9.x with CATALINA_HOME set
HOME is set to the user's home folder, i.e. /Users/tk

Installation:

This installation creates a folder named tkirkman in the $HOME folder that contains
these Trustline client and server folders:
client1
client2
server1
server2

The two servers to be run use ports 8080 and 8081, so these ports must not be
in use on the install host machine.

1. With the current folder set to $HOME, clone the 'Trustline' Github repo.

2. Launch each trustline server instance in separate terminal windows:
	<Terminal 1>
	cd ~/tkirkman/server1
	sh start-server1.sh
	<Terminal 2>
	cd ~/tkirkman/server2
	sh start-server2.sh
	
	(To stop each server, run its stop-server.sh script)

3. Run the client accounts setup application
   - Run this application only once per dual trustline server runtime session:
	cd ~/tkirkman
	sh setup-accounts.sh   

4. Launch each of the trustline CLI client applications in separate terminal windows:
	<Terminal 1>
	cd ~/tkirkman/client1
	sh start-client1.sh
	<Terminal 2>
	cd ~/tkirkman/client2
	sh start-client2.sh

5. Use the CLI client to send debt amounts:
	Enter the amount of the debt to send, as a positive number.  Negative numbers 
	will be treated as positive debt amounts.
	
	Type 'exit' to terminate the client session.
	