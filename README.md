# Power 4 Web

Un Puissance 4 jouable dans le navigateur, à deux sur le même écran. Le serveur est écrit en Go (`net/http`, templates HTML), l'interface en HTML et CSS.

Projet d'école réalisé à Ynov (projet solo).

## Fonctionnalités

- **3 niveaux de difficulté** (taille de la grille) :
  - Normal : 6 × 7
  - Difficile : 6 × 9
  - Expert : 7 × 8
- Noms des joueurs personnalisables
- Détection de la victoire et du match nul
- Bouton pour recommencer la partie

## Lancer le jeu

### Prérequis

- [Go](https://go.dev/dl/) 1.22 ou plus récent

### Installation

```bash
git clone https://github.com/zTatoune/-power4-web.git
```

```bash
cd -power4-web
```

### Démarrer le serveur

```bash
go run .
```

Puis ouvre **http://localhost:8080** dans ton navigateur.

## Comment jouer

1. Entre les noms des deux joueurs.
2. Choisis une difficulté.
3. Clique sur « Commencer la partie ».
4. Chacun son tour, clique sur une colonne pour y faire tomber un jeton.
5. Le premier qui aligne 4 jetons (horizontalement, verticalement ou en diagonale) gagne.

## Structure

| Fichier | Rôle |
|---|---|
| `main.go` | Point d'entrée |
| `src/server.go` | Routes et serveur HTTP (port 8080) |
| `src/handler.go` | Pages : accueil, partie, coup joué, remise à zéro |
| `src/game.go` | Règles du jeu : grille, chute des jetons, victoire |
| `page/`, `index.html` | Templates HTML |
| `static/style.css` | Styles |
