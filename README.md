# IaC 도구로 만들어보는 모니터링 시스템 (Elastic Stack)

## 목차

1. 로컬에서 모니터링 시스템 구축하기
   1. Virtualbox, Vagrant로 인프라스트럭처 구성하기
   2. Ansible로 모니터링 시스템 구축하기
2. AWS에서 모니터링 시스템 구축하기 (1)
   1. Terraform으로 정적 인프라스트럭처 구성하기
   2. Ansible로 모니터링 시스템 구축하기
3. AWS에서 모니터링 시스템 구축하기 (2)
   1. Ansible, Packer로 이미지 템플릿 구성하기
   2. Ansible, Terraform으로 동적 인프라스트럭처에 모니터링 시스템 구축하기
4. 쿠버네티스에서 모티너링 시스템 구축하기 (1)
   1. Virtualbox, Vagrant로 인프라스트럭처 구성하기
   2. Ansible로 쿠버네티스 클러스터 구성하기
   3. Ansible, Packer로 Docker 이미지 구성하기
   4. Ansible, Terraform으로 Kubernetes에 모니터링 시스템 구축하기
5. 쿠버네티스에서 모티너링 시스템 구축하기 (2)
   1. AWS에서 쿠버네티스 클러스터 구성하기
   2. Ansible, Terraform으로 Kubernetes에 모니터링 시스템 구축하기


## 요구 사항

각 컴포넌트가 다음 버전과 호환되어야 한다.

* Virtualbox 6.1
* Vagrant 2.2.18
* Ansible 2.11.4 (Python 3.9)
* Terraform 1.0.6
* Packer 1.7.0

또한, 다음 이상의 머신 스펙을 필요로 한다.

* Machine: MacOS pro 
* OS: Big Sur 11.2.3
* Processor: 2.6 GHz 6코어 Intel Core i7
* Memory: 16GB 2667 MHz DDR4
* Graphic: AMD Radeon Pro 5300M 4 GB, Intel UHD Graphics 630 1536 MB