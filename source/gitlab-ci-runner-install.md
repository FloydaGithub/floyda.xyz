---
title: Gitlab CI Runner Install  
tags: ["gitlab", "ci"]  
excerpt: Gitlab CI Runner Install  
date: 2020-1-19  
---

# Gitlab CI Runner Install  
> [Doc Runner Install](https://docs.gitlab.com/runner/install/linux-repository.html)  


1. Add GitLab’s official repository:  

```sh
# For Debian/Ubuntu/Mint
curl -L https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.deb.sh | sudo bash

# For RHEL/CentOS/Fedora
curl -L https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.rpm.sh | sudo bash
```

2. Install the latest version of GitLab Runner, or skip to the next step to install a specific version:  

```sh
# For Debian/Ubuntu/Mint
sudo apt-get install gitlab-runner

# For RHEL/CentOS/Fedora
sudo yum install gitlab-runner
```

3. To install a specific version of GitLab Runner:  

```sh
# for DEB based systems
apt-cache madison gitlab-runner
sudo apt-get install gitlab-runner=10.0.0

# for RPM based systems
yum list gitlab-runner --showduplicates | sort -r
sudo yum install gitlab-runner-10.0.0-1
```

4. [Register the Runner](https://docs.gitlab.com/runner/register/index.html)  


# Error  

- 确认`gitlab-runner`是否安装
```sh
systemctl status gitlab-runner
```
