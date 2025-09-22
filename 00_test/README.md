# Ansible Vault를 이용한 비밀 데이터 관리 🔐
## 📖 프로젝트 개요
이 프로젝트는 Ansible Vault를 사용하여 민감한 데이터(예: 비밀번호, API 키)를 암호화하고 관리하는 방법을 다룹니다. secret 파일에 저장된 암호화된 변수들을 vault-pass 파일에 있는 비밀번호로 복호화하여 플레이북에서 안전하게 사용하는 과정을 보여줍니다.

## 🚀 주요 학습 내용
+ Ansible Vault: 민감한 데이터를 암호화하여 플레이북에 포함시키는 보안 기능을 학습합니다.

+ 비밀번호 파일: vault-pass 파일에 비밀번호를 저장하여, 플레이북 실행 시 비밀번호를 수동으로 입력할 필요 없이 자동으로 인증하는 방법을 익힙니다.

+ 암호화된 변수 사용: 암호화된 .yml 파일에 정의된 변수들을 플레이북에서 불러와 사용하는 방법을 실습합니다.

## 📂 프로젝트 파일 구조
```bash
.
├── vault-pass
├── secret1.yml
├── secret2.yml
└── secret3.yml
```
+ vault-pass: ansible-vault를 사용할 때 필요한 비밀번호를 저장하는 파일입니다.

+ secret1.yml~secret3.yml: Ansible Vault로 암호화된 YAML 파일들로, 민감한 변수들을 포함하고 있습니다.

## 🛠️ 실행 방법
암호화된 파일 보기:
+ ansible-vault view secret1.yml 명령과 vault-pass 파일을 사용하여 암호화된 내용을 확인할 수 있습니다.

Bash

```bash
ansible-vault view secret1.yml --vault-password-file vault-pass
```
플레이북 실행:
ansible-playbook 명령에 --vault-password-file 옵션을 추가하여, 암호화된 파일에 접근하는 플레이북을 실행합니다.

### 플레이북 예시 (secret1.yml을 사용하는 플레이북)
Bash
```bash
ansible-playbook your-playbook.yml --vault-password-file vault-pass
```
