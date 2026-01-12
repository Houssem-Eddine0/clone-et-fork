# Instructions pour l'enseignant

## 🎓 Configuration du TP

### Étape 1 : Créer le repository sur GitHub Classroom

1. Allez sur [GitHub Classroom](https://classroom.github.com/)
2. Sélectionnez votre organisation
3. Créez un nouveau "Assignment"
4. Configurez :
   - **Nom** : "TP Clone vs Fork"
   - **Type** : Individual assignment
   - **Visibility** : Private (recommandé pour un contexte pédagogique)
   - **Template repository** : utilisez le repository que vous créez avec ces fichiers

### Étape 2 : Peupler le repository

1. Créez un nouveau repository dans votre organisation GitHub Classroom
2. Clonez-le localement
3. Ajoutez tous les fichiers fournis :
   - `README.md`
   - `reponses.md`
   - `exercice1.txt`
   - `exercice2.txt`
   - `INSTRUCTIONS_ENSEIGNANT.md`
   - `.gitignore`
4. Committez et poussez :
```bash
git add .
git commit -m "Initial commit - Setup du TP"
git push origin main
```

5. Dans les paramètres du repository, cochez "Template repository" si vous souhaitez le réutiliser

### Étape 3 : Distribuer aux étudiants

**Option A - Via GitHub Classroom (recommandé)**
- Partagez le lien d'invitation de l'assignment
- Chaque étudiant aura automatiquement son propre repository privé

**Option B - Manuellement**
- Partagez le lien du repository
- Les étudiants devront le forker pour travailler

---

## 📊 Critères d'évaluation suggérés

| Critère | Points | Description |
|---------|--------|-------------|
| Complétion exercice 1 | 2 | Clone réussi et tentative de push documentée |
| Complétion exercice 2 | 3 | Fork réalisé et modifications poussées |
| Pull Request créée | 3 | PR bien documentée et formatée |
| Réponses aux questions | 6 | Qualité et pertinence des réponses |
| Tableau récapitulatif | 3 | Tableau correctement rempli |
| Questions de réflexion | 3 | Réflexion personnelle pertinente |
| **TOTAL** | **20** | |

---

## ✅ Correction type

### Question 1.1 : Remote après clone
**Réponse attendue :**
```
origin  https://github.com/[ORGANISATION]/[REPO].git (fetch)
origin  https://github.com/[ORGANISATION]/[REPO].git (push)
```
Un seul remote nommé "origin" pointant vers le repository original.

### Question 1.2 : Échec du push
**Réponse attendue :**
L'étudiant doit obtenir une erreur de type "permission denied" ou "403 forbidden" car il n'a pas les droits d'écriture sur le repository original.

### Question 2.1 : Remote après fork
**Réponse attendue :**
```
origin    https://github.com/[USERNAME]/[REPO].git (fetch)
origin    https://github.com/[USERNAME]/[REPO].git (push)
upstream  https://github.com/[ORGANISATION]/[REPO].git (fetch)
upstream  https://github.com/[ORGANISATION]/[REPO].git (push)
```
Deux remotes : "origin" (son fork) et "upstream" (repository original).

### Question 2.2 : Succès du push
**Réponse attendue :**
Le push réussit car l'étudiant pousse sur son propre fork où il a tous les droits.

### Question 3.1 : Utilité de la Pull Request
**Réponse attendue :**
- Proposer des modifications au projet original
- Permettre une revue de code
- Discuter des changements avant intégration
- Tracer l'historique des contributions

### Tableau récapitulatif

| Critère | Clone | Fork |
|---------|-------|------|
| Crée une copie sur GitHub ? | ❌ Non | ✅ Oui |
| Crée une copie locale ? | ✅ Oui | ✅ Oui (après clone du fork) |
| Permet de pousser des modifications ? | ❌ Non (sauf droits) | ✅ Oui (sur le fork) |
| Visible sur votre profil GitHub ? | ❌ Non | ✅ Oui |
| Utilisé pour contribuer à l'open source ? | ❌ Rarement | ✅ Oui |
| Garde un lien avec le repo original ? | ✅ Oui (remote) | ✅ Oui (upstream) |

### Questions de réflexion

**1. Quand utiliser un clone ?**
- Projets personnels ou d'équipe où on a les droits
- Consultation rapide du code
- Travail local sans besoin de contribuer

**2. Quand utiliser un fork ?**
- Contribuer à un projet open source
- Expérimenter sans risque sur un projet
- Créer sa propre version d'un projet

**3. Plusieurs remotes ?**
Oui, on peut avoir plusieurs remotes. Utile pour :
- Synchroniser avec l'original (upstream)
- Pousser sur son fork (origin)
- Collaborer avec d'autres forks

**4. Si la PR est supprimée ?**
- Les commits restent sur le fork
- Le travail n'est pas perdu
- On peut recréer une nouvelle PR si nécessaire

---

## 🔧 Dépannage courant

### Problème : Étudiant ne peut pas pousser sur le fork
**Solution :** Vérifier qu'il a bien cloné SON fork, pas le repository original.

### Problème : Conflit lors de la synchronisation
**Solution :** Montrer comment résoudre les conflits avec `git mergetool` ou manuellement.

### Problème : Pull Request vers la mauvaise branche
**Solution :** On peut modifier la branche cible d'une PR sur GitHub.

---

## 📈 Variantes et extensions

### Pour aller plus loin
1. **Gestion des conflits** : Créer intentionnellement des conflits pour les résoudre
2. **Rebasing** : Introduire `git rebase` pour maintenir un historique propre
3. **Code review** : Faire reviewer les PR entre étudiants
4. **CI/CD** : Ajouter des GitHub Actions pour tester automatiquement les PR

### Simplification pour débutants
- Fournir les commandes complètes à copier-coller
- Faire une démonstration en direct avant le TP
- Créer des groupes de 2 pour l'entraide

---

## 📞 Support

Pour toute question sur ce TP :
- Documentation Git : https://git-scm.com/doc
- GitHub Guides : https://guides.github.com
- GitHub Classroom : https://classroom.github.com/help

Bon cours ! 🎉
