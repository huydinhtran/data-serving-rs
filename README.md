# data-serving-gem5

Install Cassandra and OpenJDK 11 for both server and client
```bash
sudo apt-get update
sudo apt-get install cassandra openjdk-11-jdk-headless
```

Install python3-yaml for server only
```bash
sudo apt-get update
sudo apt-get install python3-yaml
```

On server machine, run this to start server
```bash
sudo python ./docker-entrypoint.py --listen-ip=192.168.1.2
```

On client machine, 
```bash
To warm server:
./warmup.sh <server_ip> <record_count> <threads=1>

To load server:
./load.sh <server_ip> <record_count> <target_load> <threads=1> <operation_count=load * 60>
```
