import java.util.Random;
import java.util.Scanner;

public class GallowsGame {

	public static void main(String[] args) {
		
		// INSTRUÇÕES & SAUDAÇÕES AO USUÁRIO
		System.out.println("WELCOME to the Gallows Game!");
		System.out.println();
		
		System.out.println("	D I C A");
		System.out.println("     === Cores ===");
		System.out.println();
		System.out.println("• Você deve acertar as letras da palavra sorteada");
		System.out.println("• Sua única SKILL é a GET LYRICS \n• skill te ajuda a informar as letras da palavra");
		System.out.println("• Se errar DEATH COMES (Você perde):(");
		System.out.println("• Se acertar YOU ARE THE RAINBOW WINNER (Você ganha) :D");
		System.out.println();
		System.out.println("       BOA SORTE!");
		System.out.println();
		
		// Array denominado com 20 posições.
		// Cada posição irá conter uma palavra
		String[] palavras = { "AMARELO", "VERMELHO", "AZUL", "VERDE", "ROSA", "LARANJA", "ROXO", "XANADO", "MARROM",
				"PRETO", "AMETISTA", "BRANCO", "BEGE", "ZAFFRE", "CARAMELO", "CIANO", "CINZA", "DOURADO", "PRATEADO",
				"MAGENTA" };

		// Sortear uma posição (entre 0 e 19)
		// Obter a palavra da respectiva posição.
		Random r = new Random();
		int posição = r.nextInt(20);

		// Deverá ser armazenada no array palavraSorteada
		// (cada posição será um caractere).
		String palavraSorteada = palavras[posição];
		
		// Controla os acertos do usuário, coloca cada caracter como 0 se acertar vira 1 conta como acerto
		char[] acertos = new char[palavraSorteada.length()];
		for (int i = 0; i < acertos.length; i++) {
			acertos[i] = 0;
		}

		// Vidas designadas conforme o tamanho da palavra sorteada
		int lifes = palavraSorteada.length();

		for (int i = 0; i < palavraSorteada.length(); i++) {
			System.out.print(" _ "); // Quantidade de underlines por letra/char da palavra sorteada
		}

		// Scanner pra receber letras digitadas pelo usuário
		Scanner digita = new Scanner(System.in);

		String letrasDigitadas = ""; // String que irá receber
		char letra;

		boolean mizeravi = false; // Declaração do "acertou/mizeravi" fora do FOR como boolean = false para poder colocar dentro do while como condição de parada
		
		// Jogo inicia
		do {

			System.out.print("« Get Lyrics: ");
			letra = digita.next().toUpperCase().charAt(0); // O scanner lê e coloca em caixa alta-charAT(0) pega a primeira letra
			letrasDigitadas += " " + letra;

			// Controlador de vidas || se acertar a letra não perde vida || se errar vida--
			boolean deathComes = true;
			for (int i = 0; i < acertos.length; i++) {

				if (letra == palavraSorteada.charAt(i)) { // Executa se acertar a letra
					acertos[i] = 1;
					deathComes = false;
				}
			}
			if (deathComes) { // Executa se errar a letra
				lifes--;
			}

			// Controlador de acertos
			mizeravi = true;
			for (int i = 0; i < palavraSorteada.length(); i++) {

				if (acertos[i] == 0) { // Se não acertar entra na condição imprime o underline e false pra acerto
					System.out.print(" _ ");
					mizeravi = false;
				} else { // Então se acertar a letra imprime o caracter da palavra sorteada
					System.out.print(" " + palavraSorteada.charAt(i) + " ");
				}
			}

		} while (!mizeravi && lifes > 0);
		
		if(lifes != 0) {
			System.out.println();
			System.out.println("          _                       \n" + 
					"         (_)                      \n" + 
					"__      ___ _ __  _ __   ___ _ __ \n" + 
					"\\ \\ /\\ / / | '_ \\| '_ \\ / _ \\ '__|\n" + 
					" \\ V  V /| | | | | | | |  __/ |   \n" + 
					"  \\_/\\_/ |_|_| |_|_| |_|\\___|_|   ");
			System.out.println();
			System.out.println("   		  ██                  \n" + 
					"                ██▒▒██                \n" + 
					"              ██▒▒▒▒░░██              \n" + 
					"              ██▒▒░░░░██              \n" + 
					"            ██▒▒░░░░░░  ██            \n" + 
					"            ██░░░░░░    ██            \n" + 
					"████████████░░░░░░        ████████████\n" + 
					"██▒▒▒▒▒▒▒▒░░░░██      ██          ▒▒██\n" + 
					"  ██▒▒▒▒░░░░░░██      ██        ▒▒██  \n" + 
					"    ██░░░░░░  ██      ██      ▒▒██    \n" + 
					"      ██░░                  ▒▒██      \n" + 
					"        ██                ▒▒██        \n" + 
					"        ██              ▒▒▒▒██        \n" + 
					"      ██              ▒▒▒▒▒▒▒▒██      \n" + 
					"      ██        ██████▒▒▒▒▒▒▒▒██      \n" + 
					"    ██      ████      ████▒▒▒▒▒▒██    \n" + 
					"    ██    ██              ██▒▒▒▒██    \n" + 
					"    ██████                  ██████  ");
			
		}
		else {
			System.out.println("\n\n		       >>> DEATH COMES <<<");
			System.out.println();
			System.out.println("                   	      .___.\n" + 
		"          /)               ,-^     ^-. \n" + 
		"         //               /           \\\n" + 
		".-------| |--------------/  __     __  \\-------------------.__\n" + 
		"|WMWMWMW| |>>>>>>>>>>>>> | />>\\   />>\\ |>>>>>>>>>>>>>>>>>>>>>>:>\n" + 
		"`-------| |--------------| \\__/   \\__/ |-------------------'^^\n" + 
		"         \\\\               \\    /|\\    /\n" + 
		"          \\)               \\   \\_/   /\n" + 
		"                            |       |\n" + 
		"                            |+H+H+H+|\n" + 
		"                            \\       /\n" + 
		"                             ^-----^\n" + 
		"");
		}

		digita.close();
	}
}
