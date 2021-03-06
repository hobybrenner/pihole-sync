# pihole-sync

## Introduction
This script is meant to keep 2 PiHole instances in sync. One node is designated as the master and the other node is the slave. All maintenance (adding blocklists, adding entries to whitelist/blacklist/regex) should be done on the master node. The master node will upload its files to a central file server (locally mounted on both nodes), and the slave node will download those files to keep in sync. All activity of the script is written to a log file which is also uploaded to the file server, and is written to local syslog.

### Usage
Copy pihole_sync.sh to the folder of your choice on both PiHole nodes. Update the options in the configuration section. Setup a cron job to run the script as often as you'd like. I recommend a minimum sync interval of every 15 minutes.
