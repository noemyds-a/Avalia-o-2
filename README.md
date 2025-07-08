# Avalia-o-2import java.util.Scanner;

public class CalculadoraNotas {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        double[] notas = new double[4];
        double soma = 0;

        System.out.println("=== Cálculo de Média de 4 Notas ===");

        for (int i = 0; i < 4; i++) {
            System.out.print("Digite a " + (i + 1) + "ª nota: ");
            notas[i] = scanner.nextDouble();
            soma += notas[i];
        }

        double media = soma / 4;

        System.out.printf("Média: %.2f\n", media);

        if (media >= 7.0) {
            System.out.println("Status: Aprovado ✅");
        } else if (media >= 5.0) {
            System.out.println("Status: Recuperação ⚠️");
        } else {
            System.out.println("Status: Reprovado ❌");
        }

        scanner.close();
    }
}