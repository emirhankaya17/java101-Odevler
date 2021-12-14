# Kullanıcı Girişi

### Ödev
Eğer şifre yanlış ise kullanıcıya şifresini sıfırlayıp sıfırlamayacağını sorun, eğer kullanıcı sıfırlamak isterse yeni girdiği şifrenin hatalı girdiği ve unuttuğu şifre ile aynı olmaması gerektiğini kontrol edip , şifreler aynı ise ekrana "Şifre oluşturulamadı, lütfen başka şifre giriniz." sorun yoksa "Şifre oluşturuldu" yazan programı yazınız.
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        //def
        String usr,pas;
        Scanner sc = new Scanner(System.in);
        //input
        System.out.print("Kullanıcı Adınızı Giriniz: ");
        usr = sc.nextLine();
        System.out.print("Şifrenizi Giriniz: ");
        pas = sc.nextLine();
        //operation
        if(usr.equals("patika") && pas.equals("java123"))
            System.out.println("Başarıyla giriş yaptınız");
        else
        {
            System.out.print("Kullanıcı adı ya da Şifre hatalı. Şifrenizi değiştirmek ister misiniz? 1-> evet 2-> hayır: ");
            int inp = sc.nextInt();
            if(inp == 1)
            {
                System.out.print("Şifrenizi Giriniz: ");
                sc.nextLine();
                String newPas = sc.nextLine();
                if(newPas.equals("java123"))
                    System.out.println("Şifre oluşturulamadı, lütfen başka şifre giriniz.");
                else System.out.println("Şifre oluşturuldu");
            }
        }


    }

}
```