# Installing on Windows

Prerequisites:

- A system external to your DC/OS cluster onto which you will install the CLI

- Network access from the external system to your DC/OS cluster

- A command-line environment, such as Windows Powershell, which is installed by default on Windows 7 and later

- Disable any security or antivirus software before beginning the installation.

- Run command-line environment as Administrator.


Download the [DC/OS CLI executable](https://downloads.dcos.io/binaries/cli/windows/x86-64/dcos-1.11/dcos.exe) to your local directory.
Set up the connection from the CLI to your DC/OS cluster. In this example, http://example.com is the master node URL.
```
dcos cluster setup http://example.com
```


