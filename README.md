# mx-indexer

The indexer is just a basic `opensearch` setup. To start it just run `docker compose up -d`. Default credentials are `admin:admin`.

# Setup

Before using this repo, make sure you increase the amount of memory maps available on your host.

```sh
# Edit the sysctl config file
sudo vi /etc/sysctl.conf

# Add a line to define the desired value
# or change the value if the key exists,
# and then save your changes.
vm.max_map_count=262144

# Reload the kernel parameters using sysctl
sudo sysctl -p

# Verify that the change was applied by checking the value
cat /proc/sys/vm/max_map_count
```

# PORTS

- `opensearch`: `9200`
- `kibana`: `5601`
