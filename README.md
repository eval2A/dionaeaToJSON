# dionaeaToJSON
Version: 0.1<br>
Scripted for: Dionaea 0.8.0<br>
<br>
### Description:
Converts the SQLite database produced by Dionaea to a JSON format suitable for the ELK stack.<br>
The JSON log files includes details about connections, downloads, logins, SQL commands, etc.<br>
<br>
### Requirements for running the script:
 • Python 3<br>
 • SQLite logging enabled in Dionaea<br>
<br>
This script is meant to run every minute as a cronjob. However, it may be a little heavy to run this script the first time, so it is advised that this is done manually. This is what you should put in your crontab, it will make the script run every minute:<br>
*/1 * * * * /usr/bin/python3 /path/to/dionaeaSqliteToJson.py <br>
<br>
### Default paths
Path for the sqlite dabase file of Dionaea:<br>
/opt/dionaea/var/dionaea/dionaea.sqlite<br>
<br>
Path for the JSON log files produced by this script:<br>
/opt/dionaea/var/dionaea/json<br>
<br>
Path for the binaries captured by Dionaea (to remove HTML files):<br>
/opt/dionaea/var/dionaea/binaries<br>
<br>
If these paths don't correspond to your setup, change the script.<br>
