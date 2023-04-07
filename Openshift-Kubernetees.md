# openshift:

* Red Hat considers Kubernetes as the kernel of its distributed platform, and OpenShift as the distribution.
* OpenShift uses two primary tools to serve applications in containers: 
	1. a container runtime to create containers in Linux:
        A container runtime works on a Linux server to create and manage containers.
	2. an orchestration engine to manage a cluster of servers running containers
* In OpenShift, the service that handles the creation and management of containers is docker 
* The resources that docker uses to isolate processes in containers all exist as part of the Linux kernel.
These resources include things like SELinux, Linux namespaces, and control groups (cgroups),
* Applications running inside a container can only access the resources in the container. 
	- The applications in the container are isolated from anything running in other containers or on the host. 
	- Five types of resources are isolated with containers:
	    1. Mounted filesystems
	    2. Shared memory resources
	    3. Hostname and domain name
	    4. Network resources (IP address, MAC address, memory buffers)
	    5. Process counters



								kubernetes                                 						        									     openshift
								
Platform Support:	can be installed on almost any Linux distribution							Red Hat CoreOS for the masternodes , CoreOS or RHEL for workernodes


Installation:	offers a variety of installation tools, including kubeadm, kops,				OpenShift has different installation procedures for different versions
				and kube-spray. Some tools are designed especially for the cloud 
				
User Interface:	a complex web-based interface, which is not generally recommended			web-based console that comes with a one-touch login page. 
				for novices. To access the interface, users need to first install 						The OpenShift console provides a simple form-based interface 
				the official Kubernetes Dashboard and then forward the port address  that enables users to easily change, delete, and add resources.
				of their local machine to the cluster server by using kube-proxy.
				However, the dashboard does not have a login page
				
Updates:	lets you perform multiple upgrades,															difficult to perform mulyiple upgrades.
				you only need to invoke the kubeadm upgrade command,							To install the most recent version of OpenShift, 
				Before upgrading Kubernetes, 																you need to access the Red Hat Enterprise Linux package management system.
				be sure to backup all existing installation files.
Security
Router vs Ingress
Integrated CI/CD
Templates					Helm 																				template
Networking:			does not provide a complete networking solution              	provide a complete networking solution        
Container-
-Image Management;	Kubernetes integrates with the Docker registry.					OpenShift offers the use of an integrated image registry called Image Streams
				kubernetes does not provide a dedicated resource that 				which enables easier, more secure management of container images.
				can help you manage the workflow of building container images.		This registry offers a console that allows users to search for 
				Kubernetes users build images using the Docker build command.		information about image streams and images within a cluster.
																					Image Streams lets users download entire images and locally modify them without having to use external tools
																					