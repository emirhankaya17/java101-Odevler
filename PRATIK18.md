# Yıldızlar İle Elmas Yapımı
### Ödev
Java'da döngüler kullanarak yıldızlar ile elmas yapınız.
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        //def
        int num;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("Sayı giriniz: ");
        num = sc.nextInt();
        //operations
        int starCounter = -1;
        for (int i = 0; i < num; i++) {
            starCounter+=2;
            for (int j = 0; j < num-i-1; j++) {
                System.out.print(" ");
            }
            for (int j = 0; j < starCounter; j++) {
                System.out.print("*");
            }
            System.out.println();
        }
        for (int i = 0; i < num; i++) {
            starCounter-=2;
            for (int j = 0; j < i+1; j++) {
                System.out.print(" ");
            }
            for (int j = 0; j < starCounter; j++) {
                System.out.print("*");
            }
            System.out.println();
        }

    }
}
```