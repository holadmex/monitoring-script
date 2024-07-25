# MONITORING SCRIPT

## DETAILED GUIDE TO RUN MONITORING SCRIPT ON THE SERVER

**CREATED EXECUTION FILE SCRIPTS INCLUDES:**

```sh
installation
devopsfetch
```

**Installation:** This script handles installation of the necessary preprequisite needed for `devopsfetch` script to execute its functions. However, both shell script file needs to be given permission to execute. Below is the cmd to give file permission.

```sh
chmod 700 installation
chmod 700 devopsfetch
```
## STEPS TO EXECUTE OUR SCRIPT

**Devopsfetch:** This script provides various functionalities for monitoring and retrieving server information, such as active ports, Docker containers, Nginx configurations, user logins, and activities within a specified time range. Run the script using the command:

`./devopsfetch -h`

should display the output below

## Options

- **`-p`, `--port`**  
  Display all active ports and services or detailed information about a specific port.

- **`-d`, `--docker`**  
  List all Docker images and containers or detailed information about a specific container.

- **`-n`, `--nginx`**  
  Display all Nginx domains and their ports or detailed configuration information for a specific domain.

- **`-u`, `--users`**  
  List all users and their last login times or detailed information about a specific user.

- **`-t`, `--time`**  
  Display activities within a specified time range or for a specific date.

- **`-h`, `--help`**  
  Display this help message.


The above "options:" are for passing specific parameters to monitoring different activites on the server. 

## Use Cases
`./devopsfetch -p` **or** `--port`, `./devopsfetch --80`

## Logging

To check logging metrics carried out with the monitoring commands on the sever, kindly `cd` out of the current working directory to the root directory of the sever.

`cd /var/log/devopsfetch.log`

The command above output the metrics on the server. In other words its a path to get historical data of activites on the server.

## Monitoring

**Setup Instructions**

1. Make the Script Executable

`sudo chmod +x /your/path/to//devopsfetch`

2. Verify the Script Permissions

`ls -l /home/dmex/hng-task5/monitoring-script/devopsfetch`

3. Edit the Service Configuration

`sudo nano /etc/systemd/system/sysinfo.service` To `/your/path/to/devopsfetch -d`

4. Confirm the Service Configuration

`cat /etc/systemd/system/sysinfo.service`

**Service Description**

The devopsfetch service is designed to run continuously, executing the script periodically (every 30 seconds). It gathers vital system information and logs it to a file located at /var/log/devopsfetch.log. This setup provides an automated monitoring solution, enabling the tracking and review of:

- Docker images and containers
- Active ports and services
- Nginx domains and configurations

By automating these checks, devopsfetch helps maintain a comprehensive log of system activities, facilitating easy monitoring and troubleshooting.

**THANKS FOR READING...**