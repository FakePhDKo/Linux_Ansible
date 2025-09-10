# Ansible Study Repository
## 📖 프로젝트 개요
이 저장소는 Ansible의 다양한 기능과 개념을 학습하고 실습한 내용을 정리한 공간입니다. 플레이북 작성부터 고급 기능, 역할 및 컬렉션 관리에 이르기까지 Ansible의 핵심적인 내용을 단계별로 구성했습니다.

## 🚀 프로젝트 기술 스택
### 📂 주요 학습 내용
이 저장소는 Ansible의 학습 과정을 체계적으로 구성하기 위해 디렉터리 이름에 번호를 매겨 순서를 정리했습니다.

```
.vscode: Visual Studio Code 편집기 설정 파일입니다.

00_test: 테스트 및 실습을 위한 파일들이 포함되어 있습니다.

01_test/myrole: 역할(Role)을 생성하고 사용하는 방법에 대한 실습 내용입니다.

03_adhoc: 애드혹(Ad-hoc) 명령어를 사용해 yum_repository를 설정하는 방법을 다룹니다.

03_inventory: Ansible의 인벤토리 파일과 그룹 관리에 대한 실습 내용입니다.

03_manage: 여러 서버를 효율적으로 관리하기 위한 기본 설정과 명령어들을 다룹니다.

04_multi: 멀티 플레이를 포함하는 플레이북 작성 방법을 학습합니다.

04_playbook: 플레이북의 기본적인 구조와 실행 방법을 다룹니다.

04_web-db: 웹 서버와 데이터베이스를 함께 구성하는 플레이북 실습 내용입니다.

05_dev-vars-facts: 개발 환경의 변수와 사실(Facts) 변수 사용법을 학습합니다.

05_epel: EPEL(Extra Packages for Enterprise Linux) 저장소를 설정하는 실습 내용입니다.

05_exec-ansible-vault: ansible-vault를 사용해 암호화된 파일을 실행하는 방법을 다룹니다.

05_facts: Ansible의 사실(Facts) 변수에 대한 실습 내용입니다.

05_host_group_vars: 호스트 변수와 그룹 변수 파일을 구성하는 방법을 다룹니다.

05_hwreport: 하드웨어 보고서를 생성하고 수집하는 실습 내용입니다.

05_secret: ansible-vault를 사용해 비밀번호를 관리하는 실습 내용입니다.

05_simple_magic: Ansible의 매직 변수(Magic Variables)에 대한 실습 내용입니다.

05_variables: 플레이북에서 변수를 선언하고 사용하는 방법을 다룹니다.

05_variables_facts: 변수와 사실(Facts) 변수를 함께 활용하는 실습 내용입니다.

05_vars-inclusions: vars_files와 include_vars를 사용해 변수를 포함하는 방법을 학습합니다.

06_hosts: 호스트 파일 관리와 관련된 실습 내용입니다.

06_job_control: block, rescue, always를 활용한 작업 제어에 대한 실습 내용입니다.

06_job_control_review: 작업 제어와 관련된 내용을 복습하는 실습입니다.

06_notify_handlers: notify와 handlers를 사용해 서비스 재시작을 자동화하는 실습 내용입니다.

06_when_loop: when 조건문과 loop 구문을 함께 사용하는 실습 내용입니다.

07_files: copy, template 등 파일을 배포하는 모듈에 대한 실습 내용입니다.

07_template-hosts: template 모듈을 사용해 동적으로 hosts 파일을 생성하는 실습 내용입니다.

07_template-motd: motd 파일을 동적으로 생성하는 실습 내용입니다.

07_template-ps1: 터미널 프롬프트(PS1)를 동적으로 설정하는 실습 내용입니다.

07_usersetting: 사용자 환경을 동적으로 설정하는 실습 내용입니다.

09_role-collections: 역할과 컬렉션의 관계를 이해하고 사용하는 실습 내용입니다.

09_roles: 역할의 기본 개념과 사용법을 다룹니다.

09_roles_create: ansible-galaxy를 사용해 역할을 생성하는 실습 내용입니다.

09_roles_download: Ansible Galaxy에서 역할을 다운로드하고 설치하는 실습 내용입니다.
```

## ⚙️ 환경 설정 및 실행 방법
+ SSH 키 등록: GitHub에 SSH 공개 키를 등록하여 비밀번호 입력 없이 git 명령어를 사용할 수 있도록 설정합니다.

+ 클론: git clone git@github.com:FakePhDKo/Ansible_Study.git 명령어를 사용해 저장소를 복제합니다.

플레이북 실행:

Bash
```
cd Ansible_Study
ansible-playbook playbook.yml --ask-vault-password
--ask-vault-password # 옵션은 암호화된 파일에 접근하기 위해 필요할 수 있습니다.
```
