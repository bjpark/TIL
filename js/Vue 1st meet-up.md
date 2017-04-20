* Vue 1st meet-up

- 우당탕탕 회사에서 Vue.js를 도입한 삽질기
	* Vue 도입의 계기
		- 템플릿엔진도 없이 pure html,css,js로만 하다보니 유지보수, 코드수정의 힘듬, 코드관리가 힘들었음.
	* 리액트 도입의 실패
		- 컴포넌트 구조에 대한 이해가 부족, 충분히 공부가 안된상태에서 여러가지 적용하다보니 실패.
	* 가장 적은 비용으로 도입이 가능
		- 문서가 >>>한글<<<
		- 단일파일 컴포넌트를 사용하여 한파일로 모든지 다할수 있음
	* 실무에서 회사에서 우려할만한 사항
		- 뷰가 대중적이지 못하고 인수인계에 어려움이 생길 가능성이 있음
		- Vue의 메이저 후원사가 없음...
	* 도입과정
		- (만약) 구매한 테마가 적용 가능한지 예제 확보 (이 경우는 vue admin LTE)
		- 테마 적용 및 프로젝트 구조 잡기
			- 테마 파일 및 사용되는 jquery 라이브러리 적용,
			- 페이지 당 하나의 컴포넌트로 작업
			- 구현중 문제
				- 사용된 jquery 라이브러리의 코드가 너무 지저분함
				- Router 페이지 이동 처리,
				- Rest Parameter 데이터가 없을때 처리
		- 컴포넌트 분리
			- 코드를 보기가 편해짐.
			- 내가 만든 컴포넌트다보니 뭐가 뭔지 잘 알게 되니 관리가 더 편해짐
	* 도입후 느낀점
		- jQuery의 늪
		- Javascript의 this문제
		- 컴포넌트 기반 작업에 대한 두려움이 사라짐
			- 한 페이지를 한 컴포넌트로 만든 후 데이터 플로우에 대한 개념도 생기게 되어 더 잘 쪼갤 수 있게 됨.

- 백엔드 개발자, 입문자로서 Vue 이해하고 사용하다
	* Vue 도입의 계기
		- 엄청 유명한것 같진 않아서
		- 공식문서의 글투가 매우 다정다감
		- 전환비용이 낮아서 EJS + jQuery >> Vue.js
	* 반응형 동작과 동기식 동작
		- 스프레드시트처럼 데이터와 DOM이 연결되어 데이터가 변하면 DOM이 변함 -> 데이터 바인딩
		- AJAX로 서버로부터 비동시로 데이터를 가져와 데이터 반영  
	* 반응형 동작과 비동기식 동작
		- 데이터의 의존관계나 계층구조 설계 필요
			- Vue의 표현단은 데이터에 의해 반응하므로 결국 UI가 바응할 데이터의 의존과 계층구조를 생각해야함
			- jQuery로 DOM를 직접 제어하던 관점에서 벗어나서, 데이터를 제어하여 UI를 제어하도록 해야함
	=> 결론은 동기식이든 비동기식이든 데이터가 변해야 UI가 변하는것

	* 컴포넌트
		- >>>재사용가능한<<< UI요소 단위 
		- 관심사 단위로 UI요소를 개체화하여 재사용성과 의존성을 관리할수있도록 해야함
		- 컴포넌트의 data가 함수인 이유는?
			- 자스는 객체를 전부 참조를 하기때문에 지역성을 갖추기 위해서 컴포넌트의 Data는 함수이다
	* 패턴
		- Store패턴
			- 컴포넌트 간 상태를 공유할때 사용하는 객체
			- Store패턴 필요성이 대두됫다면 vuex의 이해와 활용이 필요한 단계.
	* REST API 관점변화
		- 쓰기 전
			- 표현단에 데이터를 전달하는걸 Raw Data비슷하게 보내줘서 접근할수 있도록.
		- Vue를 쓰게되면
			- UI가 반응할 데이터에 필요한 데이터를 생각하며 전달.

- 웹 디자이너의 도전 Vue.js 따라하기
	* Vuejs 도입의 계기
		- jQuery로 SPA개발하는데 무려 코드가 4000줄! 더 줄여보자!
	음 근데 이건 너무 기본이라 스킵해야지

- Vue.js와 firebase활용기
	* Vuejs 도입의 이유
		- 단일 파일 컴포넌트 
			- 구조와 표현과 동작이 나뉘어져 깔끔
		- 학습곡선이 낮음
		- 유연함
		- 가벼움
		- >> 한국어 가이드 문서가 잘되있음 <<
	* Firebase를 선택한 이유
		- 웹, iOS, Android개발에 필요한 기능을 제공하는 BaaS
		- 직접 백엔드를 구성할 필요가 없어서 시간단축에 도움됨
		- 자세한건 독스에서

	* 개발 프로세스
		- Firebase세팅 > Vue 프로젝트 세팅 > 프로젝트에 필요한 라이브러리 추가 > Firebase연동

	* Firebase 
		- vue fire 연동
		- firebase-tools 배포
		- vue-blu ???

- Nuxt로 사내 서비스 구현하면서 얻은 경험 공유
	* Nuxt란?
		- React진영에서 Next.js라는 서버사이드렌더링 라이브러리를 만들었는데 좀 성공해보니 Vue에서 Nuxt를 만듬
		- 'Intergrating with Nuxt is the full package, It's like more complete'
	* Webdevelopment
		- Component, Container, store
		- SSR(Server Side Rendering)
		- Router w/ History API (SPA)
		- Latest ECMAScript
		- Hot Module Reloading
		- SASS
		- ...
	* Nuxt 
		- webpack.config.js, gulpfile.js, .babelrc.... XXXXXXXX!
		- 그냥 npm install nuxt를 쓰면 끝
	* Isomorphic Javascript
		- 프론트엔드와 백엔드 모두 자스를 쓸수있음!
		- 단점
			- Context가 달라!!!!
				- 같은 언어지만 그대로 쓰면 안된다!
			- Tree Shaking
	- JSON DB를 쓰기 좋을땐 JSON SERVER
	- 와 근데 진짜 빠르다 쉬불 나도 써야지








