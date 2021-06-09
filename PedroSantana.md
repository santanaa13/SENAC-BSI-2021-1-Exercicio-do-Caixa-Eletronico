import java.util.*;

public class Main {

    public Main() {
        // TODO Auto-generated constructor stub
    }

    public static void main(String[] args) {
        int qtd100 = 0;
        int qtd50 = 0;
        int qtd20 = 0;
        int qtd10 = 0;
        int qtd5 = 0;
        int qtd2 = 0;
        int qtd1 = 0;
        int vlrSaque= 0;
        Scanner read = new Scanner(System.in);
        System.out.println("Digite o valor do saque:");
        vlrSaque = read.nextInt();

        while (vlrSaque >= 100){
            if (vlrSaque%100 == 0)
            {
                qtd100 = vlrSaque/100;
                vlrSaque = 0;
            }
            else {
            vlrSaque = vlrSaque - 100;
            qtd100++;
            }
        }

        while (vlrSaque >= 50){
            vlrSaque = vlrSaque - 50;
            qtd50++;
        }


        while (vlrSaque >= 20){
            vlrSaque = vlrSaque - 20;
            qtd20++;
        }

        while (vlrSaque >= 10){
            vlrSaque = vlrSaque - 10;
            qtd10++;
        }

        while (vlrSaque >= 5){
            vlrSaque = vlrSaque%5;
            qtd5++;
        }

        while (vlrSaque >= 2){
            vlrSaque = vlrSaque%2;
            qtd2++;
        }

        if (vlrSaque == 1)
            qtd1 = 1;

        System.out.println("O caixa liberou:");
        if (qtd100 > 0)
            System.out.println( qtd100 + " nota(s) de 100");
        if (qtd50 > 0)
            System.out.println( qtd50 + " nota de 50");
        if (qtd20 > 0)
            System.out.println( qtd20 + " nota(s) de 20");
        if (qtd10 > 0)
            System.out.println( qtd10 + " nota de 10");
        if (qtd5 > 0)
            System.out.println( qtd5 + " nota de 5");
        if (qtd2 > 0)
            System.out.println( qtd2 + " nota(s) de 2");
        if (qtd1 > 0)
           System.out.println( qtd1 + " nota de 1");
  }
}
