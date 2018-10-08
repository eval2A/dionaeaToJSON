# dionaeaToJSON
Name: dionaeaToJSON
Version: 0.1
Scripted for: Dionaea 0.6.0

Description:
Converts the SQLite database produced by Dionaea to a JSON format suitable for the ELK stack.
The JSON log files includes details about connections, downloads, logins, SQL commands, etc.

Requirements for running the script:
Python 3
SQLite logging enabled in Dionaea

This script is meant to run every minute as a cronjob. However, it may be a little heavy
to run this script the first time, so it is advised that this is done manually.
This is what you should put in your crontab, it will make the script run every minute:
*/1 * * * * /usr/bin/python3 /path/to/dionaeaSqliteToJson.py
