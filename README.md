# Description

This is a collection of plugins for use with Munin to report metrics appropriate for the Caddy webserver.

They all communicate with the caddy API, and make the assumption that the API is running on localhost:2019

Pull requests welcome.

# Plugins 

## caddy_process_fd_count

Reports how many open files caddy has.

## caddy_upstream_proxy

Reports on how many of each configured upstream are healthy.

## caddy_site_activity

Counts the number of hits for each site, grouping the hits by status. Requires read access to the logs. The easiest way is to run this plugin as the caddy user, e.g.

```
[caddy_*`]
user caddy
```


# Installation

 * Copy these files to your machine(s) running caddy, for example in /usr/local/share/munin/plugins
 * Make symlinks to these files in /etc/munin/plugins
 * Then restart the munin-node service.
