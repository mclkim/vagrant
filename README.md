# Vagrant LAMP

## Description
웹 스택을 빠르게 구성해야 할 필요가 있을 뿐만 아니라 사용자 정의 할 수 있는 이 Vagrant 프로젝트를 시도해보십시오
Vagrant를 사용하면 가상 시스템을 신속하게 설치하고 사용하기 쉽습니다.
그리고 이 프로젝트는 단 몇 분 만에 완벽한 LAMP 스택을 쉽게 생성 할 수 있도록 하는 것을 목표로 합니다.

## Prerequisites

* [VirtualBox](http://www.virtualbox.org)
* [Vagrant](http://www.vagrantup.com)
* [Git](http://git-scm.com/)
* [Docker Box](https://docs.docker.com/toolbox/toolbox_install_windows/)(option)

## Usage

### Startup
```bash
$ mkdir homepage
$ cd homepage
$ git clone https://github.com/mclkim/vagrant.git 

$ cd vagrant
$ vagrant up
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Importing base box 'ubuntu/trusty64'...
==> default: Matching MAC address for NAT networking...
==> default: Checking if box 'ubuntu/trusty64' is up to date...

$ vagrant reload
==> default: Attempting graceful shutdown of VM...
    default:
    default: Vagrant insecure key detected. Vagrant will automatically replace
    default: this with a newly generated keypair for better security.
```

### Shutdown
```bash
$ vagrant halt
==> default: Attempting graceful shutdown of VM...
```

### Connecting

#### Apache
The Apache server is available at <http://localhost:8888>

#### MySQL
Externally the MySQL server is available at port 8889, and when running on the VM it is available as a socket or at port 3306 as usual.
Username: root
Password: root

And like any other vagrant file you have SSH access with
```bash
$ vagrant ssh
```
