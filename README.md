# CFD_Projet_Dedalus

# Informations sur ce dépôt

- Ce projet a été réalisé dans le cadre du cours de M2 de Computational Fluid Dynamics à l'ENS de Lyon
- Il est décomposé en N Notebook résumé ci-dessous 

## 0. Introduction
- Les différentes méthodes numériques
- Pourquoi le projet Dedalus ?

## 1. Fondamentaux sur les méthodes spectrales

### 1.1. Méthode spectrale classique
1. Principe : décomposition et projection du problème dans une base
2. Exemple de la base de Fourrier : référence pour les problèmes périodiques
3. Exemples des Polynômes de Chebyshev : premier aperçu de la famille

> Remarque importantes :
> - Représentation spectrale numérique des fonctions
> - Calcul de produit matriciel
> - Notion de matrice dense et de matrice creuse/sparse

### 1.2. Méthode de Galerkin
1. Principe : décomposition la base d'essaie et projection dans la base de test
2. Exemples des polynômes de Chebyshev : référence pour les problèmes non périodiques

> Remarque importantes :
> - Choix de la base d'essaie et la base de test
> - Diagonalité d'un matrice diagoanle décalée 

### 1.3. Minimisation de l'erreur et imposition des conditions aux bords
1. Notion de résidu : erreur numérique
2. La méthode de "collocation" : approximation aux points spécifiques du domaine
3. Méthode "tau" : résolution exacte par ajout de termes

### 1.4 Résumé de la section
