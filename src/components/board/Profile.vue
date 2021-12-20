<template>
  <div>
      <h1>Education</h1>
    <v-divider></v-divider>
    <div class="my-3 pl-3 about-me" v-html="education"></div>
    <br />

	
	 <h1 >Skill</h1>
    <v-divider></v-divider>
	<div class="my-4 pl-3" v-for="skill of skills" v-bind:key="skill.name">
      <h3>{{skill.name}} </h3>
      <li class="my-1 grey--text text--darken-2 ml-4" v-for="(description) of skill.description" :key="description">
		 {{description}}
      </li>

    </div>
 	<br />

  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    return {
      education: `<p>
                 <p> 2017/03 ~ 2021/02</p>
                <p>&nbsp;&nbsp; 서일대학교 소프트웨어공학과</p>
                <p>&nbsp;&nbsp;산업수요 맞춤 교육 JAVA WEB 개발자 과정 수강<p>
                
                </p>`,
    
	  
	  skills:[
		  {
			  name: "Java",
			  level: "중",
			  description: [ "객체지향원칙을 이해하고 지키기 위해 노력함", "디자인 패턴 등을 이해하고 적용하기 위해 노력함"]
		  },
		   {
			  name: "html/css/js",
			  level: "중",
			  description: [ "플러그인, 이벤트가 동작하는 반응형 웹 사이트 작성 가능 node.js, jQuery 활용 가능"]
		  },
		   {
			  name: "Spring Boot",
			  level: "하",
			  description: [ "Spring MVC, IoC, AOP, JPA 개념 이해 및 사용"]
		  },
		   {
			  name: "Vue.js",
			  level: "하",
			  description: [ "vue의 구조및 웹페이지 구현가능"]
		  },
		   {
			  name: "Android",
			  level: "중",
			  description: [ "필요한 기능을 API 문서나 라이브러리를 참조하여 구현할 수 있음.", "내장db 및 안드로이드로 개발경험 있음","MVC, MVVM 패턴 등의 대한 이해"]
		  },
		   {
			  name: "mysql",
			  level: "중",
			  description: [ "쿼리문 을 통한 간단한 DB관리"]
		  }
		
		  
	  ]
    };
  }
};
</script>
