# Fiche mémo — pièges, mots-clés et plan de révision

## 1. Les paires de services que l'examen adore confondre

| Ceci… | …vs cela | Comment les distinguer |
|---|---|---|
| **CloudWatch** | **CloudTrail** | Performance/métriques/alarmes **vs** qui a appelé quelle API |
| **CloudTrail** | **Config** | Actions (API) **vs** état et conformité de la configuration |
| **GuardDuty** | **Inspector** | Menaces actives (logs) **vs** vulnérabilités logicielles (CVE) |
| **Inspector** | **Macie** | Vulnérabilités EC2/conteneurs **vs** données sensibles dans S3 |
| **Security Hub** | **Detective** | Tableau de bord centralisé **vs** enquête sur la cause racine |
| **Shield** | **WAF** | DDoS couches 3/4 **vs** filtrage applicatif couche 7 (SQLi, XSS) |
| **Security Group** | **NACL** | Instance, stateful, Allow **vs** sous-réseau, stateless, Allow+Deny |
| **KMS** | **CloudHSM** | Clés gérées, multi-locataire **vs** HSM matériel dédié |
| **Secrets Manager** | **Parameter Store** | Rotation automatique (payant) **vs** stockage de paramètres (gratuit en standard) |
| **Artifact** | **Audit Manager** | Rapports de conformité **d'AWS** **vs** preuves pour **vos** audits |
| **Trusted Advisor** | **Well-Architected Tool** | Contrôles automatiques du compte **vs** revue d'une charge de travail |
| **Trusted Advisor** | **Compute Optimizer** | Recommandations larges **vs** dimensionnement par ML |
| **Cognito** | **IAM Identity Center** | Utilisateurs **de vos applis** **vs** employés (SSO multi-comptes) |
| **IAM** | **Organizations (SCP)** | Permissions d'identités **vs** limites maximales d'un compte |
| **Organizations** | **Control Tower** | Gérer des comptes **vs** créer une *landing zone* conforme automatisée |
| **SQS** | **SNS** | File d'attente (pull, 1 consommateur) **vs** pub/sub (push, N abonnés) |
| **SNS** | **SES** | Notifications multi-canaux **vs** e-mails marketing/transactionnels |
| **EventBridge** | **Step Functions** | Routage d'événements **vs** orchestration de workflows |
| **CloudFront** | **Global Accelerator** | Cache de contenu (HTTP) **vs** routage réseau optimisé (TCP/UDP, IP statiques) |
| **Direct Connect** | **Site-to-Site VPN** | Privé, dédié, semaines **vs** chiffré via Internet, rapide, pas cher |
| **VPC Peering** | **Transit Gateway** | 2 VPC, non transitif **vs** hub pour des dizaines de VPC |
| **NAT Gateway** | **Internet Gateway** | Sortie seulement pour le privé **vs** entrée/sortie pour le public |
| **EBS** | **EFS** | 1 instance, 1 AZ **vs** milliers d'instances, multi-AZ |
| **EBS** | **Instance Store** | Persistant **vs** éphémère |
| **EFS** | **FSx for Windows** | Linux (NFS) **vs** Windows (SMB) |
| **S3 Standard-IA** | **One Zone-IA** | Multi-AZ **vs** 1 AZ (données recréables) |
| **Glacier Flexible** | **Deep Archive** | Minutes à 12 h **vs** 12–48 h (le moins cher) |
| **RDS Multi-AZ** | **Read Replica** | Disponibilité **vs** performance en lecture |
| **RDS** | **Redshift** | OLTP (transactions) **vs** OLAP (analytique) |
| **Athena** | **Redshift** | SQL ponctuel sur S3 serverless **vs** entrepôt de données |
| **DynamoDB** | **ElastiCache** | Base NoSQL **vs** cache en mémoire |
| **ECS** | **EKS** | Orchestrateur AWS **vs** Kubernetes |
| **Fargate** | **EC2** | Serverless pour conteneurs **vs** serveurs à gérer |
| **Beanstalk** | **CloudFormation** | PaaS pour déployer une appli **vs** IaC pour toute infrastructure |
| **DataSync** | **Storage Gateway** | Transfert/migration de données **vs** accès hybride permanent |
| **DMS** | **SCT** | Migre les données **vs** convertit le schéma |
| **Polly** | **Transcribe** | Texte → voix **vs** voix → texte |
| **Rekognition** | **Textract** | Images/vidéos **vs** documents |
| **Lex** | **Comprehend** | Chatbot **vs** analyse de texte |
| **Pricing Calculator** | **Cost Explorer** | Estimation du futur **vs** analyse du passé |
| **Cost Explorer** | **Budgets** | Analyse/prévision **vs** alertes et seuils |
| **Dedicated Host** | **Dedicated Instance** | Serveur physique avec visibilité sockets (licences) **vs** matériel simplement non partagé |
| **Reserved Instances** | **Savings Plans** | Engagement sur un type d'instance **vs** engagement en $/heure, plus flexible |
| **Local Zones** | **Wavelength** | Près des grandes villes **vs** dans les réseaux 5G |
| **Outposts** | **Local Zones** | Dans **votre** data center **vs** chez AWS près d'une ville |
| **Marketplace** | **Service Catalog** | Logiciels tiers à acheter **vs** catalogue interne approuvé |
| **APN Partner** | **Professional Services** | Société partenaire **vs** équipe AWS |

## 2. Mots-clés → réponse réflexe

| Si la question dit… | Pensez… |
|---|---|
| « interruptible », « flexible dans le temps », « le moins cher » (calcul) | **Spot** |
| « stable », « prévisible », « 1 ou 3 ans » | **RI / Savings Plans** |
| « court terme », « imprévisible », « sans interruption » | **On-Demand** |
| « licences par socket/cœur », « BYOL serveur » | **Dedicated Host** |
| « sans serveur », « événement », « < 15 min » | **Lambda** |
| « conteneurs sans gérer de serveurs » | **Fargate** |
| « découpler » | **SQS** |
| « notifier », « fan-out » | **SNS** |
| « API calls », « audit », « qui » | **CloudTrail** |
| « métriques », « alarme », « logs » | **CloudWatch** |
| « conformité de configuration », « historique de configuration » | **Config** |
| « rapports de conformité AWS », « SOC », « ISO », « BAA » | **Artifact** |
| « PII », « données sensibles S3 » | **Macie** |
| « menaces », « activité malveillante » | **GuardDuty** |
| « vulnérabilités », « CVE » | **Inspector** |
| « DDoS » | **Shield** |
| « SQL injection », « XSS », « couche 7 » | **WAF** |
| « latence faible mondiale pour contenu statique/vidéo » | **CloudFront** |
| « DNS », « nom de domaine », « basculement » | **Route 53** |
| « connexion privée dédiée » | **Direct Connect** |
| « pétaoctets », « hors ligne », « bande passante limitée » | **Snowball Edge** |
| « millisecondes à un chiffre », « NoSQL » | **DynamoDB** |
| « microsecondes » + DynamoDB | **DAX** |
| « data warehouse », « BI », « OLAP » | **Redshift** |
| « graphe », « relations » | **Neptune** |
| « MongoDB » | **DocumentDB** |
| « Cassandra » | **Keyspaces** |
| « temps réel », « streaming » | **Kinesis** |
| « SQL sur S3 » | **Athena** |
| « tableaux de bord », « visualisation » | **QuickSight** |
| « ETL » | **Glue** |
| « estimer avant de déployer » | **Pricing Calculator** |
| « TAM désigné », « 15 minutes » | **Support Enterprise** |
| « 24/7 téléphone » le moins cher, « tous les checks Trusted Advisor » | **Support Business** |
| « une seule facture », « remises sur volume » | **Organizations / facturation consolidée** |
| « répartir les coûts par projet » | **Cost allocation tags** |

## 3. Pièges classiques

1. **« LE MOINS d'effort opérationnel »** → choisissez le service **managé/serverless** (RDS plutôt qu'une base sur EC2, Fargate plutôt qu'ECS sur EC2, Lambda plutôt qu'EC2).
2. **« LE PLUS rentable »** → lisez bien les contraintes (interruptible ? durée ? délai de récupération ?).
3. **Questions à réponses multiples** : le nombre de réponses à choisir est indiqué — il faut **toutes** les bonnes réponses pour avoir le point.
4. **Haute disponibilité = multi-AZ**, **reprise après sinistre / latence mondiale = multi-Région**.
5. **Les Edge Locations ne sont pas des AZ** et n'hébergent pas d'instances EC2.
6. **S3 est un service régional** (même si les noms de buckets sont uniques au monde). **IAM est global.**
7. **Un volume EBS est lié à une AZ.**
8. **Le transfert entrant est gratuit**, le sortant est payant.
9. **Les SCP ne donnent jamais de permissions**, elles ne font que limiter.
10. **Le client est TOUJOURS responsable de ses données et de ses accès (IAM)**, quel que soit le service.
11. **Le chiffrement est une responsabilité du client** (même si AWS fournit les outils et l'active par défaut sur S3).
12. **AWS Support Basic n'inclut aucun support technique** par ingénieur.
13. Le **Well-Architected Framework a 6 piliers**, le **CAF a 6 perspectives** — ne les mélangez pas.
14. **Trusted Advisor ≠ Inspector** : TA ne scanne pas le code ni les vulnérabilités des OS.
15. **Shield Standard est automatique et gratuit**, pas besoin de l'activer.

## 4. Plan de révision sur 3 semaines

| Semaine | Jours | Activité |
|---|---|---|
| **1** | J1–J2 | Lire le Domaine 1 du guide (01) + Q1–Q32 du fichier 02 |
| | J3–J5 | Lire le Domaine 2 + Q33–Q78. **C'est le domaine le plus lourd après le 3 : insistez sur la responsabilité partagée et IAM** |
| | J6–J7 | Révision des erreurs + tableau « paires de services » ci-dessus |
| **2** | J8–J11 | Domaine 3 (calcul, stockage, bases, réseau, IA, analytique) + Q79–Q152 |
| | J12–J13 | Domaine 4 (facturation, support) + Q153–Q182 + scénarios S1–S7 |
| | J14 | **Examen blanc (fichier 03)** en conditions réelles |
| **3** | J15–J17 | Revoir chaque erreur de l'examen blanc dans le guide |
| | J18–J19 | Examens officiels gratuits : *AWS Skill Builder — Official Practice Question Set CLF-C02* (20 questions) + *AWS Cloud Practitioner Essentials* |
| | J20 | Relire la fiche mémo (ce fichier) et le tableau « Quel service pour quel besoin ? » du guide |
| | J21 | **Repos**, puis examen 🎯 |

## 5. Stratégie le jour de l'examen

- **90 minutes pour 65 questions** ≈ 1 min 20 par question : largement suffisant.
- **Éliminez** d'abord les réponses absurdes (souvent 2 sur 4).
- Repérez les **mots-clés** (moins cher, moins d'effort, haute disponibilité, temps réel…).
- **Marquez pour révision** (*Flag for review*) les questions douteuses et passez à la suite.
- **Ne laissez aucune question vide** — pas de pénalité.
- 15 questions ne sont pas notées : une question bizarre ne doit pas vous déstabiliser.
- Examen en centre **Pearson VUE** ou **en ligne** (OnVUE : pièce calme, bureau vide, webcam, pièce d'identité).
- Les candidats dont l'anglais n'est pas la langue maternelle peuvent demander **+30 minutes** (aménagement « ESL +30 ») *avant* de réserver l'examen — **pertinent si vous passez l'examen en anglais**.

## 6. Ressources officielles gratuites

- **AWS Skill Builder** : *AWS Cloud Practitioner Essentials* (cours gratuit), *Official Practice Question Set*.
- **Guide officiel de l'examen CLF-C02** (Exam Guide) : liste exacte des services dans le périmètre.
- **Whitepapers** : *Overview of Amazon Web Services*, *AWS Well-Architected Framework*, *How AWS Pricing Works*.
- **AWS Free Tier** : pratiquez ! Créer une instance EC2, un bucket S3, un utilisateur IAM avec MFA, un budget AWS Budgets.

Bonne chance pour votre certification ! 🚀
