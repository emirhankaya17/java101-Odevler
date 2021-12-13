# Vücut Kitle İndeksi Hesaplama
Java ile kullanıcıdan boy ve kilo değerlerini alıp bir değişkene atayın. Aşağıdaki formüle göre kullanıcının "Vücut Kitle İndeks" değerini hesaplayıp ekrana yazdırın.

Formül
Kilo (kg) / Boy(m) * Boy(m)

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        //def
        double w,h;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("Lütfen boyunuzu (metre cinsinde) giriniz : ");
        h = sc.nextDouble();
        System.out.print("Lütfen kilonuzu giriniz : ");
        w = sc.nextDouble();
        //operation
        double sum = w/(h*h);
        //output
        System.out.println("Vücut Kitle İndeksiniz : "+sum);

    }

}
```