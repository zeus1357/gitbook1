---
description: 사용방법
---

# GitBook

### **1. nodejs 설치**

프로젝트에 따라서 Node의 버전을 어려개 설치하고, 번갈아 가면서 사용해야 할 경우가 있다.

그래서 nvm(node version manager)을 이용해서 원하는 node 버전을 골라서 사용할수 있다.\


#### **NVM 설치**

[https://github.com/coreybutler/nvm-windows/releases](https://github.com/coreybutler/nvm-windows/releases)

nvm-setup.zip 파일을 다운로드해 설치한다.

#### NVM 명령어

```
nvm list                rem 설치된 node 리스트 확인
nvm list available      rem 설치가능한 node 리스트 확인, 짝수버전이 안정된 버전
nvm install 16.14.2     rem 특정 버전의 node 설치
nvm use 16.14.2         rem 특정 버전의 node 사용
nvm remove 16.14.2      rem 특정 버전의 node 삭제
```

#### 설치된 node 확인

```
node --version
```

### **2. gitbook 설치**



```
mkdir my-gitbook
cd my-gitbook                      rem gitbook을 설치할 폴더 생성후 이동

npm install gitbook-cli -g         rem gitbook-cli 글로벌 설치 명령

gitbook -V                         rem gitbook 버전보기하면 설치 시작, ver 3.2.3

gitbook init                       rem 책 초기화
gitbook serve                      rem gitbook 시작
```

{% hint style="info" %}
itbook을 설치하면 gitbook의 종속된 graceful-fs에서 오류 발생이 됩니다.

graceful-fs의 최신버전에서는 해결이 됐으나 gitbook 참조버전이 예전버전이라 오류가 발생합니다.
{% endhint %}

\
아래 글로벌 gitbook-cli 폴더 위치에 수정된 파일을 덮어 씁니다.\


```
붙여넣기 :
C:\Users\user\AppData\Roaming\npm\
node_modules\gitbook-cli\node_modules\npm\node_modules\graceful-fs\polyfills.js  

복사 :
현재 패키지에 Patch\graceful-fs-4.2.9\polyfills.js
```

정상적으로 gitbook이 시작되면 http://localhost:4000(예) 사이트가 시작됩니다.



### **3. 출력물 변환(PDF/EPUB)**

Windows 패키지관리자 calibre 설치후 PDF 변

```
winget install calibre --exact          rem calibre 설치

gitbook pdf ./ ./mybook.pdf             rem mybook.pdf로 출력
gitbook epub ./ ./mybook.epub           rem mybook.epub로 출력
```

{% hint style="info" %}
**Good to know:** Splitting your product into fundamental concepts, objects, or areas can be a great way to let readers deep dive into the concepts that matter most to them.
{% endhint %}
