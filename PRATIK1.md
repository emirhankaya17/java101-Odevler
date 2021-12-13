# Not Ortalaması Hesaplayan Program
Java ile Matematik, Fizik, Kimya, Türkçe, Tarih, Müzik derslerinin sınav puanlarını kullanıcıdan alan ve ortalamalarını hesaplayıp ekrana bastırılan programı yazın.

## Ödev
Aynı program içerisinde koşullu ifadeler kullanılarak, eğer kullanıcının ortalaması 60'dan büyük ise ekrana "Sınıfı Geçti" , küçük ise "Sınıfta Kaldı" yazsın.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        //def
        Scanner sc = new Scanner(System.in);

        //inputs
        System.out.println("Matematik notunuzu girin: ");
        int mat = sc.nextInt();

        System.out.println("Fizik notunuzu girin: ");
        int fiz = sc.nextInt();

        System.out.println("Kimya notunuzu girin: ");
        int kim = sc.nextInt();

        System.out.println("Türkçe notunuzu girin: ");
        int tur = sc.nextInt();

        System.out.println("Tarih notunuzu girin: ");
        int tar = sc.nextInt();

        System.out.println("Müzik notunuzu girin: ");
        int müz = sc.nextInt();

        double ort = (double)(mat + fiz + kim + tur + tar + müz)/ 6;
        System.out.println(ort);

        //odev
        System.out.println(ort>60 ? "Sınıfı Geçti":"Sınıfta Kaldı");
    }

}
```