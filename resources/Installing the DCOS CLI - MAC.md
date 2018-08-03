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
Tip: If your system is unable to find the executable, you may need to re-open the command prompt or add the installation directory to your PATH environment variable manually.
