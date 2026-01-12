# TP : Clone vs Fork sur GitHub

## 🎯 Objectifs pédagogiques

À la fin de ce TP, vous serez capable de :
- Comprendre la différence entre `git clone` et un fork GitHub
- Savoir quand utiliser l'un ou l'autre
- Créer et gérer un fork
- Contribuer à un projet via Pull Request

## ⏱️ Durée estimée
45 minutes

## 📋 Prérequis

- Avoir un compte GitHub
- Git installé sur votre machine
- Connaissances de base de Git (commit, push, pull)

## 📚 Partie 1 : Comprendre le CLONE

### Qu'est-ce qu'un clone ?

Un **clone** est une copie locale d'un repository Git. Il permet de :
- Travailler sur le code en local
- Récupérer tout l'historique Git
- Synchroniser avec le repository distant

### ⚠️ Limitation importante

Quand vous clonez un repository qui ne vous appartient pas, vous **ne pouvez pas** pousser de modifications directement sur le repository original (sauf si vous avez les droits d'écriture).

### 🔨 Exercice 1 : Cloner ce repository

1. Copiez l'URL de ce repository
2. Dans votre terminal, exécutez :
```bash
git clone [URL_DU_REPO]
cd [NOM_DU_REPO]
```

3. Vérifiez les remotes configurés :
```bash
git remote -v
```

**Question 1.1** : Que voyez-vous ? Notez votre réponse dans `reponses.md`

4. Créez une nouvelle branche :
```bash
git checkout -b test-clone
```

5. Modifiez le fichier `exercice1.txt` en ajoutant votre nom
6. Commitez vos modifications :
```bash
git add exercice1.txt
git commit -m "Ajout de mon nom"
```

7. Essayez de pousser :
```bash
git push origin test-clone
```

**Question 1.2** : Que se passe-t-il ? Pourquoi ? Notez votre réponse dans `reponses.md`

---

## 🍴 Partie 2 : Comprendre le FORK

### Qu'est-ce qu'un fork ?

Un **fork** est une copie complète d'un repository sur **votre compte GitHub**. Il permet de :
- Avoir votre propre version du projet
- Pousser des modifications librement
- Proposer des contributions au projet original via Pull Request
- Synchroniser avec le repository original

### 🔨 Exercice 2 : Forker ce repository

1. Cliquez sur le bouton **"Fork"** en haut à droite de la page GitHub
2. Le fork sera créé sur votre compte personnel

3. Clonez VOTRE fork :
```bash
git clone https://github.com/VOTRE_USERNAME/[NOM_DU_REPO].git
cd [NOM_DU_REPO]
```

4. Vérifiez les remotes :
```bash
git remote -v
```

**Question 2.1** : Quelle différence voyez-vous par rapport à l'exercice 1 ?

5. Ajoutez le repository original comme remote "upstream" :
```bash
git remote add upstream [URL_DU_REPO_ORIGINAL]
git remote -v
```

6. Créez une branche pour votre contribution :
```bash
git checkout -b ma-contribution
```

7. Modifiez le fichier `exercice2.txt` en ajoutant votre nom et une phrase
8. Commitez et poussez :
```bash
git add exercice2.txt
git commit -m "Ma contribution au projet"
git push origin ma-contribution
```

**Question 2.2** : Que se passe-t-il cette fois ? Pourquoi ?

---

## 🔄 Partie 3 : Créer une Pull Request

1. Allez sur votre fork sur GitHub
2. Vous devriez voir un bouton **"Compare & pull request"**
3. Cliquez dessus et créez une Pull Request vers le repository original
4. Ajoutez une description claire de votre contribution

**Question 3.1** : Quelle est l'utilité d'une Pull Request ?

---

## 🔄 Partie 4 : Synchroniser votre fork

Avec le temps, le repository original évolue. Vous devez synchroniser votre fork :

```bash
# Récupérer les dernières modifications de l'original
git fetch upstream

# Se placer sur votre branche main
git checkout main

# Fusionner les modifications
git merge upstream/main

# Pousser sur votre fork
git push origin main
```

**Exercice 4** : Exécutez ces commandes et notez ce qui se passe.

---

## 📊 Tableau récapitulatif

Complétez ce tableau dans votre fichier `reponses.md` :

| Critère | Clone | Fork |
|---------|-------|------|
| Crée une copie sur GitHub ? | ? | ? |
| Crée une copie locale ? | ? | ? |
| Permet de pousser des modifications ? | ? | ? |
| Visible sur votre profil GitHub ? | ? | ? |
| Utilisé pour contribuer à l'open source ? | ? | ? |
| Garde un lien avec le repo original ? | ? | ? |

---

## 🤔 Questions de réflexion

Répondez à ces questions dans `reponses.md` :

1. Dans quel cas utiliseriez-vous un simple clone ?
2. Dans quel cas est-il nécessaire de faire un fork ?
3. Peut-on avoir plusieurs remotes sur un repository local ? À quoi cela sert-il ?
4. Que se passe-t-il si le repository original supprime votre Pull Request ?

---

## 📤 Rendu du TP

Pour rendre ce TP :

1. Complétez tous les exercices
2. Remplissez le fichier `reponses.md`
3. Créez une Pull Request depuis votre fork vers le repository original
4. Dans la Pull Request, mentionnez : "Rendu TP - [VOTRE NOM]"

---

## 🆘 Aide

Si vous rencontrez des problèmes :
- Consultez la documentation Git : https://git-scm.com/doc
- Documentation GitHub : https://docs.github.com
- Demandez de l'aide à votre enseignant

---

## 📝 Licence

Ce TP est sous licence MIT - vous êtes libre de l'utiliser et de le modifier.
