[환경설정]
     node 설치
     vue.js 설치

	 nginx 루트를 mj-web 의 배포 위치로 설정함 (나중에는 그냥 해야할듯)


[서버 방화벽 오픈]
     

[개발 완료후 배포]
     git pull 하고
	sudo npm run build (안되면 npm install)
	sudo ngynx -s reload





# mj-web

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).



2022-07
	2022-07-05 
		- Dotnet 6.0 테스트
		- ORACLE VM 환경 재정리 (VM 은 삭제하고 DEV로 만들자)
		- DEV (오라클리눅스이미지) 에서 외부 접속 가능하도록 환경설정 안됨
		- NGINX 설치하여 dotnet 띄워두기 해볼것
	2022-07-06 
		- https://hplayground.tistory.com/105
		- Sudo npm run build
		- Sudo ngynx -s reload
		- VM 들 변경
		- Vue.js 환경설정
	2022-07-08 
		- Npm run dev
		- Npm start
		- npm instal axios  
        - root /var/www/html/mj-web/dist;

	2022-07-13
	    - front -> back 호출이 안됨, 아마도 방화벽 문제일것 같음

		npm install vue-axios-cors