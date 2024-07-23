# monitoring-script

## Here is detailed brief monitoring script function

`installation` This handles the necessary and preprequite installation for our `devopsfetch` script to execute. both shell script file needs to be given permission to run `chmod 700 <script file name >`

On exection of the main script, which is **devopsfetch.sh**,

`./devopsfetch -h`

should display the output below

Options:
-p, --port            Display all active ports and services or detailed information about a specific port
-d, --docker          List all Docker images and containers or detailed information about a specific container
-n, --nginx           Display all Nginx domains and their ports or detailed configuration information for a specific domain
-u, --users           List all users and their last login times or detailed information about a specific user
-t, --time            Display activities within a specified time range or for a specific date
-h, --help            Display this help message

The above **options:** are for passing specific parameters to monitoring different activites the server. (e.g `./devopsfetch -p` or `--port`), (`./devopsfetch --80`)

## Logging

To check logging metrics carried out with the monitoring commands on the sever, kindly `cd` out of the current working directory to the root directory of your sever.

`cd /var/log/devopsfetch.log`

The command above output the metrics on the server. In other words its a path to get historical data of activites on the server.