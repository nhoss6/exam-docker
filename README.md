# Examen Docker

## Partie 1 : graphql-auth

Vous trouverez dans le odssier graphql-auth une api graphql d'user et de post. Cette api permet également de signup/login pour obtenir un jwt.

**Exercice 1**
Créer un dockerfile de dev (appelé *DockerfileDev*) où on installera les dépendances nécessaires à savoir :
 - pnpm
 - prisma
 - node_modules (du package.json)
Ce dockerfile aura pour base une image avec node en version 20, et la commande par défaut lorsqu'on lance le conteneur devra être `pnpm dev`

**Exercice 2**