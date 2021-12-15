# Burç Bulan Program
Koç Burcu : 21 Mart - 20 Nisan

Boğa Burcu : 21 Nisan - 21 Mayıs

İkizler Burcu : 22 Mayıs - 22 Haziran

Yengeç Burcu : 23 Haziran - 22 Temmuz

Aslan Burcu : 23 Temmuz - 22 Ağustos

Başak Burcu : 23 Ağustos - 22 Eylül

Terazi Burcu : 23 Eylül - 22 Ekim

Akrep Burcu : 23 Ekim - 21 Kasım

Yay Burcu : 22 Kasım - 21 Aralık

Oğlak Burcu : 22 Aralık - 21 Ocak

Kova Burcu : 22 Ocak - 19 Şubat

Balık Burcu : 20 Şubat - 20 Mart

### Ödev
Aynı örneği switch-case kullanmadan yapınız.
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        //def
        Scanner sc = new Scanner(System.in);
        int month,day;
        //inputs
        System.out.print("Doğduğunuz ay: ");
        month = sc.nextInt();
        System.out.print("Doğduğunuz gün: ");
        day = sc.nextInt();

        //operation
        if(month == 1)
        {
            if(day <= 21 && day>0)
                System.out.println("Oğlak Burcu");
            else if(day >= 22 && day<32)
                System.out.println("Kova Burcu");
        }
        else if(month == 2)
        {
            if(day <= 19 && day>0)
                System.out.println("Kova Burcu");
            else if(day >= 20 && day<29)
                System.out.println("Balık Burcu");
        }
        else if(month == 3)
        {
            if(day <= 20 && day>0)
                System.out.println("Balık Burcu");
            else if(day >= 21 && day<32)
                System.out.println("Koç Burcu");
        }
        else if(month == 4)
        {
            if(day <= 20 && day>0)
                System.out.println("Koç Burcu");
            else if(day >= 21 && day<31)
                System.out.println("Boğa Burcu");
        }
        else if(month ==5)
        {
            if(day <= 21 && day>0)
                System.out.println("Boğa Burcu");
            else if(day >= 22 && day<32)
                System.out.println("İkizler Burcu");
        }
        else if(month == 6)
        {
            if(day <= 22 && day>0)
                System.out.println("İkizler Burcu");
            else if(day >= 23 && day<31)
                System.out.println("Yengeç Burcu");
        }
        else if(month == 7)
        {
            if(day <= 22 && day>0)
                System.out.println("Yengeç Burcu");
            else if(day >= 23 && day<32)
                System.out.println("Aslan Burcu");
        }
        else if(month == 8)
        {
            if(day <= 22 && day>0)
                System.out.println("Aslan Burcu");
            else if(day >= 23 && day<32)
                System.out.println("Başak Burcu");
        }
        else if(month == 9)
        {
            if(day <= 22 && day>0)
                System.out.println("Başak Burcu");
            else if(day >= 23 && day<31)
                System.out.println("Terazi Burcu");
        }
        else if(month == 10)
        {
            if(day <= 22 && day>0)
                System.out.println("Terazi Burcu");
            else if(day >= 23 && day<32)
                System.out.println("Akrep Burcu");
        }
        else if(month == 11)
        {
            if(day <= 21 && day>0)
                System.out.println("Akrep Burcu");
            else if(day >= 22 && day<31)
                System.out.println("Yay Burcu");
        }
        else if(month == 12)
        {
            if(day <= 21 && day>0)
                System.out.println("Yay Burcu");
            else if(day >= 22 && day<32)
                System.out.println("Oğlak Burcu");
        }

    }

}
```