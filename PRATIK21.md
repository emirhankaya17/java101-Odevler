# Palindrom Sayılar
Java ile bir sayının "Palindrom Sayı" olup olmadığını bulan bir program yapıyoruz.

Palindrom Sayı Nedir ?
Palindromik sayı, iki taraftan okunduğu zaman okunuş yönüyle aynı olan sayılardır.

Örnek: 1, 4, 8, 99, 101, 363, 4004, 9889....
```java
class Main{

    public static boolean isPalindrom(int num)
    {
        String strNum = Integer.toString(num);
        boolean returner = true;
        for (int i = 0; i < strNum.length()/2; i++) {
            if(strNum.charAt(i) != strNum.charAt(strNum.length()-1-i))
            {
                returner = false;
                break;
            }
        }

        return returner;
    }


    public static void main(String[] args) {
        System.out.println(isPalindrom(9889));
    }
}
```