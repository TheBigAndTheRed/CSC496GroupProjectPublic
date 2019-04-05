# CSC496GroupProjectPublic
Repositiory for CSC 496 Group Project

This is the project 1 repository for our group project in CSC 496.

Thomas Boudwin
Walter Snyder
Christopher Ariza
Luke Stanish


Goal

	To provide container functionality on the OpenStack default profile


Process

  I.	Launch an experiment with the OpenStack defualt profile
	
  II.	Install Zun (the container service for launching and managing application 
	    containers without any VM managements)
	   
     1. First we must install and configure the controller node 
		   
			    a. Start by creating the Zun database, service credentials, and
			       the API endpoints
			
			    b. Install and configure the components by creating Zun user 
			       and necessary directories then cloning and installing Zun which
			       will finish by populating the Zun database.
		   
			    c. Finalize installation by creating an upstart config and enabling/starting the
			       zun-api and zun-wsproxy services
		
	   2. Install and configure a compute node
		
			    a. Install Docker and Kuryr-libnetwork in the compute node and install
			       Etcd on the controller node
			
			    b. Create Zun user and necessary directories 
			
			    c. Clone and install zun, generate sample config, configure sudoers 
			       for Zun users
			   
			    d. Configure Docker and Kuryr 
			
			    e. Finalize installation by creating an upstart config and enabling/starting
			       zun-compute
			   
  III. Launch a container
	
     1. Source the demo credentials
		
		 2. Determine available networks
		
		 3. Set NET_ID environment variable to reflect ID of a networks
		
		 4. Run a CirrOS container on the selfservice network
		
		 5. Access the container and verify the access to the internet
     
  IV. Package
  
     1. Put all the commands into appropriate folders in repository or into master script so user
        can use container functionality with Zun through OpenStack 
