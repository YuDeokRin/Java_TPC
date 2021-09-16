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

![Untitled](https://user-images.githubusercontent.com/56623911/133571132-34951ca4-c575-49ba-959a-629417e1b680.png)

![Untitled 1](https://user-images.githubusercontent.com/56623911/133571180-02d99f4a-9cea-4723-8209-fc266e2c7cfe.png)

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

![Untitled 2](https://user-images.githubusercontent.com/56623911/133571264-b21391b6-b925-4db2-b666-c24ab910db84.png)

※ static  멤버 접근방법

→ 클래스이름.클래스메서드(static 메서드)

- 총정리
![제목_없음](https://user-images.githubusercontent.com/56623911/133571295-12481846-3bab-4984-8e15-547c9444c561.png)
