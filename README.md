# Notes on Daily-used command

## Pack management

- install deb package

  ```bash
  sudo dpkg -i xxx
  ```

- uninstall package

  ```bash
  sudo dpkg -r xxx
  ```

## Development environment setting

- set python environment variable

  ```bash
  export PYTHONPATH="$PYTHONPATH:/path"
  ```

- print python environment variable

  ```python
  import os
  print(os.sys.path)
  ```

- Check environment variable

  ```bash
  env
  ```

- virtual enviroment

  ```bash
  # for Python 2.7
  virtualenv --system-site-packages targetDirectory
  # for Python 3.n
  virtualenv --system-site-packages -p python3 targetDirectory 
  
  # activate environment
  source ./bin/activate
  
  # deactivate
  deactivate
  ```

  

## Hardware status

- check memory status

  ```bash
  free -m
  ```

- check GPU status

  ```bash
  nvidia-smi
  ```

- See all the processes

  ```bash
  ps -ef
  ```

- Check network status

  ```bash
  ifconfig
  ```



## SSH

- check ssh status

  ```bash
  ps -e | grep ssh
  ```

- start ssh

  ```bash
  /etc/init.d/ssh start 
  ```

- modify ssh configuration

  ```bash
  vim /etc/ssh/sshd_config
  ```

- check ssh user

  ```bash
  who
  ```

- kill user

  ```bash
  # get the user's PID
  ps aux |grep sshd 
  # kill by PID
  kill -pid
  ```

  

  

  

## User & Permissions Management

## Disk Management

- check mounted disk

  ```bash
  sudo df -l
  ```

- check Partition Status

  ```bash
  sudo fdisk -lu
  ```

- Manual Mount on the disk

  ```
  sudo mount -t ext4 /dev/sdc2 /devdata
  ```

  sdc2 is the partition which contains large dataset including imagenet or so.

  

## SHELL

- change shell

  ```bash
  sudo chsh
  ```

  