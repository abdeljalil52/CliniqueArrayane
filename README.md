# Clinique Arrayane

Application Windows de support administratif développée pour **Clinique Arrayane**.

**Version actuelle : V5.8.7 PRO**  
**Développeur : Abdeljalil Berrada**

---

## Présentation

**Clinique Arrayane** est une application desktop Windows conçue pour compléter le logiciel de gestion principal de la clinique avec des outils rapides et pratiques :

- calculs de prise en charge ;
- calcul CNOPS ;
- historique des calculs ;
- génération de lettres administratives en PDF ;
- accès aux feuilles de maladie CNOPS et CNSS ;
- impression ;
- contrôle distant via GitHub ;
- système de mises à jour ;
- personnalisation de l'interface ;
- outils d'administration et de diagnostic.

L'application est principalement destinée à un usage interne.

---

## Fonctionnalités principales

### Calcul Assurance

Permet de calculer rapidement :

- le montant accordé ;
- le montant restant à la charge du patient ;
- le taux de prise en charge.

### Calcul CNOPS

Calcul séparé pour :

- Hôpital du jour ;
- Pharmacie ;
- montant total ;
- montant accordé ;
- reste patient ;
- taux final.

Les taux CNOPS peuvent être configurés.

### Historique

L'application conserve localement l'historique des calculs avec notamment :

- recherche ;
- filtres ;
- favoris ;
- détails ;
- export CSV ;
- export PDF ;
- rapports ;
- statistiques.

---

## Documents CNOPS / CNSS

Une section **DOCUMENTS** permet d'accéder aux feuilles de maladie :

- Feuille de maladie CNOPS ;
- Feuille de maladie CNSS.

Les fichiers PDF sont récupérés depuis GitHub puis conservés dans un cache local.

Le simple clic sur **Feuille CNOPS** ou **Feuille CNSS** ouvre uniquement la page correspondante.

Le PDF n'est ouvert que lorsque l'utilisateur clique sur le bouton prévu à cet effet.

### Fichiers GitHub

```text
documents/
├── feuille_Maladie_CNOPS.pdf
└── feuille_Maladie_CNSS.pdf
```

---

## Lettres administratives

La section **LETTRES** permet de générer des courriers PDF A4 à partir de formulaires simples.

### Modèles disponibles

- Accord de prise en charge non reçu
- Relance PEC
- Demande de duplicata d'accord
- Rectification de médicament
- Rectification de quantité
- Rectification médicament + quantité
- Rectification des dates DU / AU
- Rectification du montant accordé
- Rectification Hôpital du jour
- Rectification de l'établissement
- Transmission de complément de dossier
- Prolongation / prorogation
- Annulation PEC
- Réexamen après refus
- Demande urgente
- Lettre personnalisée

### Informations demandées

Selon le modèle, l'application peut demander :

- date ;
- organisme ;
- numéro de prise en charge ;
- numéro d'immatriculation ;
- ancienne date ;
- nouvelle date ;
- médicament erroné ;
- médicament correct ;
- quantité erronée ;
- quantité correcte ;
- montant ;
- motif ;
- observation.

### Impression sur papier pré-imprimé

Depuis la **V5.8.7**, les lettres sont conçues pour être imprimées sur le papier officiel déjà utilisé par la clinique.

Le PDF généré n'ajoute donc pas :

- de logo ;
- d'en-tête Clinique Arrayane ;
- de footer logiciel ;
- de mention de version ;
- de mention « Clinique Arrayane » en signature ;
- de texte « Cachet et signature ».

Le document conserve uniquement le contenu utile du courrier avec suffisamment d'espace pour l'en-tête, le pied de page et le cachet physique.

---

## Contrôle distant GitHub

L'application peut charger une configuration distante depuis :

```text
remote_config.json
```

Cela permet notamment de gérer :

- maintenance globale ;
- verrouillage d'urgence ;
- messages globaux ;
- activation ou désactivation de fonctions ;
- paramètres CNOPS ;
- options par poste ;
- configuration des documents ;
- certains paramètres d'interface.

> **Important :** ne jamais placer de mot de passe, clé API, information médicale ou donnée patient dans un fichier JSON public sur GitHub.

---

## Branding

Le fichier :

```text
branding.json
```

peut être utilisé pour certaines options de personnalisation distante de l'application.

---

## Nouveautés

Les notes de version sont chargées depuis :

```text
releases.json
```

La page **Nouveautés** de l'application peut se synchroniser directement avec GitHub.

Versions actuellement documentées :

- V5.8.7
- V5.8.6
- V5.8.5
- V5.8.4
- V5.8.3
- V5.8.2
- V5.8.1
- V5.8
- V5.7
- V5.6
- V5.5

---

## Mise à jour automatique

Le fichier :

```text
version.json
```

indique à l'application la dernière version disponible.

Exemple :

```json
{
  "version": "5.8.7",
  "download": "https://github.com/abdeljalilberrada/CliniqueArrayane/releases/download/v5.8.7/CliniqueArrayane.exe",
  "notes": "Clinique Arrayane V5.8.7 PRO"
}
```

Le fichier exécutable de la release doit être nommé :

```text
CliniqueArrayane.exe
```

---

## Structure recommandée du dépôt

```text
CliniqueArrayane/
│
├── README.md
├── version.json
├── releases.json
├── remote_config.json
├── branding.json
│
└── documents/
    ├── feuille_Maladie_CNOPS.pdf
    └── feuille_Maladie_CNSS.pdf
```

---

## Données locales Windows

Les données de l'application sont principalement stockées dans :

```text
%LOCALAPPDATA%\CliniqueArrayane
```

Exemples :

```text
config.json
Historique_Calculs.csv
Dernier_Calcul.json
Journal_Erreurs.log
Update.log
remote_config_cache.json
branding_cache.json
releases_cache.json
Journal_Admin.jsonl
Diagnostic_CliniqueArrayane.txt
Documents\
Lettres\
Backups\
```

Les informations saisies pour générer les lettres restent localement sur le poste et ne sont pas envoyées vers GitHub.

---

## Environnement de développement

### Python

Projet développé avec Python et Tkinter.

Testé notamment avec **Python 3.14 sous Windows**.

### Dépendances

```bat
py -m pip install pillow reportlab pyinstaller
```

---

## Lancer le script

```bat
py CliniqueArrayane.py
```

---

## Compiler l'application Windows

```bat
py -m PyInstaller --clean --onefile --windowed --name CliniqueArrayane CliniqueArrayane.py
```

Le fichier final sera généré dans :

```text
dist\CliniqueArrayane.exe
```

---

## Releases GitHub

Pour publier une nouvelle version :

1. Mettre à jour la version dans le script.
2. Compiler `CliniqueArrayane.exe`.
3. Créer une nouvelle **GitHub Release**.
4. Utiliser un tag comme :

```text
v5.8.7
```

5. Ajouter :

```text
CliniqueArrayane.exe
```

6. Mettre à jour :

```text
version.json
releases.json
```

---

## Sécurité et confidentialité

Ce projet est destiné à un environnement clinique.

Quelques règles importantes :

- ne pas publier de données patients sur GitHub ;
- ne pas placer de mots de passe dans `remote_config.json` ;
- ne pas placer de clés privées ou tokens dans le dépôt ;
- conserver les informations sensibles uniquement sur les postes autorisés ;
- vérifier les documents avant impression ou transmission ;
- effectuer régulièrement des sauvegardes.

---

## Compatibilité

- Windows 10 / Windows 11
- Python 3.x pour le développement
- Version `.exe` autonome pour les postes utilisateurs

---

## Développeur

**Abdeljalil Berrada**

Projet : **Clinique Arrayane**

Repository :

```text
https://github.com/abdeljalilberrada/CliniqueArrayane
```

---

## Version actuelle

**Clinique Arrayane V5.8.7 PRO**  
Build : **30/08/2026**
