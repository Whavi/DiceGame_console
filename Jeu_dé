import java.lang.Math;
import java.lang.Thread;

public class Jeu_de_dé2 {

	public static void main(String[] args) throws InterruptedException {
		// Définir le nom des deux joueurs
		String name1, name2;

		name1 = Saisie.lire_String("Joueur 1 veuillez saisir votre nom"); // saisie du nom du joueur 1
		name2 = Saisie.lire_String("Joueur 2 veuillez saisir votre nom"); // saisie du nom du joueur 2

		System.out.println("Bienvenue au jeu de dé, allez jouer au jeu de dé " + name1 + " et " + name2);
		Thread.sleep(1000);
		System.out.println("");
		System.out.println("Le robot va choisir quel joueur commence !");
		System.out.println("");

		// définir le joueur qui commence
		int range_joueur = 1 - 0 + 1; // la variable aléatoire du random math
		boolean joueur_courant1 = false, joueur_courant2 = false; // boolean du joueur1 et du joueur2 qui ne joue pas

		for (int c = 0; c < 1; c++) {
			int joueur_commence = (int) (Math.random() * range_joueur) + 0; // random qui designe le joueur qui commence

			if (joueur_commence == 1) {
				Thread.sleep(1000);
				System.out.println("C'est " + name1 + " qui commence !");
				System.out.println("");
				joueur_courant1 = true; // boolean du joueur1 qui joue
				joueur_courant2 = false; // boolean du joueur2 qui ne joue pas

			} else {
				Thread.sleep(1000);
				System.out.println("C'est " + name2 + " qui commence !");
				System.out.println("");
				joueur_courant1 = false; // boolean du joueur1 qui ne joue pas
				joueur_courant2 = true; // boolean du joueur2 qui joue
			}
		}
		// définir le score max, les lancer et le compteur

		int score_joueur1 = 0, score_joueur2 = 0; // initialisation du score du joueur1 et joueur2
		int lancer = 1;
		// définir le min, max et la range pour les dé

		int range = 6 - 1 + 1; // la variable aléatoire du random math
		boolean fin = false; // boolean de la fin du jeu

		// definir le boolean pour break
		while (fin == false) { // tant que la fin est faux alors le programme continue

			for (var p = 0; p < 1; p++) {
				var rand1 = (int) (Math.random() * range) + 1; // random qui désigne le nombre aléatoire pour le joueur1
				var rand2 = (int) (Math.random() * range) + 1; // random qui désigne le nombre aléatoire pour le joueur2

				if (joueur_courant1 == true) {	
					System.out.println("");
					System.out.println("==========={Lancer N°" + lancer+"}============");
					Thread.sleep(1000);
					System.out.println("=============={"+name1+"}==============");
					System.out.println("");

					lancer++; // le nombre de lancer que le robot a fait
					score_joueur1 = score_joueur1 + rand1; // le score du joueur1

					System.out.println(name1 + " lance le dés et c'est le : " + rand1);
					System.out.println(name1 + " Ton score est de  :  " + score_joueur1 + " point(s)");
					System.out.println("");
					System.out.println("");

					Thread.sleep(1000);

					if (score_joueur1 >= 30 && score_joueur1 >= score_joueur2) {
						joueur_courant1 = false; // boolean du joueur1 qui ne joue pas
						joueur_courant2 = false; // boolean du joueur2 qui ne joue pas

					} else if (rand1 == 6) {
						joueur_courant1 = true; // boolean du joueur1 qui joue
						joueur_courant2 = false; // boolean du joueur2 qui ne joue pas

					} else {
						joueur_courant1 = false; // boolean du joueur1 qui ne joue pas
						joueur_courant2 = true; // boolean du joueur2 qui joue
					}

				} else if (joueur_courant2 == true) {
					System.out.println("");
					System.out.println("==========={Lancer N°" + lancer+"}============");
					Thread.sleep(1000);
					System.out.println("=============={"+name2+"}==============");
					System.out.println("");


					lancer++; // le nombre de lancer que le robot a fait
					score_joueur2 = score_joueur2 + rand2;// le score du joueur1

					System.out.println(name2 + " lance le dés et c'est le : " + rand2);
					System.out.println(name2 + " Ton score est de  : " + score_joueur2 + " point(s)");
					System.out.println("");
					System.out.println("");

					Thread.sleep(750);

					if (score_joueur2 >= 30 && score_joueur2 >= score_joueur1) {
						joueur_courant1 = false; // boolean du joueur1 qui ne joue pas
						joueur_courant2 = false; // boolean du joueur2 qui ne joue pas

					} else if (rand2 == 6) {
						joueur_courant1 = false; // boolean du joueur1 qui ne joue pass
						joueur_courant2 = true; // boolean du joueur2 qui joue

					} else {
						joueur_courant1 = true; // boolean du joueur1 qui joue
						joueur_courant2 = false; // boolean du joueur2 qui ne joue pas
					}

				} else {
					if (score_joueur1 >= score_joueur2) {
						System.out.println(name1 + " à gagné !");
						fin = true; // boolean de la fin du jeu qui s'arrete
					} else {
						System.out.println(name2 + " à gagné !");
						fin = true; // boolean de la fin du jeu qui s'arrete
					}
				}
			}
		}
	}
}
