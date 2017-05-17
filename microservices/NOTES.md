## Schedule
http://bit.ly/2pIAdSN


## Cluster
Login:
bootstrapuser/deleteme

Team Asterix
Dashboard:
http://workshop-elasticl-1wl4lysyb106c-34440364.eu-central-1.elb.amazonaws.com/
Public Slave LB DNS:
http://workshop-publicsl-lk4n4mxw3dqv-525904624.eu-central-1.elb.amazonaws.com/
Public Slave IP:
35.156.242.187



curl https://downloads.dcos.io/binaries/cli/linux/x86-64/dcos-1.9/dcos -o dcos &&
sudo mv dcos /usr/local/bin &&
sudo chmod +x /usr/local/bin/dcos &&
dcos config set core.dcos_url https://workshop-elasticl-1wl4lysyb106c-34440364.eu-central-1.elb.amazonaws.com &&
dcos auth login &&
dcos


## Service discovery
* Meoss-DNS - legacy
* virtual IPs - distributed load balancer - Minuteman - level 4 load balacner
  * layer 4 - for each request we load balance once
  * layer 7 - load balance at first req (sessions, next requests to same node + other features) - more costly to maintain, less scalable
* 
