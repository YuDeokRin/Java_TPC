# inflearn TPC 12강

1.기본자료형(PDT)  vs 사용자정의자료형(UDDT)

- 기본 자료형(PDT)

컴파일러에서 기본적으로 제공해주는 자료형

<img src = "https://user-images.githubusercontent.com/56623911/132691006-a30adda3-76c0-4dbf-91f4-1fc87fbd070d.png" width="30%" height="20%">



```java
int a;
BookDTO b; 
```

변수 a와 변수 b 두가지의 차이점 

a는 기본자료형(PDT)이고 컴파일러에서 기본적으로 제공해주는 자료형이다.
그렇다면 b는 무엇인가 ? b는 사용자정의자료형이다. 그게 무엇인가 ?

- 사용자정의자료형(UDDT)

사용자가 직접 만들어서 사용하는 자료형

<img src="https://user-images.githubusercontent.com/56623911/132691035-93d48b83-4acb-44ec-be72-3858a8012789.png"  width="30%" height="20%">


```java
//사용자 정의 자료형
public class BookDTO{
			public String title;  //책 제목
			public int    price;  // 책 가격
			public String company;// 책만든 회사
			public int    page;   // 책 페이지 수 
}
```

- 다른 클래스 가서 BookDTO 객체 생성

```java
 //다른클래스에서 BookDTO 클래스의 객체를 생성한다.
public class TPC10 {
    public static void main(String[] args) {
        BookDTO b ;  
				b= new BookDTO(); // 객체 생성
  }
```

- 객체를 생성 시  객체와 같이 생기는 생성자 메소드 
기본생성자(default constructor)가 저절로 생긴다. 
※기본 생성자는 안보인다※
- 생성자의 역할은 멤버들을 메모리에 올려서 객체를 만드는 작업을 하도록 내부적으로 설계가 되어있다.
- 객체가 메모리에 만들어지면 this라는 객체가 생성된다.

```java
public class BookDTO{
			public String title;  //책 제목
			public int    price;  // 책 가격
			public String company;// 책만든 회사
			public int    page;   // 책 페이지 수 

			public BookDTO(){
					super();
		}
}
```

- 객체가 생성되어 heap Area에 올라간 모습

![Untitled 2](https://user-images.githubusercontent.com/56623911/132691089-371ee465-e4c7-415f-a9ee-ae1ff5c9fcbd.png)


- BookDTO의 객체 번지가 들어가서 b가 BookDTO를 가리킨다.

```java
import kr.tpc.BookDTO;

public class TPC10 {
    public static void main(String[] args) {
        BookDTO b = new BookDTO(); // 객체 생성
 
    }
}
```

<img src ="https://user-images.githubusercontent.com/56623911/132691129-02242ecb-3c53-4852-8620-b939e4496a0f.png" width="60%" heigth="50%">



- import 패키지명.클래스명 ←을 이용해서 사용할 준비를한다.
- 출력은 객체명.필드명(멤버명) 써서 사용한다.

```java
import kr.tpc.BookDTO;

public class TPC10 {
    public static void main(String[] args) {
        BookDTO b = new BookDTO(); // 객체 생성
        b.title= "자바";
        b.price=17000;
        b.company="믿음사";
        b.page = 670;

        System.out.print(b.title+"\t");  // 출력할 때도 b.xx 형식으로 해야된다.
        System.out.print(b.price+"\t");
        System.out.print(b.company+"\t");
        System.out.print(b.page+"\t");
    }
}

// 출력결과

//자바	17000	믿음사	670
```
