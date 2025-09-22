# Ansible: 서버 종료 플레이북 💻
## 📖 프로젝트 개요
이 프로젝트는 Ansible을 사용하여 원격 서버와 제어 노드(Control Node)를 안전하게 종료하는 플레이북을 작성하고 실행하는 실습입니다. community.general.shutdown 모듈과 ansible.builtin.command 모듈을 사용하여 관리 대상 호스트들을 제어하는 방법을 보여줍니다.

## 🚀 주요 학습 내용
+ 원격 서버 종료: hosts: all을 대상으로 community.general.shutdown 모듈을 사용하여 모든 관리 대상 서버를 종료합니다. delay: 0 옵션은 즉시 종료를 의미합니다.

+ 제어 노드 종료: hosts: localhost를 대상으로 ansible.builtin.command 모듈을 사용하여 플레이북을 실행하는 제어 노드 자신을 종료합니다.

+ 오류 무시: ignore_errors: true 옵션을 사용하여, 서버 종료 실패와 같은 오류가 발생하더라도 플레이북이 멈추지 않고 계속 진행되도록 설정했습니다.

## 📂 프로젝트 파일 구조

Bash
```bash
.
├── controlnode.yml
└── targethost.yml
```
+ targethost.yml: 인벤토리에 등록된 모든 서버를 종료하는 플레이북입니다.

+ controlnode.yml: 플레이북을 실행하는 제어 노드 자신을 종료하는 플레이북입니다.

## 🛠️ 실행 방법
원격 서버 종료:

Bash
```bash
ansible-playbook targethost.yml
```
제어 노드 종료:

Bash
```bash
ansible-playbook controlnode.yml
```
