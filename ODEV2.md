# Manav Kasa Programı
Java ile kullanıcıların manavdan almış oldukları ürünlerin kilogram değerlerine göre toplam tutarını ekrana yazdıran programı yazın.

Meyveler ve KG Fiyatları

* Armut : 2,14 TL
* Elma : 3,67 TL
* Domates : 1,11 TL
* Muz: 0,95 TL
* Patlıcan : 5,00 TL
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        //def
        double arm=2.14,elm=3.67,dom=1.11,muz=0.95,pat=5;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("Armut Kaç Kilo ? : ");
        double armK = sc.nextDouble();
        System.out.print("Elma Kaç Kilo ? : ");
        double elmK = sc.nextDouble();
        System.out.print("Domates Kaç Kilo ? : ");
        double domK = sc.nextDouble();
        System.out.print("Muz Kaç Kilo ? : ");
        double muzK = sc.nextDouble();
        System.out.print("Patlıcan Kaç Kilo ? : ");
        double patK = sc.nextDouble();
        //operation
        double sum = arm*armK + elm*elmK + dom*domK + muz*muzK + pat*patK;
        //output
        System.out.println("Toplam Tutar : "+sum+" TL");
        
    }

}
```