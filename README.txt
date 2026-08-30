CLINIQUE ARRAYANE V5.8.5 PRO - LETTRES ADMINISTRATIVES

Nouveau module LETTRES :
- Accord de prise en charge non reçu
- Relance PEC
- Duplicata d'accord
- Rectification médicament / quantité
- Rectification dates DU / AU
- Rectification montant
- Rectification Hôpital du jour
- Rectification établissement
- Transmission complément de dossier
- Prolongation / prorogation
- Annulation PEC

Fonctionnement :
1. Ouvrir LETTRES > Lettres administratives.
2. Choisir un modèle.
3. Saisir Date, organisme, N° PEC, N° immatriculation.
4. Compléter uniquement les champs spécifiques.
5. Cliquer GÉNÉRER & OUVRIR LE PDF ou GÉNÉRER & IMPRIMER.

Les PDF sont enregistrés localement dans :
%LOCALAPPDATA%\CliniqueArrayane\Lettres

Aucune donnée saisie dans les lettres n'est envoyée à GitHub.

Dépendances recommandées :
py -m pip install pillow reportlab pyinstaller

Compilation :
py -m PyInstaller --clean --onefile --windowed --name CliniqueArrayane CliniqueArrayane_V5.8.5_PRO_LETTRES_FULL.py

GitHub :
- Remplacer releases.json par celui fourni pour afficher la V5.8.5 dans Nouveautés.
- Remplacer version.json par celui fourni uniquement au moment de publier la release v5.8.5.
- Aucun changement de remote_config.json n'est nécessaire pour ce module.
