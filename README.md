# Clinique Arrayane

Application Windows interne de gestion, d'assistance administrative et d'outils de travail pour **Clinique Arrayane**.

**Développeur : Abdeljalil Berrada**  
**Plateforme : Windows 10 / Windows 11**  
**Type : application desktop interne**

---

## À propos

Clinique Arrayane est une application conçue pour simplifier les tâches administratives répétitives, centraliser les outils utiles et améliorer le confort de travail sur les postes de la clinique.

L'application complète les logiciels métier déjà utilisés dans la clinique. Elle n'a pas pour objectif de remplacer un dossier patient ou un système hospitalier principal.

Ce fichier `README.md` est volontairement **indépendant des numéros de version**. Il décrit le projet de manière permanente et n'a pas besoin d'être modifié à chaque mise à jour. Les informations de version et les changements sont gérés séparément dans `version.json` et `releases.json`.

---

## Fonctions principales

### Tableau de bord

- Vue rapide de l'activité récente
- Nombre de calculs
- Totaux facturés, accordés et patient
- Résumé du mois
- Dernier calcul
- Accès rapide aux fonctions principales
- État du poste et de l'application

### Calculs Assurances

- Saisie du montant total
- Saisie du montant accordé
- Calcul automatique du reste patient
- Calcul automatique du taux de prise en charge
- Copie rapide du taux
- Enregistrement dans l'historique
- Impression du résultat

### Calculs CNOPS

- Montant Hôpital du jour
- Montant Pharmacie
- Taux configurables
- Calcul automatique du montant accordé
- Calcul du reste patient
- Calcul du taux global
- Historique et impression

### Historique

- Consultation des calculs enregistrés
- Recherche instantanée
- Filtres par date, type, total et taux
- Favoris
- Détails d'un calcul
- Modification selon les droits
- Suppression protégée
- Export CSV
- Export PDF
- Rapport mensuel
- Sauvegardes avant opérations sensibles

### Documents

Accès rapide aux documents administratifs utiles, notamment :

- Feuille de maladie CNOPS
- Feuille de maladie CNSS
- Ouverture manuelle
- Impression directe
- Copie locale de secours
- Fonctionnement avec cache local si Internet est indisponible

### Lettres administratives

Centre de génération de lettres avec plusieurs modèles, notamment :

- Accord non reçu
- Relance de prise en charge
- Duplicata d'accord
- Rectification médicament
- Rectification quantité
- Médicament et quantité
- Rectification de dates
- Rectification de montant
- Hôpital du jour
- Rectification d'établissement
- Complément de dossier
- Prorogation
- Annulation de prise en charge
- Réexamen après refus
- Demande urgente
- Lettre personnalisée

Les lettres sont prévues pour être imprimées sur le papier pré-imprimé de la clinique. Le PDF généré reste volontairement sobre et ne rajoute pas de logo, d'en-tête, de pied de page logiciel ou de zone de cachet inutile.

### Optimisation PC

Une section dédiée permet d'accéder à **Enterprise PC Optimizer Pro**, un outil Windows de diagnostic, maintenance et optimisation des postes de travail.

Fonctions disponibles selon l'outil installé :

- Diagnostic du PC
- Analyse CPU, RAM et stockage
- Analyse d'utilisation disque élevée
- Nettoyage de fichiers temporaires et caches
- Vérifications de santé Windows
- Maintenance SSD / HDD
- Maintenance Windows Update
- DISM et SFC
- Maintenance Microsoft Defender
- Maintenance réseau
- Points de restauration
- Rapports techniques
- Sauvegarde et restauration

Certaines opérations système peuvent demander des droits Administrateur Windows.

### Contact et assistance

- Accès rapide au support
- Message prérempli
- Informations techniques utiles
- Aide rapide intégrée
- FAQ et procédures de dépannage

### Nouveautés

La page Nouveautés affiche l'historique des versions et les changements publiés dans `releases.json`.

### Mise à jour

L'application peut :

- Vérifier la disponibilité d'une nouvelle version
- Télécharger une nouvelle version officielle
- Proposer l'installation sans demander le mot de passe Administration de l'application
- Redémarrer après installation
- Utiliser un emplacement utilisateur si le dossier courant est protégé par Windows
- Conserver un journal de mise à jour pour le diagnostic

La source technique du téléchargement n'est pas affichée dans l'interface utilisateur.

---

## Interface

L'interface est conçue pour être claire sur les postes administratifs :

- Thème sombre ou clair
- Couleur principale configurable
- Menu latéral professionnel
- Menu latéral avec défilement
- Logo personnalisable
- Mode compact
- Taille de texte configurable
- Plein écran
- Indicateur de page active
- Raccourcis clavier
- Notifications discrètes

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

Les raccourcis numériques sont prévus pour les claviers AZERTY et QWERTY.

---

## Administration

L'espace Administration permet de gérer les paramètres avancés de l'application :

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
- Configuration distante
- Diagnostic
- Mises à jour

L'accès Administration est protégé par mot de passe et peut se reverrouiller automatiquement après une période d'inactivité.

---

## Sécurité et confidentialité

- Les calculs et données locales restent sur le poste sauf fonction explicitement distante.
- Aucun mot de passe ou secret ne doit être stocké dans des fichiers publics.
- Les données médicales sensibles et dossiers patients complets doivent rester dans les systèmes métier autorisés de la clinique.
- Les identifiants techniques distants ne sont pas affichés aux utilisateurs standards.
- Les opérations sensibles sont protégées par les droits Responsable / Administrateur lorsque nécessaire.
- Les mises à jour de l'application restent accessibles sans communiquer le mot de passe Administrateur de Clinique Arrayane aux utilisateurs.

---

## Fonctionnement hors connexion

La majorité des fonctions principales restent disponibles sans Internet :

- Calculs
- Historique
- Documents déjà mis en cache
- Lettres
- Impression locale
- Paramètres
- Outils locaux déjà téléchargés

Les fonctions nécessitant un téléchargement, une synchronisation distante ou une mise à jour attendent simplement le retour de la connexion.

---

## Données locales

Les fichiers locaux de l'application sont enregistrés principalement dans :

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
Journal_Admin.jsonl
Diagnostic_CliniqueArrayane.txt
Backups\
Documents\
Lettres\
Tools\
assets\
```

---

## Configuration distante

L'application peut utiliser des fichiers de configuration distants afin de gérer certains paramètres sans modifier l'exécutable :

- Maintenance globale
- Verrouillage d'urgence
- Messages d'information
- Activation ou désactivation de fonctions
- Paramètres de support
- Taux et limites
- Règles spécifiques à un poste
- Branding
- Version minimale prise en charge

En cas d'indisponibilité du service distant, l'application privilégie le fonctionnement local et le cache disponible.

---

## Fichiers de publication

### `README.md`

Description permanente du projet.  
**Ne pas modifier ce fichier à chaque mise à jour.**

### `version.json`

Contient les informations nécessaires à la détection de la version actuellement publiée.

Il est mis à jour lorsqu'une nouvelle version est publiée.

### `releases.json`

Contient l'historique visible dans la page **Nouveautés**.

Il est mis à jour lorsqu'une nouvelle version doit apparaître dans l'historique.

### `remote_config.json`

Contient uniquement les réglages distants opérationnels. Il n'est modifié que lorsqu'un comportement distant doit changer.

### `branding.json`

Peut être utilisé pour certains réglages d'identité et d'apparence à distance.

---

## Installation

L'application est distribuée sous forme d'un exécutable Windows :

```text
CliniqueArrayane.exe
```

Aucune installation Python n'est nécessaire pour l'utilisateur final.

Lors d'une première installation manuelle, il suffit de placer l'exécutable dans un emplacement adapté puis de le lancer.

---

## Compilation développeur

Dépendances principales :

```bat
py -m pip install pillow reportlab pyinstaller
```

Compilation :

```bat
py -m PyInstaller --clean --onefile --windowed --icon=icon.ico --add-data "icon.ico;." --name CliniqueArrayane a.py
```

L'exécutable est généré dans :

```text
dist\CliniqueArrayane.exe
```

---

## Compatibilité

- Windows 10 64-bit
- Windows 11 64-bit

Certaines fonctions de maintenance système peuvent demander les droits Administrateur Windows.

---

## Organisation du projet

```text
CliniqueArrayane/
├── README.md
├── version.json
├── releases.json
├── remote_config.json
├── branding.json
├── documents/
│   ├── feuille_Maladie_CNOPS.pdf
│   └── feuille_Maladie_CNSS.pdf
└── Releases
    └── CliniqueArrayane.exe
```

---

## Règle de publication

Pour une nouvelle version :

1. Compiler `CliniqueArrayane.exe`.
2. Publier la nouvelle version avec le bon numéro de version.
3. Mettre à jour `version.json`.
4. Ajouter la nouvelle entrée dans `releases.json` si elle doit apparaître dans Nouveautés.
5. Modifier `remote_config.json` uniquement si un comportement distant doit changer.

**Le README reste inchangé.**

---

## Développeur

**Abdeljalil Berrada**

Clinique Arrayane — Outils administratifs et assistance interne Windows.
