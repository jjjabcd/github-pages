---
layout: post
title: "Ubuntu에서 Miniconda 설치"
date: 2025-03-18
categories: [linux]
tags:
  - ubuntu
  - miniconda
  - environment
description: "Miniconda 설치."
---

# Ubuntu에서 Miniconda 설치

Ubuntu 환경에서 Python 개발 환경을 구축하기 위한 간편한 방법 중 하나인 Miniconda 설치 방법을 정리한 예시입니다. 이 가이드는 SSH 접속 후 터미널을 통해 진행하는 것을 전제로 하며, Miniconda를 설치하면 이후 필요한 패키지 및 개발 환경 구성이 훨씬 수월해집니다.


## Miniconda란?

Miniconda는 Anaconda의 경량 버전으로, 기본적인 Python 실행 환경과 Conda 패키지 관리 도구만 포함하고 있습니다. 필요에 따라 필요한 패키지들을 개별적으로 설치할 수 있으므로, 가볍고 유연한 개발 환경을 구성할 수 있습니다.

## Miniconda 설치 단계


### Step 1: 설치 스크립트 다운로드

Miniconda 설치 스크립트를 공식 웹사이트에서 다운로드합니다. 예를 들어, 최신 버전의 Miniconda3 Linux용 설치 스크립트를 다운로드하는 명령어는 다음과 같습니다.

```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
```

### Step 2: 설치 스크립트 실행 권한 부여

다운로드한 스크립트에 실행 권한을 부여합니다.

```bash
chmod +x Miniconda3-latest-Linux-x86_64.sh
```

### Step 3: 설치 스크립트 실행

스크립트를 실행하여 Miniconda를 설치합니다. 스크립트 실행 시 설치 경로 및 라이선스 동의에 관한 질문이 나타납니다.

```bash
bash ./Miniconda3-latest-Linux-x86_64.sh
```

- License 동의: yes 입력
- 설치 경로 지정: 기본 경로를 사용하면 Enter키를 누르고, 원하는 경로를 지정
(예: /home/username/miniconda3)
- yes

### Step 4: 터미널 재시작

터미널을 재시작해야 base로 가상환경이 재부팅됩니다.

```bash
source ~/.bashrc
```

## Miniconda 사용 시작하기

---

설치가 완료 및 터미널 재부팅까지 했다면, Conda 환경을 활성화하고 기본적인 패키지 설치 등을 진행할 수 있습니다.

### Conda 버전 확인

```bash
conda --version
```

### 새로운 Conda 환경 생성

```bash
conda create -n myenv python=3.9
```

위 명령어를 실행하면 다음과 비슷한 화면이 나온다.

![스크린샷 2025-03-18 17.46.11.png](assets\2025-03-18-linux-conda\fig1.png)

설치되는 패키지들을 확인하고, y를 누르면 설치가 완료된다.

![스크린샷 2025-03-18 17.46.46.png](assets\2025-03-18-linux-conda\fig2.png)

설치가 완료되면 다음과 같은 안내 문구가 뜨게 된다.

y를 누르지 않아도 되는 상황에선 다음과 `-y`옵션을 사용해 바로 설치 되게 할 수 있다.

```bash
conda create -n test python -y
```

### 생성한 환경 활성화

```bash
conda activate myenv
```

활성화 한 후, (base)가 (myenv) 혹은 가상환경 이름으로 바뀌었는지 꼭 확인해야됩니다.

![스크린샷 2025-03-18 17.49.01.png](assets\2025-03-18-linux-conda\fig3.png)


### 다음글

[Conda 가상환경에 라이브러리 설치](Conda%20%EA%B0%80%EC%83%81%ED%99%98%EA%B2%BD%EC%97%90%20%EB%9D%BC%EC%9D%B4%EB%B8%8C%EB%9F%AC%EB%A6%AC%20%EC%84%A4%EC%B9%98%201baee3c1d96b80f9bce3e1ee86f18757.md) 

### [참고자료]

---

https://soundprovider.tistory.com/entry/Miniconda-Ubuntu%EC%97%90-Miniconda-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0

https://velog.io/@cosmos42/Ubuntu-22.04-miniconda-install-in-Ternimal

---

[제목 없음](Ubuntu%EC%97%90%EC%84%9C%20Miniconda%20%EC%84%A4%EC%B9%98/%EC%A0%9C%EB%AA%A9%20%EC%97%86%EC%9D%8C%201b4ee3c1d96b8062a1a9ed9a40b26611.csv)

---

<aside>
⚙ 　｜　[Main Page](https://www.notion.so/Jin-s-Study-194ee3c1d96b80a2b0cce212cc8d597e?pvs=21)　｜　[Category](https://www.notion.so/194ee3c1d96b8190b180c83ff97a5f40?pvs=21)　｜　 [Tags](https://www.notion.so/194ee3c1d96b81e98e40ce44821c019d?pvs=21)　｜　[About Me](https://www.notion.so/About-Me-194ee3c1d96b81878ad7c01e4598e60e?pvs=21)　｜　[Contact](https://www.notion.so/Contact-194ee3c1d96b815fbf95f262b2ade489?pvs=21)　｜

</aside>