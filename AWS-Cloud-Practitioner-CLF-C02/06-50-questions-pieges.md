# 50 questions pièges CLF-C02 — celles qui font échouer le plus de candidats

> **Version interactive recommandée :** `06-50-questions-pieges-interactif.html` (réponses masquées jusqu'à votre validation).
> Ces questions ciblent les **confusions les plus fréquentes** : services qui se ressemblent, responsabilité partagée,
> options d'achat, plans de support, classes de stockage. Lisez chaque mot de la question : le piège est souvent dans un détail.

---

**1.** Une entreprise veut bloquer les tentatives d'injection SQL ciblant son Application Load Balancer. Quel service utiliser ?
- A. AWS Shield Standard
- B. Amazon GuardDuty
- C. AWS Shield Advanced
- D. AWS WAF

**2.** Quel est l'objectif PRINCIPAL d'un déploiement Amazon RDS Multi-AZ ?
- A. Assurer la haute disponibilité grâce à une instance de secours synchrone et un basculement automatique
- B. Améliorer les performances de lecture
- C. Répliquer la base vers une autre Région
- D. Réduire le coût de la base de données

**3.** Qui est responsable de l'application des correctifs du système d'exploitation invité d'une instance Amazon EC2 ?
- A. AWS
- B. Le client
- C. AWS Support
- D. Le partenaire APN qui a vendu l'AMI

**4.** Quel est le plan de support AWS le MOINS cher offrant un accès 24h/24 et 7j/7 aux ingénieurs support par téléphone ?
- A. Developer
- B. Enterprise On-Ramp
- C. Business
- D. Basic

**5.** Une base Amazon RDS est surchargée par des requêtes de lecture issues de rapports. Quelle solution améliore les performances ?
- A. Activer Multi-AZ
- B. Augmenter la taille du stockage
- C. Créer des réplicas en lecture (Read Replicas)
- D. Prendre des snapshots plus fréquents

**6.** Une instance EC2 a été compromise et mine des cryptomonnaies en communiquant avec des serveurs malveillants. Quel service détecte ce comportement ?
- A. Amazon Inspector
- B. Amazon GuardDuty
- C. Amazon Macie
- D. AWS Config

**7.** Une équipe veut identifier automatiquement les logiciels non patchés présentant des vulnérabilités connues (CVE) sur ses instances EC2. Quel service ?
- A. Amazon Inspector
- B. Amazon GuardDuty
- C. AWS Trusted Advisor
- D. AWS Shield

**8.** Une entreprise utilise EC2, AWS Fargate et AWS Lambda. Elle veut une remise en échange d'un engagement d'usage, tout en gardant la flexibilité de changer de famille d'instance et de Région. Quelle option ?
- A. EC2 Instance Savings Plan
- B. Instances réservées standard
- C. Instances réservées convertibles
- D. Compute Savings Plan

**9.** Quelle affirmation sur les Security Groups est correcte ?
- A. Ils sont sans état et permettent des règles de refus
- B. Ils sont avec état et n'autorisent que des règles d'autorisation
- C. Ils s'appliquent au niveau du sous-réseau
- D. Leurs règles sont évaluées dans l'ordre de leur numéro

**10.** Quels services utilisent les Edge Locations AWS ? (Choisissez-en deux.)
- A. Amazon CloudFront
- B. Amazon RDS
- C. Amazon Route 53
- D. Amazon EBS
- E. Amazon EFS

**11.** Pour AWS Lambda, laquelle de ces tâches N'EST PAS de la responsabilité du client ?
- A. Le code de la fonction
- B. Les permissions IAM de la fonction
- C. Les correctifs du système d'exploitation de l'environnement d'exécution
- D. Les données traitées par la fonction

**12.** Quel outil génère la liste de tous les utilisateurs IAM d'un compte avec l'état de leurs mots de passe, clés d'accès et MFA ?
- A. IAM Credential Report
- B. IAM Access Advisor
- C. IAM Access Analyzer
- D. AWS CloudTrail

**13.** Qui décide de la Région AWS dans laquelle les données d'un client sont stockées ?
- A. AWS, automatiquement selon la charge
- B. Le client
- C. AWS Support
- D. L'équipe conformité d'AWS

**14.** Quel est le plan de support le MOINS cher donnant accès à l'ensemble des contrôles AWS Trusted Advisor ?
- A. Basic
- B. Developer
- C. Business
- D. Enterprise

**15.** Un responsable financier veut recevoir un e-mail dès que les dépenses PRÉVUES du mois dépassent 5 000 $. Quel service ?
- A. AWS Cost Explorer
- B. AWS Budgets
- C. AWS Pricing Calculator
- D. AWS Cost and Usage Report

**16.** Une entreprise n'a encore rien déployé sur AWS et veut estimer le coût mensuel de son architecture cible. Quel outil ?
- A. AWS Pricing Calculator
- B. AWS Cost Explorer
- C. AWS Budgets
- D. AWS Trusted Advisor

**17.** Laquelle de ces tâches ne peut être effectuée QUE par l'utilisateur root ?
- A. Lancer une instance EC2
- B. Fermer le compte AWS
- C. Créer un groupe IAM
- D. Consulter les journaux CloudTrail

**18.** Lequel de ces transferts de données est GRATUIT ?
- A. D'Amazon EC2 vers Internet
- B. Entre deux Régions AWS
- C. D'une instance EC2 vers une autre AZ
- D. D'Internet vers AWS (trafic entrant)

**19.** Un site ajoute automatiquement des serveurs pendant les pics et les supprime quand le trafic baisse. Quel concept cela illustre-t-il ?
- A. Haute disponibilité
- B. Tolérance aux pannes
- C. Élasticité
- D. Agilité

**20.** Un logiciel est licencié par socket physique et l'entreprise veut réutiliser ses licences existantes. Quelle option EC2 ?
- A. Instances dédiées
- B. Hôtes dédiés
- C. Instances Spot
- D. Instances réservées

**21.** Selon le modèle de responsabilité partagée, qui configure les politiques de bucket Amazon S3 ?
- A. Le client
- B. AWS
- C. Les deux à parts égales
- D. Personne, elles sont fixées par défaut

**22.** Combien de zones de disponibilité une Région AWS comprend-elle au MINIMUM ?
- A. 1
- B. 2
- C. 3
- D. 4

**23.** Une application doit stocker des clés d'API tierces et en effectuer la rotation automatique. Quel service ?
- A. AWS KMS
- B. AWS Secrets Manager
- C. AWS Systems Manager Parameter Store
- D. AWS Certificate Manager

**24.** Un auditeur demande le rapport SOC 2 d'AWS. Où le client peut-il le télécharger ?
- A. AWS Audit Manager
- B. AWS Security Hub
- C. AWS Config
- D. AWS Artifact

**25.** Un bucket S3 a été supprimé. Quel service indique quel utilisateur a effectué la suppression ?
- A. AWS CloudTrail
- B. Amazon CloudWatch
- C. AWS Config
- D. Amazon Macie

**26.** Une entreprise veut savoir quand une ressource devient non conforme à ses règles internes (ex. volume EBS non chiffré) et conserver l'historique de sa configuration. Quel service ?
- A. Amazon CloudWatch
- B. AWS CloudTrail
- C. Amazon Inspector
- D. AWS Config

**27.** Quel service répartit le trafic entrant entre plusieurs instances EC2 situées dans plusieurs zones de disponibilité ?
- A. Amazon Route 53
- B. Elastic Load Balancing
- C. Amazon CloudFront
- D. AWS Global Accelerator

**28.** Un même message doit être envoyé simultanément à plusieurs abonnés (e-mail, SMS et une fonction Lambda). Quel service ?
- A. Amazon SQS
- B. Amazon SNS
- C. Amazon SES
- D. AWS Step Functions

**29.** Quelle est la solution la plus simple et la moins chère pour héberger un site web composé uniquement de HTML, CSS et images ?
- A. Amazon S3
- B. Amazon EC2
- C. Amazon Lightsail
- D. AWS Elastic Beanstalk

**30.** Des données sont rarement consultées mais doivent être disponibles en quelques millisecondes et résister à la perte d'une AZ. Quelle classe S3 ?
- A. S3 One Zone-IA
- B. S3 Glacier Flexible Retrieval
- C. S3 Standard-IA
- D. S3 Glacier Deep Archive

**31.** Des copies de fichiers pouvant être facilement recréées sont rarement consultées. Quelle classe S3 est la MOINS chère tout en offrant un accès en millisecondes ?
- A. S3 One Zone-IA
- B. S3 Standard
- C. S3 Intelligent-Tiering
- D. S3 Standard-IA

**32.** Une entreprise doit conserver des archives 10 ans au coût le plus bas possible ; un délai de récupération de 48 heures est acceptable. Quelle classe ?
- A. S3 Standard-IA
- B. S3 Glacier Instant Retrieval
- C. S3 One Zone-IA
- D. S3 Glacier Deep Archive

**33.** Quelle est la portée d'un volume Amazon EBS ?
- A. Une Région
- B. Une zone de disponibilité
- C. Mondiale
- D. Une Edge Location

**34.** Des centaines d'instances EC2 Linux réparties sur plusieurs AZ doivent lire et écrire dans le même système de fichiers. Quel service ?
- A. Amazon EBS
- B. Instance Store
- C. Amazon FSx for Windows File Server
- D. Amazon EFS

**35.** Pour quelle charge de travail les instances Spot sont-elles le mieux adaptées ?
- A. Une base de données de production
- B. Un traitement d'images par lots pouvant être interrompu et relancé
- C. Une API de paiement en temps réel
- D. Un contrôleur de domaine Active Directory

**36.** Quelle est la durée maximale d'exécution d'une fonction AWS Lambda ?
- A. 5 minutes
- B. 15 minutes
- C. 1 heure
- D. Illimitée

**37.** Une banque exige un module matériel de sécurité dédié à un seul client, dont elle contrôle entièrement les clés. Quel service ?
- A. AWS KMS
- B. AWS Secrets Manager
- C. AWS CloudHSM
- D. AWS Certificate Manager

**38.** Quels avantages AWS Shield Advanced apporte-t-il par rapport à Shield Standard ? (Choisissez-en deux.)
- A. Une protection des coûts liés aux pics de mise à l'échelle pendant une attaque DDoS
- B. Il est gratuit pour tous les clients
- C. Un accès 24/7 à l'équipe Shield Response Team (SRT)
- D. Le blocage des injections SQL sans configuration
- E. L'application automatique des correctifs sur EC2

**39.** Quel est l'effet d'une Service Control Policy (SCP) dans AWS Organizations ?
- A. Elle accorde des permissions aux utilisateurs IAM
- B. Elle définit les permissions MAXIMALES disponibles dans les comptes concernés
- C. Elle s'applique aussi au compte de gestion
- D. Elle remplace les politiques IAM

**40.** Quel pilier du Well-Architected Framework porte sur la capacité d'une charge de travail à se rétablir après une panne ?
- A. Efficacité des performances
- B. Excellence opérationnelle
- C. Fiabilité
- D. Sécurité

**41.** Quelle perspective du AWS Cloud Adoption Framework couvre la formation des équipes, la culture et la gestion du changement ?
- A. Business
- B. Gouvernance
- C. Plateforme
- D. Personnes (People)

**42.** Une entreprise migre sa base MySQL auto-gérée vers Amazon RDS for MySQL sans modifier le code de l'application. Quelle stratégie ?
- A. Replatform
- B. Rehost
- C. Refactor
- D. Repurchase

**43.** Lequel de ces services est un service GLOBAL (non rattaché à une Région) ?
- A. Amazon EC2
- B. Amazon RDS
- C. AWS IAM
- D. Amazon EBS

**44.** Une entreprise veut exécuter des services AWS dans son propre data center avec les mêmes API qu'AWS. Quel service ?
- A. AWS Outposts
- B. AWS Local Zones
- C. AWS Wavelength
- D. AWS Direct Connect

**45.** Une entreprise veut réduire la latence pour des utilisateurs du monde entier en mettant en cache les vidéos et les images près d'eux. Quel service ?
- A. Amazon Route 53
- B. AWS Global Accelerator
- C. AWS Direct Connect
- D. Amazon CloudFront

**46.** Quel plan de support inclut un Technical Account Manager (TAM) DÉSIGNÉ ?
- A. Business
- B. Developer
- C. Enterprise On-Ramp
- D. Enterprise

**47.** Quels sont les avantages de la facturation consolidée d'AWS Organizations ? (Choisissez-en deux.)
- A. Une seule facture pour tous les comptes
- B. Des remises sur volume calculées sur l'usage combiné des comptes
- C. Un plan de support Business gratuit
- D. La gratuité du transfert de données entre comptes
- E. Des instances réservées illimitées

**48.** Un analyste veut exécuter des requêtes SQL directement sur des fichiers stockés dans Amazon S3, sans gérer de serveur. Quel service ?
- A. Amazon Redshift
- B. Amazon Athena
- C. Amazon EMR
- D. Amazon RDS

**49.** Une équipe atteint la limite du nombre d'instances EC2 autorisées dans une Région. Quel service permet de demander une augmentation ?
- A. AWS Trusted Advisor
- B. AWS Config
- C. Service Quotas
- D. AWS Health Dashboard

**50.** Quel service informe un client qu'une maintenance planifiée par AWS va affecter l'une de SES instances EC2 ?
- A. AWS Health Dashboard
- B. Amazon CloudWatch
- C. AWS Trusted Advisor
- D. AWS CloudTrail

---

# ✅ CORRIGÉ DÉTAILLÉ

| # | Rép. | Explication et piège |
|---|---|---|
| 1 | **D** | WAF filtre la couche 7 (SQLi, XSS). Piège : Shield protège contre le DDoS, pas contre l'injection SQL. |
| 2 | **A** | Multi-AZ = disponibilité. Piège : le standby ne sert pas les lectures ; pour la performance, ce sont les Read Replicas. |
| 3 | **B** | Sur EC2 (IaaS), l'OS invité est géré par le client. AWS s'occupe de l'hyperviseur et du matériel. |
| 4 | **C** | Business est le premier plan avec téléphone 24/7. Piège : Developer = e-mail, heures ouvrables seulement. |
| 5 | **C** | Les Read Replicas déchargent les lectures. Piège classique : Multi-AZ ne change rien aux performances de lecture. |
| 6 | **B** | GuardDuty détecte une activité malveillante en cours (logs VPC Flow, DNS, CloudTrail). |
| 7 | **A** | Inspector recherche les vulnérabilités logicielles. Piège : GuardDuty détecte des menaces, pas des CVE. |
| 8 | **D** | Seul le Compute Savings Plan couvre EC2, Fargate et Lambda, toutes familles et Régions. |
| 9 | **B** | Security Group : avec état, Allow uniquement, niveau instance. Les autres propositions décrivent une NACL. |
| 10 | **A, C** | CloudFront (cache) et Route 53 (DNS) s'appuient sur les Edge Locations, tout comme Shield et WAF. |
| 11 | **C** | Lambda est serverless : AWS gère l'OS et le runtime. Le client garde code, permissions et données. |
| 12 | **A** | Credential Report = niveau compte, tous les utilisateurs. Piège : Access Advisor montre les services utilisés par une identité. |
| 13 | **B** | Le client choisit la Région ; AWS ne déplace pas les données sans action du client. |
| 14 | **C** | Tous les contrôles Trusted Advisor dès le plan Business. Basic et Developer n'ont que les contrôles de base. |
| 15 | **B** | Budgets envoie des alertes sur les coûts réels ou prévus. Piège : Cost Explorer analyse mais n'alerte pas. |
| 16 | **A** | Rien n'est encore déployé : seul le Pricing Calculator permet d'estimer. Cost Explorer s'appuie sur des dépenses existantes. |
| 17 | **B** | Fermer le compte est réservé au root, comme modifier les paramètres du compte ou restaurer des permissions IAM. |
| 18 | **D** | Le trafic entrant est gratuit. Sortie vers Internet, inter-Régions et inter-AZ sont facturés. |
| 19 | **C** | Élasticité = ajuster automatiquement à la hausse ET à la baisse. Piège : la scalabilité seule n'implique pas la réduction. |
| 20 | **B** | Les Dedicated Hosts donnent la visibilité sur les sockets et cœurs physiques (BYOL). Les instances dédiées ne le permettent pas. |
| 21 | **A** | Configurer les accès aux données (politiques de bucket, ACL, Block Public Access) est toujours la responsabilité du client. |
| 22 | **C** | Minimum 3 AZ par Région (certaines en ont plus). |
| 23 | **B** | Secrets Manager = rotation automatique. Piège : Parameter Store stocke mais ne fait pas de rotation native ; KMS gère des clés de chiffrement. |
| 24 | **D** | Artifact fournit les rapports de conformité d'AWS. Piège : Audit Manager prépare VOS audits. |
| 25 | **A** | CloudTrail enregistre qui a fait quel appel d'API. Piège : Config montre l'état de la ressource, pas l'auteur. |
| 26 | **D** | Config évalue la conformité et garde l'historique de configuration. |
| 27 | **B** | ELB répartit le trafic entre instances et AZ. Piège : Route 53 fait du routage DNS, pas de l'équilibrage de charge au niveau des instances. |
| 28 | **B** | SNS = publication/abonnement (fan-out). SQS = file d'attente consommée par un traitement. SES = e-mails uniquement. |
| 29 | **A** | Site statique = hébergement de site web S3 (souvent avec CloudFront). Pas de serveur à gérer. |
| 30 | **C** | Standard-IA : accès rare, millisecondes, multi-AZ. Piège : One Zone-IA ne résiste pas à la perte d'une AZ. |
| 31 | **A** | Données recréables + accès rare = One Zone-IA, environ 20 % moins cher que Standard-IA. |
| 32 | **D** | Deep Archive est la classe la moins chère ; récupération en 12 à 48 h. |
| 33 | **B** | Un volume EBS est lié à une AZ. Pour le déplacer : snapshot puis restauration dans une autre AZ. |
| 34 | **D** | EFS = NFS partagé, multi-AZ, pour Linux. Piège : FSx for Windows est pour SMB/Windows ; EBS est attaché à une instance. |
| 35 | **B** | Spot convient aux tâches tolérantes aux interruptions. Jamais pour une base de production ou un service critique. |
| 36 | **B** | 15 minutes maximum. Au-delà : EC2, ECS/Fargate ou AWS Batch. |
| 37 | **C** | CloudHSM = HSM matériel dédié (single-tenant). KMS est un service managé partagé. |
| 38 | **A, C** | Shield Advanced : protection des coûts DDoS + SRT 24/7 + WAF inclus. Il est payant ; Shield Standard est gratuit. |
| 39 | **B** | Une SCP fixe un plafond ; elle n'accorde rien et ne s'applique pas au compte de gestion. |
| 40 | **C** | Fiabilité = se rétablir des pannes, scaler horizontalement, tester la reprise. |
| 41 | **D** | La perspective People couvre culture, formation, structure et changement. |
| 42 | **A** | Replatform = optimisation sans changer l'architecture. Rehost serait une base MySQL installée telle quelle sur EC2. |
| 43 | **C** | IAM est global. EC2, RDS sont régionaux ; EBS est lié à une AZ. |
| 44 | **A** | Outposts installe l'infrastructure AWS chez le client. Local Zones restent chez AWS, près d'une ville. |
| 45 | **D** | CloudFront met en cache le contenu dans les Edge Locations. Piège : Global Accelerator ne met rien en cache. |
| 46 | **D** | TAM désigné = Enterprise. Enterprise On-Ramp donne accès à un pool de TAM. |
| 47 | **A, B** | Facture unique + remises sur volume cumulées (et partage des RI/Savings Plans). La facturation consolidée est gratuite. |
| 48 | **B** | Athena = SQL serverless sur S3. Redshift est un entrepôt de données à alimenter. |
| 49 | **C** | Service Quotas permet de consulter et demander l'augmentation des limites. Trusted Advisor ne fait que signaler les limites proches. |
| 50 | **A** | AWS Health Dashboard montre les événements qui affectent VOS ressources. CloudWatch surveille les métriques. |

### Grille d'auto-évaluation
| Score | Interprétation |
|---|---|
| 45–50 | Excellent — les pièges ne vous piègent plus |
| 38–44 | Bon — revoyez vos erreurs dans la fiche mémo (fichier 04, tableau des paires de services) |
| 30–37 | Moyen — relisez le guide de cours sur les domaines concernés |
| < 30 | Reprenez le guide de cours et les cas pratiques visuels (fichier 05) avant de recommencer |
