# Examen blanc CLF-C02 — 65 questions / 90 minutes

> **Conditions réelles :** ouvrez de préférence **`03-Examen-blanc-interactif.html`** (chrono de 90 min intégré, réponses masquées
> jusqu'à ce que vous validiez chaque question, score en direct). Le **corrigé complet** se débloque une fois les 65 questions validées.
> **Objectif :** ≥ 75 % (49/65) pour être confortable le jour de l'examen (le seuil réel est de 700/1000).
> Répartition approximative : Concepts 24 % · Sécurité 30 % · Technologie 34 % · Facturation 12 %.

---

**1.** Quel avantage du cloud AWS permet à une entreprise de déployer une application pour des clients en Asie et en Europe en quelques minutes ?
- A. Économies d'échelle
- B. Devenir mondial en quelques minutes
- C. Remplacer le CapEx par l'OpEx
- D. Arrêter de deviner la capacité

**2.** Selon le modèle de responsabilité partagée, qui est responsable de la configuration des groupes de sécurité d'une instance EC2 ?
- A. Le partenaire APN
- B. Les deux
- C. AWS
- D. Le client

**3.** Une entreprise veut stocker des fichiers de logs qui seront rarement consultés après 30 jours mais qui doivent être disponibles en quelques millisecondes en cas de besoin. Quelle classe S3 est la plus économique ?
- A. S3 Glacier Deep Archive
- B. S3 Glacier Flexible Retrieval
- C. S3 Standard-IA
- D. S3 Standard

**4.** Quel service AWS permet d'enregistrer les appels d'API effectués dans un compte AWS ?
- A. AWS Config
- B. AWS CloudTrail
- C. Amazon CloudWatch
- D. AWS X-Ray

**5.** Quelles sont DEUX caractéristiques d'une zone de disponibilité ? (Choisissez-en deux.)
- A. C'est un point de présence CloudFront
- B. Elle est isolée des pannes des autres AZ
- C. Elle se trouve chez le client
- D. Elle couvre plusieurs Régions
- E. Elle est constituée d'un ou plusieurs data centers distincts

**6.** Quel service propose des recommandations en temps réel dans les catégories sécurité, coûts, performance, tolérance aux pannes et quotas de service ?
- A. AWS Trusted Advisor
- B. AWS Well-Architected Tool
- C. Amazon Inspector
- D. AWS Config

**7.** Une application doit traiter des tâches de rendu vidéo qui peuvent être interrompues et relancées. Quelle option EC2 minimise les coûts ?
- A. Instances réservées
- B. Hôtes dédiés
- C. Instances à la demande
- D. Instances Spot

**8.** Quel service permet de créer une base de données NoSQL clé-valeur entièrement managée et serverless ?
- A. Amazon DynamoDB
- B. Amazon Redshift
- C. Amazon Aurora
- D. Amazon RDS

**9.** Une entreprise souhaite recevoir une alerte quand ses coûts prévus dépassent le budget mensuel. Quel service ?
- A. AWS Trusted Advisor
- B. AWS Cost Explorer
- C. AWS Budgets
- D. AWS Pricing Calculator

**10.** Quel pilier du Well-Architected Framework inclut le principe « appliquer la sécurité à toutes les couches » ?
- A. Sécurité
- B. Fiabilité
- C. Efficacité des performances
- D. Excellence opérationnelle

**11.** Quel service AWS fournit un réseau de diffusion de contenu (CDN) ?
- A. AWS Direct Connect
- B. Elastic Load Balancing
- C. Amazon CloudFront
- D. Amazon Route 53

**12.** Quel service permet de télécharger les rapports d'audit ISO 27001 d'AWS ?
- A. AWS Security Hub
- B. Amazon Macie
- C. AWS Audit Manager
- D. AWS Artifact

**13.** Une entreprise veut exécuter son code en réponse à l'arrivée de fichiers dans un bucket S3, sans gérer de serveurs. Quel service ?
- A. Amazon Lightsail
- B. AWS Lambda
- C. AWS Elastic Beanstalk
- D. Amazon EC2

**14.** Quelle est la bonne pratique pour accorder à une instance EC2 l'accès à DynamoDB ?
- A. Utiliser l'utilisateur root
- B. Créer un groupe IAM pour l'instance
- C. Utiliser un rôle IAM
- D. Stocker des clés d'accès sur l'instance

**15.** Quel plan de support AWS est le moins cher offrant un temps de réponse inférieur à 1 heure pour un système de production en panne ?
- A. Developer
- B. Business
- C. Enterprise
- D. Enterprise On-Ramp

**16.** Une entreprise migre son application vers AWS en remplaçant sa base de données auto-gérée par Amazon RDS, sans modifier le code. Quelle stratégie de migration ?
- A. Retire
- B. Rehost
- C. Refactor
- D. Replatform

**17.** Quel service détecte les menaces en analysant les logs VPC Flow Logs, DNS et CloudTrail ?
- A. AWS Shield
- B. AWS WAF
- C. Amazon Inspector
- D. Amazon GuardDuty

**18.** Quel service permet d'interroger des données dans Amazon S3 avec du SQL standard sans charger les données ?
- A. Amazon Athena
- B. AWS Glue
- C. Amazon Redshift
- D. Amazon RDS

**19.** Quelles DEUX actions améliorent la sécurité du compte root ? (Choisissez-en deux.)
- A. Désactiver CloudTrail
- B. Ne pas utiliser le root pour les tâches quotidiennes
- C. Créer des clés d'accès pour le root
- D. Partager le mot de passe root avec les administrateurs
- E. Activer la MFA

**20.** Quel service permet de connecter un data center sur site à AWS via une connexion privée qui ne passe pas par Internet ?
- A. Internet Gateway
- B. AWS Direct Connect
- C. AWS Site-to-Site VPN
- D. Amazon VPC Peering

**21.** Une entreprise veut gérer ses coûts sur 30 comptes AWS avec une seule facture. Quel service ?
- A. IAM Identity Center
- B. AWS Organizations
- C. AWS Control Tower
- D. AWS Cost Explorer

**22.** Quel concept permet à un système de continuer à fonctionner même si l'un de ses composants tombe en panne ?
- A. Agilité
- B. Scalabilité verticale
- C. Tolérance aux pannes
- D. Élasticité

**23.** Quel service est utilisé pour les conteneurs Kubernetes managés ?
- A. Amazon ECR
- B. AWS Batch
- C. Amazon ECS
- D. Amazon EKS

**24.** Une entreprise veut protéger son application web contre les attaques par injection SQL. Quel service ?
- A. AWS WAF
- B. AWS Shield Standard
- C. Security Groups
- D. Amazon GuardDuty

**25.** Quel service permet de modéliser et provisionner des ressources AWS à l'aide de modèles ?
- A. AWS Systems Manager
- B. AWS Config
- C. AWS CloudFormation
- D. AWS OpsWorks

**26.** Quel est un avantage de l'utilisation de plusieurs AZ ?
- A. Suppression du besoin de sauvegardes
- B. Conformité automatique au RGPD
- C. Haute disponibilité
- D. Réduction des coûts de transfert de données

**27.** Quel service stocke les mots de passe de base de données et les fait tourner automatiquement ?
- A. AWS Secrets Manager
- B. AWS CloudHSM
- C. AWS KMS
- D. AWS Certificate Manager

**28.** Quel outil permet d'analyser l'historique des dépenses et de visualiser des prévisions ?
- A. AWS Marketplace
- B. AWS Cost Explorer
- C. AWS Pricing Calculator
- D. AWS Budgets

**29.** Une entreprise a besoin d'un système de fichiers partagé, élastique, accessible par plusieurs instances EC2 Linux dans plusieurs AZ. Quel service ?
- A. Amazon EBS
- B. Amazon S3
- C. Amazon EFS
- D. Instance Store

**30.** Quel élément est de la responsabilité d'AWS pour AWS Lambda ?
- A. Le système d'exploitation et l'environnement d'exécution sous-jacents
- B. Le code de la fonction
- C. Les données traitées par la fonction
- D. Les permissions IAM de la fonction

**31.** Quel service AWS aide à découvrir et protéger les données sensibles telles que les informations personnelles dans S3 ?
- A. Amazon Detective
- B. Amazon Inspector
- C. AWS Config
- D. Amazon Macie

**32.** Quels DEUX services sont des services de base de données relationnelle ? (Choisissez-en deux.)
- A. Amazon Aurora
- B. Amazon DynamoDB
- C. Amazon RDS
- D. Amazon Neptune
- E. Amazon ElastiCache

**33.** Quel service fournit le DNS et peut acheminer le trafic vers la Région offrant la latence la plus faible ?
- A. Amazon Route 53
- B. Elastic Load Balancing
- C. Amazon CloudFront
- D. AWS Global Accelerator

**34.** Une entreprise veut un support avec un Technical Account Manager (TAM) désigné. Quel plan ?
- A. Developer
- B. Enterprise On-Ramp
- C. Business
- D. Enterprise

**35.** Quel service découple les composants d'une application avec une file d'attente de messages ?
- A. Amazon SQS
- B. Amazon EventBridge
- C. AWS Step Functions
- D. Amazon SNS

**36.** Quelle perspective du AWS CAF aide à s'assurer que les investissements cloud accélèrent les résultats métier ?
- A. Plateforme
- B. Business
- C. Opérations
- D. Sécurité

**37.** Où un client peut-il trouver des logiciels tiers prêts à l'emploi sur AWS ?
- A. AWS Artifact
- B. AWS Service Catalog
- C. AWS Marketplace
- D. AWS re:Post

**38.** Quel service de calcul convient le mieux à un développeur débutant qui veut un serveur virtuel simple avec un prix mensuel fixe ?
- A. Amazon Lightsail
- B. Amazon EC2
- C. AWS Outposts
- D. AWS Fargate

**39.** Quel type de règle une Network ACL permet-elle qu'un Security Group ne permet pas ?
- A. Règles entrantes
- B. Règles de refus explicites
- C. Règles basées sur les ports
- D. Règles d'autorisation

**40.** Quel service mesure l'utilisation CPU et déclenche des alarmes ?
- A. AWS Trusted Advisor
- B. Amazon CloudWatch
- C. AWS CloudTrail
- D. AWS Config

**41.** Une entreprise doit transférer 2 Po de données de son data center vers AWS. La bande passante est limitée. Quelle solution ?
- A. AWS Site-to-Site VPN
- B. S3 Transfer Acceleration
- C. AWS Snowball Edge (plusieurs appareils)
- D. Amazon CloudFront

**42.** Lequel de ces principes est un principe de tarification AWS ?
- A. Payer à l'avance pour toute la capacité
- B. Payer moins en réservant
- C. Payer un forfait annuel fixe pour tous les services
- D. Payer plus par unité en consommant plus

**43.** Quel service fournit des identités à des utilisateurs d'une application mobile, avec connexion via des réseaux sociaux ?
- A. AWS Directory Service
- B. AWS IAM
- C. AWS IAM Identity Center
- D. Amazon Cognito

**44.** Quel service permet d'analyser les vulnérabilités logicielles des instances EC2 ?
- A. Amazon GuardDuty
- B. Amazon Inspector
- C. Amazon Macie
- D. AWS Shield

**45.** Quels DEUX éléments sont des avantages d'AWS Elastic Beanstalk ? (Choisissez-en deux.)
- A. Il remplace AWS IAM
- B. Le développeur doit configurer manuellement chaque serveur
- C. Gestion automatique de la capacité, du load balancing et du scaling
- D. Le service est facturé avec un supplément important
- E. Le développeur se concentre sur son code

**46.** Quelle option RDS améliore les performances de lecture d'une base de données très sollicitée ?
- A. Chiffrement KMS
- B. Multi-AZ
- C. Read Replicas
- D. Snapshots manuels

**47.** Quelle est la durabilité d'Amazon S3 Standard ?
- A. 100 %
- B. 99,999999999 %
- C. 99,99 %
- D. 99,9 %

**48.** Une entreprise a besoin de déployer des ressources AWS dans son data center pour répondre à des exigences de faible latence et de résidence des données. Quel service ?
- A. AWS Direct Connect
- B. AWS Outposts
- C. AWS Local Zones
- D. AWS Wavelength

**49.** Quel service permet d'appliquer des Service Control Policies (SCP) ?
- A. AWS Config
- B. AWS Organizations
- C. AWS Control Tower uniquement
- D. AWS IAM

**50.** Quel service analyse le texte pour en extraire les sentiments et les entités ?
- A. Amazon Comprehend
- B. Amazon Lex
- C. Amazon Polly
- D. Amazon Rekognition

**51.** Une entreprise exécute une charge de travail stable sur EC2, Fargate et Lambda et veut la remise maximale tout en conservant la flexibilité de changer de famille d'instance et de Région. Quelle option ?
- A. Instances réservées standard
- B. Instances à la demande
- C. Instances Spot
- D. Compute Savings Plans

**52.** Quel service fournit une protection DDoS avancée avec l'accès à la Shield Response Team ?
- A. AWS Shield Standard
- B. AWS WAF
- C. AWS Firewall Manager
- D. AWS Shield Advanced

**53.** Quel service évalue, audite et enregistre en continu la configuration des ressources AWS ?
- A. AWS Systems Manager
- B. AWS CloudTrail
- C. Amazon CloudWatch
- D. AWS Config

**54.** Quel avantage du cloud correspond à « ne plus avoir à surdimensionner l'infrastructure pour les pics » ?
- A. Arrêter de deviner la capacité
- B. Arrêter de dépenser de l'argent pour faire tourner des data centers
- C. Économies d'échelle
- D. Devenir mondial en quelques minutes

**55.** Quels DEUX services sont des services de calcul serverless ? (Choisissez-en deux.)
- A. Amazon EC2
- B. AWS Fargate
- C. AWS Lambda
- D. AWS Outposts
- E. Amazon Lightsail

**56.** Quel service fournit des certificats SSL/TLS gratuits pour les services AWS intégrés ?
- A. AWS Secrets Manager
- B. AWS CloudHSM
- C. AWS KMS
- D. AWS Certificate Manager

**57.** Une entreprise veut accéder à une communauté de questions-réponses gérée par AWS. Quelle ressource ?
- A. AWS Artifact
- B. AWS Professional Services
- C. AWS Health Dashboard
- D. AWS re:Post

**58.** Quel service permet de créer un entrepôt de données pour l'analyse de pétaoctets de données ?
- A. Amazon Aurora
- B. Amazon ElastiCache
- C. Amazon DynamoDB
- D. Amazon Redshift

**59.** Qui est responsable du chiffrement des données stockées dans Amazon S3 selon le modèle de responsabilité partagée ?
- A. Le client (choisir et configurer le chiffrement et gérer les accès)
- B. Le fournisseur d'accès Internet
- C. Personne, S3 n'est pas chiffré
- D. AWS uniquement

**60.** Quel service permet d'envoyer des notifications push à plusieurs abonnés (e-mail, SMS, HTTP) ?
- A. Amazon SES
- B. Amazon MQ
- C. Amazon SNS
- D. Amazon SQS

**61.** Une entreprise veut migrer une base de données Microsoft SQL Server vers Amazon Aurora MySQL. Quels outils doit-elle utiliser ?
- A. AWS DataSync et Snowball
- B. AWS Storage Gateway
- C. AWS Backup
- D. AWS SCT et AWS DMS

**62.** Quel service fournit des informations sur les événements AWS qui peuvent affecter vos ressources, comme une maintenance planifiée ?
- A. AWS CloudTrail
- B. AWS Health Dashboard
- C. Amazon CloudWatch
- D. AWS Trusted Advisor

**63.** Quelle est la façon la plus rentable d'archiver des données pendant 10 ans avec une récupération possible sous 48 heures ?
- A. Amazon EBS
- B. S3 Glacier Deep Archive
- C. S3 Standard-IA
- D. Amazon EFS

**64.** Une entreprise veut améliorer les performances de son application mondiale TCP en utilisant le réseau privé d'AWS et des adresses IP statiques. Quel service ?
- A. AWS Global Accelerator
- B. Amazon Route 53
- C. Amazon CloudFront
- D. AWS Transit Gateway

**65.** Quel service permet de traiter des flux de données en temps réel, comme des clics sur un site web ?
- A. Amazon QuickSight
- B. Amazon Athena
- C. AWS Glue
- D. Amazon Kinesis

---
---

# ✅ CORRIGÉ DÉTAILLÉ

| # | Rép. | Explication |
|---|---|---|
| 1 | **B** | Déployer dans plusieurs Régions en quelques clics = *Go global in minutes*. |
| 2 | **D** | Les Security Groups sont configurés par le client (sécurité *dans* le cloud). |
| 3 | **C** | Accès rare + récupération en millisecondes + multi-AZ → Standard-IA (Glacier Flexible = minutes/heures ; Deep Archive = 12–48 h). |
| 4 | **B** | CloudTrail = historique des appels API. |
| 5 | **B, E** | Une AZ = data center(s) isolé(s) dans une Région. |
| 6 | **A** | Trusted Advisor couvre ces catégories (+ excellence opérationnelle). |
| 7 | **D** | Charge interruptible = Spot (jusqu'à −90 %). |
| 8 | **A** | DynamoDB = NoSQL serverless. |
| 9 | **C** | Budgets envoie des alertes sur les coûts réels ou prévus. |
| 10 | **A** | Principe du pilier Sécurité. |
| 11 | **C** | CloudFront = CDN. |
| 12 | **D** | Artifact = rapports de conformité d'AWS. |
| 13 | **B** | Lambda déclenché par un événement S3. |
| 14 | **C** | Rôle IAM = identifiants temporaires, pas de clés stockées. |
| 15 | **B** | Business : production en panne < 1 h. |
| 16 | **D** | Replatform = petite optimisation sans changer le cœur de l'appli. |
| 17 | **D** | GuardDuty = détection des menaces par ML. |
| 18 | **A** | Athena = SQL serverless sur S3. |
| 19 | **B, E** | MFA + ne pas l'utiliser au quotidien. |
| 20 | **B** | Direct Connect = connexion privée dédiée. |
| 21 | **B** | Organizations → facturation consolidée. |
| 22 | **C** | Définition de la tolérance aux pannes. |
| 23 | **D** | EKS = Kubernetes managé (ECR = registre d'images). |
| 24 | **A** | WAF = protection couche 7 (SQLi, XSS). |
| 25 | **C** | CloudFormation = Infrastructure as Code. |
| 26 | **C** | Multi-AZ = haute disponibilité. |
| 27 | **A** | Secrets Manager = rotation automatique. |
| 28 | **B** | Cost Explorer = analyse passée + prévisions. |
| 29 | **C** | EFS = NFS partagé multi-AZ pour Linux. |
| 30 | **A** | Service managé : AWS gère OS, runtime, infrastructure. |
| 31 | **D** | Macie = données sensibles dans S3. |
| 32 | **A, C** | Aurora et RDS sont relationnels (DynamoDB = NoSQL, Neptune = graphe, ElastiCache = cache). |
| 33 | **A** | Route 53 : routage basé sur la latence. |
| 34 | **D** | TAM *désigné* = Enterprise (On-Ramp = pool de TAM). |
| 35 | **A** | SQS = file d'attente (SNS = pub/sub). |
| 36 | **B** | Perspective Business. |
| 37 | **C** | AWS Marketplace. |
| 38 | **A** | Lightsail = simple et prix fixe. |
| 39 | **B** | Les NACL permettent des règles Deny ; les SG uniquement Allow. |
| 40 | **B** | CloudWatch = métriques et alarmes. |
| 41 | **C** | Pétaoctets + bande passante limitée = Snowball Edge. |
| 42 | **B** | Les principes : payer à l'usage, payer moins en réservant, payer moins par unité en consommant plus, payer moins quand AWS grandit. |
| 43 | **D** | Cognito = identités des utilisateurs d'applications. |
| 44 | **B** | Inspector = vulnérabilités. |
| 45 | **C, E** | Beanstalk est gratuit (on paie les ressources) et gère l'infrastructure. |
| 46 | **C** | Read Replicas = performance en lecture (Multi-AZ = disponibilité). |
| 47 | **B** | 11 neuf. |
| 48 | **B** | Outposts = AWS dans votre data center. |
| 49 | **B** | Les SCP font partie d'AWS Organizations (Control Tower s'en sert aussi, mais le service est Organizations). |
| 50 | **A** | Comprehend = NLP. |
| 51 | **D** | Compute Savings Plans = flexibilité EC2/Fargate/Lambda, toutes Régions. |
| 52 | **D** | Shield Advanced + SRT. |
| 53 | **D** | AWS Config. |
| 54 | **A** | *Stop guessing capacity*. |
| 55 | **B, C** | Lambda et Fargate sont serverless. |
| 56 | **D** | ACM. |
| 57 | **D** | re:Post. |
| 58 | **D** | Redshift = data warehouse. |
| 59 | **A** | S3 chiffre par défaut (SSE-S3), mais le client choisit/configure le chiffrement et gère les accès. |
| 60 | **C** | SNS = pub/sub. (SES = e-mails applicatifs.) |
| 61 | **D** | Moteurs différents → SCT (schéma) + DMS (données). |
| 62 | **B** | AWS Health Dashboard. |
| 63 | **B** | Glacier Deep Archive = le moins cher, récupération 12–48 h. |
| 64 | **A** | Global Accelerator = IP anycast statiques + réseau AWS. |
| 65 | **D** | Kinesis = streaming temps réel. |

### Grille d'auto-évaluation
| Score | Interprétation |
|---|---|
| 58–65 | Excellent — vous êtes prêt(e) |
| 49–57 | Bon — révisez vos erreurs puis planifiez l'examen |
| 40–48 | Moyen — relisez le guide de cours (fichier 01) sur vos domaines faibles |
| < 40 | Reprenez le guide de cours et les Q/R du fichier 02 avant de refaire cet examen |
