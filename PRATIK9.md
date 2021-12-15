# Sayıları Sıralama

### Ödev
Girilen 3 sayıyı "küçükten büyüğe" sıralayan programı yazınız.

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        //def
        Scanner sc = new Scanner(System.in);
        int s1,s2,s3,temp;
        //inputs
        System.out.print("Sayıları sırasıyla giriniz \ns1: ");
        s1 = sc.nextInt();
        System.out.print("s2: ");
        s2 = sc.nextInt();
        System.out.print("s3: ");
        s3 = sc.nextInt();

        temp = Math.min(Math.min(s1,s2),s3);
        if(temp == s1)
            System.out.println(s1+"<"+Math.min(s2,s3)+"<"+Math.max(s2,s3));
        else if(temp == s2)
            System.out.println(s2+"<"+Math.min(s1,s3)+"<"+Math.max(s1,s3));
        else
            System.out.println(s3+"<"+Math.min(s2,s1)+"<"+Math.max(s2,s1));
    }

}
```