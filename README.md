import java.util.Scanner;

public class conversion {
    public static void main(String[] args) {

            /* On demande à l'utilisateur quelle conversion veut-il effectuer, puis on initialise une variable
             * 'primaryAnswer' de type Scanner qui va créer un espace de stockage pour pouvoir être ensuite
             * récupérer par la variable 'initialisation' de type String.
             * L'utilisateur va ensuite taper dans la console 1 ou 2, pour faire son choix.
             *
             * On crée ensuite une condition IF pour orienter le programme selon ceux qu'a choisi de faire
             * l'utilisateur
             *
             * SI la conversion est égal à 1, (donc la conversion Celsius - Fahrenheit), alors le programme demande
             * à l'utilisateur d'entrer un réel (ce dernier sera stocker dans la variable celsiusValue qui a pour
             * type Double). Puis la variable conversionValue se chargera de convertir la valeur en Fahrenheit.
             * On affiche ensuite le résultat calculer.
             *
             * SI la conversion est égal à 0, (donc la conversion - Fahrenheit), alors le programme demande
             * à l'utilisateur d'entrer un réel (ce dernier sera stocker dans la variable fahrenheitValue qui a pour
             * type Double). Puis la variable conversion2Value se chargera de convertir la valeur en Celsius.
             * On affiche ensuite le résultat calculer.
             */

            int first = 1, second = 2;
            System.out.println("Choisir le mode de Conversion: ");
            System.out.println(first + " - Convertisseur Celsius - Fahrenheit");
            System.out.println(second + " - Convertisseur Fahrenheit - Celsius");

            Scanner primaryAnswer  = new Scanner(System.in);
            int initialisation = primaryAnswer.nextInt();

            if (initialisation == 1) {
                System.out.println("Température à convertir : ");
                Scanner reponseA = new Scanner(System.in);
                double celsiusValue = reponseA.nextDouble();
                double conversionValue = celsiusValue * 9 / 5 + 32;
                System.out.println("La valeur en Fahrenheit est de : " + conversionValue);
            }
            else {

                System.out.println("Température à convertir : ");
                Scanner reponseB = new Scanner(System.in);
                double fahrenheitValue = reponseB.nextDouble();
                double conversion2Value = ((fahrenheitValue - 32) * 5) / 9;
                System.out.println("La Valeur en Celsius est de : " + conversion2Value);
            }
    }
}
