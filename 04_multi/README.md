# Ansible: 웹 서버 자동화 및 테스트 🌐
## 📖 프로젝트 개요
이 프로젝트는 Ansible을 사용하여 단일 웹 서버를 자동으로 설정하고, 테스트하며, 초기화하는 과정을 담고 있습니다. 웹 서버의 패키지 설치부터 방화벽 설정, 서비스 기동, 그리고 최종 웹 요청 테스트까지의 전 과정을 플레이북으로 자동화했습니다.

## 🚀 주요 학습 내용
+ 웹 서버 자동화: yum, systemd, firewalld 모듈을 사용하여 웹 서버를 한 번에 설치, 설정, 기동하는 방법을 익힙니다.

+ 플레이북 재사용: Restore_intranet.yml 플레이북을 통해 웹 서버를 처음 상태로 되돌리는 자동화된 정리(Cleanup) 과정을 학습합니다.

+ 상태 검증: uri 모듈을 사용하여 웹 서버가 정상적으로 응답하는지 확인하고, debug 모듈로 응답 내용을 출력하여 자동화된 테스트의 중요성을 이해합니다.

+ 루프(Loop) 활용: systemd 모듈에서 loop를 사용하여 여러 서비스를 한 번에 제어하는 효율적인 방법을 익힙니다.

## 📂 프로젝트 파일 구조
+ intranet.yml: web1.example.com 서버에 Apache 웹 서버를 설치, 설정하고 방화벽을 구성하는 플레이북입니다. 또한, uri 모듈을 사용해 웹 서버의 동작을 검증합니다.

+ Restore_intranet.yml: intranet.yml 플레이북으로 설정된 모든 내용을 되돌려, 서버를 초기 상태로 복원하는 플레이북입니다.

+ Restore_firewalld.yml: intranet.yml 플레이북으로 설정된 방화벽 규칙을 되돌려, 서버를 초기 상태로 복원하는 플레이북입니다.

## 🛠️ 실행 방법
웹 서버 설정 및 테스트:

Bash
```bash
ansible-playbook intranet.yml
```
웹 서버 초기화:

Bash
```bash
ansible-playbook Restore_intranet.yml
```
방화벽 규칙 제거:

Bash
```bash
ansible-playbook Restore_firewalld.yml
```
