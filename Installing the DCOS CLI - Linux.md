# Installing the DC/OS CLI

Download the DC/OS CLI binary (dcos) to your local directory (for example, /usr/local/bin/).
```
curl -O https://downloads.dcos.io/binaries/cli/linux/x86-64/dcos-1.11/dcos
```
Important: The CLI must be installed on a system that is external to your DC/OS cluster.

Move the CLI binary to your local bin directory.
```
sudo mv dcos /usr/local/bin
```
Make the CLI binary executable.
```
chmod +x /usr/local/bin/dcos
```
Set up the connection from the CLI to your DC/OS cluster. In this example, http://example.com is the master node URL.
```
dcos cluster setup http://example.com
```
Follow the instructions in the DC/OS CLI. For more information about security, see the documentation.

Your CLI should now be authenticated with your cluster! Enter dcos to get started.

