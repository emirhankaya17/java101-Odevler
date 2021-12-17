# Üslü Sayı Hesaplayan Program
### Ödev
Java ile kullanıcının girdiği değerler ile üslü sayı hesaplayan programı "For Döngüsü" kullanarak yapınız.
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        //def
        int num, exp,sum =1;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("Sayı giriniz: ");
        num  = sc.nextInt();
        System.out.print("Üs giriniz: ");
        exp  = sc.nextInt();
        //operation
        for (int i = 0; i < exp; i++) {
            sum *= num;
        }
        System.out.println("sonuç: "+sum);

    }

}
```