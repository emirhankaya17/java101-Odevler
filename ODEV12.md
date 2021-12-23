# Asal Sayı Bulan Program
Java dilinde "Recursive" metot kullanarak, kullanıcıdan alınan sayının "Asal" sayı olup olmadığını bulan programı yazın.
```java
import java.util.Scanner;

class Main{

    private static boolean isPrime(int num)
    {
        if(num < 2 )
            return  false;
        else if(num == 2)
            return true;
        else return isPrime(num,2);

    }
    private static boolean isPrime(int num,int divider)
    {
        if(num < 2 )
            return  false;
        else if(num == 2)
            return true;
        else if(num % divider == 0)
            return false;
        else if (divider * divider > num)
            return true;
        else
            return isPrime(num,divider+1);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Sayı Giriniz : ");
        int num = sc.nextInt();
        boolean rslt = isPrime(num);
        if(rslt)
            System.out.println(num+" sayısı ASALDIR !");
        else
            System.out.println(num+" sayısı ASAL değildir !");

    }

}
```