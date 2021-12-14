# Hava Sıcaklığına Göre Etkinlik Önerme
Koşullar :
* Sıcaklık 5'dan küçük ise "Kayak" yapmayı öner.
* Sıcaklık 5 ve 15 arasında ise "Sinema" etkinliğini öner.
* Sıcaklık 15 ve 25 arasında ise "Piknik" etkinliğini öner.
* Sıcaklık 25'ten büyük ise "Yüzme" etkinliğini öner.
### Ödev
Aynı örnek üzerinden if koşulları başka hangi şekilde oluşturulabilirdi farklı çözüm yolları bulunuz.
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        //def
        Scanner sc = new Scanner(System.in);
        int heat;
        //inputs
        System.out.print("Sıcaklığı giriniz: ");
        heat = sc.nextInt();
        if(heat>25)
            System.out.println("Yüzme yapabilirsiniz");
        else if(heat>15)
            System.out.println("Pikniğe gidebilirsiniz");
        else if(heat>5)
            System.out.println("Sinemaya gidebilirsiniz");
        else
            System.out.println("Kayak yapabilirsiniz");

    }

}
```