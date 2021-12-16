# Çin Zodyağı Hesaplama
Java ile kullanıcıdan doğum tarihini alıp Çin Zodyağı değerini hesaplayan program yazınız.

Çin Zodyağı nedir?

4000 bin yıldır kullanılan bir astroloji çeşididir Çin astrolojisi ve insanları 12 değişik burç ve sembollerle tanımlar. Çin Zodyağı bu 12 burcun eşit aralıklarla(10 derece genişliğinde) sıralandığı bir hayvan halkasıdır ve yıldızlarla pek bir ilgisi yoktur.

Çin Zodyağı nasıl hesaplanır?

Çin zodyağı hesaplanırken kişinin doğum yılının 12 ile bölümünde kalana göre bulunur.

Doğum Tarihi %12 = 0 ➜ Maymun

Doğum Tarihi %12 = 1 ➜ Horoz

Doğum Tarihi %12 = 2 ➜ Köpek

Doğum Tarihi %12 = 3 ➜ Domuz

Doğum Tarihi %12 = 4 ➜ Fare

Doğum Tarihi %12 = 5 ➜ Öküz

Doğum Tarihi %12 = 6 ➜ Kaplan

Doğum Tarihi %12 = 7 ➜ Tavşan

Doğum Tarihi %12 = 8 ➜ Ejderha

Doğum Tarihi %12 = 9 ➜ Yılan

Doğum Tarihi %12 = 10 ➜ At

Doğum Tarihi %12 = 11 ➜ Koyun
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        //def
        Scanner sc = new Scanner(System.in);
        int year,modulus;
        //inputs
        System.out.print("Doğum Yılınızı Giriniz : ");
        year = sc.nextInt();
        //operation
        modulus = year % 12;
        //condition
        if(modulus == 0)
            System.out.println("Çin Zodyağı Burcunuz : Maymun");
        if(modulus == 1)
            System.out.println("Çin Zodyağı Burcunuz : Horoz");
        if(modulus == 2)
            System.out.println("Çin Zodyağı Burcunuz : Köpek");
        if(modulus == 3)
            System.out.println("Çin Zodyağı Burcunuz : Domuz");
        if(modulus == 4)
            System.out.println("Çin Zodyağı Burcunuz : Fare");
        if(modulus == 5)
            System.out.println("Çin Zodyağı Burcunuz : Öküz");
        if(modulus == 6)
            System.out.println("Çin Zodyağı Burcunuz : Kaplan");
        if(modulus == 7)
            System.out.println("Çin Zodyağı Burcunuz : Tavşan");
        if(modulus == 8)
            System.out.println("Çin Zodyağı Burcunuz : Ejderha");
        if(modulus == 9)
            System.out.println("Çin Zodyağı Burcunuz : Yılan");
        if(modulus == 10)
            System.out.println("Çin Zodyağı Burcunuz : At");
        if(modulus == 11)
            System.out.println("Çin Zodyağı Burcunuz : Koyun");

    }

}
```