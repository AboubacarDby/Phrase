# Phrase
package fr.gouv.finances.exo;

import java.util.Scanner;

public class exercicePhrase {

    public static void main(String[] args) {
	// creation du tableau de caractère avec les voyelles concernées.
	// creation de la variable Scanner pour pouvoir insérer la phrase.
	// creation de plusieurs boucles pour savoir si la phrase écrite contient le
	// nombre de voyelles possibles.
	// ne peut pas utiliser contains.
	char[] texte = { 'a', 'A', 'e', 'E', 'i', 'I', 'o', 'O', 'u', 'U', 'y', 'Y' };
	String maPhrase;
	int nbVoyelle = 0;
	int i;
	int j;
	Scanner saisie = new Scanner(System.in);

	maPhrase = saisie.nextLine();// saisir la phrase que l'on veut.
	for (i = 0; i < maPhrase.length(); i++) {
	    char c = maPhrase.charAt(i);

	    for (j = 0; j < texte.length; j++) {

		if (maPhrase.charAt(i) == texte[j]) {
		    nbVoyelle++;
		}
	    }

	}
	System.out.println("Nombre de voyelles :" + nbVoyelle);
	saisie.close();
    }
}
