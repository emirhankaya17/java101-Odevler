# Sınıfı Geçme Durumu

Dersler : Matematik, Fizik, Türkçe, Kimya, Müzik

Geçme Notu : 55

Ödev
Eğer girilen ders notları 0 veya 100 arasında değil ise ortalamaya katılmasın.
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        //def
        Scanner sc = new Scanner(System.in);
        int passGrade = 55;
        int invalidGrades = 0;

        //inputs
        System.out.println("Matematik notunuzu girin: ");
        int mat = sc.nextInt();
        if(mat == 0 ||mat == 100) {++invalidGrades; mat = 0;}

        System.out.println("Fizik notunuzu girin: ");
        int fiz = sc.nextInt();
        if(fiz == 0 ||fiz == 100) {++invalidGrades; fiz = 0;}

        System.out.println("Kimya notunuzu girin: ");
        int kim = sc.nextInt();
        if(kim == 0 ||kim == 100) {++invalidGrades; kim = 0;}

        System.out.println("Türkçe notunuzu girin: ");
        int tur = sc.nextInt();
        if(tur == 0 ||tur == 100) {++invalidGrades; tur = 0;}

        System.out.println("Müzik notunuzu girin: ");
        int muz = sc.nextInt();
        if(muz == 0 ||muz == 100) {++invalidGrades; muz = 0;}

        //operation
        double ort = 0;
        if(invalidGrades != 5)
            ort = (double)(mat + fiz + kim + tur + muz)/ (5-invalidGrades);
        System.out.println("Ortalama: "+ort);

        //odev
        System.out.println(ort>=passGrade ? "Sınıfı Geçti":"Sınıfta Kaldı");
        
    }

}
```