package questões;

import java.util.Arrays;
import java.util.Random;

public class Q6 {

    public static void main(String[] args) {

        // Define as dimensões das matrizes
        int linhas1 = 3;
        int colunas1 = 4;
        int linhas2 = 4;
        int colunas2 = 2;

        // Cria as matrizes randomicamente
        int[][] matriz1 = criarMatriz(linhas1, colunas1);
        int[][] matriz2 = criarMatriz(linhas2, colunas2);

        // Imprime as matrizes
        System.out.println("Matriz 1:");
        imprimirMatriz(matriz1);
        System.out.println("Matriz 2:");
        imprimirMatriz(matriz2);

        // Multiplica as matrizes
        int[][] resultado = multiplicarMatrizes(matriz1, matriz2);

        // Imprime o resultado
        System.out.println("Resultado:");
        imprimirMatriz(resultado);
    }

    private static int[][] criarMatriz(int linhas, int colunas) {
        int[][] matriz = new int[linhas][colunas];
        Random random = new Random();
        for (int i = 0; i < linhas; i++) {
            for (int j = 0; j < colunas; j++) {
                matriz[i][j] = random.nextInt(10); // números inteiros entre 0 e 9
            }
        }
        return matriz;
    }

    private static void imprimirMatriz(int[][] matriz) {
        for (int[] linha : matriz) {
            System.out.println(Arrays.toString(linha));
        }
    }

    private static int[][] multiplicarMatrizes(int[][] matriz1, int[][] matriz2) {
        int linhas1 = matriz1.length;
        int colunas1 = matriz1[0].length;
        int linhas2 = matriz2.length;
        int colunas2 = matriz2[0].length;
        if (colunas1 != linhas2) {
            throw new IllegalArgumentException("As matrizes não podem ser multiplicadas");
        }
        int[][] resultado = new int[linhas1][colunas2];
        for (int i = 0; i < linhas1; i++) {
            for (int j = 0; j < colunas2; j++) {
                for (int k = 0; k < colunas1; k++) {
                    resultado[i][j] += matriz1[i][k] * matriz2[k][j];
                }
            }
        }
        return resultado;
    }
}
