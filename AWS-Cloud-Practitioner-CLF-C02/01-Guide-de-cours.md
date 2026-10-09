# AWS Certified Cloud Practitioner (CLF-C02) — Guide de cours complet

> Ce guide résume **tout ce qu'il faut savoir** pour l'examen, organisé selon les 4 domaines officiels.
> Lisez-le d'abord, puis entraînez-vous avec les fichiers 02 (Q/R par domaine) et 03 (examen blanc).

---

## 0. L'examen en bref

| Élément | Détail |
|---|---|
| Code | CLF-C02 |
| Nombre de questions | 65 (50 notées + 15 non notées, indiscernables) |
| Durée | 90 minutes |
| Format | QCM (1 bonne réponse sur 4) et réponses multiples (2+ bonnes réponses sur 5+) |
| Score | 100 à 1000 — **réussite à 700** |
| Pénalité mauvaise réponse | Aucune → **ne laissez jamais une question sans réponse** |
| Prix | 100 USD (bon de 50 % pour la certification suivante après réussite) |
| Validité | 3 ans |
| Langues | Dont le français |

### Pondération des domaines

| Domaine | Poids |
|---|---|
| 1. Concepts du cloud | 24 % |
| 2. Sécurité et conformité | 30 % |
| 3. Technologie et services cloud | 34 % |
| 4. Facturation, tarification et support | 12 % |

---

## DOMAINE 1 — Concepts du cloud (24 %)

### 1.1 Définition du cloud computing
Fourniture **à la demande** de ressources informatiques (calcul, stockage, bases de données, etc.) via Internet, avec une **tarification à l'usage** (pay-as-you-go).

### 1.2 Les 6 avantages du cloud AWS (à connaître PAR CŒUR)
1. **Remplacer les dépenses d'investissement (CapEx) par des dépenses variables (OpEx)** — on ne paie que ce qu'on consomme.
2. **Profiter d'économies d'échelle massives** — AWS achète en masse, les prix baissent pour tous.
3. **Arrêter de deviner la capacité** — on monte ou descend selon le besoin réel.
4. **Augmenter la vitesse et l'agilité** — nouvelles ressources en minutes.
5. **Arrêter de dépenser de l'argent pour faire tourner des data centers** — se concentrer sur ses clients.
6. **Devenir mondial en quelques minutes** — déployer dans plusieurs régions facilement.

### 1.3 Termes clés
| Terme | Signification |
|---|---|
| **Élasticité** | Ajuster automatiquement les ressources à la demande (augmenter ET diminuer) |
| **Scalabilité** | Capacité à grandir pour absorber plus de charge (verticale = plus gros serveur ; horizontale = plus de serveurs) |
| **Haute disponibilité** | Le système reste accessible (ex. multi-AZ) |
| **Tolérance aux pannes** | Le système continue de fonctionner malgré la panne d'un composant |
| **Agilité** | Rapidité d'expérimentation et de mise sur le marché |
| **Résilience / Fiabilité** | Capacité à se remettre d'une panne |

### 1.4 Modèles de service
| Modèle | Vous gérez | Exemples AWS |
|---|---|---|
| **IaaS** (Infrastructure) | OS, applications, données | EC2, VPC, EBS |
| **PaaS** (Plateforme) | Application et données | Elastic Beanstalk, RDS, Lambda (souvent classé serverless) |
| **SaaS** (Logiciel) | Uniquement l'usage | Amazon WorkMail, Amazon Chime, Gmail |

### 1.5 Modèles de déploiement
- **Cloud public** : tout sur AWS.
- **Sur site (on-premises / cloud privé)** : dans votre propre data center (ex. avec virtualisation).
- **Hybride** : connexion entre on-premises et cloud (ex. Direct Connect, VPN, Storage Gateway, Outposts).

### 1.6 Infrastructure mondiale AWS
- **Région** : zone géographique contenant **au minimum 3 AZ** (ex. eu-west-3 Paris). Les données **ne quittent pas une région** sans votre action.
- **Zone de disponibilité (AZ)** : un ou plusieurs data centers séparés, avec alimentation, réseau et refroidissement redondants, reliés par des liens à très faible latence.
- **Points de présence (Edge Locations)** : utilisés par **CloudFront**, **Route 53**, **Global Accelerator**, **Shield**, **WAF** pour rapprocher le contenu des utilisateurs.
- **Regional Edge Caches** : cache intermédiaire de CloudFront.
- **Local Zones** : extension d'une région près d'une grande ville (latence < 10 ms).
- **Wavelength Zones** : calcul AWS à l'intérieur des réseaux **5G** des opérateurs télécom.
- **AWS Outposts** : racks AWS installés **dans votre data center** (hybride).

**Choisir une Région — 4 critères :**
1. **Conformité / réglementation** (souveraineté des données — souvent le critère n°1)
2. **Latence / proximité des clients**
3. **Disponibilité des services** (tous les services ne sont pas dans toutes les régions)
4. **Prix** (varie selon la région)

**Services globaux** (pas liés à une région) : IAM, Route 53, CloudFront, WAF (pour CloudFront), AWS Organizations.

### 1.7 AWS Well-Architected Framework — 6 piliers
| Pilier | Idée clé |
|---|---|
| **Excellence opérationnelle** | Exécuter et surveiller les systèmes, automatiser, infrastructure as code, petites modifications fréquentes et réversibles |
| **Sécurité** | Protéger données et systèmes, moindre privilège, traçabilité, chiffrement, sécurité à toutes les couches |
| **Fiabilité** | Récupérer des pannes, scaler horizontalement, tester les procédures de reprise, arrêter de deviner la capacité |
| **Efficacité des performances** | Utiliser les ressources efficacement, démocratiser les technologies avancées, devenir mondial en minutes, serverless |
| **Optimisation des coûts** | Éviter les dépenses inutiles, modèle de consommation, mesurer l'efficacité |
| **Durabilité** | Minimiser l'impact environnemental, maximiser l'utilisation, services managés |

Outil : **AWS Well-Architected Tool** (dans la console, gratuit) pour évaluer ses charges de travail.

**Principes de conception à retenir :** concevoir pour la panne (*design for failure*), découpler les composants (SQS, SNS), utiliser l'élasticité, penser parallèle, éviter les points de défaillance uniques.

### 1.8 AWS Cloud Adoption Framework (CAF) — 6 perspectives
- **Business**, **Personnes (People)**, **Gouvernance** → capacités *métier*
- **Plateforme**, **Sécurité**, **Opérations** → capacités *techniques*

Bénéfices attendus : réduction des risques métier, amélioration ESG, augmentation des revenus, efficacité opérationnelle.
Phases de transformation : **Envisager → Aligner → Lancer → Scaler** (Envision, Align, Launch, Scale).

### 1.9 Stratégies de migration — les 7 R
| Stratégie | Description |
|---|---|
| **Retire** (Retirer) | Supprimer ce qui ne sert plus |
| **Retain** (Conserver) | Garder sur site pour l'instant |
| **Rehost** (« lift and shift ») | Déplacer tel quel sur EC2 |
| **Relocate** | Déplacer vers AWS sans modification (ex. VMware Cloud on AWS) |
| **Replatform** (« lift, tinker and shift ») | Petites optimisations (ex. passer sa base sur RDS) |
| **Repurchase** (« drop and shop ») | Passer à un SaaS (ex. CRM → Salesforce) |
| **Refactor / Re-architect** | Réécrire en cloud natif (serverless, microservices) |

**Outils de migration :** AWS Migration Hub, AWS Application Migration Service (MGN, rehost), AWS Database Migration Service (DMS), AWS Schema Conversion Tool (SCT), AWS Application Discovery Service, AWS DataSync, famille AWS Snow.

### 1.10 Économie du cloud
- **Coûts fixes vs variables**, **CapEx vs OpEx**.
- **TCO (Total Cost of Ownership)** : inclut matériel, électricité, refroidissement, locaux, personnel, licences…
- **Économies sur le personnel** : moins d'administration matérielle.
- **Licences** : *BYOL* (Bring Your Own License) vs licences incluses.
- **Right-sizing** : dimensionner correctement les ressources.
- **Automatisation** (CloudFormation) = réduction des coûts opérationnels.
- **Services managés** (RDS, ECS, EFS…) = moins de travail d'administration.

---

## DOMAINE 2 — Sécurité et conformité (30 %)

### 2.1 Modèle de responsabilité partagée (TRÈS IMPORTANT)
- **AWS = sécurité DU cloud** : matériel, data centers physiques, réseau global, hyperviseur, infrastructure des Régions/AZ/Edge, logiciel des services managés.
- **Client = sécurité DANS le cloud** : données, IAM (utilisateurs/permissions), OS invité sur EC2 (patchs), applications, configuration des security groups, chiffrement côté client/serveur, configuration du réseau.

**Contrôles partagés :** gestion des correctifs (AWS patche l'infra, vous patchez votre OS/apps), gestion de la configuration, sensibilisation et formation.
**Contrôles hérités :** physiques et environnementaux (100 % AWS).

| Service | Responsabilité du client |
|---|---|
| EC2 (IaaS) | OS, patchs, pare-feu (SG), applis, données |
| RDS | Données, accès, security groups, chiffrement — AWS patche le moteur et l'OS |
| Lambda | Code, permissions IAM — AWS gère tout le reste |
| S3 | Données, politiques de bucket, chiffrement, accès public |

### 2.2 IAM (Identity and Access Management) — service global, gratuit
- **Utilisateur root** : créé avec le compte. **Activer MFA**, ne pas l'utiliser au quotidien, ne pas créer de clés d'accès pour lui.
  - Tâches **réservées au root** : changer les paramètres du compte (email, nom, mot de passe root), fermer le compte, changer le plan de support, restaurer les permissions IAM, s'inscrire comme vendeur sur la marketplace de Reserved Instances, configurer MFA Delete sur S3, certaines tâches de facturation.
- **Utilisateurs IAM** : une personne ou application. 
- **Groupes IAM** : ensemble d'utilisateurs (pas de groupes imbriqués).
- **Rôles IAM** : identités temporaires assumées par des services AWS (ex. EC2 accédant à S3), des utilisateurs d'autres comptes, ou des identités fédérées. **Bonne pratique : rôle plutôt que clés d'accès sur EC2.**
- **Politiques (Policies)** : documents JSON (Effect, Action, Resource, Condition). Un **Deny explicite** l'emporte toujours.
- **Principe du moindre privilège** : n'accorder que les permissions nécessaires.
- **MFA** : authentification multifacteur.
- **Politique de mot de passe** configurable.
- **IAM Access Analyzer** : identifie les ressources partagées avec l'extérieur.
- **IAM Credential Report** (niveau compte) / **Access Advisor** (niveau utilisateur, services utilisés).
- **AWS IAM Identity Center** (ex-AWS SSO) : authentification unique pour plusieurs comptes AWS et applications.
- **AWS STS** : identifiants temporaires.
- **Amazon Cognito** : identités pour les **utilisateurs de vos applications web/mobiles** (inscription, connexion, fédération Google/Facebook).
- **AWS Directory Service** : Microsoft Active Directory managé.

### 2.3 Gouvernance multi-comptes
- **AWS Organizations** : gestion centralisée de plusieurs comptes, **facturation consolidée** (une facture, remises sur volume cumulées), **SCP** (Service Control Policies) qui limitent les permissions maximales des comptes membres (ne s'appliquent pas au compte de gestion).
- **Unités organisationnelles (OU)** : regroupement de comptes.
- **AWS Control Tower** : mise en place automatisée d'un environnement multi-comptes sécurisé (*landing zone*) avec des garde-fous (guardrails).
- **AWS RAM (Resource Access Manager)** : partager des ressources entre comptes.
- **AWS Service Catalog** : catalogue de produits approuvés (modèles CloudFormation) que les utilisateurs peuvent déployer.

### 2.4 Protection réseau et applicative
| Service | Rôle |
|---|---|
| **Security Group** | Pare-feu **au niveau de l'instance**, **stateful**, règles **Allow uniquement** |
| **Network ACL (NACL)** | Pare-feu **au niveau du sous-réseau**, **stateless**, règles Allow **et Deny** |
| **AWS WAF** | Pare-feu applicatif web (couche 7) : injection SQL, XSS, filtrage IP/pays, rate limiting. Sur CloudFront, ALB, API Gateway, AppSync |
| **AWS Shield Standard** | Protection DDoS **gratuite** et automatique (couches 3/4) pour tous |
| **AWS Shield Advanced** | DDoS avancé, payant (~3000 $/mois), équipe **SRT** (Shield Response Team) 24/7, protection des coûts liés aux pics DDoS |
| **AWS Firewall Manager** | Gestion centralisée des règles WAF/Shield/SG dans une organisation |
| **AWS Network Firewall** | Pare-feu managé pour le VPC |

### 2.5 Détection, surveillance et audit
| Service | Rôle — mot-clé examen |
|---|---|
| **Amazon GuardDuty** | **Détection de menaces** intelligente (ML) à partir des logs CloudTrail, VPC Flow Logs, DNS |
| **Amazon Inspector** | **Analyse de vulnérabilités** automatisée (EC2, images de conteneurs ECR, Lambda) |
| **Amazon Macie** | Découverte de **données sensibles (PII)** dans **S3** via ML |
| **Amazon Detective** | **Enquête** sur la cause racine des incidents de sécurité |
| **AWS Security Hub** | **Vue centralisée** des alertes de sécurité et contrôles de conformité |
| **AWS CloudTrail** | **Audit des appels API** : qui a fait quoi, quand, d'où |
| **AWS Config** | **Historique de configuration** des ressources et **conformité** aux règles |
| **Amazon CloudWatch** | **Métriques, logs, alarmes** (performance) |
| **AWS Audit Manager** | Collecte automatisée de preuves pour les audits |
| **AWS Artifact** | **Rapports de conformité AWS** (SOC, ISO, PCI) et accords (BAA HIPAA) à la demande |
| **AWS Trusted Advisor** | Recommandations (dont sécurité) |
| **AWS Health Dashboard** | État des services AWS et événements affectant **votre** compte |

### 2.6 Chiffrement et secrets
- **Chiffrement au repos** (stockage) et **en transit** (TLS/SSL).
- **AWS KMS** : création et gestion des **clés de chiffrement** (intégré à S3, EBS, RDS…). Matériel partagé, multi-locataire.
- **AWS CloudHSM** : **HSM dédié** (matériel physique dédié, FIPS 140-2 niveau 3) — vous gérez les clés.
- **AWS Secrets Manager** : stockage et **rotation automatique** des secrets (mots de passe de bases de données, clés API).
- **AWS Systems Manager Parameter Store** : stockage de paramètres/configuration (rotation non automatique).
- **AWS Certificate Manager (ACM)** : certificats SSL/TLS gratuits et renouvellement automatique.

### 2.7 Conformité
- **AWS Artifact** → rapports de conformité.
- **AWS Compliance Center / Compliance Programs** → informations par pays et secteur.
- **Tests d'intrusion** : autorisés sans approbation préalable sur 8 services courants (EC2, RDS, Aurora, CloudFront, API Gateway, Lambda, Lightsail, Elastic Beanstalk…) ; interdits : DoS/DDoS, flood, attaques sur l'infra AWS.
- **AWS Abuse team** : signaler une utilisation abusive de ressources AWS (spam, attaques).

### 2.8 Ressources de sécurité
AWS Knowledge Center, AWS Security Center, AWS Security Blog, AWS Marketplace (solutions de sécurité tierces), AWS Prescriptive Guidance.

---

## DOMAINE 3 — Technologie et services cloud (34 %)

### 3.1 Méthodes d'accès et de déploiement
- **AWS Management Console** (web), **AWS CLI** (ligne de commande), **SDK** (code), **AWS CloudShell** (terminal dans le navigateur).
- **Infrastructure as Code (IaC)** : **AWS CloudFormation** (modèles JSON/YAML → *stacks*), **AWS CDK** (IaC avec langages de programmation).
- **AWS Elastic Beanstalk** : PaaS — vous fournissez le code, AWS déploie (capacité, load balancing, scaling, monitoring).
- Options de connectivité : **Internet public**, **AWS Site-to-Site VPN** (chiffré via Internet, rapide à mettre en place), **AWS Direct Connect** (**connexion privée dédiée**, bande passante constante, ne passe pas par Internet, plusieurs semaines de mise en place), **AWS Client VPN**.

### 3.2 Calcul (Compute)
**Amazon EC2** — serveurs virtuels.
- **Familles d'instances** : Usage général (t, m), Optimisé calcul (c), Optimisé mémoire (r, x), Calcul accéléré (p, g – GPU), Optimisé stockage (i, d).
- **AMI** : image de la machine.
- **User data** : script exécuté au démarrage.
- **Stockage** : EBS (persistant) ou Instance Store (éphémère, perdu à l'arrêt).

**Options d'achat EC2 (très fréquent à l'examen) :**
| Option | Cas d'usage | Remise max. |
|---|---|---|
| **À la demande (On-Demand)** | Court terme, imprévisible, sans engagement, ne doit pas être interrompu | 0 % |
| **Instances réservées (RI)** | Charge stable 1 ou 3 ans (ex. base de données) — Standard (jusqu'à 72 %) / Convertible (jusqu'à 66 %, peut changer de famille) | 72 % |
| **Savings Plans** | Engagement en **$/heure** sur 1 ou 3 ans — *Compute SP* (EC2, Fargate, Lambda, toutes régions, jusqu'à 66 %) / *EC2 Instance SP* (jusqu'à 72 %) | 72 % |
| **Instances Spot** | Capacité inutilisée, **peut être interrompue** (préavis 2 min) — batch, big data, tâches tolérantes aux pannes | **90 %** |
| **Hôtes dédiés (Dedicated Hosts)** | Serveur physique entier pour vous — **licences liées au serveur (BYOL par socket/cœur)**, conformité | — (le plus cher) |
| **Instances dédiées** | Matériel non partagé avec d'autres clients, mais pas de contrôle sur le placement | — |
| **Réservations de capacité (On-Demand Capacity Reservations)** | Garantir une capacité dans une AZ, sans engagement de durée | 0 % |

**Mise à l'échelle et répartition :**
- **Amazon EC2 Auto Scaling** : ajoute/supprime des instances selon la demande (min, souhaité, max) → élasticité + disponibilité.
- **Elastic Load Balancing (ELB)** : répartit le trafic. *ALB* (HTTP/HTTPS, couche 7), *NLB* (TCP/UDP, couche 4, ultra-performant), *GWLB* (appliances réseau), CLB (ancien).

**Conteneurs :**
- **Amazon ECS** (orchestration AWS), **Amazon EKS** (Kubernetes managé), **AWS Fargate** (exécution **serverless** des conteneurs pour ECS/EKS — pas de serveurs à gérer), **Amazon ECR** (registre d'images Docker).

**Serverless :**
- **AWS Lambda** : exécute du code en réponse à des événements, **max 15 minutes**, facturé à la requête et à la durée (ms). Pas de serveur à gérer.

**Autres :**
- **Amazon Lightsail** : VPS simple à prix fixe (sites web, WordPress, débutants).
- **AWS Batch** : traitements par lots à grande échelle.
- **AWS App Runner** : déployer facilement des applications web conteneurisées.
- **AWS Outposts**, **Local Zones**, **Wavelength** (voir domaine 1).

### 3.3 Stockage
**Amazon S3 (stockage d'objets)**
- Objets dans des **buckets** (nom globalement unique, mais bucket créé dans une région). Objet max **5 To**.
- Durabilité **99,999999999 % (11 neuf)**.
- Usages : sauvegardes, data lake, **hébergement de site web statique**, médias.
- Fonctionnalités : **versioning**, **règles de cycle de vie** (passer automatiquement vers une classe moins chère), **réplication** (CRR inter-régions / SRR même région), **S3 Transfer Acceleration**, **chiffrement** (activé par défaut, SSE-S3), **Block Public Access**, **politiques de bucket**, **S3 Object Lock** (WORM), **MFA Delete**, presigned URLs.

| Classe S3 | Usage |
|---|---|
| **S3 Standard** | Données fréquemment accédées |
| **S3 Intelligent-Tiering** | Accès **inconnu ou changeant** — déplacement automatique entre niveaux |
| **S3 Standard-IA** | Accès peu fréquent, récupération rapide, multi-AZ |
| **S3 One Zone-IA** | Accès peu fréquent, **une seule AZ** (données recréables) |
| **S3 Glacier Instant Retrieval** | Archives consultées ~1 fois/trimestre, récupération en ms |
| **S3 Glacier Flexible Retrieval** | Archives, récupération de minutes à 12 h |
| **S3 Glacier Deep Archive** | **Le moins cher**, conservation longue (7–10 ans), récupération 12–48 h |
| **S3 Express One Zone** | Très haute performance, latence de l'ordre de la ms, une AZ |

**Stockage bloc et fichiers**
| Service | Type | Points clés |
|---|---|---|
| **Amazon EBS** | Bloc | Disque réseau pour **une** instance EC2, **lié à une AZ**, persistant, snapshots (stockés dans S3) |
| **Instance Store** | Bloc | Disque physique de l'hôte, **éphémère**, très performant |
| **Amazon EFS** | Fichiers (NFS) | **Linux**, partagé entre **des milliers d'instances**, multi-AZ, élastique |
| **Amazon FSx for Windows File Server** | Fichiers (SMB) | Partage de fichiers **Windows**, Active Directory |
| **Amazon FSx for Lustre** | Fichiers | **Calcul haute performance (HPC)**, ML |
| FSx for NetApp ONTAP / OpenZFS | Fichiers | Migration de NAS existants |

**Hybride, transfert et sauvegarde**
- **AWS Storage Gateway** : relie le stockage sur site à AWS (File Gateway, Volume Gateway, Tape Gateway).
- **AWS DataSync** : transfert de données en ligne automatisé entre on-premises et AWS.
- **Famille AWS Snow** (transfert hors ligne de grands volumes et edge computing) : **Snowball Edge** (Storage Optimized / Compute Optimized). *(Snowcone et Snowmobile ont été retirés, mais peuvent encore apparaître dans des questions.)* Règle : si le transfert réseau prendrait plus d'une semaine → Snow.
- **AWS Transfer Family** : SFTP/FTPS/FTP vers S3/EFS.
- **AWS Backup** : sauvegarde centralisée et automatisée de plusieurs services.
- **AWS Elastic Disaster Recovery** : reprise après sinistre.

### 3.4 Bases de données
| Service | Type | Mot-clé examen |
|---|---|---|
| **Amazon RDS** | Relationnel (SQL) managé | MySQL, PostgreSQL, MariaDB, Oracle, SQL Server, Db2. **Multi-AZ** (haute dispo), **Read Replicas** (performance lecture) |
| **Amazon Aurora** | Relationnel compatible MySQL/PostgreSQL | **5x plus rapide que MySQL**, 3x PostgreSQL, 6 copies sur 3 AZ, Aurora Serverless |
| **Amazon DynamoDB** | NoSQL clé-valeur | **Serverless**, latence en **millisecondes à un chiffre**, scale massif ; **DAX** = cache en microsecondes ; Global Tables |
| **Amazon ElastiCache** | Cache en mémoire | Redis/Valkey/Memcached — réduire la charge des bases |
| **Amazon MemoryDB** | Base en mémoire durable compatible Redis | |
| **Amazon Redshift** | **Entrepôt de données** (data warehouse) | Analytique **OLAP**, colonnes, pétaoctets, BI |
| **Amazon DocumentDB** | Documents | Compatible **MongoDB** |
| **Amazon Neptune** | **Graphe** | Réseaux sociaux, recommandations, détection de fraude |
| **Amazon Keyspaces** | Colonnes larges | Compatible **Apache Cassandra** |
| **Amazon Timestream** | Séries temporelles | IoT, métriques |
| **Amazon QLDB** | Registre immuable | *(fin de support 2025, peut encore apparaître)* |

Bon à savoir : sur RDS, impossible d'accéder à l'OS (sauf RDS Custom) ; si on a besoin du contrôle total → base installée sur **EC2**.
**Migration** : **AWS DMS** (migration avec un minimum d'interruption, base source reste opérationnelle) + **AWS SCT** (conversion de schéma entre moteurs différents, ex. Oracle → Aurora).

### 3.5 Réseau
- **Amazon VPC** : réseau privé virtuel isolé logiquement.
  - **Sous-réseau public** (route vers une **Internet Gateway**) / **privé**.
  - **NAT Gateway** : permet aux instances privées d'**accéder** à Internet sans être accessibles depuis Internet.
  - **Internet Gateway** : connecte le VPC à Internet.
  - **Security Groups / NACL** (voir domaine 2).
  - **VPC Flow Logs** : journal du trafic IP.
  - **VPC Peering** : connecter deux VPC (non transitif).
  - **AWS Transit Gateway** : hub central pour connecter **de nombreux VPC** et réseaux sur site.
  - **VPC Endpoints / AWS PrivateLink** : accéder aux services AWS (S3, DynamoDB…) **sans passer par Internet**.
- **Amazon Route 53** : **DNS** managé, enregistrement de domaines, contrôles de santé, politiques de routage (simple, pondéré, latence, basculement/failover, géolocalisation, géoproximité, multivaleur).
- **Amazon CloudFront** : **CDN** — met en cache le contenu dans les edge locations (latence réduite), intégré avec Shield et WAF.
- **AWS Global Accelerator** : améliore les performances en utilisant le **réseau mondial AWS** (IP anycast statiques), pour TCP/UDP non HTTP aussi.
- **Amazon API Gateway** : créer, publier et sécuriser des **API** (souvent avec Lambda).

### 3.6 Intégration d'applications
| Service | Rôle |
|---|---|
| **Amazon SQS** | **File d'attente** de messages — **découplage** des composants (pull) |
| **Amazon SNS** | **Publication/abonnement (pub/sub)** — notifications push (email, SMS, Lambda, SQS) |
| **Amazon EventBridge** | Bus d'événements, règles, planification (ex-CloudWatch Events) |
| **AWS Step Functions** | Orchestration de **workflows** (machines à états) |
| **Amazon MQ** | Broker de messages managé (ActiveMQ, RabbitMQ) pour migrer l'existant |
| **Amazon SES** | Envoi d'**e-mails** marketing/transactionnels |
| **Amazon Connect** | **Centre de contact** (call center) cloud |

### 3.7 Analytique
| Service | Rôle |
|---|---|
| **Amazon Athena** | Requêtes **SQL serverless directement sur S3** |
| **Amazon EMR** | Big data (Hadoop, Spark) managé |
| **AWS Glue** | **ETL** serverless + Data Catalog |
| **Amazon Kinesis** | Données en **temps réel / streaming** (Data Streams, Data Firehose, Video Streams) |
| **Amazon MSK** | Apache Kafka managé |
| **Amazon QuickSight** | **Tableaux de bord / BI** |
| **Amazon OpenSearch Service** | Recherche et analyse de logs (ex-Elasticsearch) |
| **AWS Lake Formation** | Construire un data lake sécurisé |
| **AWS Data Exchange** | Trouver et s'abonner à des données tierces |

### 3.8 Intelligence artificielle et Machine Learning
| Service | Rôle |
|---|---|
| **Amazon SageMaker AI** | Construire, entraîner et déployer des modèles ML |
| **Amazon Bedrock** | **IA générative** via modèles de fondation (API) |
| **Amazon Q** | Assistant IA générative (Q Business, Q Developer) |
| **Amazon Rekognition** | Analyse d'**images et vidéos** (visages, objets) |
| **Amazon Comprehend** | **Analyse de texte** (NLP, sentiments, entités) |
| **Amazon Translate** | **Traduction** |
| **Amazon Transcribe** | **Voix → texte** |
| **Amazon Polly** | **Texte → voix** |
| **Amazon Lex** | **Chatbots** (technologie d'Alexa) |
| **Amazon Textract** | Extraire texte et données de **documents scannés** |
| **Amazon Kendra** | **Recherche intelligente** dans des documents d'entreprise |
| **Amazon Personalize** | **Recommandations** personnalisées |
| **Amazon Forecast** | Prévisions de séries temporelles |
| **Amazon Fraud Detector** | Détection de fraude en ligne |

### 3.9 Gestion, surveillance et gouvernance
| Service | Rôle |
|---|---|
| **Amazon CloudWatch** | Métriques, **alarmes**, logs, tableaux de bord |
| **AWS CloudTrail** | Historique des appels API (audit) |
| **AWS Config** | Inventaire et conformité de configuration |
| **AWS Systems Manager** | Gestion opérationnelle d'un parc (patchs, Run Command, **Session Manager** = connexion sans SSH, Parameter Store) |
| **AWS Trusted Advisor** | Recommandations de bonnes pratiques |
| **AWS Compute Optimizer** | Recommandations de **dimensionnement** (EC2, EBS, Lambda) via ML |
| **AWS Health Dashboard** | Santé des services AWS et de vos ressources |
| **AWS License Manager** | Gestion des licences logicielles |
| **AWS X-Ray** | **Traçage/débogage** des applications distribuées |
| **AWS Launch Wizard**, **AWS Proton** | Déploiements guidés |

### 3.10 Outils pour développeurs
**AWS CodePipeline** (CI/CD), **AWS CodeBuild** (compile et teste), **AWS CodeDeploy** (déploie sur EC2, Lambda, on-premises), **AWS CodeCommit** (dépôt Git), **AWS CodeArtifact** (dépôt de paquets), **AWS Cloud9** (IDE cloud), **AWS X-Ray**, **AWS AppConfig**, **Amazon CodeGuru** (revue de code ML).

### 3.11 Autres services à connaître
- **Amazon WorkSpaces** : **bureaux virtuels** (VDI). **Amazon AppStream 2.0** : streaming d'applications.
- **AWS IoT Core** : connecter des objets connectés.
- **AWS Amplify** : développer des applications web/mobiles full-stack.
- **AWS AppSync** : API GraphQL.
- **AWS Device Farm** : tester des applis sur de vrais appareils mobiles.
- **AWS Ground Station** : contrôle de satellites.
- **Amazon Managed Blockchain**.

---

## DOMAINE 4 — Facturation, tarification et support (12 %)

### 4.1 Principes de tarification
1. **Payez à l'usage** (pay-as-you-go)
2. **Payez moins en réservant** (RI, Savings Plans)
3. **Payez moins par unité en consommant plus** (remises sur volume, ex. S3)
4. **Payez moins à mesure qu'AWS grandit**

**Facteurs de coût fondamentaux :** **calcul**, **stockage**, **transfert de données sortant**.
- Transfert de données **entrant** (vers AWS) : **gratuit**.
- Transfert **sortant** vers Internet : **payant**.
- Transfert entre régions : payant. Entre AZ : généralement payant (faible).
- **Gratuits** : IAM, VPC (hors NAT Gateway, etc.), CloudFormation, Elastic Beanstalk, Auto Scaling, Organizations, facturation consolidée (vous payez les ressources créées).

### 4.2 Offre gratuite (Free Tier)
- **Toujours gratuit** (ex. 1 million de requêtes Lambda/mois, 25 Go DynamoDB).
- **12 mois gratuits** pour les comptes créés avant le 15 juillet 2025 (ex. 750 h/mois d'EC2 t2/t3.micro, 5 Go S3).
- **Essais** de courte durée.
- *Depuis juillet 2025, les nouveaux comptes reçoivent des **crédits** (jusqu'à 200 $) avec un plan gratuit de 6 mois.*

### 4.3 Outils de gestion des coûts
| Outil | Usage — mot-clé examen |
|---|---|
| **AWS Pricing Calculator** | **Estimer le coût** d'une architecture **avant** de la déployer |
| **AWS Billing Dashboard** | Vue d'ensemble de la facture |
| **AWS Cost Explorer** | **Visualiser et analyser** les coûts **passés**, **prévisions** jusqu'à 12 mois, recommandations RI/SP |
| **AWS Budgets** | Définir des **budgets** et recevoir des **alertes** (coût, usage, RI, SP), actions automatiques |
| **AWS Cost and Usage Report (CUR) / Data Exports** | Rapport **le plus détaillé** (heure par heure), exporté vers S3, analysable avec Athena/QuickSight |
| **AWS Cost Anomaly Detection** | Détection d'**anomalies** de dépenses par ML |
| **Balises de répartition des coûts (cost allocation tags)** | Attribuer les coûts par projet/équipe/département |
| **AWS Billing Conductor** | Facturation personnalisée (refacturation, revendeurs) |
| **Facturation consolidée (Organizations)** | Une seule facture, **remises sur volume partagées**, partage des RI/SP |
| **AWS Compute Optimizer** / **Trusted Advisor** | Recommandations d'optimisation |

### 4.4 Plans de support AWS
| Plan | Prix | Points clés |
|---|---|---|
| **Basic** | Gratuit | Service client, documentation, forums (re:Post), Health Dashboard, **checks Trusted Advisor de base** (sécurité principaux + quotas) |
| **Developer** | À partir de 29 $/mois | Accès **par e-mail** aux Cloud Support Associates **pendant les heures ouvrables** ; Général < 24 h ouvrables ; Système altéré < 12 h ouvrables |
| **Business** | À partir de 100 $/mois | **24/7** téléphone, chat, e-mail ; **tous les checks Trusted Advisor** ; API AWS Support ; Système de production altéré < 4 h ; **Production en panne < 1 h** |
| **Enterprise On-Ramp** | À partir de 5 500 $/mois | **Pool de TAM** (Technical Account Managers), Concierge ; **Système critique en panne < 30 min** |
| **Enterprise** | À partir de 15 000 $/mois | **TAM désigné**, **Concierge Support Team** (facturation/compte), **Infrastructure Event Management**, Well-Architected Reviews ; **Système critique en panne < 15 min** |

Astuces examen :
- « Réponse en moins de **15 minutes** » → **Enterprise**.
- « **TAM désigné/dédié** » → **Enterprise**.
- « Accès complet à **Trusted Advisor** » le moins cher → **Business**.
- « Support 24/7 par téléphone » le moins cher → **Business**.
- « Uniquement e-mail, test/dev » → **Developer**.

### 4.5 AWS Trusted Advisor — 6 catégories
**Optimisation des coûts**, **Performance**, **Sécurité**, **Tolérance aux pannes**, **Quotas de service (limites)**, **Excellence opérationnelle**.
Exemples : instances EC2 sous-utilisées, buckets S3 publics, MFA root non activé, ports ouverts dans les SG, snapshots EBS manquants, quotas proches de la limite.

### 4.6 Autres ressources d'aide
| Ressource | Usage |
|---|---|
| **AWS re:Post** | Forum communautaire de Q/R (remplace les forums AWS) |
| **AWS Knowledge Center** | Réponses aux questions fréquentes |
| **AWS Documentation / Whitepapers** | Documentation officielle |
| **AWS Prescriptive Guidance** | Guides et modèles éprouvés |
| **AWS Professional Services** | Équipe d'experts AWS pour vous accompagner |
| **AWS Partner Network (APN)** | Partenaires conseil (consulting) et technologiques (ISV) certifiés |
| **AWS Marketplace** | Catalogue de **logiciels tiers** (AMI, SaaS) à acheter/déployer |
| **AWS IQ** | Trouver des **experts freelances** certifiés AWS *(service fermé en 2025, mais encore possible à l'examen)* |
| **AWS Training and Certification / Skill Builder** | Formation |
| **AWS Activate** | Crédits et ressources pour **startups** |
| **AWS Solutions Architects** | Conseils techniques |
| **AWS Managed Services (AMS)** | AWS opère votre infrastructure pour vous |
| **AWS Trust & Safety (Abuse)** | Signaler un abus |
| **AWS Service Quotas** | Consulter et demander l'augmentation des limites |

---

## Récapitulatif : « Quel service pour quel besoin ? »

| Besoin | Service |
|---|---|
| Qui a supprimé ma ressource ? | **CloudTrail** |
| Alarme quand CPU > 80 % | **CloudWatch** |
| Ma ressource est-elle conforme ? Historique de config | **AWS Config** |
| Rapports SOC/ISO/PCI d'AWS | **AWS Artifact** |
| Détecter un comportement malveillant | **GuardDuty** |
| Scanner les vulnérabilités EC2 | **Inspector** |
| Trouver des données personnelles dans S3 | **Macie** |
| Protection DDoS gratuite | **Shield Standard** |
| Bloquer injection SQL / XSS | **WAF** |
| Estimer un coût futur | **Pricing Calculator** |
| Analyser les coûts passés | **Cost Explorer** |
| Alerte si dépassement de budget | **AWS Budgets** |
| Contenu statique rapide dans le monde | **CloudFront** |
| DNS | **Route 53** |
| Connexion privée dédiée au data center | **Direct Connect** |
| Connexion chiffrée rapide via Internet | **Site-to-Site VPN** |
| Exécuter du code sans serveur | **Lambda** |
| Conteneurs sans gérer de serveurs | **Fargate** |
| Déployer une appli web sans gérer l'infra | **Elastic Beanstalk** |
| Infrastructure as code | **CloudFormation** |
| Découpler des composants | **SQS** |
| Envoyer des notifications | **SNS** |
| Base relationnelle managée | **RDS / Aurora** |
| NoSQL serverless faible latence | **DynamoDB** |
| Entrepôt de données | **Redshift** |
| SQL sur des fichiers S3 | **Athena** |
| Transférer des pétaoctets hors ligne | **Snowball Edge** |
| Stockage partagé Linux | **EFS** |
| Stockage partagé Windows | **FSx for Windows** |
| Archivage le moins cher | **S3 Glacier Deep Archive** |
| Logiciels tiers prêts à l'emploi | **AWS Marketplace** |
| Gérer plusieurs comptes et une facture unique | **AWS Organizations** |
| Rotation automatique de mots de passe de base | **Secrets Manager** |
| Gérer les clés de chiffrement | **KMS** (dédié : **CloudHSM**) |
| Connexion des utilisateurs d'une appli mobile | **Cognito** |
| Single sign-on multi-comptes | **IAM Identity Center** |
