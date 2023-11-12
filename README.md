# Linux-SSH-SSL plan project

## I. Introduction au Réseau*

   A. Définition du réseau informatique
      1. Interconnexion de systèmes et de dispositifs
      2. Partage de ressources et d'informations

   B. Modèles de référence
      1. OSI (Open Systems Interconnection)
         - Expliquer les sept couches du modèle OSI
      2. TCP/IP (Transmission Control Protocol/Internet Protocol)
         - Présenter les quatre couches principales du modèle TCP/IP
         
## II. Positionnement de SSH dans les Modèles de Référence*

   A. Modèle OSI
      1. Identifier la couche correspondante pour SSH dans le modèle OSI
      2. Brève explication du rôle de cette couche

   B. Modèle TCP/IP
      1. Localiser SSH dans les couches du modèle TCP/IP
      2. Mettre en avant le rôle de SSH dans le contexte du modèle TCP/IP

## III. Introduction à SSH (Secure Shell)*

   A. Définition de SSH
      1. Protocole de communication sécurisé
      2. Utilisé pour l'accès distant et la gestion de systèmes

   B. Fonctionnalités de sécurité de SSH
      1. Chiffrement des données
      2. Authentification forte

## IV. Simulation de Contrôle avec SSH*

   A. Scénario de simulation
      1. Explication du cas d'utilisation
      2. Mise en place d'une connexion SSH entre deux machines
      
   B. Démonstration en temps réel
      1. Utilisation d'outils de simulation pour le contrôle à distance
      2. Illustration du chiffrement des données par SSH

## V. Introduction à Wireshark*

   A. Présentation de Wireshark
      1. Outil d'analyse de paquets réseau
      2. Utilisation pour la capture et l'inspection du trafic réseau

## VI. Attaque Simulée avec Wireshark*

   A. Scénario d'attaque
      1. Explication du processus d'attaque simulée
      2. Mise en évidence des risques potentiels

   B. Capture de trafic avec Wireshark
      1. Démonstration en temps réel de la capture du trafic non chiffré
      2. Analyse des données capturées

## VII. Analyse des Résultats*

   A. Comparaison des données chiffrées et non chiffrées
      1. Mettre en évidence la différence de sécurité entre les deux scénarios
      2. Montrer que les données SSH sont sécurisées

## VIII. Conclusion*

   A. Récapitulation des points clés
   B. Confirmation de la sécurité de SSH grâce à l'analyse avec Wireshark
   C. Possibilités d'amélioration de la sécurité


-----------------------------------------------------------------------------------------------


# I. Introduction au Réseau**

## A. Définition du réseau informatique**

### 1. Interconnexion de systèmes et de dispositifs :**
   - Un réseau informatique est un ensemble de systèmes informatiques interconnectés, tels que des ordinateurs, des serveurs, des périphériques, et des dispositifs de communication.
   - Ces systèmes sont liés par des équipements réseau tels que des routeurs, des commutateurs, des concentrateurs, et des câbles, permettant la communication et le partage de ressources.

### 2. Partage de ressources et d'informations :**
   - L'un des objectifs principaux d'un réseau informatique est de permettre le partage efficace des ressources, y compris des fichiers, des imprimantes, des applications, et d'autres services.
   - En facilitant la communication entre les systèmes, un réseau permet également le partage rapide et fiable d'informations entre les utilisateurs et les dispositifs connectés.

## B. Modèles de référence**

### 1. OSI (Open Systems Interconnection) :**
   - Le modèle OSI est une norme de référence internationale pour la conception et le fonctionnement des réseaux informatiques. Il est divisé en sept couches, chacune ayant des fonctions spécifiques.
   
   - **Couches du modèle OSI :**
     1. **Couche physique (1) :**
        - Responsable de la transmission brute des bits sur un support physique.
        - Exemples : câbles, connecteurs, signaux électriques.
     2. **Couche liaison de données (2) :**
        - Gère l'accès au support physique, la détection d'erreurs, et le contrôle de flux.
        - Exemples : Ethernet, PPP (Point-to-Point Protocol).
     3. **Couche réseau (3) :**
        - Routage des données à travers le réseau.
        - Exemple : IP (Internet Protocol).
     4. **Couche transport (4) :**
        - Gère la fiabilité de la communication.
        - Exemple : TCP (Transmission Control Protocol).
     5. **Couche session (5) :**
        - Établit, maintient, et termine les sessions entre les applications.
     6. **Couche présentation (6) :**
        - Gère la traduction, la compression et le chiffrement des données.
     7. **Couche application (7) :**
        - Fournit des interfaces pour les applications réseau.
        - Exemples : HTTP, FTP.

### 2. TCP/IP (Transmission Control Protocol/Internet Protocol) :**
   - Le modèle TCP/IP est un ensemble de protocoles largement utilisé pour les communications sur Internet. Il est divisé en quatre couches, souvent regroupées en deux catégories : la couche hôte et la couche réseau.

   - **Couches principales du modèle TCP/IP :**
     1. **Couche d'application :**
        - Correspondant aux couches session, présentation et application du modèle OSI.
        - Fournit des services réseau directement aux applications utilisateur.
     2. **Couche transport :**
        - Correspond à la couche transport du modèle OSI.
        - Gère le transport des données de bout en bout.
     3. **Couche Internet :**
        - Correspond à la couche réseau du modèle OSI.
        - Responsable du routage des paquets à travers le réseau.
     4. **Couche d'accès au réseau :**
        - Correspond aux couches physiques et de liaison de données du modèle OSI.
        - Gère l'accès au support physique et la transmission des données.

   - Ces couches sont modulaires et permettent une évolutivité et une flexibilité accrues dans la conception des réseaux, en particulier sur Internet.


-----------------------------------------------------------------------------------------------


# II. Positionnement de SSH dans les Modèles de Référence**

## A. Modèle OSI**

1. **Identifier la couche correspondante pour SSH dans le modèle OSI :**
   - SSH (Secure Shell) se positionne principalement au niveau de la couche application du modèle OSI.
   - Il opère au-dessus des couches de transport (par exemple, TCP) et de réseau (par exemple, IP), assurant ainsi une sécurisation des données à un niveau élevé dans la pile de protocoles.

2. **Brève explication du rôle de cette couche :**
   - La couche application du modèle OSI est la couche la plus proche de l'utilisateur final et des applications logicielles. C'est à ce niveau que les protocoles fournissent des services de communication directement aux applications.
   - SSH, en tant que protocole de la couche application, offre un moyen sécurisé d'accéder à distance à des systèmes et de transférer des données de manière cryptée. Il facilite l'authentification et la confidentialité des communications entre les utilisateurs et les systèmes distants.

## B. Modèle TCP/IP**

### 1. Localiser SSH dans les couches du modèle TCP/IP :**
   - Dans le modèle TCP/IP, SSH s'insère également au niveau de la couche application, correspondant à la couche d'application du modèle OSI.
   - Il utilise des protocoles de transport sous-jacents tels que TCP pour assurer la fiabilité de la communication.

### 2. Mettre en avant le rôle de SSH dans le contexte du modèle TCP/IP :**
   - La couche application du modèle TCP/IP englobe les protocoles qui fournissent des services directs aux applications utilisateur. SSH, en tant que protocole de cette couche, joue un rôle crucial dans la sécurisation des communications.
   - En utilisant le chiffrement et l'authentification forte, SSH assure un échange sécurisé d'informations entre un client et un serveur, que ce soit pour l'accès à distance, le transfert de fichiers, ou d'autres opérations réseau.

   - SSH utilise généralement le protocole TCP pour le transport fiable des données. Cela garantit que les informations échangées entre les parties sont intégres, confidentielles et qu'elles parviennent à destination sans altération.

En résumé, SSH occupe une place stratégique au niveau de la couche application dans les modèles OSI et TCP/IP, offrant une sécurité robuste pour les communications réseau, en particulier lorsqu'il s'agit d'accès distant et de transfert de données sensibles.


-----------------------------------------------------------------------------------------------


# III. Introduction à SSH (Secure Shell)

## A. Définition de SSH

   Protocole de communication sécurisé :
        SSH, qui signifie "Secure Shell", est un protocole de communication sécurisé conçu pour permettre l'accès sécurisé à des systèmes distants sur un réseau non sécurisé.
        Il fournit un canal sécurisé sur une connexion non sécurisée, typiquement l'Internet, en utilisant des techniques de chiffrement pour protéger les données transitant entre le client et le serveur.

   Utilisé pour l'accès distant et la gestion de systèmes :
        SSH est largement utilisé pour l'accès distant à des systèmes, permettant aux utilisateurs de se connecter à des serveurs distants de manière sécurisée.
        En plus de l'accès distant, SSH est également utilisé pour la gestion sécurisée des systèmes, le transfert de fichiers sécurisé (SFTP), et l'exécution de commandes à distance de manière sécurisée.

## B. Fonctionnalités de sécurité de SSH

   Chiffrement des données :
        L'une des principales fonctionnalités de sécurité de SSH est le chiffrement des données. Les informations échangées entre le client SSH et le serveur SSH sont cryptées, rendant extrêmement difficile pour des tiers non autorisés d'intercepter et de comprendre le contenu des communications.
        Le chiffrement est appliqué à toutes les données, y compris les commandes, les informations d'identification, et tout autre trafic entre le client et le serveur.

   Authentification forte :
        SSH utilise un mécanisme d'authentification forte, ce qui signifie que l'identité des parties en communication est vérifiée de manière robuste.
        Il prend en charge plusieurs méthodes d'authentification, telles que les clés publiques/privées, les mots de passe, et même l'authentification à deux facteurs. Ces méthodes renforcent la sécurité en s'assurant que seules les parties autorisées ont accès au système.
        L'utilisation de clés publiques/privées est courante dans SSH. Dans ce cas, une clé publique est partagée avec le serveur, et la clé privée est conservée par l'utilisateur. L'authentification se fait en prouvant la possession de la clé privée.

En résumé, SSH offre un environnement de communication sécurisé en chiffrant les données échangées et en utilisant des méthodes d'authentification forte pour s'assurer de l'identité des parties impliquées. Ces caractéristiques font de SSH un choix privilégié pour la gestion à distance sécurisée des systèmes et des communications sensibles.


-----------------------------------------------------------------------------------------------


# IV. Simulation de Contrôle avec SSH**

## A. Scénario de simulation**

### 1. Explication du cas d'utilisation :**
   - Imaginons un scénario où un administrateur système (utilisateur A) souhaite gérer à distance un serveur (machine B) en utilisant SSH. L'objectif est d'illustrer comment SSH permet un accès sécurisé et une gestion à distance.

### 2. Mise en place d'une connexion SSH entre deux machines :**
   - L'administrateur (A) commence par établir une connexion SSH sécurisée avec le serveur distant (B) en utilisant un client SSH. Cela peut être réalisé en utilisant la commande SSH dans un terminal, en spécifiant l'adresse IP ou le nom de domaine du serveur, ainsi que les informations d'identification appropriées.

   - Par exemple :
     ```bash
     ssh utilisateurA@adresse_IP_serveur
     ```

   - Lors de la première connexion, l'utilisateur peut être invité à accepter la clé publique du serveur pour établir une relation de confiance. Une fois l'authentification réussie, l'utilisateur (A) a un accès distant sécurisé à la machine (B).

## B. Démonstration en temps réel**

1. ### Utilisation d'outils de simulation pour le contrôle à distance :**
   - Pour la démonstration, nous utiliserons des outils de simulation pour illustrer le contrôle à distance. Cela peut être réalisé à l'aide de logiciels de virtualisation de systèmes, tels que VirtualBox, où deux machines virtuelles seront configurées pour représenter le client et le serveur.

   - L'administrateur (utilisateur A) peut se connecter à la machine distante (machine B) en utilisant un client SSH, émulant une connexion réelle sur un réseau.

2. ### Illustration du chiffrement des données par SSH :**
   - Pendant la démonstration, nous mettrons en évidence le chiffrement des données par SSH en utilisant des outils tels que Wireshark pour capturer le trafic réseau. La comparaison entre une connexion SSH sécurisée et une connexion non sécurisée soulignera l'efficacité du chiffrement.

   - Lors de l'analyse du trafic capturé, on peut observer que les données échangées entre le client et le serveur via SSH sont illisibles pour un observateur externe en raison du chiffrement. Cela confirmera visuellement comment SSH garantit la confidentialité des données pendant la communication.

En résumé, la simulation de contrôle avec SSH permettra de démontrer concrètement comment SSH assure un accès distant sécurisé, en établissant une connexion chiffrée entre un utilisateur et une machine distante, renforçant ainsi la sécurité des opérations de gestion à distance.


-----------------------------------------------------------------------------------------------


# V. Introduction à Wireshark**

## A. Présentation de Wireshark**

### 1. Outil d'analyse de paquets réseau :**
   - Wireshark est un outil open-source d'analyse de paquets réseau qui permet de capturer, visualiser, et inspecter le trafic sur un réseau. Il offre une compréhension approfondie du fonctionnement des communications réseau en examinant les paquets de données qui transitent entre les différents points du réseau.

### 2. Démonstration en temps réel de la capture du trafic non chiffré :**
   - Pour la démonstration, Wireshark sera utilisé pour capturer le trafic entre le client et le serveur pendant une session non chiffrée. Cela peut être simulé en utilisant des configurations réseau où le chiffrement n'est pas activé.

   - L'attaquant, utilisant Wireshark, peut capturer les paquets de données échangés entre le client et le serveur. Ces paquets peuvent contenir des informations sensibles, et la démonstration permettra de visualiser comment ces données peuvent être facilement interceptées.

-----------------------------------------------------------------------------------------------


# VII. Analyse des Résultats**

## A. Montrer que les données SSH sont sécurisées :**

   - En examinant les résultats de la simulation avec SSH, on peut montrer que les données échangées entre le client et le serveur sont sécurisées. Le chiffrement des données par SSH garantit que même si un attaquant intercepte les paquets, il ne peut pas comprendre le contenu, car il est chiffré.

   - La comparaison visuelle des données capturées avec Wireshark dans les deux scénarios soulignera la sécurité renforcée offerte par SSH. Les informations sensibles, telles que les identifiants de connexion, les commandes, ou les données confidentielles, restent confidentielles et ne peuvent pas être exploitées par un tiers non autorisé.

   - On peut également mettre en avant le mécanisme d'authentification forte de SSH, qui ajoute une couche supplémentaire de sécurité en vérifiant l'identité des parties impliquées dans la communication.


-----------------------------------------------------------------------------------------------

# VIII. Conclusion**

Dans cette présentation, nous avons exploré les fondamentaux des réseaux, mettant en évidence les modèles OSI et TCP/IP, ainsi que le rôle crucial de SSH dans la sécurisation des communications. La démonstration en temps réel a illustré l'établissement sécurisé de connexions avec SSH et a souligné les risques associés à la communication non chiffrée, démontrés via Wireshark





$ sudo apt install openssh-server         [On Debian, Ubuntu and Mint]
$ sudo yum install openssh                [On RHEL/CentOS/Fedora and Rocky/AlmaLinux]
$ sudo emerge -a openssh                  [On Gentoo Linux]
$ sudo apk add openssh                    [On Alpine Linux]
$ sudo pacman -S openssh                  [On Arch Linux]
$ sudo zypper install openssh             [On OpenSUSE]    

