# Notes of Ubuntu 20.04

## 1. Source:

1. Terminal:

   ```bash
   sudo gedit /etc/apt/sources.list
   ```

2. Copy:

   ```bash
   deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ eoan main restricted universe multiverse
   deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ eoan main restricted universe multiverse
   deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ eoan-updates main restricted universe multiverse
   deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ eoan-updates main restricted universe multiverse
   deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ eoan-backports main restricted universe multiverse
   deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ eoan-backports main restricted universe multiverse
   deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ eoan-security main restricted universe multiverse
   deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ eoan-security main restricted universe multiverse
   deb https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ eoan-proposed main restricted universe multiverse
   deb-src https://mirrors.tuna.tsinghua.edu.cn/ubuntu/ eoan-proposed main restricted universe multiverse
   deb https://typora.io/linux ./
   # deb-src https://typora.io/linux ./
   ```

3. Terminal

   ```bash
   sudo apt-get update
   sudo apt-get upgrade
   ```

## 2. Typora

1. Terminal

   ```bash
   sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys BA300B7755AFCFAE
      
   # add Typora repository
   sudo add-apt-repository 'deb https://typora.io/linux ./'
   sudo apt-get update
      
   # install Typora
   sudo apt-get install typora
   ```

2. Run

   ```bash
   sudo gedit .bashrc   # add: alias typora="/opt/Typora-linux-x64/Typora"
   source .bashrc       # refresh
   ```

## 3. Git

1. Terminal

   ```bash
   git checkout
   git pull
   git add -A
   git commit -m "commit"
   git push --all
   ```

## 4. Docker

1. Curl

   ```bash
   $ sudo apt-get install libcurl4=7.65.3-1ubuntu3
   $ sudo apt-get install curl
   ```

2. Dependencies

   ```bash
   $ sudo apt-get install \
       apt-transport-https \
       ca-certificates \
       curl \
       gnupg-agent \
       software-properties-common
   ```

3. Key

   ```bash
   $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
   ```

4. Repoository

   ```bash
   $ sudo add-apt-repository \
   "deb [arch=amd64] https://mirrors.aliyun.com/docker-ce/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
   ```

5. Docker Engine

   ```bash
   $ sudo apt-get update
   $ sudo apt-get install docker-ce docker-ce-cli containerd.io
   ```

6. Check

   ```bash
   $ apt-cach madison docker-ce
   $ sudo docker run hello-world
   ```


7. Usermod

   ```bash
   $ sudo usermod -aG docker [username]
   $ sudo systemctl restart docker
   $ reboot
   ```

## 5. Python

1. pip

   ```bash
   python3 --version #check python3
   sudo apt-get install python3-pip
   pip3 --version #check pip3
   ```

2. alpine

   ```bash
   # for "no module named setuptools"
   sudo apt-get install python3-pkg-resources=41.1.0-1
   sudo apt-get install python3-setuptools
   pip3 install alpine
   ```

3. pycharm

   ```bash
   # download and install step by step from the official website
   # or you can refer [1] in chinese
   sudo apt-get install python3-distutils # may not necessary
   ```

4. anaconda

   ```bash
   # download Anaconda3-2020.02-linux-x86_64.sh from the official website
   bash Anaconda3-2020.02-Linux-x86_64.sh
   # restart the terminal
   python3
   ```

   



> References

[1] https://www.jb51.net/article/185785.htm

[2] 

[FATFOO](https://github.com/snowyben)

<div class="footer">
&copy; 2018 FatFoo Corporation
</div>

