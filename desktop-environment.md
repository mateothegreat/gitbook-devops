# Desktop Environment Setup

[![asciicast](https://asciinema.org/a/uB6fukBhwP33fe4Z2MdYIILH8.png)](https://asciinema.org/a/uB6fukBhwP33fe4Z2MdYIILH8)

### Install the epel-release
The epel-release package will configure the epel repository for yum.

> Extra Packages for Enterprise Linux (or EPEL) is a Fedora Special Interest Group that creates, maintains, and manages a high quality set of additional packages for Enterprise Linux, including, but not limited to, Red Hat Enterprise Linux (RHEL), CentOS and Scientific Linux (SL), Oracle Linux (OL).

```
yum install -y epel-release
```

### Use yum groups install the desktop environment

You can use yum groups to easily install a wide range of packages and desktop environments. Run `you grouplist` to see your available options.

```
yum groupinstall Xfce
```

### Update firewall
We need to allow RDP port 3389 on the local firewall.

_Note: You may also need to update your firewall rules if you're using a cloud provider (AWS, Google, Azure, etc..)_

```
firewall-cmd --permanent --add-port=3389/tcp
firewall-cmd --reload
```

### Connecting to your desktop
Simply open up your Remote Desktop Connection Client and connect to the host/ip of your new box.
Your username and password will be the values we previously set.