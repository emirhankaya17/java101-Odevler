# KDV Tutarı Hesaplayan Program
Java ile kullanıcıdan alınan para değerinin KDV'li fiyatını ve KDV tutarını hesaplayıp ekrana bastıran programı yazın.

(Not : KDV tutarını 18% olarak alın)

KDV'siz Fiyat = 10;

KDV'li Fiyat = 11.8;

KDV tutarı = 1.8;

## Ödev
Eğer girilen tutar 0 ve 1000 TL arasında ise KDV oranı %18 , tutar 1000 TL'den büyük ise KDV oranını %8 olarak KDV tutarı hesaplayan programı yazınız.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        //def
        Scanner sc = new Scanner(System.in);
        double taxRate = 0.18;
        //operation
        System.out.println("Urunun fiyatını giriniz: ");
        double input = sc.nextDouble();
        taxRate = input>1000 ? 0.08 : 0.18;
        double tax = input * taxRate;
        //print
        System.out.println("Kdvsiz fiyat: "+input);
        System.out.println("Kdv tutarı: "+tax);
        System.out.println("Kdv oranı: "+taxRate);
        System.out.println("Kdvli fiyat: "+(input+tax));
        
    }

}
```