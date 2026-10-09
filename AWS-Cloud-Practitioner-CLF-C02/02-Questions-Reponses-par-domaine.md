# CLF-C02 — Questions / Réponses pratiques par domaine

> **Comment utiliser ce fichier :** ouvrez de préférence la version **`02-Questions-Reponses-interactif.html`** :
> les réponses y sont masquées et ne s'affichent qu'après avoir choisi (ou écrit) votre réponse.
> Répondez d'abord, puis lisez l'explication — **l'explication est aussi importante que la réponse**.
> Les questions sont au format de l'examen réel (scénarios, « Lequel… », « Quels sont les DEUX… »).

---

# DOMAINE 1 — Concepts du cloud (24 %)

**Q1.** Une entreprise souhaite éviter d'acheter des serveurs à l'avance et ne payer que les ressources qu'elle consomme. Quel avantage du cloud AWS cela décrit-il ?
- A. Profiter d'économies d'échelle massives
- B. Remplacer les dépenses d'investissement par des dépenses variables
- C. Devenir mondial en quelques minutes
- D. Augmenter la vitesse et l'agilité

> ✅ **Réponse : B** — Passer du CapEx (achat initial) à l'OpEx (paiement à l'usage) = « trade capital expense for variable expense ».

**Q2.** Quel avantage du cloud permet à une entreprise de réduire ses coûts grâce au fait qu'AWS regroupe l'usage de centaines de milliers de clients ?
- A. Élasticité
- B. Économies d'échelle massives
- C. Haute disponibilité
- D. Agilité

> ✅ **Réponse : B** — L'agrégation de l'usage permet à AWS d'obtenir des prix plus bas, répercutés sur les clients.

**Q3.** Un site e-commerce connaît des pics de trafic pendant les soldes. Il souhaite ajouter automatiquement des serveurs pendant les pics et les retirer ensuite. Quel concept cela illustre-t-il ?
- A. Tolérance aux pannes
- B. Élasticité
- C. Durabilité
- D. Haute disponibilité

> ✅ **Réponse : B** — L'élasticité = ajuster automatiquement les ressources à la demande, à la hausse ET à la baisse (via EC2 Auto Scaling).

**Q4.** Quelle est la différence entre la scalabilité verticale et horizontale ?
> ✅ **Réponse :** La scalabilité **verticale** consiste à augmenter la taille d'une ressource (ex. passer d'une t3.medium à une m5.2xlarge). La scalabilité **horizontale** consiste à ajouter plus de ressources (ex. passer de 2 à 10 instances derrière un Load Balancer). AWS recommande la scalabilité horizontale (pas de point de défaillance unique).

**Q5.** Une zone de disponibilité (AZ) est :
- A. Un emplacement de cache pour CloudFront
- B. Une zone géographique contenant plusieurs Régions
- C. Un ou plusieurs data centers distincts dotés d'une alimentation, d'un réseau et d'une connectivité redondants au sein d'une Région
- D. Un data center situé dans les locaux du client

> ✅ **Réponse : C** — A = Edge Location ; D = Outposts.

**Q6.** Combien de zones de disponibilité une Région AWS comporte-t-elle au minimum ?
- A. 1  - B. 2  - C. 3  - D. 6

> ✅ **Réponse : C** — Toute nouvelle Région AWS compte au minimum 3 AZ.

**Q7.** Quels sont les DEUX facteurs les plus importants pour choisir une Région AWS ? (Choisissez-en deux.)
- A. Exigences de conformité et de souveraineté des données
- B. Le nombre d'Edge Locations dans le pays
- C. La proximité avec les clients (latence)
- D. Le fuseau horaire du support AWS
- E. Le nombre de comptes IAM

> ✅ **Réponses : A et C** — Les 4 critères sont : conformité, latence, disponibilité des services, prix.

**Q8.** Comment concevoir une application hautement disponible sur AWS ?
- A. Déployer sur une seule grande instance EC2
- B. Déployer sur plusieurs zones de disponibilité
- C. Déployer dans plusieurs Edge Locations
- D. Utiliser une seule AZ avec des snapshots

> ✅ **Réponse : B** — Le multi-AZ est la base de la haute disponibilité. Le multi-Région sert pour la reprise après sinistre ou la latence mondiale.

**Q9.** Une entreprise a besoin de latence ultra-faible pour des applications mobiles 5G. Quel service utiliser ?
- A. AWS Outposts - B. AWS Local Zones - C. AWS Wavelength - D. Amazon CloudFront

> ✅ **Réponse : C** — Wavelength intègre le calcul AWS dans les réseaux 5G des opérateurs.

**Q10.** Une entreprise doit garder des données dans son propre data center pour des raisons réglementaires, mais veut utiliser les mêmes API et services AWS. Quelle solution ?
- A. AWS Wavelength - B. AWS Outposts - C. AWS Local Zones - D. AWS Direct Connect

> ✅ **Réponse : B** — Outposts installe une infrastructure AWS dans vos locaux.

**Q11.** Quel pilier du Well-Architected Framework se concentre sur la capacité d'un système à se remettre de pannes et à acquérir dynamiquement des ressources ?
- A. Efficacité des performances - B. Fiabilité - C. Excellence opérationnelle - D. Sécurité

> ✅ **Réponse : B — Fiabilité.**

**Q12.** « Effectuer des modifications petites, fréquentes et réversibles » et « exécuter les opérations en tant que code » sont des principes de quel pilier ?
- A. Excellence opérationnelle - B. Fiabilité - C. Optimisation des coûts - D. Durabilité

> ✅ **Réponse : A — Excellence opérationnelle.**

**Q13.** Quel pilier a été ajouté en 2021 et vise à réduire l'impact environnemental ?
> ✅ **Réponse : Durabilité (Sustainability).** Les 6 piliers : Excellence opérationnelle, Sécurité, Fiabilité, Efficacité des performances, Optimisation des coûts, Durabilité.

**Q14.** Quel pilier recommande d'« utiliser des architectures serverless » et de « devenir mondial en quelques minutes » ?
- A. Efficacité des performances - B. Fiabilité - C. Sécurité - D. Optimisation des coûts

> ✅ **Réponse : A — Efficacité des performances.**

**Q15.** Quel outil gratuit permet d'évaluer une charge de travail par rapport aux bonnes pratiques AWS ?
- A. AWS Trusted Advisor - B. AWS Well-Architected Tool - C. AWS Config - D. AWS Inspector

> ✅ **Réponse : B** — Trusted Advisor vérifie le compte ; le Well-Architected Tool évalue une architecture/charge de travail par questionnaire.

**Q16.** Quelle perspective du AWS CAF concerne la formation du personnel, la gestion du changement et la culture organisationnelle ?
- A. Business - B. Personnes (People) - C. Gouvernance - D. Opérations

> ✅ **Réponse : B — People.**

**Q17.** Quelle perspective du CAF aide à gérer et optimiser les dépenses cloud, la gestion des risques et la gestion des données ?
- A. Gouvernance - B. Plateforme - C. Sécurité - D. Business

> ✅ **Réponse : A — Gouvernance.**

**Q18.** Quelles perspectives du CAF sont « techniques » ?
> ✅ **Réponse :** Plateforme, Sécurité, Opérations. (Les métier : Business, People, Gouvernance.)

**Q19.** Une entreprise migre une application vers EC2 sans aucune modification. Quelle stratégie de migration ?
- A. Replatform - B. Refactor - C. Rehost - D. Repurchase

> ✅ **Réponse : C — Rehost (« lift and shift »).**

**Q20.** Une entreprise remplace son CRM installé localement par une solution SaaS. Quelle stratégie ?
- A. Retain - B. Repurchase - C. Relocate - D. Rehost

> ✅ **Réponse : B — Repurchase (« drop and shop »).**

**Q21.** Une entreprise migre sa base MySQL auto-gérée vers Amazon RDS sans changer le code de l'application. Quelle stratégie ?
> ✅ **Réponse : Replatform** (« lift, tinker and shift ») — une optimisation sans changer l'architecture de base.

**Q22.** Une application monolithique est réécrite en microservices avec Lambda et DynamoDB. Stratégie ?
> ✅ **Réponse : Refactor / Re-architect.**

**Q23.** Quels coûts une entreprise peut-elle réduire en migrant vers AWS ? (Choisissez-en deux.)
- A. Coûts de développement des applications métier
- B. Coûts d'électricité et de refroidissement des data centers
- C. Coûts du matériel serveur
- D. Coûts de formation de ses clients
- E. Coûts de licences des logiciels métier développés en interne

> ✅ **Réponses : B et C** — Les coûts d'infrastructure physique sont transférés à AWS.

**Q24.** Quelle affirmation décrit le mieux le TCO (coût total de possession) ?
> ✅ **Réponse :** Le TCO compare le coût complet d'une infrastructure sur site (serveurs, stockage, réseau, électricité, locaux, refroidissement, personnel IT, maintenance) avec celui du cloud — pas uniquement le prix des serveurs.

**Q25.** Quel est un avantage des services managés comme Amazon RDS par rapport à une base de données installée sur EC2 ?
- A. Accès root complet au système d'exploitation
- B. AWS gère les sauvegardes, les correctifs et la haute disponibilité
- C. Aucuns frais
- D. Possibilité d'utiliser n'importe quel moteur de base de données

> ✅ **Réponse : B** — Moins de charge opérationnelle (« undifferentiated heavy lifting »).

**Q26.** Quel modèle de service offre le plus de contrôle au client ?
- A. SaaS - B. PaaS - C. IaaS - D. FaaS

> ✅ **Réponse : C — IaaS** (ex. EC2 : vous gérez l'OS).

**Q27.** AWS Elastic Beanstalk est un exemple de :
- A. IaaS - B. PaaS - C. SaaS - D. Déploiement sur site

> ✅ **Réponse : B — PaaS.**

**Q28.** Une entreprise connecte son data center à AWS et exécute une partie de ses applications dans chaque environnement. Quel modèle de déploiement ?
> ✅ **Réponse : Hybride.**

**Q29.** Quel principe de conception recommande de faire en sorte qu'un composant défaillant n'entraîne pas la panne de l'ensemble du système ?
- A. Couplage fort - B. Couplage faible (découplage) - C. Scalabilité verticale - D. Monolithe

> ✅ **Réponse : B** — Le découplage (ex. avec SQS) isole les pannes.

**Q30.** Une entreprise souhaite expérimenter rapidement de nouvelles idées à faible coût et les abandonner si elles échouent. Quel avantage du cloud ?
> ✅ **Réponse : Augmenter la vitesse et l'agilité** — le coût de l'échec est faible car les ressources peuvent être supprimées immédiatement.

**Q31.** Quel service AWS aide à suivre l'avancement des migrations d'applications à travers plusieurs outils AWS et partenaires ?
- A. AWS Migration Hub - B. AWS DMS - C. AWS Snowball - D. AWS DataSync

> ✅ **Réponse : A.**

**Q32.** Quel service collecte des informations sur les serveurs sur site (configuration, utilisation, dépendances) pour planifier une migration ?
> ✅ **Réponse : AWS Application Discovery Service.**

---

# DOMAINE 2 — Sécurité et conformité (30 %)

**Q33.** Selon le modèle de responsabilité partagée, laquelle de ces tâches relève d'AWS ?
- A. Appliquer les correctifs du système d'exploitation invité d'EC2
- B. Configurer les groupes de sécurité
- C. Sécuriser physiquement les data centers
- D. Chiffrer les données client

> ✅ **Réponse : C** — AWS = sécurité **du** cloud (physique, matériel, réseau global, hyperviseur).

**Q34.** Lesquelles sont de la responsabilité du client ? (Choisissez-en deux.)
- A. Gestion des identités et des accès IAM
- B. Maintenance du matériel réseau
- C. Configuration du pare-feu de l'instance (security groups)
- D. Destruction des disques en fin de vie
- E. Correctifs de l'hyperviseur

> ✅ **Réponses : A et C.**

**Q35.** Pour Amazon RDS, qui applique les correctifs du moteur de base de données ?
> ✅ **Réponse : AWS** (pendant la fenêtre de maintenance que vous choisissez). Le client reste responsable des données, des accès, des security groups et du chiffrement.

**Q36.** Quel contrôle est considéré comme « partagé » entre AWS et le client ?
- A. Contrôles physiques et environnementaux
- B. Gestion des correctifs (patch management)
- C. Classification des données du client
- D. Destruction du matériel

> ✅ **Réponse : B** — Autres contrôles partagés : gestion de la configuration, sensibilisation et formation. A et D sont hérités (AWS), C est client.

**Q37.** Quelle est la meilleure pratique concernant l'utilisateur root d'un compte AWS ?
- A. L'utiliser pour les tâches d'administration quotidiennes
- B. Partager ses identifiants avec l'équipe d'administration
- C. Activer MFA et l'utiliser uniquement pour les tâches qui l'exigent
- D. Créer des clés d'accès pour l'automatisation

> ✅ **Réponse : C.**

**Q38.** Laquelle de ces tâches nécessite l'utilisateur root ?
- A. Créer un utilisateur IAM
- B. Changer le plan de support AWS
- C. Lancer une instance EC2
- D. Créer un bucket S3

> ✅ **Réponse : B** — Autres : fermer le compte, modifier l'e-mail/paramètres du compte root, restaurer des permissions IAM, s'inscrire comme vendeur de RI.

**Q39.** Une application sur EC2 doit lire des objets dans S3. Quelle est la méthode la plus sécurisée ?
- A. Stocker les clés d'accès d'un utilisateur IAM dans le code
- B. Associer un rôle IAM à l'instance EC2
- C. Utiliser les identifiants root
- D. Rendre le bucket public

> ✅ **Réponse : B** — Les rôles fournissent des identifiants temporaires gérés automatiquement.

**Q40.** Quel principe consiste à n'accorder que les permissions strictement nécessaires ?
> ✅ **Réponse : Principe du moindre privilège.**

**Q41.** Un groupe de 20 développeurs a besoin des mêmes permissions. Quelle est la méthode la plus efficace ?
- A. Attacher une politique à chaque utilisateur
- B. Créer un groupe IAM, y attacher la politique, ajouter les utilisateurs
- C. Partager un seul utilisateur IAM
- D. Utiliser le compte root

> ✅ **Réponse : B.**

**Q42.** Quel format utilisent les politiques IAM ?
- A. XML - B. YAML - C. JSON - D. CSV

> ✅ **Réponse : C — JSON.**

**Q43.** Si une politique autorise une action et une autre la refuse explicitement, quel est le résultat ?
> ✅ **Réponse : Refus.** Un *Deny explicite* l'emporte toujours. Par défaut, tout est refusé (deny implicite).

**Q44.** Quel rapport IAM liste tous les utilisateurs du compte et l'état de leurs identifiants (mots de passe, clés, MFA) ?
- A. IAM Access Advisor - B. IAM Credential Report - C. AWS Config - D. CloudTrail

> ✅ **Réponse : B.**

**Q45.** Une entreprise veut que ses employés se connectent une seule fois pour accéder à plusieurs comptes AWS et applications métier. Quel service ?
- A. Amazon Cognito - B. AWS IAM Identity Center - C. AWS Directory Service - D. IAM Access Analyzer

> ✅ **Réponse : B** (anciennement AWS Single Sign-On).

**Q46.** Une application mobile doit permettre à des millions d'utilisateurs de s'inscrire et se connecter avec Google ou Facebook. Quel service ?
> ✅ **Réponse : Amazon Cognito.**

**Q47.** Comment limiter les services que les comptes membres d'une organisation peuvent utiliser, même pour leurs administrateurs ?
- A. Politiques IAM - B. Service Control Policies (SCP) - C. Security groups - D. Network ACL

> ✅ **Réponse : B** — Les SCP (AWS Organizations) définissent les permissions maximales des comptes.

**Q48.** Quel service permet de configurer rapidement un environnement multi-comptes sécurisé et conforme selon les bonnes pratiques ?
- A. AWS Organizations - B. AWS Control Tower - C. AWS Config - D. AWS Service Catalog

> ✅ **Réponse : B** — Control Tower automatise une *landing zone* avec des garde-fous (s'appuie sur Organizations).

**Q49.** Quelle est la différence entre un Security Group et une Network ACL ?
> ✅ **Réponse :**
> | | Security Group | Network ACL |
> |---|---|---|
> | Niveau | Instance (ENI) | Sous-réseau |
> | État | **Stateful** (le retour est automatiquement autorisé) | **Stateless** (règles entrantes et sortantes explicites) |
> | Règles | Allow uniquement | Allow et Deny |
> | Évaluation | Toutes les règles | Par ordre de numéro |

**Q50.** Une entreprise doit bloquer une adresse IP spécifique au niveau d'un sous-réseau. Que doit-elle utiliser ?
> ✅ **Réponse : Une Network ACL** (les security groups ne permettent pas de règles Deny).

**Q51.** Quel service protège une application web contre l'injection SQL et le cross-site scripting (XSS) ?
- A. AWS Shield - B. AWS WAF - C. Amazon GuardDuty - D. Amazon Inspector

> ✅ **Réponse : B.**

**Q52.** Quel service fournit gratuitement une protection DDoS à tous les clients AWS ?
- A. AWS Shield Standard - B. AWS Shield Advanced - C. AWS WAF - D. Amazon Macie

> ✅ **Réponse : A.**

**Q53.** Une entreprise veut une protection DDoS avancée, l'accès 24/7 à une équipe d'experts DDoS et une protection contre les coûts liés aux pics de mise à l'échelle lors d'une attaque. Quel service ?
> ✅ **Réponse : AWS Shield Advanced** (accès à la Shield Response Team — SRT).

**Q54.** Quel service utilise le machine learning pour analyser les logs CloudTrail, VPC Flow Logs et DNS afin de détecter des activités malveillantes ?
- A. Amazon Inspector - B. Amazon GuardDuty - C. Amazon Macie - D. AWS Config

> ✅ **Réponse : B.**

**Q55.** Quel service analyse automatiquement les instances EC2 et images de conteneurs pour détecter des vulnérabilités logicielles et une exposition réseau non intentionnelle ?
> ✅ **Réponse : Amazon Inspector.**

**Q56.** Une entreprise veut identifier des numéros de cartes bancaires et données personnelles stockés dans ses buckets S3. Quel service ?
> ✅ **Réponse : Amazon Macie.**

**Q57.** Quel service agrège les résultats de GuardDuty, Inspector, Macie et effectue des vérifications de conformité automatisées en un seul endroit ?
- A. Amazon Detective - B. AWS Security Hub - C. AWS Trusted Advisor - D. CloudWatch

> ✅ **Réponse : B.**

**Q58.** Quel service aide à analyser et visualiser les données de sécurité pour trouver la cause racine d'un problème de sécurité ?
> ✅ **Réponse : Amazon Detective.**

**Q59.** Un administrateur veut savoir quel utilisateur a supprimé une instance EC2 hier. Quel service ?
- A. Amazon CloudWatch - B. AWS CloudTrail - C. AWS Config - D. AWS X-Ray

> ✅ **Réponse : B** — CloudTrail enregistre les appels API (qui, quoi, quand, d'où).

**Q60.** Une entreprise doit vérifier en continu que tous ses volumes EBS sont chiffrés et conserver l'historique des modifications de configuration. Quel service ?
> ✅ **Réponse : AWS Config.**

**Q61.** Où un client peut-il télécharger les rapports de conformité SOC 2 ou les attestations PCI DSS d'AWS ?
- A. AWS Artifact - B. AWS Audit Manager - C. AWS Security Hub - D. AWS Trusted Advisor

> ✅ **Réponse : A — AWS Artifact** (rapports et accords comme le BAA HIPAA).

**Q62.** Quel service automatise la collecte de preuves pour préparer vos propres audits ?
> ✅ **Réponse : AWS Audit Manager.**

**Q63.** Quel service permet de créer et contrôler les clés de chiffrement utilisées par S3, EBS et RDS ?
- A. AWS KMS - B. AWS Secrets Manager - C. AWS Certificate Manager - D. IAM

> ✅ **Réponse : A.**

**Q64.** Une banque exige un module matériel de sécurité (HSM) dédié et à locataire unique, validé FIPS 140-2 niveau 3. Quel service ?
> ✅ **Réponse : AWS CloudHSM.**

**Q65.** Quel service stocke les identifiants de bases de données et en effectue la rotation automatique ?
- A. Systems Manager Parameter Store - B. AWS Secrets Manager - C. AWS KMS - D. Amazon Cognito

> ✅ **Réponse : B.**

**Q66.** Quel service fournit gratuitement des certificats SSL/TLS publics et les renouvelle automatiquement ?
> ✅ **Réponse : AWS Certificate Manager (ACM).**

**Q67.** Quelle est la différence entre le chiffrement au repos et en transit ?
> ✅ **Réponse :** *Au repos* = données stockées (S3, EBS, RDS — via KMS). *En transit* = données qui circulent sur le réseau (TLS/HTTPS, VPN).

**Q68.** Un client souhaite effectuer un test d'intrusion sur ses instances EC2. Que doit-il faire ?
- A. Obtenir l'approbation écrite d'AWS au préalable
- B. Il peut le faire sans approbation préalable pour les services autorisés, en respectant la politique AWS
- C. C'est interdit
- D. Contacter AWS Support Enterprise

> ✅ **Réponse : B** — Pas besoin d'approbation pour les services listés ; les attaques DoS/DDoS restent interdites.

**Q69.** Une ressource AWS est utilisée pour envoyer du spam à votre entreprise. Qui contacter ?
> ✅ **Réponse : L'équipe AWS Trust & Safety (AWS Abuse).**

**Q70.** Quel service identifie les ressources (buckets S3, rôles IAM, clés KMS) partagées avec une entité externe à votre compte ?
> ✅ **Réponse : IAM Access Analyzer.**

**Q71.** Quel service permet de gérer centralement les règles AWS WAF et Shield Advanced sur tous les comptes d'une organisation ?
> ✅ **Réponse : AWS Firewall Manager.**

**Q72.** Quelles sont DEUX bonnes pratiques de sécurité IAM ? (Choisissez-en deux.)
- A. Activer MFA pour les utilisateurs privilégiés
- B. Partager les clés d'accès entre applications
- C. Faire tourner (rotation) régulièrement les identifiants
- D. Accorder AdministratorAccess à tous
- E. Utiliser le compte root pour l'automatisation

> ✅ **Réponses : A et C.**

**Q73.** Quelle couche du modèle OSI AWS Shield Standard protège-t-il principalement ?
> ✅ **Réponse : Couches 3 et 4** (réseau et transport — ex. SYN flood, UDP reflection). WAF protège la couche 7.

**Q74.** Comment empêcher qu'un bucket S3 soit accidentellement rendu public ?
> ✅ **Réponse : Activer S3 Block Public Access** (activé par défaut sur les nouveaux buckets) et utiliser des politiques de bucket restrictives.

**Q75.** Comment protéger des objets S3 contre la suppression accidentelle ? (Choisissez-en deux.)
- A. Activer le versioning
- B. Activer MFA Delete
- C. Activer S3 Transfer Acceleration
- D. Utiliser CloudFront
- E. Utiliser S3 One Zone-IA

> ✅ **Réponses : A et B.** (S3 Object Lock peut aussi empêcher la suppression — modèle WORM.)

**Q76.** Où trouver des informations sur les programmes de conformité d'AWS (HIPAA, RGPD, etc.) ?
> ✅ **Réponse : AWS Compliance Center / page AWS Compliance Programs**, et les rapports dans **AWS Artifact**.

**Q77.** Les données d'un client dans la Région Europe (Paris) peuvent-elles être déplacées par AWS vers une autre Région sans action du client ?
> ✅ **Réponse : Non.** Les données restent dans la Région choisie, sauf si le client les réplique ou les déplace lui-même.

**Q78.** Quel service permet de se connecter à une instance EC2 sans ouvrir le port SSH ni gérer de clés SSH ?
> ✅ **Réponse : AWS Systems Manager Session Manager.**

---

# DOMAINE 3 — Technologie et services cloud (34 %)

### Accès, déploiement et connectivité

**Q79.** Quel service permet de provisionner l'infrastructure à partir de modèles JSON ou YAML (Infrastructure as Code) ?
- A. AWS Elastic Beanstalk - B. AWS CloudFormation - C. AWS CodeDeploy - D. AWS Systems Manager

> ✅ **Réponse : B.** (AWS CDK permet de faire de l'IaC avec Python, TypeScript, Java…)

**Q80.** Un développeur veut déployer une application web Java sans se soucier du provisionnement, du load balancing et du scaling. Quel service ?
> ✅ **Réponse : AWS Elastic Beanstalk.**

**Q81.** Quelles sont les TROIS manières d'accéder aux services AWS ?
> ✅ **Réponse :** AWS Management Console, AWS CLI, AWS SDK (+ AWS CloudShell, terminal intégré à la console).

**Q82.** Une entreprise a besoin d'une connexion réseau privée, dédiée et à bande passante constante entre son data center et AWS. Quel service ?
- A. AWS Site-to-Site VPN - B. AWS Direct Connect - C. Amazon CloudFront - D. Internet Gateway

> ✅ **Réponse : B.** Le VPN passe par Internet (chiffré) et se met en place rapidement ; Direct Connect est privé mais prend des semaines.

**Q83.** Une entreprise a besoin d'une connexion chiffrée vers son VPC à mettre en place **aujourd'hui** et au moindre coût. Quel service ?
> ✅ **Réponse : AWS Site-to-Site VPN.**

### Calcul

**Q84.** Une charge de travail d'analyse par lots peut être interrompue et reprise à tout moment. Quelle option d'achat EC2 est la plus économique ?
- A. On-Demand - B. Reserved Instances - C. Spot Instances - D. Dedicated Hosts

> ✅ **Réponse : C** — jusqu'à 90 % de remise, mais interruptible avec 2 minutes de préavis.

**Q85.** Une base de données doit tourner 24h/24 pendant 3 ans. Quelle option est la plus économique ?
- A. On-Demand - B. Spot - C. Reserved Instances (3 ans, paiement intégral à l'avance) - D. Dedicated Hosts

> ✅ **Réponse : C** — Charge stable et prévisible → réservation. Paiement *All Upfront* + 3 ans = remise maximale.

**Q86.** Une entreprise doit utiliser ses licences logicielles existantes liées au nombre de sockets physiques de serveur. Quelle option EC2 ?
> ✅ **Réponse : Dedicated Hosts** (visibilité sur les sockets et cœurs physiques).

**Q87.** Un développeur teste une nouvelle application pendant 2 semaines, de manière imprévisible et sans interruption possible. Quelle option ?
> ✅ **Réponse : On-Demand.**

**Q88.** Quel modèle de tarification offre une flexibilité sur EC2, Fargate et Lambda en échange d'un engagement en dollars par heure sur 1 ou 3 ans ?
- A. EC2 Instance Savings Plan - B. Compute Savings Plan - C. Reserved Instances Standard - D. Spot

> ✅ **Réponse : B.**

**Q89.** Quel service ajoute ou supprime automatiquement des instances EC2 en fonction de la demande ?
> ✅ **Réponse : Amazon EC2 Auto Scaling.**

**Q90.** Quel type de load balancer convient pour du trafic HTTP/HTTPS avec routage selon le chemin d'URL ?
- A. Network Load Balancer - B. Application Load Balancer - C. Gateway Load Balancer - D. Classic Load Balancer

> ✅ **Réponse : B** (couche 7). NLB = couche 4, millions de requêtes/s, très faible latence.

**Q91.** Quel service permet d'exécuter du code en réponse à des événements sans provisionner de serveurs, facturé à la milliseconde ?
> ✅ **Réponse : AWS Lambda** (durée maximale d'exécution : 15 minutes).

**Q92.** Une tâche de traitement dure 3 heures. Peut-on utiliser AWS Lambda ?
> ✅ **Réponse : Non** — Lambda est limité à 15 minutes. Utiliser EC2, AWS Batch, ou ECS/Fargate.

**Q93.** Quel service permet d'exécuter des conteneurs sans gérer de serveurs ni de clusters EC2 ?
- A. Amazon ECS sur EC2 - B. AWS Fargate - C. Amazon EC2 - D. Amazon Lightsail

> ✅ **Réponse : B.**

**Q94.** Une entreprise utilise déjà Kubernetes sur site et veut un service managé équivalent sur AWS. Quel service ?
> ✅ **Réponse : Amazon EKS.**

**Q95.** Où stocker les images Docker sur AWS ?
> ✅ **Réponse : Amazon ECR (Elastic Container Registry).**

**Q96.** Une petite entreprise sans expertise cloud veut lancer un site WordPress avec un prix mensuel fixe et prévisible. Quel service ?
> ✅ **Réponse : Amazon Lightsail.**

**Q97.** Quel type d'instance EC2 choisir pour une application d'apprentissage automatique nécessitant des GPU ?
> ✅ **Réponse : Calcul accéléré (Accelerated Computing)** — familles P, G, Inf, Trn.

**Q98.** Qu'est-ce qu'une AMI ?
> ✅ **Réponse : Amazon Machine Image** — modèle contenant l'OS, la configuration et les logiciels nécessaires pour lancer une instance EC2.

### Stockage

**Q99.** Quel est le niveau de durabilité d'Amazon S3 Standard ?
> ✅ **Réponse : 99,999999999 % (11 neuf).** La disponibilité de S3 Standard est de 99,99 %.

**Q100.** Une entreprise conserve des données d'audit pendant 10 ans, rarement consultées, et accepte un délai de récupération de 48 h. Quelle classe la moins chère ?
- A. S3 Standard-IA - B. S3 Glacier Instant Retrieval - C. S3 Glacier Deep Archive - D. S3 One Zone-IA

> ✅ **Réponse : C.**

**Q101.** Les schémas d'accès à des données sont imprévisibles. Quelle classe S3 optimise automatiquement les coûts ?
> ✅ **Réponse : S3 Intelligent-Tiering.**

**Q102.** Des miniatures d'images peuvent être régénérées facilement et sont rarement consultées. Quelle classe la plus économique ?
> ✅ **Réponse : S3 One Zone-IA** (données recréables, une seule AZ).

**Q103.** Comment déplacer automatiquement des objets S3 vers Glacier après 90 jours ?
> ✅ **Réponse : Avec une règle de cycle de vie S3 (Lifecycle policy).**

**Q104.** Quel service S3 permet d'héberger un site web composé uniquement de HTML, CSS, JavaScript et images ?
> ✅ **Réponse : Hébergement de site web statique sur Amazon S3** (souvent combiné à CloudFront).

**Q105.** Un volume Amazon EBS peut-il être utilisé par une instance située dans une autre AZ ?
> ✅ **Réponse : Non directement.** Un volume EBS est lié à une AZ. Il faut créer un **snapshot**, puis restaurer un volume dans l'autre AZ.

**Q106.** Plusieurs centaines d'instances EC2 Linux réparties dans plusieurs AZ doivent accéder simultanément au même système de fichiers. Quel service ?
- A. Amazon EBS - B. Amazon EFS - C. Instance Store - D. S3 Glacier

> ✅ **Réponse : B.**

**Q107.** Des serveurs Windows ont besoin d'un partage de fichiers SMB intégré à Active Directory. Quel service ?
> ✅ **Réponse : Amazon FSx for Windows File Server.**

**Q108.** Quel stockage EC2 offre les meilleures performances mais perd ses données à l'arrêt de l'instance ?
> ✅ **Réponse : Instance Store** (stockage éphémère).

**Q109.** Une entreprise doit transférer 500 To de données vers AWS, mais sa connexion Internet est lente. Quelle solution ?
- A. AWS DataSync - B. AWS Snowball Edge - C. S3 Transfer Acceleration - D. AWS Direct Connect

> ✅ **Réponse : B** — Transfert physique hors ligne.

**Q110.** Quel service hybride permet aux applications sur site d'utiliser un stockage cloud illimité via des protocoles standards (NFS, SMB, iSCSI) ?
> ✅ **Réponse : AWS Storage Gateway.**

**Q111.** Quel service centralise et automatise les sauvegardes d'EBS, RDS, DynamoDB, EFS… ?
> ✅ **Réponse : AWS Backup.**

**Q112.** Quelle fonctionnalité accélère les transferts longue distance vers un bucket S3 en utilisant les edge locations ?
> ✅ **Réponse : S3 Transfer Acceleration.**

### Bases de données

**Q113.** Quelle option d'Amazon RDS améliore la **disponibilité** en maintenant une copie synchrone dans une autre AZ ?
- A. Read Replicas - B. Multi-AZ - C. Snapshots - D. ElastiCache

> ✅ **Réponse : B.** Les *Read Replicas* améliorent la **performance en lecture**.

**Q114.** Quelle base de données relationnelle AWS est compatible MySQL et PostgreSQL et jusqu'à 5 fois plus rapide que MySQL standard ?
> ✅ **Réponse : Amazon Aurora.**

**Q115.** Une application de jeu mobile a besoin d'une base NoSQL serverless avec une latence en millisecondes à un chiffre, quelle que soit l'échelle. Quel service ?
- A. Amazon RDS - B. Amazon DynamoDB - C. Amazon Redshift - D. Amazon Neptune

> ✅ **Réponse : B.**

**Q116.** Quel service fournit un cache en mémoire pour améliorer les performances des applications et réduire la charge sur la base de données ?
> ✅ **Réponse : Amazon ElastiCache** (Redis/Valkey/Memcached). Pour DynamoDB spécifiquement : **DAX**.

**Q117.** Une entreprise veut exécuter des requêtes analytiques complexes sur des pétaoctets de données structurées pour de la BI. Quel service ?
> ✅ **Réponse : Amazon Redshift** (entrepôt de données, OLAP).

**Q118.** Un réseau social doit modéliser des relations complexes entre utilisateurs (amis d'amis). Quel service ?
> ✅ **Réponse : Amazon Neptune** (base de données graphe).

**Q119.** Une entreprise utilise MongoDB et veut une base de données managée compatible. Quel service ?
> ✅ **Réponse : Amazon DocumentDB.**

**Q120.** Une entreprise veut migrer une base Oracle vers Amazon Aurora PostgreSQL avec un minimum d'interruption. Quels DEUX services ? (Choisissez-en deux.)
- A. AWS DMS - B. AWS Schema Conversion Tool - C. AWS Snowball - D. AWS DataSync - E. AWS Glue

> ✅ **Réponses : A et B** — SCT convertit le schéma, DMS migre les données (la source reste opérationnelle).

**Q121.** Une entreprise a besoin d'un accès complet à l'OS de sa base de données Oracle. Quelle solution ?
> ✅ **Réponse : Installer Oracle sur Amazon EC2** (ou RDS Custom). RDS standard ne donne pas accès à l'OS.

### Réseau

**Q122.** Quel composant permet aux instances d'un sous-réseau public d'accéder à Internet ?
> ✅ **Réponse : Internet Gateway** (avec une route dans la table de routage).

**Q123.** Des instances dans un sous-réseau privé doivent télécharger des mises à jour sur Internet sans être accessibles depuis Internet. Quelle solution ?
> ✅ **Réponse : NAT Gateway** (placée dans un sous-réseau public).

**Q124.** Quel service est le service DNS d'AWS ?
> ✅ **Réponse : Amazon Route 53** (enregistrement de domaines, routage, contrôles de santé).

**Q125.** Quelle politique de routage Route 53 redirige le trafic vers un site de secours si le site principal est défaillant ?
- A. Simple - B. Pondérée - C. Basculement (Failover) - D. Géolocalisation

> ✅ **Réponse : C.**

**Q126.** Une entreprise veut diffuser des vidéos et du contenu statique à des utilisateurs du monde entier avec une faible latence. Quel service ?
> ✅ **Réponse : Amazon CloudFront** (CDN utilisant les edge locations).

**Q127.** Quel service améliore la disponibilité et les performances d'applications TCP/UDP mondiales en fournissant des adresses IP anycast statiques et en utilisant le réseau AWS ?
> ✅ **Réponse : AWS Global Accelerator.**

**Q128.** Une entreprise doit connecter 50 VPC et ses réseaux sur site via un hub central. Quel service ?
- A. VPC Peering - B. AWS Transit Gateway - C. Internet Gateway - D. NAT Gateway

> ✅ **Réponse : B.**

**Q129.** Comment accéder à Amazon S3 depuis un VPC sans passer par Internet ?
> ✅ **Réponse : VPC Endpoint (Gateway Endpoint pour S3 et DynamoDB)** ou AWS PrivateLink (Interface Endpoint).

**Q130.** Quel service permet de créer, publier et sécuriser des API REST et WebSocket ?
> ✅ **Réponse : Amazon API Gateway.**

### Intégration, analytique, IA

**Q131.** Une application de commandes doit être découplée afin que le front-end continue de recevoir des commandes même si le traitement est lent. Quel service ?
- A. Amazon SNS - B. Amazon SQS - C. Amazon Kinesis - D. AWS Step Functions

> ✅ **Réponse : B** — File d'attente de messages.

**Q132.** Une entreprise veut envoyer une notification par e-mail et SMS à plusieurs abonnés lorsqu'un événement se produit. Quel service ?
> ✅ **Réponse : Amazon SNS** (pub/sub, push).

**Q133.** Quel service permet d'orchestrer plusieurs fonctions Lambda dans un workflow visuel avec gestion des erreurs ?
> ✅ **Réponse : AWS Step Functions.**

**Q134.** Quel service permet de déclencher une fonction Lambda tous les jours à 8h ou de réagir à des événements de services AWS et SaaS ?
> ✅ **Réponse : Amazon EventBridge.**

**Q135.** Un analyste veut exécuter des requêtes SQL directement sur des fichiers CSV stockés dans S3 sans gérer d'infrastructure. Quel service ?
- A. Amazon Redshift - B. Amazon Athena - C. Amazon EMR - D. AWS Glue

> ✅ **Réponse : B.**

**Q136.** Quel service permet de traiter des flux de données en temps réel (clics, IoT, logs) ?
> ✅ **Réponse : Amazon Kinesis.**

**Q137.** Quel service ETL serverless prépare et transforme les données pour l'analyse ?
> ✅ **Réponse : AWS Glue.**

**Q138.** Quel service permet de créer des tableaux de bord interactifs de business intelligence ?
> ✅ **Réponse : Amazon QuickSight.**

**Q139.** Quel service exécute Apache Hadoop et Spark à grande échelle ?
> ✅ **Réponse : Amazon EMR.**

**Q140.** Associez chaque besoin au bon service IA :
> ✅ **Réponses :**
> - Convertir des appels audio du centre d'appels en texte → **Amazon Transcribe**
> - Lire du texte à voix haute dans une application → **Amazon Polly**
> - Détecter des visages et objets dans des photos → **Amazon Rekognition**
> - Analyser le sentiment d'avis clients → **Amazon Comprehend**
> - Traduire un site en 10 langues → **Amazon Translate**
> - Créer un chatbot conversationnel → **Amazon Lex**
> - Extraire des données de factures scannées → **Amazon Textract**
> - Recommandations de produits → **Amazon Personalize**
> - Recherche intelligente dans des documents internes → **Amazon Kendra**
> - Construire, entraîner et déployer ses propres modèles ML → **Amazon SageMaker AI**
> - Créer une application d'IA générative avec des modèles de fondation → **Amazon Bedrock**

### Gestion et surveillance

**Q141.** Une équipe veut recevoir une alerte lorsque l'utilisation CPU d'une instance EC2 dépasse 80 %. Quel service ?
> ✅ **Réponse : Amazon CloudWatch** (alarme) + SNS pour la notification.

**Q142.** Quelle est la différence entre CloudWatch, CloudTrail et Config ?
> ✅ **Réponse :**
> - **CloudWatch** = *performance* : métriques, logs, alarmes (« Comment se porte ma ressource ? »)
> - **CloudTrail** = *audit* : appels API (« Qui a fait quoi ? »)
> - **Config** = *configuration* : état et historique, conformité (« À quoi ressemblait ma ressource et est-elle conforme ? »)

**Q143.** Quel service permet d'appliquer des correctifs à un parc de 500 instances EC2 et serveurs sur site ?
> ✅ **Réponse : AWS Systems Manager (Patch Manager).**

**Q144.** Quel service recommande des tailles d'instances EC2 optimales en analysant l'historique d'utilisation par ML ?
> ✅ **Réponse : AWS Compute Optimizer.**

**Q145.** Un développeur veut identifier les goulets d'étranglement de performance dans une application distribuée composée de microservices. Quel service ?
> ✅ **Réponse : AWS X-Ray.**

**Q146.** Quel service affiche les événements AWS qui affectent spécifiquement vos ressources (ex. maintenance planifiée d'une instance) ?
> ✅ **Réponse : AWS Health Dashboard** (vue « Your account health », anciennement Personal Health Dashboard).

**Q147.** Quels services forment un pipeline CI/CD complet sur AWS ?
> ✅ **Réponse : AWS CodePipeline** (orchestration) + **CodeBuild** (compilation/tests) + **CodeDeploy** (déploiement).

**Q148.** Une entreprise veut fournir à ses employés des bureaux Windows virtuels accessibles de partout. Quel service ?
> ✅ **Réponse : Amazon WorkSpaces.**

**Q149.** Quel service connecte des milliards d'appareils IoT au cloud ?
> ✅ **Réponse : AWS IoT Core.**

**Q150.** Quel service permet de créer rapidement un centre de contact client omnicanal dans le cloud ?
> ✅ **Réponse : Amazon Connect.**

**Q151.** Quel service envoie des e-mails marketing et transactionnels à grande échelle ?
> ✅ **Réponse : Amazon SES (Simple Email Service).**

**Q152.** Quel service permet aux administrateurs de créer un catalogue de produits IT approuvés que les utilisateurs peuvent déployer en libre-service ?
> ✅ **Réponse : AWS Service Catalog.**

---

# DOMAINE 4 — Facturation, tarification et support (12 %)

**Q153.** Quels sont les TROIS principaux facteurs de coût sur AWS ?
> ✅ **Réponse : Calcul, stockage et transfert de données sortant.**

**Q154.** Lequel de ces transferts de données est gratuit ?
- A. De S3 vers Internet
- B. D'Internet vers AWS (entrant)
- C. Entre deux Régions
- D. D'EC2 vers Internet

> ✅ **Réponse : B.**

**Q155.** Une entreprise veut estimer le coût mensuel d'une nouvelle architecture **avant** de la déployer. Quel outil ?
- A. AWS Cost Explorer - B. AWS Budgets - C. AWS Pricing Calculator - D. Cost and Usage Report

> ✅ **Réponse : C.**

**Q156.** Un responsable financier veut visualiser les dépenses des 6 derniers mois par service et prévoir les dépenses des prochains mois. Quel outil ?
> ✅ **Réponse : AWS Cost Explorer.**

**Q157.** Une entreprise veut être alertée par e-mail lorsque ses dépenses mensuelles prévues dépassent 1 000 $. Quel service ?
> ✅ **Réponse : AWS Budgets.** (Une alarme de facturation CloudWatch est aussi possible, mais Budgets gère les **prévisions**.)

**Q158.** Quel outil fournit les données de coûts et d'utilisation les plus détaillées (horaires, par ressource) pouvant être analysées avec Athena ?
> ✅ **Réponse : AWS Cost and Usage Report (CUR) / AWS Data Exports.**

**Q159.** Comment répartir les coûts AWS par département ou par projet ?
> ✅ **Réponse : Utiliser des balises de répartition des coûts (cost allocation tags)**, activées dans la console de facturation (et/ou des comptes séparés dans AWS Organizations).

**Q160.** Quels sont DEUX avantages de la facturation consolidée d'AWS Organizations ? (Choisissez-en deux.)
- A. Une seule facture pour tous les comptes
- B. Support Enterprise gratuit
- C. Remises sur volume grâce à l'usage combiné
- D. Instances Spot gratuites
- E. Suppression des frais de transfert de données

> ✅ **Réponses : A et C.** (Le partage des remises RI/Savings Plans entre comptes est aussi possible.)

**Q161.** Quel service détecte automatiquement des dépenses inhabituelles grâce au machine learning ?
> ✅ **Réponse : AWS Cost Anomaly Detection.**

**Q162.** Lesquels de ces services sont gratuits (seules les ressources créées sont facturées) ? (Choisissez-en deux.)
- A. AWS CloudFormation - B. Amazon EC2 - C. AWS Elastic Beanstalk - D. Amazon RDS - E. NAT Gateway

> ✅ **Réponses : A et C.** (Aussi gratuits : IAM, VPC de base, Auto Scaling, Organizations.)

**Q163.** Quel plan de support est le moins cher offrant un accès 24/7 par téléphone aux ingénieurs support ?
- A. Basic - B. Developer - C. Business - D. Enterprise

> ✅ **Réponse : C — Business.**

**Q164.** Quel plan de support est le moins cher donnant accès à **tous** les contrôles AWS Trusted Advisor ?
> ✅ **Réponse : Business.**

**Q165.** Une entreprise exige un temps de réponse de **15 minutes** en cas de panne d'un système critique pour l'entreprise et un TAM désigné. Quel plan ?
> ✅ **Réponse : Enterprise.**

**Q166.** Quel plan de support offre un temps de réponse de 30 minutes pour un système critique en panne et un accès à un pool de TAM ?
> ✅ **Réponse : Enterprise On-Ramp.**

**Q167.** Une startup en phase de test a besoin de conseils généraux par e-mail pendant les heures ouvrables, au moindre coût. Quel plan ?
> ✅ **Réponse : Developer.**

**Q168.** Quel plan de support inclut l'**AWS Concierge Support Team** pour les questions de facturation et de compte ?
> ✅ **Réponse : Enterprise** (et Enterprise On-Ramp).

**Q169.** Que fournit le plan Basic ?
> ✅ **Réponse :** Service client 24/7 pour le compte et la facturation, documentation, whitepapers, AWS re:Post, AWS Health Dashboard, contrôles **de base** de Trusted Advisor. **Aucun support technique** par un ingénieur.

**Q170.** Quelles sont les catégories d'AWS Trusted Advisor ?
> ✅ **Réponse :** Optimisation des coûts, Performance, Sécurité, Tolérance aux pannes, Quotas de service, Excellence opérationnelle.

**Q171.** Lequel de ces éléments Trusted Advisor peut-il signaler ? (Choisissez-en deux.)
- A. Des instances EC2 sous-utilisées
- B. Des vulnérabilités dans le code de l'application
- C. Des buckets S3 avec un accès public
- D. Des utilisateurs ayant supprimé des ressources
- E. Des données personnelles dans S3

> ✅ **Réponses : A et C.** (B = Inspector/CodeGuru, D = CloudTrail, E = Macie.)

**Q172.** Où trouver et acheter des logiciels tiers (pare-feu, solutions de sécurité, AMI préconfigurées) prêts à être déployés sur AWS ?
> ✅ **Réponse : AWS Marketplace.**

**Q173.** Une entreprise a besoin d'aide pour concevoir et migrer sa charge de travail ; elle cherche une société de conseil certifiée AWS. Où chercher ?
> ✅ **Réponse : AWS Partner Network (APN)** — partenaires de conseil. Aussi possibles : **AWS Professional Services**.

**Q174.** Où un utilisateur peut-il poser des questions techniques à la communauté AWS ?
> ✅ **Réponse : AWS re:Post.**

**Q175.** Quel service permet de consulter et demander l'augmentation des limites (quotas) de services AWS ?
> ✅ **Réponse : Service Quotas** (ou via le Support Center).

**Q176.** Quelle option de paiement des Instances Réservées offre la remise la plus importante ?
- A. No Upfront - B. Partial Upfront - C. All Upfront

> ✅ **Réponse : C — All Upfront** (paiement intégral à l'avance), idéalement sur 3 ans.

**Q177.** Qu'est-ce que l'offre gratuite AWS (Free Tier) « Always Free » ?
> ✅ **Réponse :** Des offres sans date d'expiration, ex. 1 million de requêtes AWS Lambda par mois, 25 Go de stockage DynamoDB.

**Q178.** Comment Amazon S3 est-il facturé ?
> ✅ **Réponse :** Selon la quantité stockée (Go/mois), la classe de stockage, le nombre de requêtes (PUT, GET…), le transfert de données sortant, et les fonctionnalités (réplication, récupération Glacier…).

**Q179.** Comment AWS Lambda est-il facturé ?
> ✅ **Réponse :** Au nombre de requêtes et à la durée d'exécution (en millisecondes), en fonction de la mémoire allouée.

**Q180.** Quel programme offre des crédits AWS et des ressources aux startups ?
> ✅ **Réponse : AWS Activate.**

**Q181.** Quel service permet à AWS d'opérer votre infrastructure (surveillance, correctifs, sauvegardes, sécurité) pour vous ?
> ✅ **Réponse : AWS Managed Services (AMS).**

**Q182.** Où trouver des réponses aux questions et demandes les plus fréquentes des clients AWS ?
> ✅ **Réponse : AWS Knowledge Center.**

---

## 🎯 Questions de scénario (réponses ouvertes)

**S1.** Une startup lance une application web. Le trafic est imprévisible. Elle veut minimiser l'administration et ne payer que ce qu'elle consomme. Proposez une architecture.
> ✅ **Réponse type :** Front-end statique sur **S3 + CloudFront**, API via **API Gateway + Lambda**, données dans **DynamoDB** (mode à la demande), authentification **Cognito**. Tout est serverless → pas de serveurs, mise à l'échelle automatique, paiement à l'usage.

**S2.** Une entreprise héberge une application à 3 niveaux et veut une haute disponibilité. Que recommandez-vous ?
> ✅ **Réponse type :** **Application Load Balancer** sur plusieurs AZ, instances EC2 dans un **Auto Scaling Group** multi-AZ, base **RDS Multi-AZ** (ou Aurora), DNS **Route 53** avec contrôles de santé, contenu statique sur **S3 + CloudFront**.

**S3.** Après un incident, un auditeur demande : qui a modifié le security group, quelle était la configuration précédente, et l'instance avait-elle un CPU élevé ?
> ✅ **Réponse type :** **CloudTrail** (qui), **AWS Config** (configuration avant/après), **CloudWatch** (CPU).

**S4.** La facture AWS a doublé ce mois-ci. Quelles étapes suivre ?
> ✅ **Réponse type :** Analyser avec **Cost Explorer** (par service/compte/tag), vérifier **Cost Anomaly Detection**, consulter les recommandations **Trusted Advisor** et **Compute Optimizer** (ressources inutilisées, sous-utilisées), mettre en place **AWS Budgets** avec alertes, appliquer des **tags** de répartition des coûts, envisager **Savings Plans/RI** pour les charges stables.

**S5.** Une entreprise de santé doit stocker des données de patients sur AWS conformément à HIPAA. Que faire ?
> ✅ **Réponse type :** Signer le **BAA** via **AWS Artifact**, utiliser des services éligibles HIPAA, chiffrer au repos (**KMS**) et en transit (TLS), contrôler les accès avec **IAM** (moindre privilège, MFA), journaliser avec **CloudTrail**, détecter les données sensibles avec **Macie**, surveiller avec **GuardDuty** et **Security Hub**. Rappel : la conformité reste une **responsabilité partagée**.

**S6.** Une entreprise veut migrer 200 serveurs sur site vers AWS rapidement, sans réécriture.
> ✅ **Réponse type :** Inventaire avec **Application Discovery Service**, suivi via **Migration Hub**, stratégie **Rehost** avec **AWS Application Migration Service (MGN)**, bases de données avec **DMS**, gros volumes hors ligne avec **Snowball Edge**, connectivité via **Direct Connect** ou **VPN**.

**S7.** Comment protéger une application web publique contre les attaques ?
> ✅ **Réponse type :** **CloudFront** + **AWS WAF** (couche 7 : SQLi, XSS, rate limiting) + **Shield Standard** (gratuit) ou **Shield Advanced** (DDoS avancé), **ALB** devant des EC2 en sous-réseaux privés, **Security Groups** restrictifs, certificats **ACM** pour HTTPS, **GuardDuty** pour la détection des menaces.
