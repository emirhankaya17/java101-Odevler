# ATM Projesi
### Ödev
Aynı projedeki ATM işlemlerini "Switch-Case" kullanarak yapınız.
```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        //def
        String userName, password;
        Scanner input = new Scanner(System.in);
        int right = 0;
        int balance = 1500;
        int select;
        boolean token = false;
        //input
        while (right<3)
        {
            System.out.print("Kullanıcı Adınız :");
            userName = input.nextLine();
            System.out.print("Parolanız : ");
            password = input.nextLine();
            if(userName.equals("patika") && password.equals("dev123"))
            {
                token = true;
                break;
            }
            right++;
            System.out.println("Hatalı kullanıcı adı veya şifre. Tekrar deneyiniz.");
        }
        if(token)
        {
            System.out.println("Merhaba, Kodluyoruz Bankasına Hoşgeldiniz!");
            while (token)
            {
                System.out.println("1-Para yatırma\n" +
                        "2-Para Çekme\n" +
                        "3-Bakiye Sorgula\n" +
                        "4-Çıkış Yap");
                System.out.print("Lütfen yapmak istediğiniz işlemi seçiniz : ");
                select = input.nextInt();
                switch(select) {
                    case 1:
                        System.out.print("Para miktarı : ");
                        int price = input.nextInt();
                        balance += price;
                        break;
                    case 2:
                        System.out.print("Para miktarı : ");
                        price = input.nextInt();
                        if (price > balance) {
                            System.out.println("Bakiye yetersiz.");
                        } else {
                            balance -= price;
                        }
                        break;
                    case 3:
                        System.out.println("Bakiyeniz : " + balance);
                        break;
                    case 4:
                        token = false;
                        System.out.println("Tekrar görüşmek üzere.");
                        break;
                    default:
                        // code block
                }
            }
        }

    }
}
```