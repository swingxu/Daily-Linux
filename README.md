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

- use natapp to ssh

  ~~~bash
  ./natapp -authtoken=c404277c2756bb08
  ~~~

  

  

## User & Permissions Management

* Access Permissions

  ~~~bash
  444 r--r--r--
  600 drw-------
  644 drw-r--r--
  666 drw-rw-rw-
  700 drwx------
  744 drwxr--r--
  755 drwxr-xr-x
  777 drwxrwxrwx
  # r-4 w-2 x-1
  ~~~

* List file/directory access permissions info

  ~~~bash
  ls -l xxx.xxx 
  # return filetype/user/group/other
  ~~~

  

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

pytorch 


## Shadowsocks

* enable local

  ~~~bash
   sslocal -c /home/yelab/shadowsocks.json
  ~~~




## Set tensorflow

* cuda environment 

  ~~~ bash
  export LD_LIBRARY_PATH=LD_LIBRARY_PATH:/usr/local/cuda-9.0/lib64/
  ~~~

  

