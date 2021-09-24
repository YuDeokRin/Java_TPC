# inflearn TPC 14강

# 8.객체가 메모리에 어떻게 만들어지나

### 3.생성자 메소드 (Constructor)

이것은 꼭 알아가자

1) 객체를 생성할 때  사용되는 메서드

2) 객체 생성 후 객체의 초기화를 하는 역할 수행

3) 특징

- 클래스이름과 동일한 메서드
- 메서드의 return type이 없다.(void 아님)
- public 접근 권한을 가진다.(단,  private  생성자도 있음)
- 생성자가 없을 때는 기본 생성자가 만들어 진다.

---


![Untitled](https://user-images.githubusercontent.com/56623911/134606840-b85dcaf8-be26-45e4-b08b-2941ef761631.png)

```java
public class BookVO {
    public String title;
    public int price;
    public String company;
    public int page;
    //디폴트 생성자 메서드 (생략)

    public BookVO(){
        //초기화 작업
        this.title="자바";
        this.price=14000;
        this.company="이지스";
        this.page=780;
    }
    //생성자 메소드의 중복정의(Overloading)
    public BookVO(String title, int price, String company, int page){
        this.title=title;
        this.price=price;
        this.company=company;
        this.page=page;
    }
}
```


![제목_없음](https://user-images.githubusercontent.com/56623911/134606873-56d1a11a-b74d-4314-8d5a-d418b856203e.png)

```java
public class TPC12 {
    public static void main(String[] args) {
        //생성자 -> 생성 + 초기화 -> 중복정의 가능
        BookVO b1 = new BookVO();
        System.out.print(b1.title + "\t");
        System.out.print(b1.price + "\t");
        System.out.print(b1.company + "\t");
        System.out.print(b1.page + "\t");

        BookVO b2 = new BookVO();
        System.out.print(b2.title + "\t");
        System.out.print(b2.price + "\t");
        System.out.print(b2.company + "\t");
        System.out.print(b2.page + "\t");

        BookVO b3 = new BookVO("Python", 18000, "대림",920);
        System.out.print(b3.title + "\t");
        System.out.print(b3.price + "\t");
        System.out.print(b3.company + "\t");
        System.out.print(b3.page + "\t");
    }
}
```

![Untitled 1](https://user-images.githubusercontent.com/56623911/134606987-ae6cdc05-3d08-4a78-a473-fda746710f5f.png)

