# Clinique Arrayane

Application Windows interne conçue pour simplifier le travail administratif, centraliser les outils utiles et assister les postes de travail de **Clinique Arrayane**.

**Développeur : Abdeljalil Berrada**  
**Plateforme : Windows 10 / Windows 11**  
**Type : application desktop interne**

---

## À propos

Clinique Arrayane regroupe dans une seule interface les fonctions administratives et techniques utilisées au quotidien dans la clinique.

L'application complète les logiciels métier déjà présents. Elle n'a pas pour objectif de remplacer le système principal de gestion des patients ou les logiciels hospitaliers existants.

Ce `README.md` est volontairement **permanent et indépendant des numéros de version**. Il n'a pas besoin d'être modifié après chaque mise à jour. Les informations de version sont gérées séparément dans `version.json` et `releases.json`.

---

## Fonctions principales

### Tableau de bord

- Vue rapide de l'activité
- Calculs du jour
- Totaux facturés, accordés et patient
- Résumé mensuel
- Dernier calcul
- Actions rapides
- État du poste et de l'application

### Assurances

- Montant total
- Montant accordé
- Reste patient automatique
- Taux de prise en charge automatique
- Copie rapide du taux
- Historique automatique
- Impression du résultat

### CNOPS

- Montant Hôpital du jour
- Montant Pharmacie
- Taux configurables
- Calcul automatique du montant accordé
- Calcul du reste patient
- Calcul du taux global
- Historique et impression

### Historique

- Recherche instantanée
- Filtres par période, type, montant et taux
- Favoris
- Détails d'un calcul
- Modification selon les droits
- Suppression protégée
- Export CSV
- Export PDF
- Rapport mensuel
- Sauvegardes locales

### Documents

- Feuille de maladie CNOPS
- Feuille de maladie CNSS
- Ouverture manuelle
- Impression directe
- Cache local hors connexion
- Mise à jour distante des documents

### Lettres administratives

Le centre de lettres comprend notamment :

- Accord non reçu
- Relance PEC
- Duplicata d'accord
- Rectification médicament
- Rectification quantité
- Médicament + quantité
- Rectification des dates DU/AU
- Rectification du montant
- Hôpital du jour
- Rectification établissement
- Complément de dossier
- Prorogation
- Annulation PEC
- Réexamen après refus
- Demande urgente
- Lettre personnalisée

Les PDF sont adaptés au papier pré-imprimé de la clinique : pas de logo logiciel, pas d'en-tête ajouté, pas de footer logiciel et pas de zone de cachet imprimée.

### Optimisation PC

Une section dédiée donne accès à l'outil **Enterprise PC Optimizer Pro** pour le diagnostic, l'entretien et l'optimisation des postes Windows.

Fonctions possibles selon la version de l'outil :

- Diagnostic du PC
- Analyse CPU, RAM et stockage
- Analyse d'utilisation disque élevée
- Nettoyage des fichiers temporaires et caches
- Vérifications de santé Windows
- Maintenance SSD / HDD
- Maintenance Windows Update
- DISM et SFC
- Maintenance Microsoft Defender
- Maintenance réseau
- Points de restauration
- Rapports techniques
- Sauvegarde et restauration

Certaines opérations système peuvent demander les droits Administrateur Windows.

### Assistance

- Aide rapide intégrée
- Contact / Support
- Informations techniques utiles
- Procédures de dépannage

### Nouveautés

La page **Nouveautés** affiche les changements publiés dans `releases.json`.

### Mise à jour

L'application peut :

- Vérifier une nouvelle version
- Télécharger la version officielle
- Proposer l'installation sans mot de passe Administration de l'application
- Redémarrer automatiquement après installation
- Utiliser un emplacement utilisateur si le dossier courant est protégé
- Conserver un journal de mise à jour pour le diagnostic

La source technique des téléchargements n'est pas affichée dans l'interface utilisateur.

---

## Interface

- Design sombre professionnel
- Thème clair disponible
- Couleur principale configurable
- Menu latéral scrollable
- Logo personnalisable
- Logo sidebar optimisé à 80 px
- Sélection active clairement visible
- Mode compact
- Taille de texte configurable
- Plein écran
- Notifications discrètes
- Compatible clavier AZERTY et QWERTY

---

## Raccourcis clavier

| Raccourci | Action |
|---|---|
| `Ctrl+1` | Accueil |
| `Ctrl+2` | Assurances |
| `Ctrl+3` | CNOPS |
| `Ctrl+4` | Historique |
| `Ctrl+5` | Contact / Support |
| `Ctrl+6` | Aide rapide |
| `Ctrl+7` | Administration |
| `Ctrl+8` | Feuille CNOPS |
| `Ctrl+9` | Feuille CNSS |
| `Ctrl+0` | Lettres administratives |
| `Ctrl+O` | Optimisation PC |
| `Ctrl+U` | Mise à jour |
| `Ctrl+Shift+R` | Nouveautés |
| `Ctrl+N` | Nouveau calcul |
| `Ctrl+P` | Imprimer |
| `F5` | Actualiser |
| `F11` | Plein écran |
| `Échap` | Quitter le plein écran |

---

## Administration

L'espace Administration permet de gérer :

- Identité et branding
- Logo
- Apparence
- Taux CNOPS
- Fonctions du menu
- Historique
- Impression
- Support
- Sécurité
- Maintenance
- Sauvegardes
- Synchronisation distante
- Diagnostic
- Mises à jour

L'accès Administration est protégé par mot de passe et peut se reverrouiller automatiquement après une période d'inactivité.

---

## Sécurité et confidentialité

- Les calculs restent locaux sauf fonction explicitement distante.
- Les lettres et documents générés restent sur le poste.
- Les mots de passe ne doivent jamais être placés dans les fichiers publics de configuration.
- Les fichiers distants ne doivent contenir aucune donnée patient.
- L'application continue à fonctionner localement lorsqu'Internet est indisponible pour les fonctions qui ne nécessitent pas de connexion.
- Les opérations sensibles sont protégées par les rôles et confirmations prévus dans l'application.

---

## Données locales

Les données de l'application sont principalement enregistrées dans :

```text
%LOCALAPPDATA%\CliniqueArrayane
```

Ce dossier peut contenir notamment :

```text
config.json
Historique_Calculs.csv
Dernier_Calcul.json
Journal_Erreurs.log
Update.log
Backups\
Documents\
Lettres\
Tools\
assets\
```

---

## Configuration distante

L'application peut utiliser plusieurs fichiers de configuration distants :

- `version.json` : version publiée et téléchargement
- `releases.json` : historique des nouveautés
- `remote_config.json` : règles opérationnelles distantes
- `branding.json` : identité et apparence

Le système distant peut notamment gérer :

- Maintenance globale
- Verrouillage d'urgence
- Messages d'information
- Activation ou désactivation de fonctions
- Paramètres de support
- Taux et limites
- Règles spécifiques à un poste
- Branding
- Version minimale prise en charge

En cas d'indisponibilité du service distant, l'application privilégie le fonctionnement local et les caches disponibles.

---

## Fichiers du projet

### `README.md`

Description permanente du projet.  
**Ne pas modifier ce fichier à chaque mise à jour.**

### `version.json`

Contient la version actuellement publiée et l'adresse de téléchargement officielle.

### `releases.json`

Contient l'historique affiché dans la page **Nouveautés**.

### `remote_config.json`

Contient les réglages distants opérationnels.

### `branding.json`

Contient les réglages distants d'identité et d'apparence.

### `requirements.txt`

Contient les dépendances Python nécessaires au développement et à la compilation.

---

## Installation utilisateur

L'application est distribuée sous forme d'un exécutable Windows :

```text
CliniqueArrayane.exe
```

L'utilisateur final n'a pas besoin d'installer Python, Pillow ou ReportLab lorsque l'exécutable a été correctement compilé.

---

## Compilation développeur

Installation des dépendances :

```bat
py -m pip install -r requirements.txt
```

Compilation recommandée :

```bat
py -m PyInstaller --clean --onefile --windowed --icon=icon.ico --add-data "icon.ico;." --collect-all reportlab --name CliniqueArrayane a.py
```

L'exécutable final est généré dans :

```text
dist\CliniqueArrayane.exe
```

---

## Compatibilité

- Windows 10 64-bit
- Windows 11 64-bit

Certaines fonctions de maintenance système peuvent demander les droits Administrateur Windows.

---

## Organisation recommandée

```text
CliniqueArrayane/
├── README.md
├── branding.json
├── releases.json
├── remote_config.json
├── requirements.txt
├── version.json
├── documents/
│   ├── feuille_Maladie_CNOPS.pdf
│   └── feuille_Maladie_CNSS.pdf
└── Releases
    └── CliniqueArrayane.exe
```

---

## Règle de publication

Le `README.md` reste inchangé.

Pour une nouvelle version, seuls les fichiers nécessaires à la publication ou au comportement distant doivent être modifiés, principalement `version.json`, `releases.json` et éventuellement `remote_config.json` / `branding.json`.

---

## Développeur

**Abdeljalil Berrada**

Clinique Arrayane — Outils administratifs et assistance interne Windows.
