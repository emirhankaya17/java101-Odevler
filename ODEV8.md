# Ters Üçgen Yapımı
Java ile basamak sayısının kullanıcıdan alınan ve döngüler kullanılarak, yıldızlar(*) ile ekrana ters üçgen çizen programı yazın.
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
        int starCounter = num * 2 + 1;
        for (int i = 0; i < num; i++) {
            starCounter -= 2;
            for (int j = 0; j < i ; j++) {
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