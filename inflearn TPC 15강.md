# inflearn TPC 15강

# 8.private 생성자도 있어요 ? (Static과 관계)

이것은 꼭 알아가자 !

# 4. private  생성자 메서드(Constrctor)

→ 객체생성에 관여하는 생성자 메서드가 private 접근제어를 가지면 객체를 생성할 수 없다는 뜻이 된다.

→ 그러므로 객체를 생성하지 않고도 사용가능 해야 된다.(모든 클래스의 멤버가 static  멤버가 되어야 한다.)

---

→ non-static 멤버인 경우(인스턴스 메서드)

 객체 생성 후 접근 가능

```java
Inflearn Inf = new Inflearn(); // 생성자가 public인 경우 

inf.tpc();
```

→static 멤버인 경우 (클래스 메서드)

객체생성 없이 접근가능(클래스 이름으로 접근)

![Untitled](inflearn%20TPC%2015%E1%84%80%E1%85%A1%E1%86%BC%2085fb1d084302449d9edd564bcedadf34/Untitled.png)

![Untitled](inflearn%20TPC%2015%E1%84%80%E1%85%A1%E1%86%BC%2085fb1d084302449d9edd564bcedadf34/Untitled%201.png)

※ Java API 중에서도 생성자가 private인 클래스도 많이 있다.
System, Math .... System sys = new System(); →X
→자주 사용하는 객체나, 동작은 static  멤버로 만든다.

```java
public class Inflearn {
	private Inflearn() {

	} 

//인스턴스 메서드
public void tpc(){
	System.out.println("TPC강의 너무 재미있다.");
	}

//클래스 메서드
public static void java(){
		System.out.println("Java강의 너무 재미있다.");
	}
}
```

![Untitled](inflearn%20TPC%2015%E1%84%80%E1%85%A1%E1%86%BC%2085fb1d084302449d9edd564bcedadf34/Untitled%202.png)

※ static  멤버 접근방법

→ 클래스이름.클래스메서드(static 메서드)

- 총정리

![제목 없음.png](inflearn%20TPC%2015%E1%84%80%E1%85%A1%E1%86%BC%2085fb1d084302449d9edd564bcedadf34/%EC%A0%9C%EB%AA%A9_%EC%97%86%EC%9D%8C.png)