import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        final int LIMITE_PESSOAS = 5;
        final double LIMITE_PESO = 300.0;

        Scanner scanner = new Scanner(System.in);
        int pessoas = 0;
        double pesoTotal = 0;

        while (pessoas < LIMITE_PESSOAS) {
            System.out.print("Digite o peso da pessoa (ou 0 para encerrar): ");
            double peso = scanner.nextDouble();

            if (peso <= 0) break;

            if (pesoTotal + peso > LIMITE_PESO) {
                System.out.println("Limite de peso atingido! Esta pessoa não pode entrar.");
                break;
            }

            pessoas++;
            pesoTotal += peso;
            System.out.println("Elevador atual: " + pessoas + " pessoa(s) e " + pesoTotal + " kg.\n");
        }

        System.out.println("\nsubindo com " + pessoas + " pessoas e " + pesoTotal + " kg");
        scanner.close();
    }
}
