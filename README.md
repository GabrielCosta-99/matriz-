import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int tamanho = 12;
        int soma = 0;
        int contador = 0;
        String entrada = " ";
        char[][] matriz = {
                { '.', '.', '.', '.', '.', '.', '.', '.', '.', '.', '.', '.' },
                { '.', '.', '.', '.', '.', '.', '.', '.', '.', '.', '.', 'x' },
                { '.', '.', '.', '.', '.', '.', '.', '.', '.', '.', 'x', 'x' },
                { '.', '.', '.', '.', '.', '.', '.', '.', '.', 'x', 'x', 'x' },
                { '.', '.', '.', '.', '.', '.', '.', '.', 'x', 'x', 'x', 'x' },
                { '.', '.', '.', '.', '.', '.', '.', 'x', 'x', 'x', 'x', 'x' },
                { '.', '.', '.', '.', '.', '.', '.', 'x', 'x', 'x', 'x', 'x' },
                { '.', '.', '.', '.', '.', '.', '.', '.', 'x', 'x', 'x', 'x' },
                { '.', '.', '.', '.', '.', '.', '.', '.', '.', 'x', 'x', 'x' },
                { '.', '.', '.', '.', '.', '.', '.', '.', '.', '.', 'x', 'x' },
                { '.', '.', '.', '.', '.', '.', '.', '.', '.', '.', '.', 'x' },
                { '.', '.', '.', '.', '.', '.', '.', '.', '.', '.','.', '.', '.', '.', '.', '.', '.', '.', '.', '.', '.', '.' }
        };

        // Solicitando ao usuário soma ou média
        System.out.println("Digite 'S' para soma ou 'M' para média: ");
        entrada = scanner.nextLine();

        // Calculando a soma ou média dos elementos 'x' da matriz
        for (int linha = 0; linha < tamanho; linha++) {
            for (int coluna = 0; coluna < tamanho; coluna++) {
                if (matriz[linha][coluna] == 'x') {
                    soma++; // Incrementa a soma para cada 'x' encontrado
                    contador++;
                }
            }
        }

        // Verificando e imprimindo o resultado
        if (entrada.equals("M")) {
            System.out.println("Média: " + (double) soma / contador);
        } else if (entrada.equals("S")) {
            System.out.println("Soma: " + soma);
        } else {
            System.out.println("Opção inválida!");
        }
        // Imprimindo a matriz
        System.out.println("Matriz:");
        for (int linha = 0; linha < tamanho; linha++) {
            for (int coluna = 0; coluna < tamanho; coluna++) {
                System.out.print(matriz[linha][coluna] + " ");
            }
            System.out.println();
        }
        // Finalizando o programa
        System.out.println("Fim do programa!");
    }
}
