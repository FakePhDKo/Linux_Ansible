# Ansible: 3-Tier 웹 애플리케이션 구축 🌐
## 📖 프로젝트 개요
이 프로젝트는 Ansible을 사용하여 3-Tier 아키텍처를 자동으로 구축하는 플레이북을 다룹니다. 웹 서버(Apache), 애플리케이션 서버(PHP), 그리고 데이터베이스 서버(MariaDB)를 단일 플레이북으로 설정하고, 이 과정을 효율적으로 복원하는 방법을 익힙니다.

## 🚀 주요 학습 내용
+ 3-Tier 아키텍처 자동화: webservers 호스트 그룹에 Apache, PHP, MariaDB를 동시에 설치하고 연동하는 방법을 배웁니다.

+ 데이터베이스 보안 설정: community.mysql 모듈을 사용하여 익명 사용자 제거, 테스트 DB 삭제, 어플리케이션 계정 생성 등 MariaDB의 초기 보안 설정을 자동화합니다.

+ 원격 파일 관리: get_url 모듈을 사용하여 원격지의 index.php 파일을 관리 대상 서버로 가져오는 방법을 익힙니다.

+ 서비스 상태 검증: uri 모듈을 사용해 index.php가 정상적으로 서비스되고 있는지 확인하는 자동화된 테스트를 구현합니다.

+ 환경 복원: Restore-web-db.yml 플레이북을 통해 웹 애플리케이션의 모든 설정을 되돌려 서버를 초기 상태로 복원하는 과정을 학습합니다.

## 📂 프로젝트 파일 구조
+ 3-Tier-Architecture.yml: Apache 웹 서버, PHP, MariaDB를 설치하고 방화벽을 설정하며, MySQL의 보안 및 사용자 설정을 자동화하는 플레이북입니다.

+ Restore-web-db.yml: 3-Tier-Architecture.yml 플레이북으로 설정된 모든 내용을 되돌려, 서버를 초기 상태로 복원하는 플레이북입니다.

## 🛠️ 실행 방법
웹 애플리케이션 구축:

Bash
```bash
ansible-playbook 3-Tier-Architecture.yml
```
웹 애플리케이션 복원:

Bash
```bash
ansible-playbook Restore-web-db.yml
```
