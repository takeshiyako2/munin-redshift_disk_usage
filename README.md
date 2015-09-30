# munin-redshift_disk_usage

This is munin plugin of redshift desk usage check.

# how to set up

1) install pg by gem

```
gem install pg
```


2) set plugin-conf.d/redshift

```
# vim /etc/munin/plugin-conf.d/redshift
[redshift*]
env.host xxxxxxx.ap-northeast-1.redshift.amazonaws.com
env.port 5439
env.user admin
env.password xxxxxx
env.dbname xxxxxx
```

3) put this plugin script to plugins dir

```
/usr/share/munin/plugins/redshift_rtb_bid_response
```

4) make link

```
# ln -s /usr/share/munin/plugins/redshift_disk_usage /etc/munin/plugins/redshift_disk_usage
```

5) run test

```
# cd /etc/munin/plugins
# munin-run redshift_disk_usage
usage.value 23
```


