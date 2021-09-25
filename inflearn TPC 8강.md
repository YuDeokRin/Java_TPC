# inflearn TPC 8강

1.변수와 메서드(method)

변수(Variable) : 데이터를 한 개 만(한 개의 형태) 저장 가능하다. 

→저장만 한다.

메서드(Method) →메서드 이름이 변수 역할을 한다.

메서드(Method) : 동작을 한 후에 데이터를 한 개 만 만들어 낸다.

→동작 후 저장한다.

![1](https://user-images.githubusercontent.com/56623911/134775503-45dda1f8-0b3d-41b7-a1f5-8c137effac7c.png)


```java
public class TPC06 {
    public static void main(String[] args) {
        //5.메서드 -> 동작(method), 기능(function)
        int a = 67;
        int b = 98;
        // a + b = ?
        int result = sum(a, b);
        System.out.println(result);

        int[] arr =makeArr(); //10, 20, 30
        int hap = 0;
        for(int i =0; i<arr.length; i++){
           hap+=arr[i];
        }
        System.out.println(hap);
    }

    // 정수 2개를 더하여 총합을 구하여 리턴하는 메서드를 정의하시오.
    public static int sum(int a, int b) {
        int v = a + b;
        return v;
    }
    // 10, 20 , 30
    public static int[] makeArr() {
        int x = 10;
        int y = 20;
        int z = 30;
        int[] arr = new int[3];
        arr[0]=x;
        arr[1]=y;
        arr[2]=z;

        return arr;
    }
}
```
