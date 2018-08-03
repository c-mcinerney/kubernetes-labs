# Installing the DC/OS CLI - MAC
Download the DC/OS CLI binary (dcos) to your local directory (for example, /usr/local/bin/).
```
curl -O https://downloads.dcos.io/binaries/cli/darwin/x86-64/dcos-1.11/dcos
```
Important: The CLI must be installed on a system that is external to your DC/OS cluster.

Make the CLI binary executable.
```
chmod +x dcos
```
Set up the connection from the CLI to your DC/OS cluster. In this example, http://example.com is the master node URL.
```
dcos cluster setup http://example.com
```

When prompted for a password:
```
Username: bootstrapuser
Password: deleteme
```

Output should look like this:
```
[centos@ip-10-0-0-243 ~]$ [ -d /usr/local/bin ] || sudo mkdir -p /usr/local/bin &&
> curl https://downloads.dcos.io/binaries/cli/linux/x86-64/dcos-1.11/dcos -o dcos &&
> sudo mv dcos /usr/local/bin &&
> sudo chmod +x /usr/local/bin/dcos &&
> dcos cluster setup https://34.201.120.43 &&
> dcos
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 14.0M  100 14.0M    0     0  3834k      0  0:00:03  0:00:03 --:--:-- 3835k
SHA256 fingerprint of cluster certificate bundle:
91:31:31:A8:83:E8:05:94:E1:9B:23:34:EE:41:21:32:C8:A1:EB:7F:0D:B1:4C:A5:67:5A:BF:ED:70:B0:1D:C2 [yes/no] yes
34.201.120.43's username: bootstrapuser
bootstrapuser@34.201.120.43's password:
Command line utility for the Mesosphere Datacenter Operating
System (DC/OS). The Mesosphere DC/OS is a distributed operating
system built around Apache Mesos. This utility provides tools
for easy management of a DC/OS installation.

Available DC/OS commands:

	auth           	Authenticate to DC/OS cluster
	cluster        	Manage your DC/OS clusters
	config         	Manage the DC/OS configuration file
	help           	Display help information about DC/OS
	job            	Deploy and manage jobs in DC/OS
	marathon       	Deploy and manage applications to DC/OS
	node           	View DC/OS node information
	package        	Install and manage DC/OS software packages
	service        	Manage DC/OS services
	task           	Manage DC/OS tasks

Get detailed command description with 'dcos <command> --help'.
```

Confirm that dcos is installed and connected to your cluster by running following command

```
dcos node
```

The output should be a list of nodes in the cluster:
```

   HOSTNAME        IP                         ID                     TYPE                 REGION          ZONE       
  10.0.0.101   10.0.0.101  94141db5-28df-4194-a1f2-4378214838a7-S0   agent            aws/us-west-2  aws/us-west-2a  
  10.0.2.100   10.0.2.100  94141db5-28df-4194-a1f2-4378214838a7-S4   agent            aws/us-west-2  aws/us-west-2a
```

[Return to Lab 1](https://github.com/c-mcinerney/kubernetes-labs/blob/master/Lab%201%20-%20Installing%20Kubernetes.md)

 
