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

## 4. Todo

1. todo







> References

[1] 

[2] 

[FATFOO](https://github.com/snowyben)

<div class="footer">
&copy; 2018 FatFoo Corporation
</div>

