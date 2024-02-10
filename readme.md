# Rapport sur le Projet FlopSecurity - Injections XSS et SQL [BTS SIO Grp2]


Salut à tous ! Je suis ravi de partager avec vous mon retour d'expérience suite au TP Flopsecurity portant sur les injections XSS/SQL dans les applications web.

Créateur TP : <a href="https://github.com/fabrice1618">fabrice1618</a> | Projet : <a href="https://github.com/fabrice1618/flopsecurity">FlopSecurity</a>

🔍 Explorez | 🧠 Apprenez | 🤝 Connectez-vous !

Projet : Centre de Formation Saint-Etienne (CFAI)

## Introduction 🚀

> Le TP nous montre comment une application web peut avoir des failles de sécurité, mettant en lumière les injections SQL (SQLI) et les attaques Cross-Site Scripting (XSS).

### Contexte du TP 🌐

La sensibilisation aux risques de sécurité dans le développement d'applications web est cruciale, surtout dans un monde où les cybermenaces sont omniprésentes.

### Objectifs du TP 🎯

L'objectif est de comprendre des vulnérabilités telles que les injections SQL et XSS, et d'apprendre à sécuriser de manière efficace une application web.

## Installation du serveur LAMP 💻

### Étapes pour installer et configurer le serveur LAMP (Linux, Apache, MySQL, PHP) 🛠️:

1. **Linux (L):**
   - **Exemple:** Choisissez Ubuntu comme distribution Linux.
   - **Installation:** Exécutez la commande `sudo apt-get install ubuntu`.

2. **Apache (A):**
   - **Exemple:** Installez Apache avec `sudo apt-get install apache2`.

3. **MySQL (M):**
   - **Exemple:** Installez MySQL avec `sudo apt-get install mysql-server`.
   - **Configuration:** Définissez le mot de passe root en suivant les étapes du document FlopSecurity.

4. **PHP (P):**
   - **Exemple:** Installez PHP avec `sudo apt-get install php libapache2-mod-php php-mysql`.
   - **Configurer Apache pour PHP:** Activez le module avec `sudo a2enmod php`.

### Différences entre la configuration d'un serveur de développement et un serveur de production 🛤️:

- **Serveur de Développement:**
  - Configuration moins stricte, favorisant la facilité de développement.
  - Affichage des erreurs activé pour un débogage efficace.
  - Utilisation d'extensions supplémentaires pour le développement (ex: `php-mbstring`).
   - **Exemple:** Activez l'affichage des erreurs pour faciliter le débogage (`php.ini`).
  - **Utilisation:** Installez des extensions comme `php-mbstring` pour le développement.

- **Serveur de Production:**
  - Configuration plus sécurisée, minimisant les risques.
  - Affichage des erreurs désactivé ou logué de manière sécurisée.
  - Paramètres spécifiques pour la performance et la stabilité.
  - **Exemple:** Désactivez l'affichage des erreurs et configurez le logging sécurisé.
  - **Paramètres:** Optimisez pour la sécurité, la performance et la stabilité.

### Choix du Serveur 🚦:

- **Développement:** Configuration facilitant le débogage et la flexibilité.

- **Production:** Configuration sécurisée pour garantir la sécurité, la performance optimale et la stabilité face à un trafic réel.

## SQL Injection (SQLI) 🚫:
### Description:
L'injection SQL consiste à insérer des requêtes malveillantes dans les bases de données.

### Risques encourus:
Entrée d'un utilisateur malveillante pouvant contourner l'authentification.

### Solution technique:
Utilisation de requêtes préparées pour éviter l'injection de code SQL.

## Cross-Site Scripting (XSS) ⚠️:
### Description:
XSS injecte des scripts malveillants dans des pages web consultées par d'autres utilisateurs.

### Risques encourus:
**Exemple:** Injection de script dans un champ de commentaire volant des sessions utilisateur.

### Solution technique:
Validation et échappement des données en sortie, utilisation de Content Security Policies (CSP).

## Sécurisation de l'application et du système 🛡️:
- **Exemple:** Mise en place d'un pare-feu pour filtrer le trafic indésirable.
- **Exemple:** Gestion stricte des permissions pour limiter l'accès.
- **Exemple:** Mise à jour régulière des composants pour corriger les vulnérabilités.
- **Exemple:** Intégrer des bibliothèques de requêtes préparées dans le code pour filtrer et valider les entrées utilisateur. Utiliser des frameworks (*Ruby on Rails*) qui intègrent des mécanismes automatiques d'échappement des données pour prévenir les attaques XSS.

## Mon avis sur le TP 🤔

Durant cette séance pratique, on s'est plongé dans l'univers complexe du développement d'applications web. J'ai abordé la gestion de bases de données, mettant en lumière des concepts comme les injections SQL et XSS. Expérimenter ces vulnérabilités m'a permis de comprendre leur impact, de réfléchir à leurs causes, et de proposer des solutions pour renforcer la sécurité de l'application web. 👨‍💻



## L'importance de la sécurité ! 🤝

Ce qui m'a particulièrement frappé, c'est le poids de la sécurité. On ne parle pas seulement de créer des fonctionnalités qui marchent, mais de garantir que nos réalisations sont résistantes face aux attaques. La protection des données et la configuration système, c'est un enjeu majeur. Les failles de sécurité sont un peu comme des menaces invisibles qu'il faut détecter avant qu'elles ne deviennent problématiques.

## Mon avis pour l'avenir de la sécurité des apps 🚨

Honnêtement, en regardant vers l'avenir, je suis convaincu qu'il est essentiel de rester vigilant. Les menaces évoluent constamment, et il faut être prêt à y faire face. Les mises à jour ne concernent pas seulement l'ajout de nouvelles fonctionnalités, mais aussi la fermeture des failles de sécurité. Et n'oublions pas les tests de sécurité, un peu comme des gardiens invisibles qui scrutent en permanence pour s'assurer que tout est en ordre. C'est comme un bouclier protecteur pour nos applications, et franchement, c'est super, il faut vraiment en apprendre d'avantage. 🛡️📲

<br>

Créé avec ❤️ par Dimitri Chassignol - 2024
