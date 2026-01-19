<h1>Let's Learn Jenkins Concept</h1>
-----------------------------

Jenkins Master and Slave Concept { Building on a Built-in node will be a security issue }
-----------------------------------------------------------------------------------------------------------------------------
We can setup the distributed builds by setting up the Agent Node.

1. In the prduction environment we generally create that Master node and the Agent Node (Slave).
2. In Agent node only Java must be installed on the Agent Node and no need to install jenkins on it.

Step 1.  Create the EC2 instance for the Agent node and install Java on it.

Now to connect Master node with the Slave node we need to SSH and for that we have to create the key pairs
Step 2. Crate the key pairs on the Master Server
$cd ~/.ssh
$ls
$ssh-keygen
Now we have the Public key and the private key 

Now the public key will be on the agent server and the private key will be on the Master server.

Step 3. Now create the Agent Node from the Jenkins console and add the Public IP of the Agent node in the configuration.
$cd ~/.ssh
$vim authorized_keys (append the key in the file)

Step 4. Now update the pipeline script's agent
for example: agent {label 'NAME_OF_YOUR_AGENT'}

Step 5. Now, build the Job on the slave node
-----------------------------------------------------------------------------------------------------------------------------
