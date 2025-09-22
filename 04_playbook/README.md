# Ansible: 웹 서버 설치 및 복원 플레이북 🌐
## 📖 프로젝트 개요
이 프로젝트는 Ansible을 사용하여 웹 서버(Apache)를 자동으로 설치하고 설정하는 플레이북과, 그 설정을 초기 상태로 되돌리는 복원 플레이북을 다룹니다. yum, service, firewalld와 같은 핵심 모듈을 사용해 서버를 효율적으로 관리하는 방법을 보여줍니다.

## 🚀 주요 학습 내용
+ 웹 서버 자동 설치: yum 모듈로 httpd 및 firewalld 패키지를 설치하고, copy 모듈로 웹 페이지를 설정하는 방법을 익힙니다.

+ 서비스 및 방화벽 관리: service 모듈을 사용해 httpd와 firewalld 서비스를 기동하고, firewalld 모듈로 http 서비스를 방화벽에 영구적으로 등록하는 방법을 학습합니다.

+ 플레이북 복원: Restore_site.yml 플레이북을 통해 웹 서버의 설정, 서비스, 패키지까지 모든 변경 사항을 되돌리는 자동화된 복원(Restore) 과정을 다룹니다.

## 📂 프로젝트 파일 구조
+ intranet.yml: webservers 그룹에 속한 서버에 Apache 웹 서버를 설치하고 설정하며 방화벽 규칙을 적용하는 플레이북입니다.

+ Restore_site.yml: intranet.yml 플레이북으로 설정된 모든 내용을 되돌려, 서버를 초기 상태로 복원하는 플레이북입니다.

## 🛠️ 실행 방법
웹 서버 설정:

Bash
```bash
ansible-playbook intranet.yml
```
웹 서버 복원:

Bash
```bash
ansible-playbook Restore_site.yml
```
