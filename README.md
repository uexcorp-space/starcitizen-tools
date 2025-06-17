# starcitizen-tools".

Introduction : Brève description du projet (StarCitizen.tools MediaWiki) et note sur l'archivage du dépôt original.
Prérequis :
XAMPP (ou équivalent comme WAMP, MAMP) installé et fonctionnel.
Git installé (https://git-scm.com/downloads).
Composer installé (https://getcomposer.org/download/).
Étapes d'installation :
Cloner le dépôt original :
git clone https://github.com/StarCitizenTools/starcitizen-tools.git nom_du_dossier_local
Installer les dépendances PHP :
cd nom_du_dossier_local
composer install --no-dev --optimize-autoloader
Préparer la base de données (via phpMyAdmin dans XAMPP) :
Ouvrir phpMyAdmin (généralement http://localhost/phpmyadmin).
Créer une nouvelle base de données (ex: starcitizen_tools_wiki). Choisir un interclassement comme utf8mb4_unicode_ci.
Créer un nouvel utilisateur de base de données (ex: sct_user avec mot de passe votre_mot_de_passe_securise).
Donner tous les privilèges à cet utilisateur sur la base de données starcitizen_tools_wiki.
Copier les fichiers dans htdocs :
Copier le contenu de nom_du_dossier_local (qui inclut maintenant le dossier vendor/) dans un nouveau dossier sous htdocs de XAMPP (ex: C:\xampp\htdocs\sct_wiki).
Lancer l'assistant d'installation MediaWiki :
Ouvrir votre navigateur et aller à http://localhost/sct_wiki/ (ou le nom de dossier que vous avez choisi).
Suivre les instructions de l'assistant MediaWiki.
Quand il demande les informations de la base de données :
Hôte de la base de données : localhost
Nom de la base de données : (celui que vous avez créé, ex: starcitizen_tools_wiki)
Utilisateur de la base de données : (celui que vous avez créé, ex: sct_user)
Mot de passe de la base de données : (celui que vous avez défini)
Compléter toutes les étapes de l'assistant. Il générera un fichier LocalSettings.php à la racine de votre dossier sct_wiki. Téléchargez-le si l'assistant vous le propose et placez-le dans ce dossier.
Accéder à votre wiki :
Une fois LocalSettings.php en place, vous devriez pouvoir accéder à votre wiki à l'adresse http://localhost/sct_wiki/.
