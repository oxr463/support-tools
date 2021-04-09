# logs-collector

The script needs to be downloaded and run directly on the node using the `root` user or using `sudo`.

## How to use

* Download the script and save as: `rancher_logs_collector.sh`
* Make sure the script is executable: `chmod +x rancher_logs_collector.sh`
* Run the script: `./rancher_logs_collector.sh`

The script will create a .tar.gz log collection in /tmp by default, all flags are optional.

## Flags

```
Rancher 2.x logs-collector
  Usage: rancher2_logs_collector.sh [ -d <directory> -s <days> -r <container runtime> -p -f -u -c <case number> -l <location> ]

  All flags are optional

  -d    Output directory for temporary storage and .tar.gz archive (ex: -d /var/tmp)
  -s    Number of days history to collect from container and journald logs (ex: -s 7)
  -r    Override container runtime if not automatically detected (docker|k3s)
  -p    When supplied runs with the default nice/ionice priorities, otherwise use the lowest priorities
  -f    Force log collection if the minimum space isn't available
  -u    Upload log collection archive via FTP
  -c    Case number, required for log uploading (ex: -c 00012345)
  -l    Location, required for log uploading (us|emea)
```

