# JCL1 – Making Things Happen

## 🎯 Objectif du challenge

Découvrir les bases du JCL sur z/OS en :
- allouant et utilisant des data sets personnels,
- copiant et adaptant des jobs existants,
- exécutant un programme COBOL compilé,
- manipulant des utilitaires système (`IEBGENER`, `IEFBR14`),
- générant une sortie séquentielle structurée dans un membre `JCL3OUT`.

## 🛠️ Étapes réalisées

- ✅ Copie de JCL2 et JCL3 depuis `ZXP.PUBLIC.JCL` vers `&SYSUID..JCL`.
- ✅ Correction du job `JCL1` pour inclure `SYSIN DD DUMMY`.
- ✅ Analyse du code COBOL `CBL0001` pour lier les bons `DDNAME` (`FNAMES`, `LNAMES`, `COMBINED`).
- ✅ Modification de `JCL2` pour faire correspondre les noms logiques COBOL et les noms DD JCL.
- ✅ Compilation et exécution sans ABEND (`CC=0000`).
- ✅ Construction d’un fichier `JCL3OUT` via plusieurs étapes `IEBGENER`, avec gestion des en-têtes et des données `in-stream`.
- ✅ Ajout d’une étape `IEFBR14` pour suppression automatique du dataset avant nouvelle soumission.
- ✅ Vérification du contenu : 23 lignes dans `JCL3OUT`, sans doublons, avec les 10 gares + informations de début et de fin.

## 🧠 Ce que j’ai appris

- La structure syntaxique d’un job JCL multi-étapes.
- La liaison explicite entre un `SELECT` COBOL et un `DD` JCL via le `DDNAME`.
- Le rôle des paramètres `DISP`, `CATLG`, `PASS`, `DELETE`.
- L’utilisation des programmes utilitaires `IEBGENER` et `IEFBR14`.
- Les pratiques pour éviter les erreurs `JCL ERROR`, `ABEND`, et `DUPLICATE DATASET`.

## ✅ Statut

✔ Challenge terminé avec succès. Fichier `JCL3OUT` correct généré et visible dans mon data set personnel.