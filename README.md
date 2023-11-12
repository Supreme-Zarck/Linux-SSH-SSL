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
