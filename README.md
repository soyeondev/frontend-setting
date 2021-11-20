## frontend-setting ⚙
- vanillaJS를 사용하여 SPA를 구현하는 프로젝트를 위한 프론트엔드 설정 레포 입니다.  
- 사이드 프로젝트는 하고싶은데 매번 프로젝트를 설정하고자 하니 초반에 시간이 들어 빠른 시작을 위해 만들었습니다.
- Util이나 설정에서 유용한 것들이 있다면 채워나갈 계획입니다.

## ⏩ 설정 순서


### babel 설정
- npm package 설치
`npm i -D @babel/cli @babel/core @babel/preset-env @babel/polyfill`
- babel 설정파일 `.babelrc`
```
{
  "presets": [
    ["@babel/preset-env", { "targets": { "browsers": ["last 2 versions", ">= 5% in KR"] } }]
  ]
}
```


### package.json 설정
- npm init 입력하면 package.json과 package-lock.json 파일이 생성됨
`npm init`
- `package.json` 파일 설정
```
"scripts": {
  "build": "babel src -d dist -w",
}
```


### ESLint 설정
- `npm install eslint`
- `node_modules/.bin/eslint --init`
- 위 명령어를 입력하고 난 후 몇가지 옵션을 선택하면 eslintrc.js가 생성된다.
- package.json 설정
```
"scripts": {
  "lint": "eslint src/**/*.js",
}
```
- .eslintignore
```
node_modules
```
.gitignore와 비슷하게 lint 검사에서 제외할 디렉토리를 명시한다.

[eslint getting started 문서] (https://eslint.org/docs/4.0.0/user-guide/getting-started)



