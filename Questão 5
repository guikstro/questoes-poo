package questões;

import java.io.File;
import java.io.FileNotFoundException;
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

public class Q5 {

    public static void main(String[] args) {

        // Cria um objeto File para representar o arquivo de texto
        File file = new File("arquivo.txt");

        try {
            // Cria um Scanner para ler o arquivo de texto
            Scanner scanner = new Scanner(file);

            // Cria uma lista para armazenar as palavras que contêm "link"
            List<String> palavrasComLink = new ArrayList<>();

            // Itera sobre cada palavra do arquivo de texto e verifica se contém "link"
            while (scanner.hasNext()) {
                String palavra = scanner.next();
                if (palavra.contains("link")) {
                    palavrasComLink.add(palavra);
                }
            }

            // Exibe as palavras que contêm "link"
            System.out.println("Palavras com 'link':");
            for (String palavra : palavrasComLink) {
                System.out.println(palavra);
            }

            // Fecha o Scanner
            scanner.close();

        } catch (FileNotFoundException e) {
            System.out.println("O arquivo não foi encontrado: " + e.getMessage());
        }
    }
}
