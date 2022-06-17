# VScode-Settings
tj/n, ESLint, Prettier, typescript, extensions


### VSCode JavaScript Development Setup
||Formatting|Linting|Type checking|
|:----:|:-----:|:--------:|:-------:|
|Package|Prettier|ESLint|typescript|
|Additional <br> dependencies||eslint-config-airbnb-base <br> eslint-config-prettier <br> eslint-plugin-import <br> eslint-plugin-node |@types/node|
|Config file|.prettierrc|.eslintrc.js|jsconfig.json|
|VSCode<br>Extensions install|O|O|X|
<br>

------------
#### 0. Install Homebrew
###### 단. npm 설치 된 경우 다음 단계로
https://brew.sh/
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
<br>

------------
#### 1. Install n
https://github.com/tj/n
```
brew install n
```
```
npm install -g n  // npm 설치된 경우
```
&nbsp;&nbsp;1-1. 환경변수 설정(해당 쉘에 맞게 설정)
```
vi ~/.zshrc

// 맨 하단에 작성 후 저장
export N_PREFIX=$HOME/.n
export PATH=$N_PREFIX/bin:$PATH
```
&nbsp;&nbsp;1-2 package.json 생성
```
npm init -y
```
<br>

--------------
#### 2. Install Prettier
```
npm install -D prettier
```
&nbsp;&nbsp; 2-1. Prettier 환경설정
```
.prettierrc 생성

// 필요한 옵션에 따라서 적용시키면 된다
{
  "semi": false,
  "singleQuote": false
}
```
&nbsp;&nbsp; 2-2. vsCode 환경설정(local Setting)
```
.vscode/settings.json 생성(현재 프로젝트에서만 유효)

{
  "[javascript]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  }
}
```
&nbsp;&nbsp; 2-3. vsCode Prettier Extension 설치
<br>

--------------------
#### 3. Install ESLint
```
npm install -D eslint
```
&nbsp;&nbsp; 3-1. 
```
install -D eslint-config-airbnb-base, eslint-plugin-import
install -D eslint-prettier
install -D eslint-plugin-node
```
&nbsp;&nbsp; 3-2. ESLint 환경설정
```
.eslintrc.js 생성
module.exports = {
  extends: ["airbnb-base", "prettier"]
}
```
&nbsp;&nbsp; 3-3. vsCode ESLint Extension 설치
<br>

--------------------
#### 4. Install TypeScript
```

```
