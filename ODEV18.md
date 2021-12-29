# Mayın Tarlası Oyunu
Java dilinde Mayın Tarlası oyunu yapmanızı bekliyoruz.

Oyun Kuralları :
Oyun metin tabanlıdır.
Çift boyutlu diziler üzerinden oynanmalı ve MineSweeper sınıfı içerisinde tasarlanmalı.
Matris boyutunu yani satır ve sütun sayısını kullanıcı belirlemeli.
Diziye ait eleman sayısının çeyreği (elemanSayisi / 4) kadar rastgele mayın yerleştirilmeli. Örneğin dizi 4x3 boyutunda ise eleman sayısı (satırSayısı * sütunSayısı) formülü ile hesaplanmalı ve boyutu 12 olmalı. Bu durumda mayın sayısı 12 / 4 = 3 adet olmalıdır. (ipucu : bu mayınların konumlarını tutacak ikinci bir dizi oluşturabilirsiniz.)
Kullanıcı matris üzerinden bir nokta seçmeli. Nokta seçimi için satır ve sütun değerlerini girmeli.
Seçilen noktanın dizinin sınırları içerisinde olup olmadığını kontrol edilmeli ve koşul sağlanmazsa tekrar nokta istenmeli.
Kullanıcının girdiği noktada mayın var ise oyunu kaybetmeli.
Mayın yok ise, ilgili noktaya değen tüm konumlarına bakılmalı (sağı, solu, yukarısı, aşağısı, sol üst çapraz, sağ üst çapraz, sağ alt çapraz, sol alt çapraz) ve etrafındaki mayınların sayısının toplamı ilgili noktaya yazılmalı. Noktaya değen herhangi bir mayın yok ise "0" değeri atanmalı.
Kullanıcı hiç bir mayına basmadan tüm noktaları seçebilirse oyunu kazanmalı.
```java
import java.util.Random;
import java.util.Scanner;

public class MineSweeper {

    public static void drawTable(int[][] gameTable,int [][] mineTable)
    {
        for (int i = 0; i <mineTable.length ; i++) {
            for (int j = 0; j <mineTable[0].length ; j++) {
                if(gameTable[i][j] == 0)
                    System.out.print("- ");
                else
                {
                    if(mineTable[i][j] <9)
                        System.out.print(mineTable[i][j]+" ");
                    else
                        System.out.println("* ");
                }
            }
            System.out.println();
        }
    }
    public static boolean isWin(int[][] gameTable,int [][] mineTable)
    {
        for (int i = 0; i <mineTable.length ; i++) {
            for (int j = 0; j <mineTable[0].length ; j++) {
               if(gameTable[i][j] == 0 && mineTable[i][j] <9) {
                   return false;
               }
            }
        }
        return true;
    }

    public static void main(String[] args) {
        //def
        int row,col;
        boolean isGameOver = false;
        Random rand = new Random();
        Scanner sc = new Scanner(System.in);
        System.out.print("Oyun alanının satır sayısını girin: ");
        row = sc.nextInt();
        System.out.print("Oyun alanının sütun sayısını girin: ");
        col = sc.nextInt();
        int[][] mineTable = new int[row][col];
        int[][] gameTable = new int[row][col];
        //set mines
        int mineCount = (row*col)/4 ;
        for (int i = 0; i < mineCount; i++) {
            int randRow = rand.nextInt(row);
            int randCol = rand.nextInt(col);
            if(mineTable[randRow][randCol] != 0)
                --i;
            else
                mineTable[randRow][randCol] = 9;
        }
        // draw mines
        System.out.println("---------Mines-------");
        for (int i = 0; i <mineTable.length ; i++) {
            for (int j = 0; j <mineTable[0].length ; j++) {
                if(mineTable[i][j] < 9)
                    System.out.print("- ");
                else // değişecek
                    System.out.print("* ");
            }
            System.out.println();
        }
        System.out.println("--------------------");
        //set numbers
        for (int i = 0; i <mineTable.length ; i++) {
            for (int j = 0; j < mineTable[0].length; j++){
                if(mineTable[i][j] >= 9)
                {
                    if(i-1 >= 0)
                    {
                        mineTable[i-1][j] ++;
                        if(j-1 >= 0)
                            mineTable[i-1][j-1] ++;
                        if(j+1 < mineTable[0].length)
                            mineTable[i-1][j+1] ++;
                    }
                    if(i+1 < mineTable.length)
                    {
                        mineTable[i+1][j] ++;
                        if(j-1 >= 0)
                            mineTable[i+1][j-1] ++;
                        if(j+1 < mineTable[0].length)
                            mineTable[i+1][j+1] ++;
                    }
                    if(j-1 >= 0)
                        mineTable[i][j-1] ++;
                    if(j+1 < mineTable[0].length)
                        mineTable[i][j+1] ++;

                }

            }

        }
        System.out.println("--------------------");
        while(!isGameOver)
        {
            drawTable(gameTable,mineTable);
            System.out.print("satır giriniz: ");
            row = sc.nextInt();
            System.out.print("sütun giriniz: ");
            col = sc.nextInt();
            if(row < 0 || row >= mineTable.length || col < 0 || col >= mineTable[0].length)
            {
                System.out.println("Hatalı girdi !!"); continue;
            }
            if(mineTable[row][col] >= 9)
            {
                isGameOver = true;
                System.out.println("MAYINA BASTINIZ");
            }
            if(mineTable[row][col] < 9)
            {
                gameTable[row][col] = 1;
            }
            if(isWin(gameTable,mineTable)) {
                System.out.println("KAZANDINIZ");
                isGameOver = true;
            }
        }
    }

}

```