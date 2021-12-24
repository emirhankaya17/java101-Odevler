# Maaş Hesaplayıcı
Java'da "Employee" adında fabrika çalışanlarını temsil eden ve metotları ile çalışanların maaşlarını hesaplayan bir sınıf yazmalısınız. Bu sınıf 4 nitelik ve 5 metoda sahip olacaktır.

### Sınıfın Nitelikleri

name : Çalışanın adı ve soyadı
salary : Çalışanın maaşı
workHours : Haftalık çalışma saati
hireYear : İşe başlangıç yılı
Sınıfın Metotları

Employee(name,salary,workHours,hireYear) : Kurucu metot olup 4 parametre alacaktır.
tax() : Maaşa uygulanan vergiyi hesaplayacaktır.
Çalışanın maaşı 1000 TL'den az ise vergi uygulanmayacaktır.
Çalışanın maaşı 1000 TL'den fazla ise maaşının %3'ü kadar vergi uygulanacaktır.
bonus() : Eğer çalışan haftada 40 saatten fazla çalışmış ise fazladan çalıştığı her saat başına 30 TL olacak şekilde bonus ücretleri hesaplayacaktır.
raiseSalary() : Çalışanın işe başlangıç yılına göre maaş artışını hesaplayacaktır. Şuan ki yılı 2021 olarak alın.
Eğer çalışan 10 yıldan az bir süredir çalışıyorsa maaşına %5 zam yapılacaktır.
Eğer çalışan 9 yıldan fazla ve 20 yıldan az çalışıyorsa maaşına %10 zam yapılacaktır.
Eğer çalışan 19 yıldan fazla çalışıyorsa %15 zam yapılacaktır.
toString() : Çalışana ait bilgileri ekrana bastıracaktır.
```java
public class Main {
    public static void main(String[] args) {
        Employee emp = new Employee("Kemal",2000,45,1985);
        emp.print();

    }
}
```
```java
public class Employee {
    String name;
    double salary;
    int workHours;
    int hireYear;

    public Employee(String name, int salary, int workHours, int hireYear) {
        this.name = name;
        this.salary = salary;
        this.workHours = workHours;
        this.hireYear = hireYear;
    }
    public double tax()
    {
        if(salary<1000)
            return 0;
        else
            return salary* .03;
    }

    public int bonus()
    {
        if(workHours > 40)
            return (workHours-40)*30;
        else
            return 0;
    }

    public double raiseSalary()
    {
        if(2021-hireYear<0)
        {
            System.out.println("Tarihi yanlış girdiniz. Ücrete zam yapılamadı");
            return 0;
        }

        else if(2021-hireYear<10)
        {
            double dif = salary * .5;
            salary +=dif;
            return dif;
        }
        else if(2021-hireYear<20)
        {
            double dif = salary * .10;
            salary +=dif;
            return dif;
        }
        else
        {
            double dif = salary * .15;
            salary +=dif;
            return dif;
        }
    }

    public void print() //toString() needs override method
    {
        System.out.println("Adı : "+name);
        System.out.println("Maaşı : "+salary);
        System.out.println("Çalışma Saati : "+workHours);
        System.out.println("Başlangıç Yılı : "+hireYear);
        System.out.println("Vergi : "+tax());
        System.out.println("Bonus : "+bonus());
        System.out.println("Maaş Artışı : "+raiseSalary());
        System.out.println("Vergi ve Bonuslar ile birlikte maaş : "+(salary + bonus() - tax()));
        System.out.println("Toplam Maaş : "+salary);
    }
}

```