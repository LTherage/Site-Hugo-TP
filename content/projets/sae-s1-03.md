+++
title = "SAÉ S1.03 - Comparaison d'approches algorithmiques (Partie 2)"
date = 2025-05-30
draft = false
description = "Programmation et comparaison de différents algorithmes de tri sur des tableaux de coordonnées GPS au format DMS (Degrés, Minutes, Secondes)."
tags = ["HTML", "CSS", "Gestion de Projet", "Marketing", "Événementiel"]
image = "https://fakeimg.pl/640x150/b319b3/ebe2e2&text=SAE+S1.05-06"
texte_alt = "Image de SAÉ S1.03"
languages = ["Java", "Algorithmique", "Tri"]
+++


# SAÉ S1.02 - Comparaison d'approches algorithmiques (Partie 2)
*22 janvier 2025 - IUT de Lens*

## Résumé du Projet
Implementation et comparaison de différents algorithmes de tri sur des tableaux de coordonnées GPS au format DMS (Degrés, Minutes, Secondes).

### Objectif
Programmer et comparer l'efficacité de différents algorithmes de tri sur des tableaux de coordonnées GPS au format DMS (Degrés, Minutes, Secondes).

### Algorithmes à Implémenter
- Tri par fusion (récursif)
- Tri rapide (récursif)
- Tri à bulles bidirectionnel
- Le meilleur algorithme de la partie 1 (adapté)

### Structure de Données
- Tableaux 2D de taille n×3 (n lignes, 3 colonnes pour DMS)
- Tri par ordre croissant : degrés → minutes → secondes

### Tests et Évaluation
- Tailles de tableaux : 10000, 20000, 30000, 50000, 70000
- 10 tests par algorithme et taille
- Mesures : temps min, max et moyen

### Conditions Techniques
- Programmation en Java
- Génération aléatoire des données depuis sourceData.txt
- Documentation complète du code (spécifications, paramètres, commentaires)

### Livrables
- Code source commenté
- Rapport PDF (2-3 pages) incluant :
    - Résumé du travail
    - Répartition des tâches
    - Tableaux comparatifs des résultats
    - Difficultés rencontrées
    - Conclusion

### Notation
- Partie 1 (novembre 2024) : 40%
- Partie 2 (janvier 2025) : 60%

```java
public class TriBullesBidirectionnel {
    /**
     * Tri à bulles bidirectionnel pour un tableau de coordonnées DMS
     * @param tableau Tableau 2D où chaque ligne contient [degrés, minutes, secondes]
     */
    public static void trier(int[][] tableau) {
        boolean echange;
        int debut = 0;
        int fin = tableau.length - 1;
        
        do {
            echange = false;
            
            // Phase aller (gauche vers droite)
            for (int i = debut; i < fin; i++) {
                if (comparer(tableau[i], tableau[i + 1]) > 0) {
                    echanger(tableau, i, i + 1);
                    echange = true;
                }
            }
            
            if (!echange) {
                break;
            }
            
            echange = false;
            fin--;
            
            // Phase retour (droite vers gauche)
            for (int i = fin - 1; i >= debut; i--) {
                if (comparer(tableau[i], tableau[i + 1]) > 0) {
                    echanger(tableau, i, i + 1);
                    echange = true;
                }
            }
            
            debut++;
            
        } while (echange && debut < fin);
    }
    
    /**
     * Compare deux coordonnées DMS
     * @param coord1 Première coordonnée [degrés, minutes, secondes]
     * @param coord2 Seconde coordonnée [degrés, minutes, secondes]
     * @return -1 si coord1 < coord2, 0 si égaux, 1 si coord1 > coord2
     */
    private static int comparer(int[] coord1, int[] coord2) {
        // Comparaison des degrés
        if (coord1[0] != coord2[0]) {
            return coord1[0] - coord2[0];
        }
        // Si degrés égaux, comparaison des minutes
        if (coord1[1] != coord2[1]) {
            return coord1[1] - coord2[1];
        }
        // Si minutes égales, comparaison des secondes
        return coord1[2] - coord2[2];
    }
    
    /**
     * Échange deux éléments dans le tableau
     * @param tableau Tableau de coordonnées
     * @param i Index du premier élément
     * @param j Index du second élément
     */
    private static void echanger(int[][] tableau, int i, int j) {
        int[] temp = tableau[i];
        tableau[i] = tableau[j];
        tableau[j] = temp;
    }
    
    /**
     * Exemple d'utilisation
     */
    public static void main(String[] args) {
        // Exemple de tableau de coordonnées DMS
        int[][] coordonnees = {
            {54, 2, 23},
            {25, 33, 23},
            {4, 14, 5},
            {31, 26, 47},
            {0, 32, 37},
            {8, 14, 52},
            {25, 14, 36},
            {47, 17, 14},
            {14, 59, 48},
            {53, 29, 9}
        };
        
        System.out.println("Avant le tri :");
        afficherTableau(coordonnees);
        
        trier(coordonnees);
        
        System.out.println("\nAprès le tri :");
        afficherTableau(coordonnees);
    }
    
    /**
     * Affiche le tableau de coordonnées
     * @param tableau Tableau à afficher
     */
    private static void afficherTableau(int[][] tableau) {
        for (int[] coords : tableau) {
            System.out.printf("(%d° %d' %d\") %n", 
                            coords[0], coords[1], coords[2]);
        }
    }
}
```
