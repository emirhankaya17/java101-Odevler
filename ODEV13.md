# Desene Göre Metot Oluşturma
Java dilinde kullanıcıdan alınan n değerine göre aşağıdaki kurala uyan döngü kullanmadan bir "Recursive" metot yazın.

Kural : Girilen sayı 0 veya negatif olduğu yere kadar girilen sayıdan 5 rakamını çıkarın. Her çıkarma işlemi sırasında ekrana son değeri yazdırın. Sayı negatif veya 0 olduktan sonra tekrar 5 ekleyin. Yine her ekleme işleminde sayının son değerini ekrana yazdırın.
```java
import java.util.Scanner;

class Main{

    //user function
    public static void getSequence(int num)
    {
        if(num <= 0)
            System.out.println("Lütfen pozitif bir sayı giriniz!! ");
        else
            getSequence(num,0,num);
    }
    //recursion overload
    private static void getSequence(int num,int goalNum,int baseNumber)
    {
         if(num < goalNum)
        {
            System.out.print(num+" ");
            if(num+5>= goalNum)
                System.out.println((num+5)+" ");
            else
                getSequence(num+5,goalNum,baseNumber);
        }
         else if(num > goalNum)
         {
             System.out.print(num+" ");
             if((num-5)<= goalNum)
                 getSequence(num-5,baseNumber,baseNumber);
             else
                 getSequence(num-5,goalNum,baseNumber);
         }
    }

    //main
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Bir sayı giriniz: ");
        int num = sc.nextInt();
        getSequence(num);
    }

}
```