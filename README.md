# Desafio Round 6
Jogo do serie Round 6 onde o desafio é acertar o caminho correto para atravessar.


       import java.util.Random;

        import javax.swing.JOptionPane;

        public class DesafioRound6 {

	public static void main(String[] args) {

		String jogador = JOptionPane.showInputDialog("Digite seu numero de cadastro:", "XXX");
		
		int j = 0;
		
		do {
		
		int c = 0;
		int x = 0;
		int b = 0;

			JOptionPane.showMessageDialog(null, "ATENÇÃO \n O JOGO VAI COMEÇAR!", "ULTIMO JOGO",
					JOptionPane.INFORMATION_MESSAGE);

			while (c < 6 && b != 1) {

				Random r = new Random();
				int d = r.nextInt(100);
				System.out.println(d);

				if (d % 2 == 0) {
					d = 0;
				}
				if (d % 2 != 0) {
					d = 1;
				}

				String entrada = JOptionPane.showInputDialog("Direita (D) ou Esquerda (E)", "ESCOLHA COM CUIDADO!");
				entrada = entrada.toUpperCase();
				c++;

				if (entrada.contentEquals("DIREITA") || entrada.contentEquals("D")) {
					x = 0;
					JOptionPane.showMessageDialog(null, "Você pulou para a DIREITA.", "JOGADOR Nº: " + jogador,
							JOptionPane.WARNING_MESSAGE);
				}
				if (entrada.contentEquals("ESQUERDA") || entrada.contentEquals("E")) {
					x = 1;
					JOptionPane.showMessageDialog(null, "Você pulou para a ESQUERDA.", "JOGADOR Nº: " + jogador,
							JOptionPane.WARNING_MESSAGE);
				}
				if (x != d) {
					b = 1;
					JOptionPane.showMessageDialog(null, "Você MORREU!", "JOGADOR Nº: " + jogador,
							JOptionPane.ERROR_MESSAGE);
				}
				if (x == d && c < 6) {
					b = 2;
					JOptionPane.showMessageDialog(null, "Seguro, dê o proximo passo!", "JOGADOR Nº: " + jogador,
							JOptionPane.INFORMATION_MESSAGE);
				}
				if (c == 6) {
					JOptionPane.showMessageDialog(null, "!!! PARABENS VOCÊ ATRAVESSOU !!!", "JOGADOR Nº: " + jogador,
							JOptionPane.INFORMATION_MESSAGE);
				}
			}
			String novamente = JOptionPane.showInputDialog("Jogar novamente? 1 - Sim | 0 - Não");
			j = Integer.parseInt(novamente);
		} while (j == 1);
	}
    }
    
!!!ENGLISH!!!

# Squid Game Challenge
Squid Game Challenge that you have to find the right path to cross.

       import java.util.Random;

        import javax.swing.JOptionPane;

        public class SquidGameChallenge {

	public static void main(String[] args) {

		String player = JOptionPane.showInputDialog("Type your number:", "XXX");
		
		int j = 0;
		
		do {
		
		int c = 0;
		int x = 0;
		int b = 0;

			JOptionPane.showMessageDialog(null, "WATCH \n THE GAME HAS BEGUN!", "LAST CHALLENGE.",
					JOptionPane.INFORMATION_MESSAGE);

			while (c < 6 && b != 1) {

				Random r = new Random();
				int d = r.nextInt(100);
				System.out.println(d);

				if (d % 2 == 0) {
					d = 0;
				}
				if (d % 2 != 0) {
					d = 1;
				}

				String in = JOptionPane.showInputDialog("Right (R) ou Left (L)", "CHOOSE WISELY!");
				in = in.toUpperCase();
				c++;

				if (in.contentEquals("RIGHT") || entrada.contentEquals("R")) {
					x = 0;
					JOptionPane.showMessageDialog(null, "You jumped to the RIGHT.", "PLAYER Nº: " + player,
							JOptionPane.WARNING_MESSAGE);
				}
				if (entrada.contentEquals("LEFT") || entrada.contentEquals("L")) {
					x = 1;
					JOptionPane.showMessageDialog(null, "You jumped to the LEFT.", "PLAYER Nº: " + player,
							JOptionPane.WARNING_MESSAGE);
				}
				if (x != d) {
					b = 1;
					JOptionPane.showMessageDialog(null, "YOU DIED!", "PLAYER Nº: " + player,
							JOptionPane.ERROR_MESSAGE);
				}
				if (x == d && c < 6) {
					b = 2;
					JOptionPane.showMessageDialog(null, "Safety, choose the next step!", "PLAYER Nº: " + player,
							JOptionPane.INFORMATION_MESSAGE);
				}
				if (c == 6) {
					JOptionPane.showMessageDialog(null, "!!! CONGRATULATIONS YOU CROSSED !!!", "PLAYER Nº: " + player,
							JOptionPane.INFORMATION_MESSAGE);
				}
			}
			String again = JOptionPane.showInputDialog("AGAIN? 1 - Yes | 0 - No");
			j = Integer.parseInt(again);
		} while (j == 1);
	}
    }
