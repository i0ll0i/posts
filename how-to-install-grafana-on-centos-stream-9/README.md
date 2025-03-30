# How to Install Grafana on CentOS
Grafana is an open-source platform used for monitoring, visualizing, and analyzing metrics and logs from various data sources. It is widely used by IT teams, developers, and data analysts to track the performance of systems, applications and infrastructures in real time.
In the guide, we will look at how to install Grafana on CentOS Stream 9.
## How to Install Grafana on CentOS Stream 9
Since the Grafana repository is not included by default in CentOS Stream, you need to manually add the official Grafana repository to your system’s repository list.
To do this navigate to the directory `/etc/yum.repos.d/`:
```
cd /etc/yum.repos.d/
```
Add the official Grafana repository by creating a new repository configuration file in the directory `/etc/yum.repos.d/`:
```
sudo vi grafana.repo
```
Add the following content to the file `grafana.repo`:
```
[grafana]
name=grafana
baseurl=https://packages.grafana.com/oss/rpm
repo_gpgcheck=1
enabled=1
gpgcheck=1
gpgkey=https://packages.grafana.com/gpg.key
```
Save the file and exit.
Update the package list:
```
sudo dnf update
```
Install Grafana:
```
sudo dnf install grafana
```
Continued on the [iolloi.icu](https://iolloi.icu/index.php/2024/09/19/how-to-install-grafana-on-centos-stream-9/)
