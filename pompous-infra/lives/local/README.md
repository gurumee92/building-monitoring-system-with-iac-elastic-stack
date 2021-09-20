# 로컬 인프라스트럭처 구축

## 요구 사항

각 컴포넌트는 다음 버전에 호환되는 버전이어이야 한다.

* Virtualbox 6.1
* Vagrant 2.2.18

## 인프스트럭처 구성

실행 환경 `lives/local`이 구성하는 인프라스트럭처는 다음과 같다.

모두 `CentOS 8` 버전을 실행한다.

## 명령어

`vagrant`를 통해서 로컬 인프라스트럭처를 구성할 수 있다. 필수적인 명령어는 아래를 참고하자.

### 인프라스트럭처 구축

다음 명령어로 인프라스트럭처를 구성할 수 있다.

```bash
$ vagrant up
```


또한 머신 이름을 붙여서 특정 머신만 실행할 수도 있다.

```bash
# vagrant up <머신 이름>
$ vagrant up mysql
```

### 인프라스트럭처 VM 상태 확인

현재 실행되는 `VM`들의 상태를 확인할 수 있다.

```bash
$ vagrant status
Current machine states:

es-master                 running (virtualbox)
es-data01                 running (virtualbox)
es-data02                 running (virtualbox)
agent01                   running (virtualbox)
agent02                   running (virtualbox)
logstash                  running (virtualbox)
kibana                    running (virtualbox)
mysql                     running (virtualbox)

This environment represents multiple VMs. The VMs are all listed
above with their current state. For more information about a specific
VM, run `vagrant status NAME`.
```

특정 `VM` 상태를 확인하고 싶다면, `VM`의 이름을 입력하면 된다.

```bash
# vagrant status <머신 이름>
$ vagrant status mysql
Current machine states:

mysql                     running (virtualbox)

The VM is running. To stop this VM, you can run `vagrant halt` to
shut it down forcefully, or you can run `vagrant suspend` to simply
suspend the virtual machine. In either case, to restart it again,
simply run `vagrant up`.
```

### VM SSH 접속

다음 명령어로 특정 `VM`에 `SSH` 접속할 수 있다.

```bash
# vagrant ssh <머신 이름>
$ vagrant ssh mysql
[vagrant@mysql ~]$ 
```

접속 해제하려면 `exit` 명령어를 입력해야 한다.

### 인프라스트럭처 VM 종료

모든 `VM`의 실행을 종료하고 싶다면 다음 명령어를 사용하면 된다.

```bash
$ vagrant halt
```

또한, 머신 이름을 붙여서 특정 머신만 종료시킬 수 있다.

```bash
# vagrant halt <머신 이름>
$ vagrant halt mysql
```

### 인프라스트럭처 삭제

현재 구성된 인프라스트럭처를 모두 삭제할 수 있다. 

```bash
$ vagrant destroy
```

이 후 모두 "y"를 입력해주어야 한다.