# Dotfiles de florianspk

Ce dépôt contient mes fichiers de configuration (dotfiles) gérés avec [Chezmoi](https://www.chezmoi.io/).

## Installation

### Prérequis
- [Chezmoi](https://www.chezmoi.io/install/) installé
- Git installé

### Déploiement des dotfiles
```sh
chezmoi init --apply florianspk
```

Si le dépôt est déjà cloné :
```sh
chezmoi apply
```

## Gestion des modifications

### Modifier un fichier suivi par Chezmoi
Utiliser :
```sh
chezmoi edit ~/.bashrc  # Exemple avec .bashrc
```

### Ajouter un nouveau fichier
```sh
chezmoi add ~/.config/nvim/init.lua
```

### Mettre à jour les dotfiles dans le dépôt
```sh
chezmoi cd
git add .
git commit -m "Mise à jour des dotfiles"
git push
```

## Synchronisation des mises à jour
Si des changements sont faits sur une autre machine :
```sh
chezmoi update
```

## Structure du dépôt
- `.local_*` : Fichiers spécifiques à une machine
- `run_once_*` : Scripts exécutés une seule fois à l’installation
- `scripts/` : Scripts d’installation et de configuration

## Licence
Ce projet est sous licence MIT. Voir [LICENSE](LICENSE) pour plus de détails.

