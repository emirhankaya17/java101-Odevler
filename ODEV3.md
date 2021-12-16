# Uçak Bileti Fiyatı Hesaplama
Java ile mesafeye ve şartlara göre uçak bileti fiyatı hesaplayan programı yapın. Kullanıcıdan Mesafe (KM), yaşı ve yolculuk tipi (Tek Yön, Gidiş-Dönüş) bilgilerini alın. Mesafe başına ücret 0,10 TL / km olarak alın. İlk olarak uçuşun toplam fiyatını hesaplayın ve sonrasında ki koşullara göre müşteriye aşağıdaki indirimleri uygulayın ;

Kullanıcıdan alınan değerler geçerli (mesafe ve yaş değerleri pozitif sayı, yolculuk tipi ise 1 veya 2) olmalıdır. Aksi takdirde kullanıcıya "Hatalı Veri Girdiniz !" şeklinde bir uyarı verilmelidir.
Kişi 12 yaşından küçükse bilet fiyatı üzerinden %50 indirim uygulanır.
Kişi 12-24 yaşları arasında ise bilet fiyatı üzerinden %10 indirim uygulanır.
Kişi 65 yaşından büyük ise bilet fiyatı üzerinden %30 indirim uygulanır.
Kişi "Yolculuk Tipini" gidiş dönüş seçmiş ise bilet fiyatı üzerinden %20 indirim uygulanır.
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        //def
        Scanner sc = new Scanner(System.in);
        double distance,totalCost = 0,costPerKM= 0.10;
        int age,flyType;
        //inputs
        System.out.print("Mesafeyi km türünden giriniz: ");
        distance = sc.nextDouble();
        System.out.print("Yaşınızı giriniz: ");
        age = sc.nextInt();
        System.out.print("Yolculuk tipini giriniz (1 => Tek Yön , 2 => Gidiş Dönüş ): ");
        flyType = sc.nextInt();
        //operations
        totalCost = distance * costPerKM;
        //conditions
        if(distance<=0 || age<=0 || !(flyType == 1 ||flyType == 2))
            System.out.println("Hatalı Veri Girdiniz !");
        else
        {
            if(age<12)
                totalCost = totalCost * .5;
            else if(age<24)
                totalCost = totalCost * .9;
            else if(age>65)
                totalCost = totalCost* .7;
            if(flyType == 2)
                totalCost = totalCost* .8 * 2;
            System.out.println("Toplam Tutar = "+totalCost+" TL");
        }


    }

}
```