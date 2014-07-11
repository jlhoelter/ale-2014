## Infrastructure Setup

### Build Server

The following Software is installed on the build server.

* Jenkins Server (Master)
* Jenkins Slave
* Nginx
* Sonar
* Nexus

### Installation

#### Jenkins Server

Install Jenkins Server including Plugins.

```
sudo puppet module install rtyler-jenkins
sudo puppet apply puppet/jenkins.pp
```

#### Nginx

Install Nginx as Proxy Server for Jenkins, Nexus and Sonar.

```
sudo puppet module install jfryman-nginx
sudo puppet apply puppet/nginx.pp
sudo cp puppet/proxy.conf /etc/nginx/conf.d/proxy.conf  
```


