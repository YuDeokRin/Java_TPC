# inflearn TPC 13강

# 8. 객체가 메모리에 어떻게 만들어지나

이것은 꼭 알아가자

# 2.객체 생성 과정

## 객체 생성

```java
BookVO b = new BookVO(); new 연산자와 생성자 매소드 호출
```

Value Object = VO

현실세계의 책을 컴퓨터로 구현을 시킬려면 두 가지가 필요하다

1) 상태정보(변수): attribute, property, member

                            → 제목, 출판사, 저자, 가격, 페이지수, ISBN, 이미지, 두깨, 무게, 재질 ....

책을 만드는데 여러가지 상태 정보가 있다. 하지만 거기서 내가 사용할 것들만 추출한다. 그것이 모델링 이라고 한다. 

제목, 가격, 출판사, 페이지수 → Head First Java, 30000, 한빛미디어, 700

Modeling : 필요한 속성만 뽑아내는 과정

2) 행위정보 : 동작(method), 기능(function) 
![Untitled](https://user-images.githubusercontent.com/56623911/133805715-006cc0b1-de98-436c-80bf-17a2e7473d38.png)


## 객체가 메모리에서의 생성 그림

```java
public class BookVO{
			public String title;
			public int price;
			public String company;
			public int page;
}
```

![Untitled 1](https://user-images.githubusercontent.com/56623911/133805793-21779ea6-e123-4d64-9a3d-1fa9088ccad1.png)

## .(dot)연산자 접근, 참조연산자

![Untitled 2](https://user-images.githubusercontent.com/56623911/133805835-38e1e401-a078-4387-9099-1aab9f0f8507.png)

![제목_없음](https://user-images.githubusercontent.com/56623911/133805987-6ec7bc9c-e79c-4676-9268-af49f811c7da.png)

