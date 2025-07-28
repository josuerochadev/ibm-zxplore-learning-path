# 🧩 FILES1 – Data Sets and Members on z/OS

## 🎯 Objectif
Apprendre à manipuler différents types d’ensembles de données sur z/OS (partitionnés et séquentiels), ainsi que les opérations courantes : renommer, supprimer, copier, créer.

## 🛠️ Étapes réalisées
- 🔎 Ajustement du filtre : `Z74115, ZXP.PUBLIC`
- 📂 Accès en lecture à `ZXP.PUBLIC.JCL`
- 📜 Soumission du job `PDSBUILD` pour générer mes data sets
- 🧾 Visualisation des data sets `INPUT` et `SEQDS`
- ✏️ Renommage, suppression et création de membres dans `INPUT`
- 📥 Copie depuis `SURPRISE` vers `INPUT`
- 📄 Édition de `SEQDS` avec ajout d’un enregistrement personnalisé
- ✅ Validation finale via le job `CHKFILES` → **CC 0000**

## 🧠 Ce que j’ai appris
- La différence entre **data sets partitionnés (PDS)** et **séquentiels**
- Les actions courantes à effectuer depuis Zowe Explorer
- La logique d’organisation des fichiers sur z/OS
- L’utilisation de JCL prédéfini pour automatiser la génération de structures

## 💡 Remarques
- Certains membres ont des noms "codés" (couleurs)
- L’environnement VSCode permet une interaction très intuitive avec z/OS

## ✅ Statut
✔️ Challenge validé avec succès le 28/07/2025 (Code de retour 0000)