# 이클립스로 스프링 부트 프로젝트 시작하기

### File > New > Spring starter Project를 선택하여 새 스프링 부트 프로젝트를 생성한다.

![image](https://user-images.githubusercontent.com/38831314/119295786-a5552580-bc92-11eb-89a8-fc03a04d577b.png)

### Next를 클릭 후 버전 및 의존성을 설정. Spring Web과 Spring Boot DevTools를 선택한다

![image](https://user-images.githubusercontent.com/38831314/119295851-c7e73e80-bc92-11eb-92b4-94d3b2edc49f.png)

### 실행

![image](https://user-images.githubusercontent.com/38831314/119295893-ddf4ff00-bc92-11eb-8b44-f0bfa4c7536d.png)

### 정상 로그 화면

![image](https://user-images.githubusercontent.com/38831314/119295921-f49b5600-bc92-11eb-85f1-8d5b83142ec2.png)

### 웹 브라우저에서 localhost:8080 입력

![image](https://user-images.githubusercontent.com/38831314/119295958-08df5300-bc93-11eb-875d-e3bc1269d7db.png)

### src/main/java -> 패키지 이름뒤에 .controller 추가한 패키지 만들기 -> 해당 클래스에서 HelloWorldController 만들기

![image](https://user-images.githubusercontent.com/38831314/119296170-670c3600-bc93-11eb-8977-8f5bbeceac6c.png)

### HelloWorldController 클래스 만들고 아래 내용 추가

@RestController 어노테이션을 이용하여 해당 클래스가 REST 컨트롤러 기능을 수행하도록 한다.

@RequestMapping 어노테이션은 해당 메서드를 실행할 수 있는 주소를 설정한다. 여기서는 애플리케이션의 기본 주소를 /로 지정

```java

package com.ckbs.MariaDbTest.controller;

import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

@RestController
public class HelloWorldController {

    @RequestMapping("/")
    public String hello() {
        return "Hello World!";
    }
}

```

### 웹 브라우저에서 localhost:8080 입력

![image](https://user-images.githubusercontent.com/38831314/119296238-8acf7c00-bc93-11eb-9e69-d13dcdf1f89d.png)




