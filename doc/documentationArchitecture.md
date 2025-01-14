

# Documentation de l'architecture du laboratoire de LOG430
- [Documentation de l'architecture du laboratoire de LOG430](#documentation-de-larchitecture-du-laboratoire-de-log430)
- [Page titre](#page-titre)
- [Introduction](#introduction)
- [Scénario d'objectif d'affaire](#scénario-dobjectif-daffaire)
  - [OA-1. Faciliter le recrutement des nouveaux chargés de laboratoire.](#oa-1-faciliter-le-recrutement-des-nouveaux-chargés-de-laboratoire)
  - [OA-2. Validez si le transport par autobus est toujours plus rapide, peu importe l'heure de la journée](#oa-2-validez-si-le-transport-par-autobus-est-toujours-plus-rapide-peu-importe-lheure-de-la-journée)
- [Cas d'utilisations](#cas-dutilisations)
    - [**CU01** - Veux comparer les temps de trajet.](#cu01---veux-comparer-les-temps-de-trajet)
      - [CU01-D1 **Disponibilité**](#cu01-d1-disponibilité)
      - [CU01-M1 **Modifiabilité**](#cu01-m1-modifiabilité)
      - [CU01-P1 **Performance**](#cu01-p1-performance)
      - [CU01-S1 **Sécurité**](#cu01-s1-sécurité)
      - [CU01-T1 **Testabilité**](#cu01-t1-testabilité)
      - [CU01-U1 **Usabilité**](#cu01-u1-usabilité)
      - [CU01-I1 **Interopérabilité**](#cu01-i1-interopérabilité)
    - [**CU02** - Veux pouvoir mettre le chaos dans les microservices.](#cu02---veux-pouvoir-mettre-le-chaos-dans-les-microservices)
      - [CU02-D1 **Disponibilité**](#cu02-d1-disponibilité)
      - [CU02-M1 **Modifiabilité**](#cu02-m1-modifiabilité)
      - [CU02-P1 **Performance**](#cu02-p1-performance)
      - [CU02-S1 **Sécurité**](#cu02-s1-sécurité)
      - [CU02-T1 **Testabilité**](#cu02-t1-testabilité)
      - [CU02-U1 **Usabilité**](#cu02-u1-usabilité)
      - [CU02-I1 **Interopérabilité**](#cu02-i1-interopérabilité)
    - [**CU03** - Pas de CU03](#cu03-NA)
    - [**CU04** - Veux pouvoir s'authentifier.](#cu04---veux-pouvoir-sauthentifier)
      - [CU04-D1 **Disponibilité**](#cu04-d1-disponibilité)
      - [CU04-M1 **Modifiabilité**](#cu04-m1-modifiabilité)
      - [CU04-P1 **Performance**](#cu04-p1-performance)
      - [CU04-S1 **Sécurité**](#cu04-s1-sécurité)
      - [CU04-T1 **Testabilité**](#cu04-t1-testabilité)
      - [CU04-U1 **Usabilité**](#cu04-u1-usabilité)
      - [CU04-I1 **Interopérabilité**](#cu04-i1-interopérabilité)
    - [**CU05** - Avoir une intercommunication entre microservices à l’aide d’une source unique de découverte de route.](#cu05---avoir-une-intercommunication-entre-microservices-à-laide-dune-source-unique-de-découverte-de-route)
      - [CU05-D1 **Disponibilité**](#cu05-d1-disponibilité)
      - [CU05-M1 **Modifiabilité**](#cu05-m1-modifiabilité)
      - [CU05-P1 **Performance**](#cu05-p1-performance)
      - [CU05-S1 **Sécurité**](#cu05-s1-sécurité)
      - [CU05-T1 **Testabilité**](#cu05-t1-testabilité)
      - [CU05-U1 **Usabilité**](#cu05-u1-usabilité)
      - [CU05-I1 **Interopérabilité**](#cu05-i1-interopérabilité)
    - [**CU06** - Veux informer le mainteneur sur le status de vie des microservices](#cu06---veux-informer-le-mainteneur-sur-le-status-de-vie-des-microservices)
      - [CU06-D1 **Disponibilité**](#cu06-d1-disponibilité)
      - [CU06-M1 **Modifiabilité**](#cu06-m1-modifiabilité)
      - [CU06-P1 **Performance**](#cu06-p1-performance)
      - [CU06-S1 **Sécurité**](#cu06-s1-sécurité)
      - [CU06-T1 **Testabilité**](#cu06-t1-testabilité)
      - [CU06-U1 **Usabilité**](#cu06-u1-usabilité)
      - [CU06-I1 **Interopérabilité**](#cu06-i1-interopérabilité)
    - [**CU07** - Veux pouvoir informer le mainteneur sur l’état interne d’un service (exemple l’état du CPU)](#cu07---veux-pouvoir-informer-le-mainteneur-sur-létat-interne-dun-service-exemple-létat-du-cpu)
      - [CU07-D1 **Disponibilité**](#cu07-d1-disponibilité)
      - [CU07-M1 **Modifiabilité**](#cu07-m1-modifiabilité)
      - [CU07-P1 **Performance**](#cu07-p1-performance)
      - [CU07-S1 **Sécurité**](#cu07-s1-sécurité)
      - [CU07-T1 **Testabilité**](#cu07-t1-testabilité)
      - [CU07-U1 **Usabilité**](#cu07-u1-usabilité)
      - [CU07-I1 **Interopérabilité**](#cu07-i1-interopérabilité)
    - [**CU08** - Veux avoir le temps d’un trajet en autobus](#cu08---veux-avoir-le-temps-dun-trajet-en-autobus)
      - [CU08-D1 **Disponibilité**](#cu08-d1-disponibilité)
      - [CU08-M1 **Modifiabilité**](#cu08-m1-modifiabilité)
      - [CU08-P1 **Performance**](#cu08-p1-performance)
      - [CU08-S1 **Sécurité**](#cu08-s1-sécurité)
      - [CU08-T1 **Testabilité**](#cu08-t1-testabilité)
      - [CU08-U1 **Usabilité**](#cu08-u1-usabilité)
      - [CU08-I1 **Interopérabilité**](#cu08-i1-interopérabilité)
    - [**CU09** - Veux avoir le temps de trajet en auto](#cu09---veux-avoir-le-temps-de-trajet-en-auto)
      - [CU09-D1 **Disponibilité**](#cu09-d1-disponibilité)
      - [CU09-M1 **Modifiabilité**](#cu09-m1-modifiabilité)
      - [CU09-P1 **Performance**](#cu09-p1-performance)
      - [CU09-S1 **Sécurité**](#cu09-s1-sécurité)
      - [CU09-T1 **Testabilité**](#cu09-t1-testabilité)
      - [CU09-U1 **Usabilité**](#cu09-u1-usabilité)
      - [CU09-I1 **Interopérabilité**](#cu09-i1-interopérabilité)
    - [**CU10** - Pas de CU10](#cu10-NA)
- [Vue architecturale de contexte](#vue-architecturale-de-contexte)
  - [Présentation primaire](#présentation-primaire)
  - [Catalogue d'éléments](#catalogue-déléments)
  - [Guide de variabilité](#guide-de-variabilité)
    - [Services Externes](#services-externes)
    - [Base de Données pour l'authentification](#base-de-données-pour-lauthentification)
    - [Ajout ou Retrait d'un microservice](#ajout-ou-retrait-dun-microservice)
  - [Raisonnement](#raisonnement)
    - [Architecture Microservices](#architecture-microservices)
    - [Patron Discovery](#patron-discovery)
- [Conception axée sur les attributs de qualité](#conception-axée-sur-les-attributs-de-qualité)
  - [ADD-Disponibilité](#add-disponibilité)
    - [ADD-détection de faute](#add-détection-de-faute)
    - [ADD-Préparation et réparation](#add-préparation-et-réparation)
    - [ADD-Réintroduction](#add-réintroduction)
    - [ADD-Prévention des fautes](#add-prévention-des-fautes)
  - [ADD-Modifiabilité](#add-modifiabilité)
    - [ADD-Réduire la taille des modules](#add-réduire-la-taille-des-modules)
    - [ADD-Augmenter la cohésion](#add-augmenter-la-cohésion)
    - [ADD-Réduire le couplage](#add-réduire-le-couplage)
    - [ADD-Defer binding](#add-defer-binding)
  - [ADD-Performance](#add-performance)
    - [ADD-Contrôler la demande en ressources](#add-contrôler-la-demande-en-ressources)
    - [ADD-Gérer les ressources](#add-gérer-les-ressources)
  - [ADD-Sécurité](#add-sécurité)
    - [ADD-Détecter les attaques](#add-détecter-les-attaques)
    - [ADD-Résister aux attaques](#add-résister-aux-attaques)
    - [ADD-Réagir aux attaques](#add-réagir-aux-attaques)
    - [ADD-Récupérer d'une attaque](#add-récupérer-dune-attaque)
  - [ADD-Testabilité](#add-testabilité)
    - [ADD-Controle and observe l'état du système](#add-controle-and-observe-létat-du-système)
    - [ADD-Limiter la complexité](#add-limiter-la-complexité)
  - [ADD-Usabilité](#add-usabilité)
    - [ADD-Supporter l'initiative de l'usager](#add-supporter-linitiative-de-lusager)
    - [ADD-Supporter l'initiative du système](#add-supporter-linitiative-du-système)
  - [ADD-Interopérabilité](#add-interopérabilité)
    - [ADD-Localiser](#add-localiser)
    - [ADD-Gérer les interfaces](#add-gérer-les-interfaces)
- [Réalisation des cas d'utilisation](#réalisation-des-cas-dutilisation)
    - [**RDCU-CU01** - Veux comparer les temps de trajet.](#rdcu-cu01---veux-comparer-les-temps-de-trajet)
    - [**RDCU-CU02** - Veux pouvoir mettre le chaos dans les services en mode.](#rdcu-cu02---veux-pouvoir-mettre-le-chaos-dans-les-services-en-mode)
    - [**RDCU-CU03**](#rdcu-cu03)
    - [**RDCU-CU04** - Veux pouvoir s'authentifier](#rdcu-cu04---veux-pouvoir-sauthentifier)
    - [**RDCU-CU05** -](#rdcu-cu05--)
    - [**RDCU-CU06** -](#rdcu-cu06--)
    - [**RDCU-CU07** -](#rdcu-cu07--)
    - [**RDCU-CU08** -](#rdcu-cu08--)
    - [**RDCU-CU09** -](#rdcu-cu09--)
    - [**RDCU-CU10** -](#rdcu-cu10--)
- [Réalisation des attributs de qualité](#réalisation-des-attributs-de-qualité)
  - [RDAQ-Disponibilité](#rdaq-disponibilité)
    - [RDTQ-Détection de faute](#rdtq-détection-de-faute)
    - [RDTQ-Préparation et réparation](#rdtq-préparation-et-réparation)
    - [RDTQ-Réintroduction](#rdtq-réintroduction)
    - [RDTQ-Prévention des fautes](#rdtq-prévention-des-fautes)
    - [Relation entre les éléments architecturaux et les exigences de disponibilité](#relation-entre-les-éléments-architecturaux-et-les-exigences-de-disponibilité)
  - [RDAQ-Modifiabilité](#rdaq-modifiabilité)
    - [RDTQ-Réduire la taille des modules](#rdtq-réduire-la-taille-des-modules)
    - [RDTQ-Augmenter la cohésion](#rdtq-augmenter-la-cohésion)
    - [RDTQ-Réduire le couplage](#rdtq-réduire-le-couplage)
    - [RDTQ-Defer binding](#rdtq-defer-binding)
    - [Relation entre les éléments architecturaux et les exigences de disponibilité](#relation-entre-les-éléments-architecturaux-et-les-exigences-de-disponibilité-1)
  - [RDAQ-Performance](#rdaq-performance)
    - [RDTQ-Contrôler la demande en ressources](#rdtq-contrôler-la-demande-en-ressources)
    - [RDTQ-Gérer les ressources](#rdtq-gérer-les-ressources)
    - [Relation entre les éléments architecturaux et les exigences de performance](#relation-entre-les-éléments-architecturaux-et-les-exigences-de-performance)
  - [RDAQ-Sécurité](#rdaq-sécurité)
    - [RDTQ-Détecter les attaques](#rdtq-détecter-les-attaques)
    - [RDTQ-Résister aux attaques](#rdtq-résister-aux-attaques)
    - [RDTQ-Réagir aux attaques](#rdtq-réagir-aux-attaques)
    - [RDTQ-Récupérer d'une attaque](#rdtq-récupérer-dune-attaque)
    - [Relation entre les éléments architecturaux et les exigences de sécurité](#relation-entre-les-éléments-architecturaux-et-les-exigences-de-sécurité)
  - [RDAQ-Testabilité](#rdaq-testabilité)
    - [RDTQ-Contrôle et observe l'état du système](#rdtq-contrôle-et-observe-létat-du-système)
    - [RDTQ-limiter la complexité](#rdtq-limiter-la-complexité)
    - [Relation entre les éléments architecturaux et les exigences de testabilité](#relation-entre-les-éléments-architecturaux-et-les-exigences-de-testabilité)
  - [RDAQ-Usabilité](#rdaq-usabilité)
    - [RDTQ-Supporter l'initiative de l'usager](#rdtq-supporter-linitiative-de-lusager)
    - [RDTQ-Supporter l'initiative du système](#rdtq-supporter-linitiative-du-système)
    - [Relation entre les éléments architecturaux et les exigences d'usabilité](#relation-entre-les-éléments-architecturaux-et-les-exigences-dusabilité)
  - [RDAQ-Interopérabilité](#rdaq-interopérabilité)
    - [RDTQ-Localiser](#rdtq-localiser)
    - [RDTQ-Gérer les interfaces](#rdtq-gérer-les-interfaces)
    - [Relation entre les éléments architecturaux et les exigences d'interopérabilité](#relation-entre-les-éléments-architecturaux-et-les-exigences-dinteropérabilité)
- [Vues architecturales](#vues-architecturales)
  - [Vues architecturales de type Module](#vues-architecturales-de-type-module)
    - [Vue #1](#vue-1)
  - [Vues architecturales de type composant et connecteur](#vues-architecturales-de-type-composant-et-connecteur)
    - [Vue #1](#vue-1-1)
  - [Vues architecturales de type allocation](#vues-architecturales-de-type-allocation)
    - [Vue #1 - Déploiement pour authentification](#vue-1---déploiement-pour-authentification)
- [Conclusion](#conclusion)
- [Documentation des interfaces](#documentation-des-interfaces)
# Page titre

# Introduction
Un service offert aux utilisateurs comporte souvent plusieurs microservices qui travaillent ensemble. Il est difficile de visualiser la complexité que cela peut engendrer en ce qui a trait à l'implémentation. Chaque système est unique et doit atteindre des objectifs de qualité différents. C'est pourquoi la bonne architecture d'un projet est cruciale pour la réalisation et la compréhension des clients externes.

Il est important pour un usager du transport en commun de savoir quel moyen de transport est le plus rapide entre la voiture et l'autobus. C'est pourquoi le but de ce laboratoire est de créer un système, fait de plusieurs microservices, qui offre une comparaison entre les deux moyens de transports.

Le laboratoire comporte 3 tâches, soit la réalisation de cas d'utilisation, la rédaction de la documentation architecturale et finalement l'intégration de microservices faits par d'autres équipes. Ces trois parties permettront d'avoir un système complet et fonctionnel qui possède tous les attributs de qualité. La réalisation des CU choisis par l'équipe, soit l'authentification et le chaos monkey, s'est faite à l'aide de Javascript et de Typescript. La rédaction de l'architecture s'est faite tout au long du développement afin de bien refléter les changements du système. L'intégration s'est faite à la toute fin, avec les cas d'utilisation réalisés par les autres équipes.


# Scénario d'objectif d'affaire
## OA-1. Faciliter le recrutement des nouveaux chargés de laboratoire.
<span>Notre architecture permet la réalisation du scénario qui a pour objectif de faciliter le recrutement de nouveaux chargés grâce à nos choix concernant l'usabilité. Nous avons choisi de séparer notre architecture en petits modules pour tous nos cas d'utilisation, ce qui rends la correction plus facile pour le chargé de laboratoire et lui permet de passer moins de temps à comprendre notre système. Nous croyons aussi que les diagrammes que nous avons réalisés pour chaque vue contribuent à faciliter la compréhension de nos choix d'architecture. Nous pensons que d'autres éléments faciliteraient le recrutement de nouveaux chargés de laboratoire. Notamment, la division du laboratoire en plusieurs étapes de réalisation. Cela éviterait que toutes les équipes ne demandent une correction complète durant les deux mêmes périodes. De plus, l'obligation d'intégrer le service d'autres équipes peut-être difficile à corriger si certaines équipes n'ont pas terminé leur laboratoire, nous croyons donc que d'offrir une alternative lorsque ce scénario se présente serait bénéfique pour recruter d'autres chargés.</span>


## OA-2. Validez si le transport par autobus est toujours plus rapide, peu importe l'heure de la journée
<span>Bien que notre équipe n'ai pas eu comme tâche de réaliser la comparaison des trajets, nous croyons que notre intégration de ce microservice facilite la réalisation de cet objectif d'affaire. En effet, les décisions que nous avons prises an réalisant nos microservices ont le potentiel de permettre au système d'être facilement modifié et de modifier l'itneraction avec d'autres services. Bien que cette fonction ne soit pas implémentée, nos choix architecturaux concernant la modifiabilité, soit de réduire le couplage et d'augmenter la cohésion, permettraient facilement d'ajouter des fonctions et donc, d'ajouter les éléments nécessaires à cet objectif d'affaire. </span>

# Cas d'utilisations
### **CU01** - Veux comparer les temps de trajet.

**Acteurs externe:** 
- Utilisateur: Veut pouvoir comparer le temps de trajet en automobile versus autobus.

**Précondition:** 
- L’utilisateur est connecté sur le site Web de comparaisons de trajet.
- Le microservice de comparaison temps de trajet est opérationnel.

**Évènement déclencheur:** 
- L’utilisateur veut se rendre à un endroit en particulier et se demande quel est le meilleur trajet en termes de temps.

**Scénario**
    
1. L’utilisateur sélectionne une intersection de départ et une intersection d'arrivée, ainsi que le taux de rafraichissement de la prise de mesure.
2. L’utilisateur sélectionne le service externe qu'il veut utiliser pour faire la comparaison des temps de trajet avec les donnés temps réel de la STM.
3. Le système affiche un graphique du temps de déplacement et met celui-ci à jour selon le taux de rafraîchissement.

**Évènement résultant:**
- Le système affiche un graphique des comparatifs de temps de déplacement qui se met à jour selon le taux de rafraîchissement.

**Postcondition:**  
- Le système est en attente d'une nouvelle commande de l'utilisateur

**Cas alternatifs:**

1. a  **Service externe:** Utiliser plusieurs [services externes](service-externe.md) disponibles pour faire le comparatif.

**Attributs de qualité**
Documenter l'ensemble des attributs de qualité qui s'appliquent à ce scénario en terme d'objectif et de mesure.    
#### CU01-D1 [**Disponibilité**](#add-disponibilité)
- (SC) Détecter les fautes
- (SC) Préparation et réparation
#### CU01-M1 [**Modifiabilité**](#add-modifiabilité)
- (SC) Augmenter la cohésion
- (SC) Différer la liaison
#### CU01-P1 [**Performance**](#add-performance)
- (SC) Contrôler la demande de ressources
#### CU01-S1 [**Sécurité**](#add-sécurité)
- (SC) Résister aux attaques
#### CU01-T1 [**Testabilité**](#add-testabilité)
- (SC) Limiter la complexité
#### CU01-U1 [**Usabilité**](#add-testabilité)
- (SC) Supporter l’initiative du système
- (SC) Supporter l’initiative de l’utilisateur
#### CU01-I1 [**Interopérabilité**](#add-interopérabilité)
- N/A

**Commentaires:**
### **CU02** - Veux pouvoir mettre le chaos dans les microservices.

**Acteurs externe:** 
- Chargé de laboratoire: Veut pouvoir faire la correction de chaque cas d'utilisation.

**Précondition:** 
- Tous les microservices sont opérationnels

**Évènement déclencheur:** 
- La documentation pour cet attribut est terminé et l'équipe demande au chargé de laboratoire de corriger celle-ci. 
- L'intégration est complété et l'équipe demande au chargé de laboratoire de corriger celle-ci
- L'implémentation est complété est l'équipe demande au chargé de laboratoire de corriger celle-ci.

**Scénario**
  1. Un mécanisme automatique et aléatoire de perturbation vient modifier l'architecture de votre système et vous devez vous assurer de quand même respecter les exigences client en terme d'attribut de qualité et de fonctionnalité.
    
**Évènement résultant:**
- L'architecture de votre système est perturbé par le mécanisme.
- Le système conserve un log des perturbations
- Le système conserve un log de comment le système a réagit pour résoudre le problème.

**Postcondition:**  
- Les mécanismes de traitement des attributs de qualité détectent le problème et modifie automatiquement l'architecture de votre système pour qu'il continue à respecter les exigences client.

**Cas alternatifs:**
- 1.a La perturbation consiste à détruire un microservice
- 1.b La perturbation consiste à augmenter la latence d'un microservice

**Attributs de qualité**

Documenter l'ensemble des attributs de qualité qui s'appliquent à ce scénario en terme d'objectif et de mesure.    

#### CU02-D1 [**Disponibilité**](#add-disponibilité) 
*Prévention de fautes*
- Augmenter les compétences

#### CU02-M1 [**Modifiabilité**](#add-modifiabilité)
N/A
#### CU02-P1 [**Performance**](#add-performance) 
N/A
#### CU02-S1 [**Sécurité**](#add-sécurité)
N/A
#### CU02-T1 [**Testabilité**](#add-testabilité) 
N/A
#### CU02-U1 [**Usabilité**](#add-usabilité)
*Supporter l'initiative de l'usager*
- "Aggregate"

*Supporter l'initiative du système*
- Maintenir le modèle de tâches
#### CU02-I1 [**Interopérabilité**](#add-interopérabilité)
*Gérer les interfaces*
- "Tailor interface"

*Localiser*
- Découvrir le service


### **CU03** - <span>Pas de CU03</span>

### **CU04** - Veux pouvoir s'authentifier.

**Acteurs externe:** 
- **Chargé de laboratoire:** Veut pouvoir faire la correction de chaque cas d'utilisation.

**Précondition:**
- tous les microservices sont opérationnels.

**Évènement déclencheur:** 
- La documentation pour cet attribut est terminé et l'équipe demande au chargé de laboratoire de corriger celle-ci. 
- L'implémentation est complété est l'équipe demande au chargé de laboratoire de corriger celle-ci.

**Scénario**
1.  Le (chargé de laboratoire) CL crée un compte utilisateur.
2. Le CL navige vers la page d'authentification
3.  Le CL entre le courriel utilisé pour créer le compte dans la fenêtre appropriée.
4.  Le CL entre le mot de passe utilisé pour créer le compte dans la fenêtre appropriée.
5. Le CL clique sur le bouton afin de se connecter.
6. Le service s'ouvre.

**Évènement résultant:**
- Le CL est authentifié en tant qu'utilisateur du service.
- Le système reconnaît les préférences (s'il y a lieu) de l'utilisateur.

**Postcondition:** 
- Le CL peut naviguer en étant connecté.

**Cas alternatifs:**
- 1.
	a) Le CL possède déjà un compte, le système rejette la création du compte.
- 6.
	a) Le courriel et le mot de passe ne correspondent pas à un compte existant, le système rejette l'authentification.

**Attributs de qualité**

#### CU04-D1 [**Disponibilité**](#add-disponibilité) 
*Détection de fautes*
- Doit répondre au ping/echo du service de monitoring.

*Détection de fautes*
- Si la copie passive (warm) ne reçoit pas de "heartbeat" pendant un certain temps, elle devient la copie principale et averti le service discovery.

*Réintroduction*
- Redémarrer le service qui s'est arrêté et il devient une copie passive (warm).

*Prévention de fautes*
- Dans le cas d’une perte de connexion avec la base de données, garder les opérations en mémoire et effectuer une synchronisation.

#### CU04-M1 [**Modifiabilité**](#add-modifiabilité)
*Réduire le couplage*
- Chaque module du système reste de petite taille.

*Augmenter la cohésion*
- Chaque module du système d'authentification a un rôle défini.

*Defer binding*
- Utilisation de l'injection de dépendances.

#### CU04-P1 [**Performance**](#add-performance) 
*Contrôler la demande en ressources*
- Utilisation d'une couche de “cache” afin d’éviter de contacter la base de données trop souvent.

#### CU04-S1 [**Sécurité**](#add-sécurité)
*Détecter les attaques*
- Conserver les adresses IP reçues précédemment pour les analyser.

*Résister aux attaques*
- Encrypter l'information du mot de passe des utilisateurs.
- Refuser les requêtes reçues par les adresses IP inconnues lors du login.

*Réagir aux attaques*
- Refuser l'accès après 3 demandes d'authentification erronées avec un minuteur.

#### CU04-T1 [**Testabilité**](#add-testabilité) 
*Contrôle et observe l’état du système*
- Utilisation de sources de données abstraites, pour pouvoir facilement injecter des "mocks" avec l’injection de dépendances.

*Limiter la complexité*
- Utilisation d’injection de dépendances pour bien cibler les responsabilités des modules et pouvoir les tester indépendamment.

#### CU04-U1 [**Usabilité**](#add-usabilité)
*Convivialité*
- Ce service doit être intuitif et suivre les normes des pages de connexion des applications en utilisant une adresse courriel et un mot de passe.

#### CU04-I1 [**Interopérabilité**](#add-interopérabilité)
*Localiser*
- Utilisation du service de découverte pour communiquer avec les autres micro services.


### **CU05** - Avoir une intercommunication entre microservices à l’aide d’une source unique de découverte de route.

**Acteurs externe:** 
- **Chargé de laboratoire :** Devra corriger ce cas d'utilisation.
- **Service d'authentification :** Devra authentifier les requêtes externes.
- **Tout autre microservice :** Seront en mesure de s'enregistrer.
- **Tout autre microservice :** Seront en mesure de faire rediriger leurs requêtes vers le bon microservice.

**Précondition:**
- Tous les microservices sont opérationnels.

**Évènement déclencheur:** 
- La documentation pour ce cas d'utilisation est terminé et l'équipe demande au chargé de laboratoire de corriger celle-ci.
- L'intégration est complété et l'équipe demande au chargé de laboratoire de corriger celle-ci

**Scénario**

1. Dans Postman, le chargé de laboratoire entre une route qu'il aimerait accéder.
2. La réponse en provenance de la route est renvoyée.

**Évènement résultant:**
- La réponse en provenance de la route est renvoyée.

**Postcondition:**
- Le système est en attente d'une nouvelle requête.

**Cas alternatifs:**
1. Scénario 1
    - a) Le chargé de laboratoire n'a pas attaché un jeton d'authentification à sa requête.
    - b) Le chargée de laboratoire a entré une route qui n'existe pas.
2. Scénario 2
    - a) Le microservice est indisponible.

**Attributs de qualité**

#### CU05-D1 [**Disponibilité**](#add-disponibilité) 
- **Détection de faute :** Ping/Echo
- **Préparation et réparation :** Rollback

#### CU05-M1 [**Modifiabilité**](#add-modifiabilité)
- **Réduire la taille des modules :** Split Module
- **Augmenter la cohésion :** Increase semantic coherence

#### CU05-P1 [**Performance**](#add-performance) 
- **Contrôler la demande en ressources :** Manage sampling rate

#### CU05-S1 [**Sécurité**](#add-sécurité)
- **Résister aux attaques :** Authenticate actors
- **Réagir aux attaques :** Lock computer

#### CU05-T1 [**Testabilité**](#add-testabilité) 
- **Limiter la complexité :** Limit structural complexity

#### CU05-U1 [**Usabilité**](#add-usabilité)

#### CU05-I1 [**Interopérabilité**](#add-interopérabilité)
- **Locate :** Discover service

**Commentaires:**

### **CU06** - Veux informer le mainteneur sur le status de vie des microservices

**Acteurs externe:** 
Les autres microservices

**Précondition:** 
- Connaitre l'adresse du Discovery Service
- Tous les microservices sont abonnés au microservice "Service Discovery"
- Le microservice de Monitoring connait la route du microservice "Service Discovery"

**Évènement déclencheur:** 
- Le système doit s'assurer que l'ensemble de ses microservices sont fonctionnels.

**Scénario**

1- Le microservice de Monitoring questionne le microservice "Service Discovery" sur les routes à ping

2- Le microservice "Service Discovery" retourne les routes des autres microservices

3- Le microservice de Monitoring questionne les microservices à savoir s'ils sont actifs (ping)

4- Les microservices répondent (echo) avec un 200 OK

**Évènement résultant:**
- Les microservices communiquent leur statut de vie
- Connaître quel microservice est en panne

**Postcondition:** 
S'assurer que les microservices sont fonctionnels.

**Cas alternatifs:**

4a- Un microservice ne répond pas.

5- Le microservice de Monitoring envoie un message d'alerte pour informer tous les microservices qu'un miscroservice est en panne.

**Attributs de qualité**

#### CU06-D1 [**Disponibilité**](#add-disponibilité) 
- (SC) Détection des fautes
- (SC) Prévention des fautes
- (SC) Préparation et réparation
- (SC) Réintroduction
#### CU06-M1 [**Modifiabilité**](#add-modifiabilité)
- (SC) Réduire la taille des modules
- (SC) Augmenter la cohésion
- (SC) Réduire le couplage
#### CU06-P1 [**Performance**](#add-performance) 
- (SC) Contrôler la demande en resources
#### CU06-S1 [**Sécurité**](#add-sécurité)
- (SC) Détecter les attaques
- (SC) Résister aux attaques
- (SC) Réagir aux attaques
- (SC) Récupérer d'une attaque

#### CU06-T1 [**Testabilité**](#add-testabilité)
- (SC) Controle et observe l’état du système
#### CU06-U1 [**Usabilité**](#add-usabilité)
- (SC) Supporter l'initiative du système
#### CU06-I1 [**Interopérabilité**](#add-interopérabilité)
- (SC) Gérer les interfaces.

**Commentaires:**

### **CU07** - Veux pouvoir informer le mainteneur sur l’état interne d’un service (exemple l’état du CPU)

**Acteurs externe:** 
- Le microservice "Service Discovery"
- Le microservice de Monitoring
- Les machines virtuelles

**Précondition:** 
- Connaitre l'adresse du Discovery Service
- Tous les microservices sont abonnés au microservice "Service Discovery"
- Le microservice "Service Discovery" connaît les routes des machines virtuelles

**Évènement déclencheur:** 
- Après s'être authentifié au système, le microservice de Monitoring vérifie si toute les machines virtuelles des autres microservices sont en bon état

**Scénario**

1- Après s'être authentifié au système, le microservice de Monitoring va récupérer les adresses IP des autres microservices

2- Le microservice de Monitoring demande aux VMs des statistiques sur leur composantes internes (CPU, GPU, RAM, etc...)

3- Si les statistiques sont normales, alors le microservice envoi un message pour lui indiquer que les machines virtuelles sur lesquelles les autres microservices sont hébergés vont bien et sont prêtes à être exploitées

4- Le système continue alors son bon fonctionnement

**Évènement résultant:**
- Le système connait quelle(s) machine(s) virtuelle(s) est/sont dysfonctionnelle(s)
- Le système ne se lancera pas tant que les machines virtuelles des autres microservices ne sont pas fonctionnelles

**Postcondition:** 
- S'assurer que les machines virtuelles et leurs composantes sont fonctionnelles

**Cas alternatifs:**

3a.1- Les statistiques d'une ou de plusieurs machines virtuelles sont anormales, indiquant un dysfonctionnement

3a.2- Le système indique aux machines virtuelles dysfonctionnelles de redémarrer

Retour à l'étape 2

**Attributs de qualité**

#### CU07-D1 [**Disponibilité**](#add-disponibilité) 
- (SC) Détection des fautes
- (SC) Prévention des fautes
- (SC) Préparation et réparation
- (SC) Réintroduction
#### CU07-M1 [**Modifiabilité**](#add-modifiabilité)
- (SC) Réduire la taille d'une module
- (SC) Augmenter la cohésion
- (SC) Réduir le couplage
- (SC) Defer binding
#### CU07-P1 [**Performance**](#add-performance) 
- (SC) Contrôler la demande en resources
#### CU07-S1 [**Sécurité**](#add-sécurité)
- (SC) Détecter les attaques
- (SC) Résister aux attaques
- (SC) Réagir aux attaques
- (SC) Récupérer d'une attaque
#### CU07-T1 [**Testabilité**](#add-testabilité) 
- (SC) Controle et observe l’état du système.
#### CU07-U1 [**Usabilité**](#add-usabilité)
- Supporter l'initiative du système
#### CU07-I1 [**Interopérabilité**](#add-interopérabilité)
- Gérer les interfaces

**Commentaires:**

### **CU08** - Veux avoir le temps d’un trajet en autobus

**Acteurs externe:** 
- Utilisateur: Veut pouvoir obtenir le temps d'un trajet en auto

**Précondition:** 
- Les microservices de proxy, d'authentification et d'obtention de trajet sont opérationnels
- Le serveur du service externe est opérationnel.

**Évènement déclencheur:** 
- L'utilisateur veut le temps d’un trajet en auto.

**Scénario**
1. L'utilisateur sélectionne une adresse de départ et une adresse d'arrivée.
2. L'utilisateur sélectionne le service externe qu'il veut utiliser pour obtenir le temps de trajet.
3. Le système affiche le temps de trajet le plus court.

**Évènement résultant:**
- Le système affiche les trois temps de trajet les plus courts avec des départs proches, ainsi que leurs heures de départ.

**Postcondition:** 
- Le système est en attente d'une nouvelle commande de l'utilisateur.

**Cas alternatifs:**
- N/A

**Attributs de qualité**

#### CU08-D1 [**Disponibilité**](#add-disponibilité) 
- (SC) Détecter les fautes
- (SC) Préparation et réparation
#### CU08-M1 [**Modifiabilité**](#add-modifiabilité)
- (SC) Augmenter la cohésion
- (SC) Réduire le couplage
- (SC) Différer la liaison
#### CU08-P1 [**Performance**](#add-performance) 
- N/A
#### CU08-S1 [**Sécurité**](#add-sécurité)
- (SC) Résister aux attaques
#### CU08-T1 [**Testabilité**](#add-testabilité) 
- (SC) Limiter la complexité
#### CU08-U1 [**Usabilité**](#add-usabilité)
- (SC) Supporter l’initiative système
#### CU08-I1 [**Interopérabilité**](#add-interopérabilité)
- N/A

**Commentaires:**

### **CU09** - Veux avoir le temps de trajet en auto

**Acteurs externe:**
- Utilisateur: Veut pouvoir obtenir le temps d'un trajet en auto

**Précondition:** 
- Les microservices de proxy, d'authentification et d'obtention de trajet sont opérationnels
- Le serveur du service externe est opérationnel.

**Évènement déclencheur:** 
- L'utilisateur veut le temps d’un trajet en auto.

**Scénario**
1. L'utilisateur sélectionne une adresse de départ et une adresse d'arrivée.
2. L'utilisateur sélectionne le service externe qu'il veut utiliser pour obtenir le temps de trajet.
3. Le système affiche le temps de trajet le plus court.

**Évènement résultant:**
- Le système affiche le temps de trajet le plus court.

**Postcondition:** 
- Le système est en attente d'une nouvelle commande de l'utilisateur.

**Cas alternatifs:**
- N/A

**Attributs de qualité**

#### CU09-D1 [**Disponibilité**](#add-disponibilité) 
- (SC) Détecter les fautes
- (SC) Préparation et réparation
#### CU09-M1 [**Modifiabilité**](#add-modifiabilité)
- (SC) Augmenter la cohésion
- (SC) Réduire le couplage
- (SC) Différer la liaison
#### CU09-P1 [**Performance**](#add-performance) 
- N/A
#### CU09-S1 [**Sécurité**](#add-sécurité)
- (SC) Résister aux attaques
#### CU09-T1 [**Testabilité**](#add-testabilité) 
- (SC) Limiter la complexité
#### CU09-U1 [**Usabilité**](#add-usabilité)
- (SC) Supporter l’initiative système
#### CU09-I1 [**Interopérabilité**](#add-interopérabilité)
- N/A

**Commentaires:**

### **CU10** - <span>Pas de CU10</span>

# Vue architecturale de contexte


## Présentation primaire
![Diagramme de contexte](./assets/context-diagram.png)
## Catalogue d'éléments
| Élement               | Description                                                                                                                                                                                                                                                                                                                                                                                                                            | lien vers document d'interfaces                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| Monitoring            | Ce microservice a en charge le monitoring du système en entier, afin de surveiller son bon fonctionnement et d'alerter les autres microservices en cas de panne ou de problème. Les autres microservices doivent s'enregistrer auprès de ce dernier, afin qu'il puisse les ping de temps à autre, en attendant une réponse de ces derniers.                                                                                        | http://www.etsmtl.ca                                                   |
| Chaos Monkey          | Ce microservice a été créé pour perturber les autres microservices, en simulant une panne. Il est utilisé pour les tuer, forçant la bonne implémentation du redémarrage ainsi que de s'assurer de la disponibilité du service.                                                                                                                                                                                                        |                                                                        |
| Discovery             | Le service Discovery est un patron d'architecture utilisé pour simplifier l'interaction entre un élément du système et un autre. Il agit comme une façade, centralisant toutes les interactions entre les différents microservices, ainsi que les acteurs utilisant le système. Le chargé de laboratoire ne pourra accéder aux autres microservices uniquement via ce service, afin de respecter l'esprit du patron.                |                                                                        |
| Authentification      | Ce service d'authentification et d'autorisation sert à verifier que l'utilisation du système par un utilisateur est sincère est justifié. L'utilisateur concerné doit alors s'authentifier dans le système avant de pouvoir effectuer une action, qui devra être autorisée par ce microservice. Les informations essentielles seront stockées dans une base de données afin d'assurer la persistence et la continuité du service. | [Document d'interface Authentification](interface-authentification.md) |
| Trajet                | Ce microservice est le point central de nos objectifs d'affaires pour les utilisateurs, Effectuer et comparer un trajet. Ce service contient la logique métier pour réaliser cette opération, en interargissant avec les services externes appropriés  afin de récolter les informations ainsi que pour "process" la requête du client et lui retourner les informations voulues.                                                     |                                                                        |
| Services Externes     | Cet élément représente l'ensemble des services avec lesquels le microservice de trajet devra communiquer pour récupérer les informations pertinentes. Il s'agit par exemple des horaires de la STM.                                                                                                                                                                                                                                    |                                                                        |
| Chargé de Laboratoire | Le chargé de Laboratoire est le principal utilisateur du système, chargé de vérifier son bon fonctionnement et de corriger les étudiants sur le travail qui a été accompli sur ce système.                                                                                                                                                                                                                                           |                                                                        |

## Guide de variabilité
### Services Externes
Les services externes sont configurables, divers et variés, ne s'agissant pas d'un seul service centralisé. Il peut s'agir de Google Maps, de la STM, etc. Ces différents services sont interchangeables et leur accès configurable.
### Base de Données pour l'authentification
Les paramètres pour l'accès à la base de données contenant les éléments pour l'identification, l'authentification et l'autorisation des utilisateurs est configurable via un fichier de configuration. Ces paramètres prennent la forme d'une URL.
### Ajout ou Retrait d'un microservice
Dans le cas du service de Chaos Monkey, du service de monitoring ainsi que du service Discovery, les différents microservices devant êtres appelés/notifiés/retournés/etc doivent d'abord êtres enregistrés auprès de ces derniers, via les routes correspondantes.
## Raisonnement
### Architecture Microservices
Une architecture microservices a été choisir pour une meilleure répartition de la charge de travail entre les différentes équipes. En effet, chaque microservice est indépendant et hautement cohésif, seule une interface commune doit être négociée et documentée pour être partagée avec les autres équipes dans un but commun. Cela permet une meilleure lisibilité du système et une plus grande harmonie, ainsi qu'une répartion équilibrée.
### Patron Discovery
Le patron d'architecture Discovery a été choisi afin d'agir comme un Guichet Unique. Dans le cadre d'une architecture microservices, cela a un grand avantage, qui est une meilleure accessibilité pour l'utilisateur, n'ayant qu'un intermédiaire avec qui communiquer, mais aussi pour les autres services : Chaque requête doit être faite via ce microservice avant d'atteindre le service demandé. Cela augmente la clarté pour les équipes de développement, n'ayant qu'un intermédiaire avec qui communiquer, diminue le couplage et augmente le potentiel de scalability du système.

# Conception axée sur les attributs de qualité
A partir des qualités associées à tous vos cas d'utilisation, réaliser un mini ADD pour comparer les différents tactiques et identifier clairement la raison de votre choix.

## ADD-[Disponibilité](#rdaq-disponibilité)

  |Identifiant|Description|
  |-----------|------------|
  |[CU01-D1](#cu01-d1-disponibilité)| N/A|
  |[CU02-D1](#cu02-d1-disponibilité)| Ce service est concerné par la sous-catégorie "Prévention des fautes" |
  |[CU03-D1](#cu03-d1-disponibilité) |N/A
  |[CU04-D1](#cu04-d1-disponibilité)| Ce service est concerné par les sous-catégories "Détection de faute", "Préparation et réparation", et "Réintroduction" |
  |[CU05-D1](#cu05-d1-disponibilité) |N/A
  |[CU06-D1](#cu06-d1-disponibilité) |N/A
  |[CU07-D1](#cu07-d1-disponibilité) |N/A
  |[CU08-D1](#cu08-d1-disponibilité) |N/A
  |[CU09-D1](#cu09-d1-disponibilité) |N/A
  |[CU10-D1](#cu10-d1-disponibilité) |N/A

### ADD-[détection de faute](#rdtq-détection-de-faute)
<div class="concept disponibilite">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Ping/Echo</li>|<li>Relativement simple à implémenter</li>| <li>Nécessite que la copie secondaire connaisse l'adresse de la copie principale</li>|M|M|
| <li>Heartbeat</li>|<li>Relativement simple à implémenter</li>| <li>Nécessite que la copie principale connaisse l'adresse de la copie secondaire</li>|M|L|
| <li>Self-test</li>|<li>Réduit le nombre de communications inter-processus</li>| <li>Une autre tactique serait nécessaire pour notifier la copie secondaire que la copie principale n'est plus fonctionnelle</<li>|M|H|
</div>
<span>En combinaison avec les autres tactiques de disponibilité que nous avons décidé d'utiliser, nous avons déterminé que la tactique "Heartbeat" était le plus logique à utiliser. En effet, dans le cadre de la gestion de la copie principale/secondaire, la copie principale sait automatiquement comment communiquer avec la copie secondaire. Un envoi de messages dans cette direction était donc naturel. Si nous avions décidé d'utiliser la tactique "Ping/echo", nous aurions dû également ajouter une configuration initiale permettant à la copie secondaire de communiquer avec la copie principale. Cela aurait augmenté la complexité de la logique de disponibilité. Pour la même raison, utiliser un Self-test aurait été plus compliqué, car il aurait été difficile de notifier la copie secondaire d'un problème au niveau de la copie principale (perte de réseau, crash complet, etc.).</span>

### ADD-[Préparation et réparation](#rdtq-préparation-et-réparation)
<div class="concept disponibilite">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Redondance active</li>|<li>Permet de remplacer la copie principale par une copie secondaire</li>| <li>Nécessite que la copie secondaire reçoive tous les messages envoyés à la copie principale</li><li>Ajoute de la complexité à l'application</li>|M|H|
| <li>Redondance passive</li>|<li>Permet de remplacer la copie principale par une copie secondaire</li><li>Dans notre contexte, la copie secondaire n'a pas à se synchroniser avec la copie principale</li>| <li>Ajoute de la complexité à l'application</li><li>Nécessite de persister à la base de données toutes les opérations</li>|M|M|

<span>Nous avons décidé d'utiliser la tactique de redondance passive, car nous trouvions cette solution plus simple en raison du contexte particulier de notre application. En effet, puisque nous persistons tous les changements à la base de données, aucune synchronisation n'est nécessaire; la copie secondaire est toujours à jour car ses opérations nécessitent de communiquer avec la base de données, qui est à jour. Ainsi, une copie active n'apporterait pas de valeur ajoutée, mais ajouterait encore plus de complexité.</span>

### ADD-[Réintroduction](#rdtq-réintroduction)
<div class="concept disponibilite">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Shadow</li>|<li>Permet de valider le comportement de la copie avant de la rendre disponible au monde extérieur</li>| <li>Augmente la complexité</li><li>Augmente le temps avant que le composant soit disponible</li>|M|H|
| <li>State Resynchronization</li>|<li>Permet de mettre à jour la copie afin qu'elle soit prête à recevoir des appels si elle doit devenir la copie principale </li>| <li>Ajoute la tâche de synchroniser la copie secondaire aux responsabilités de la copie principale</li>|M|M|
| <li>Escalating restart</li>|<li>Permet de rajouter des fonctionnalités à la copie secondaire progressivement</li>|<li>La complexité de l'application ne justifie pas l'ajout progressif de fonctionnalités, puisqu'elle est relativement simple</li>|L|H|
</div>
<span>Nous avons choisi d'implémenter la tactique "State Resynchronization" puisque notre stratégie de copies principale/secondaire s'y prêtait bien. En effet, lorsque la copie secondaire devient la copie principale et démarre une nouvelle copie secondaire, celle-ci doit être synchronisée. Si on utilisait les tactiques "Shadow" ou "Escalating restart", cela augmenterait simplement le temps avant que la copie secondaire soit prête, sans augmenter la valeur associée.</span>

### ADD-[Prévention des fautes](#rdtq-prévention-des-fautes)  
<div class="concept disponibilite">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Transactions</li>|<li>Permet d'éviter des problèmes de corruption de la base de données</li>|<li>Les requêtes envoyées à la base de données sont trop simples pour profiter des transactions</li>|L|M|
| <li>Exception Prevention</li>|<li>Permet de réduire le nombre d'exceptions, ou de cas d'erreurs, qui apparaissent lors de l'exécution de l'application</li>| <li>L'utilisation de Typescript et Javascript cachent déjà la majorité des exceptions normalement associées à cette tactique</li>|L|L|
| <li>Increase Competence Set</li>|<li>Permet au logiciel de fonctionner même si d'autres microservices ont des erreurs</li>|<li>Se heurte au [théorème de Brewer](https://fr.wikipedia.org/wiki/Th%C3%A9or%C3%A8me_CAP); la cohérence est sacrifiée au profit de la disponbilité et de la tolérance au partionnement lors d'une erreur</li>|H|M|
</div>
<span>Nous avons choisi d'utiliser la tactique "Increase Competence Set". En effet, si le microservice nous donnant la liste des microservices meurt, ce qui est très probable puisque cette tactique est utilisée dans le cadre du microservice de Chaos, nous devons être en mesure de contrôler les autres microservices en attendant qu'il redémarre.</span>

## ADD-[Modifiabilité](#rdaq-modifiabilité)
  |Identifiant|Description|
  |-----------|------------|
  |[CU01-M1](#cu01-m1-modifiabilité) | N/A|
  |[CU02-M1](#cu02-m1-modifiabilité) | N/A|
  |[CU03-M1](#cu03-m1-modifiabilité) | N/A|
  |[CU04-M1](#cu04-m1-modifiabilité) | Ce service est concerné|
  |[CU05-M1](#cu05-m1-modifiabilité) | N/A|
  |[CU06-M1](#cu06-m1-modifiabilité) | N/A|
  |[CU07-M1](#cu07-m1-modifiabilité) | N/A|
  |[CU08-M1](#cu08-m1-modifiabilité) | N/A|
  |[CU09-M1](#cu09-m1-modifiabilité) | N/A|
  |[CU10-M1](#cu10-m1-modifiabilité) | N/A|

### ADD-[Réduire la taille des modules](#rdtq-réduire-la-taille-des-modules)
<div class="concept modifiabilite">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Split Module</li>| réduit le couts de changement future | N/A |H|H|
</div>
<span>Nous avons choisi cette tatique parce que si le module en cours de modification comprend de nombreuses fonctionnalités, le coût de la modification sera probablement élevé. Pour remedier a cette situation, nous pouvons affiner le module en plusieurs modules plus petits ce qui devrait réduire le coût moyen des changements futurs</span>

### ADD-[Augmenter la cohésion](#rdtq-augmenter-la-cohésion)
<div class="concept modifiabilite">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Increase Sementic Coherance</li> | <li>Si la responsabilité de A et B dans un module n'a pas le même objectif, elles doivent être placées dans des modules différents</li>| N/A |H|H|
</div>
<span> La tactique choisie est <i>Increase Sementic coherance</i>. Nous avons choisi cette tactique pour que chaque module possède ses responsabilités ce qui crée un code facile à comprendre et à modifier. De plus, cette tactique garde les dépenses séparées ce qui réduit le couplage et augmente la cohésion. </span>

### ADD-[Réduire le couplage](#rdtq-réduire-le-couplage)
<div class="concept modifiabilite">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Encapsulate</li>| <li>réduit la probabilité qu'un changement fait dans un module ce propage dans un autre module.</li>| limite les façons dont les responsabilités externes peuvent interagir avec le module |H|M|
| <li>Refactor</li>|<li>Réduis la duplication de code.</li>| Couteux|M|H|
| <li>Abstract common service</li>|<li>Toute modification du service se produirait en un seul endroit</li>| Peut devenir très complexe à implémenter |B|M|
</div>
<span>La tactique choisie est <i>Encapsulate</i>. Nous avons choisie cette tactique pour réduire la probabilité qu'un changement fait dans un module ce propage dans un autre module. </span>

### ADD-[Defer binding](#rdtq-defer-binding)
<div class="concept modifiabilite">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Defer binding</li>|<li>laisser les ordinateurs gérer un changement autant que possible réduira presque toujours le coût de ce changement</li>| <li>Mettre en place les mécanismes pour faciliter cette liaison tardive a tendance à être plus coûteux</li>|M|M|
</div>
<span>Nous avons utilisé la tactique de defer binding pour liers des valuers au moment du déploiment de l'application en utilisant un fichier de ressource (.env) .</span>


## ADD-[Performance](#rdaq-performance)
  |Identifiant|Description|
  |---------------------------------|--------------------------|
  |[CU01-P1](#cu01-p1-performance) | N/A |
  |[CU02-P1](#cu02-p1-performance) | N/A |
  |[CU03-P1](#cu03-p1-performance) | N/A |
  |[CU04-P1](#cu04-p1-performance) | Ce service est concerné |
  |[CU05-P1](#cu05-p1-performance) | N/A |
  |[CU06-P1](#cu06-p1-performance) | N/A |
  |[CU07-P1](#cu07-p1-performance) | N/A |
  |[CU08-P1](#cu08-p1-performance) | N/A |
  |[CU09-P1](#cu09-p1-performance) | N/A |
  |[CU10-P1](#cu10-p1-performance) | N/A |
  
### ADD-[Contrôler la demande en ressources](#rdtq-contrôler-la-demande-en-ressources)
<div class="concept performance">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Incrémenter l'efficacité des ressources</li>|Augmenter l'efficacité des algorithmes permettrait une connexion plus rapide lorsque le système recherche les informations nécessaire pour connecter l'utilisateur| Étant donné qu'il y a peu de calculations, il n'y aura pas une grande différence dans la performance|M|M|
| <li>Couper le temps d'exécution</li>|Si la requête d'un utilisateur prends trop de temps à s'effectuer, cela ne bloquera pas d'autres utilisateurs potentiels ayant besoin de l'accès| Un utilisateur pourrait demeurer bloquer et ne jamais pouvoir se connecter|M|M|
| <li>Réduire les coûts d'utilisation</li>|Utiliser un intermédiaire pour réduire les coûts permet un accès moins fréquent à la base de données et donc un temps de réponse plus rapide| La fidélité de la cache par rapport à la base de données dépends du délai de temps auquel elle est mise à jour, cela pourrait donc conduire à une cache contenant des données qui ne sont plus les bonnes |M|M|
</div>
<span> Nous avons choisi la tactique "Réduire les coûts d'utilisation" puisque la cache est un intermédiaire qui non seulement augmente la performance, mais conserve aussi une copie de certaines données en cas d'erreur. De plus, c'est un méchanisme qui, s'il est mis à jour fréquemment, est généralement très fiable.</span>

### ADD-[Gérer les ressources](#rdtq-gérer-les-ressources)
<div class="concept performance">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Introduire la concurrence </li>|De la concurrence permettrait à beaucoup de connexions d'être effectuées en même temps, réduisant la charge et l'attente. | Plusieurs fils sont complexes à implémenter dans le cas de l'authentification|M|M|
| <li>Maintenir plusieurs copies des données </li>|L'utilisation d'un load balancer permettrait de s'assurer que toutes le nombre de requête ne dépasse pas la limite du serveur en utilisant plusieurs serveurs, cela veut dire qu'il y aurait moins de chance qu'une connexion soit refusée par manque de ressources et que les autres connexions se font plus rapidement | L'utilisation de plusieurs serveurs peut s'avérer couteuse et ne s'applique pas à notre laboratoire|M|M|
| <li>tactique 3</li>|avantages| désavantages|M|M|
</div>
<span>Nous avons choisi la tactique "xxx"</span>

## ADD-[Sécurité](#rdaq-sécurité)

| Identifiant                  | Description              |
|------------------------------|--------------------------|
| [CU01-P1](#cu01-s1-sécurité) | N/A                      |
| [CU02-P1](#cu02-s1-sécurité) | N/A                      |
| [CU03-P1](#cu03-s1-sécurité) | N/A                      |
| [CU04-P1](#cu04-s1-sécurité) | Ce service est concerné. |
| [CU05-P1](#cu05-s1-sécurité) | N/A                      |
| [CU06-P1](#cu06-s1-sécurité) | N/A                      |
| [CU07-P1](#cu07-s1-sécurité) | N/A                      |
| [CU08-P1](#cu08-s1-sécurité) | N/A                      |
| [CU09-P1](#cu09-s1-sécurité) | N/A                      |
| [CU10-P1](#cu10-s1-sécurité) | N/A                      |

### ADD-[Détecter les attaques](#rdtq-détecter-les-attaques)
<div class="concept securite">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Détecter l'intrusion</li>|Permet d'identifier des motifs récurrents et connaitre les bons utilisateurs| Aucun dans ce contexte|M|M|
| <li>Vérifier l'intégrité du message</li>|Un très petit changement sera détecté| Difficile dans le cas de l'authentification|M|M|
</div>
<span>Nous avons choisi la tactique "Détecter l'intrusion" puisqu'elle est une bonne manière de reconnaître un utilisateur qui n'est pas normal et qu'elle est simple à implémenter en comparant les adresses IP</span>

### ADD-[Résister aux attaques](#rdtq-résister-aux-attaques)
<div class="concept securite">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Identifier les acteurs</li>|L'identification permet de facilement refuser un utilisateur anormal| Pourrait refuser l'accès à un utilisateur légitime|M|M|
| <li>Limiter l'accès</li>|Permet de résister aux utilisateurs mal intentionnés| Tous les utilisateurs doivent avoir accès au service|M|M|
| <li>Encrypter les données</li>|Permet de garantir que les données des utilisateurs ne sont pas volées|L'encryption n'est pas sans failles|M|M|
</div>
<span>Nous avons choisi la tactique "Identifier les acteurs" puisque malgré qu'il y ait un risque qu'un utilisateur légitime se voit refuser l'accès, cette technique est sécuritaire et s'applique bien au contexte de l'authentification où les utilisateurs reviennent plus d'une fois.</span>


### ADD-[Réagir aux attaques](#rdtq-réagir-aux-attaques)
<div class="concept securite">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Barrer l'ordinateur</li>|Barrer le site assure qu'aucune autre attaque n'ait lieu| plus aucun utilisateur ne peut accéder au service|M|M|
| <li>Révoquer l'accès</li>|Permet de protéger le service d,une personne qui essaie plusieurs mots de passes| pourrait bloquer un utilisateur légitime qui a oublié son mot de passe|M|M|
</div>
<span>Nous avons choisi la tactique "Révoquer l'accès" puisqu'un utilisateur qui oublie son mot de passe peut potentiellement créer un autre compte, tandis qu'une attaque sera certainement bloquée.</span>

### ADD-[Récupérer d'une attaque](#rdtq-récupérer-dune-attaque)
<div class="concept securite">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Maintenir une piste d'audits</li>|La piste d'audits permet de retracer les attaqueurs| ne change pas le système si des dommages ont été faits|M|M|
</div>
<span>Nous avons choisi la tactique "Maintenir une piste d'audits"</span>


## ADD-[Testabilité](#rdaq-testabilité)

| Identifiant                     | Description              |
|---------------------------------|--------------------------|
| [CU01-P1](#cu01-t1-testabilité) | N/A                      |
| [CU02-P1](#cu02-t1-testabilité) | N/A                      |
| [CU03-P1](#cu03-t1-testabilité) | N/A                      |
| [CU04-P1](#cu04-t1-testabilité) | Ce service est concerné. |
| [CU05-P1](#cu05-t1-testabilité) | N/A                      |
| [CU06-P1](#cu06-t1-testabilité) | N/A                      |
| [CU07-P1](#cu07-t1-testabilité) | N/A                      |
| [CU08-P1](#cu08-t1-testabilité) | N/A                      |
| [CU09-P1](#cu09-t1-testabilité) | N/A                      |
| [CU10-P1](#cu10-t1-testabilité) | N/A                      |


### ADD-[Controle and observe l'état du système](#rdtq-contrôle-et-observe-létat-du-système)
<div class="concept testabilite">

| Concept de design               | Pour                                                                                                                                                                 | Contre                                                                                                | Valeur | Cout |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|--------|------|
| <li>Abstract Data Sources</li>  | <li>Isolation des modules importants</li><li>Encourage cohésion</li><li>Encourage indépendance des modules</li><li>Encourage meilleur définition des interfaces</li> | <li>Il faut déterminer quels modules sont concernés. La limite, frontière peut être floue.</li>     | H      | M    |
| <li>Specialized Interfaces</li> | <li>Très utile dans de nombreux scénarios</li><li>Encourage généralisation et standardisation des modules</li>                                                      | <li>Peu utile dans notre microservice d'authentification pour du test</li><li>"Bloating" du code</li> | B      | B    |
| <li>Sandbox</li>                | <li>Isolation complète</li><li>Forte cohésion</li>                                                                                                                  | <li>Impossible de tester les modules indépendamment</li>                                              | M      | H    |
</div>
Nous avons choisi Abstract Data Sources.
Cette tactique a été peu coûteuse à implémenter, car nous avons pensé notre système autour de modules indépendants dès le départ (Separation of Concerns).
Il a just fallu déterminer quels modules devraient êtres testés et si cette tactique pouvait être appliquée à ceux ci ou non.
De plus, cette tactique rapporte la plus haute valeur ajoutée à note application.
Non seulement elle est plus testable, mais également plus modifiable et plus maintenable.
Cette tactique a donc la plus haute valeur ajoutée.

### ADD-[Limiter la complexité](#rdtq-limiter-la-complexité)

<div class="concept testabilite">

| Concept de design                    | Pour                                                                                                           | Contre                                                                                                                                      | Valeur | Cout |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|--------|------|
| <li>Limit Structural Complexity</li> | <li>Permet d'accomplir d'autres AQs comme Modifiabilité</li><li>Réduit couplage</li><li>Augmente cohésion</li> | <li>Complexe à mettre en oeuvre en général</li><li>Risque d'entrer en contradiction avec d'autres patterns utilisant le polymorphisme</li> | H      | M    |
| <li>Limit Nondeterminism</li>        | <li>Augmente prédictabilité du système</li>                                                                   | <li>Pas applicable dans le cadre d'un service d'authentification/autorisation</li>                                                          | B      | M    |
</div>
Nous avons choisi Limit Structural Complexity. Ce choix a été assez rapide, pour 2 raisons principales.
La première, la tactique de limiter le nondéterminisme ne s'applique peu, voir pas du tout, dans le cadre d'un microservice d'authentification et d'authorisation, qui est déterministe par définition (un login correspond à un token qui est unique. Il ne peut pas en générer un autre à un même instant T).
La deuxième raison est qu'il a été facile d'implémenter cette tactique pour notre système, facielement découpable en modules indépendants, très cohésifs avec peu de couplage.


## ADD-[Usabilité](#rdaq-usabilité)
  |Identifiant|Description|
  |-----------|------------|
  |[CU01-U1](#cu01-u1-usabilité) | N/A
  |[CU02-U1](#cu02-u1-usabilité) |Ce service est concerné|
  |[CU03-U1](#cu03-u1-usabilité) | N/A
  |[CU04-U1](#cu04-u1-usabilité) | N/A
  |[CU05-U1](#cu05-u1-usabilité) | N/A
  |[CU06-U1](#cu06-u1-usabilité) | N/A
  |[CU07-U1](#cu07-u1-usabilité) | N/A
  |[CU08-U1](#cu08-u1-usabilité) | N/A
  |[CU09-U1](#cu09-u1-usabilité) | N/A
  |[CU10-U1](#cu10-u1-usabilité) | N/A

### ADD-[Supporter l'initiative de l'usager](#rdtq-supporter-linitiative-de-lusager)
<div class="concept usabilite">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Cancel</li>|<li>Permettre à l'utilisateur d'annuler une erreur commise</li>| <li>Ajoute beaucoup de complexité à l'exécution de la requête</li>|M|H|
| <li>Undo</li>|<li>Permettre à l'utilisateur d'annuler une erreur commise</li>| <li>Ajoute beaucoup de complexité à l'exécution de la requête</li>|M|H|
| <li>Pause/Resume</li>|<li>Permettre à l'utilisateur de valider que sa commande est correcte avant de continuer</li>| <li>Ajoute beaucoup de complexité à l'exécution de la requête</li>|M|H|
| <li>Aggregate</li>|<li>Permet à l'utilisateur d'effectuer plusieurs actions en même temps, ce qui réduit le nombre de clics nécessaires</li>|<li>Ajoute un peu de complexité à l'exécution de la requête</li> |H|L|
</div>
<span>Nous avons choisi d'utiliser la tactique "Aggregate", puisqu'elle est la plus simple à implémenter et que la valeur ajoutée est plus grande. En effet, toutes les autres tactiques se concentrent sur la modification d'une requête après son envoi, ce qui est moins utile dans notre contexte puisque la simplicité des requêtes réduit le risque d'erreurs. Il est ainsi plus utile de pouvoir permettre à l'utilisateur de réduire le nombre de clics pour affecter plusieurs microservices, ce qui réduit également le nombre d'erreurs.</span>

### ADD-[Supporter l'initiative du système](#rdtq-supporter-linitiative-du-système)
<div class="concept usabilite">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Maintain task model</li>|N/A| Ne s'applique pas|L|M|
| <li>Maintain user model</li>|N/A| Ne s'applique pas|L|M|
| <li>Maintain system model</li>|<li>Permet à l'utilisateur de connaître l'état de sa requête</li>| <li>Ajoute beaucoup de complexité au système</li>|M|H|
</div>
<span>On ne peut pas utiliser la tactique "Maintain task model" puisque la tâche à effectuer par l'utilisateur est beaucoup trop simple pour en bénéficier, et on ne peut pas utiliser la tactique "Maintain user model" pour la même raison. On doit donc utiliser la tactique "Maintain system model", implémentée de manière à pouvoir fournir à l'utilisateur l'état d'une requête. Cette tactique demande cependant beaucoup d'effort à implémenter puisque l'on doit retourner à l'utilisateur une manière de suivre l'état de sa requête avant la complétion de celle-ci, ce qui demande d'ajouter des tâches en arrière-plan.</span>

## ADD-[Interopérabilité](#rdaq-interopérabilité)
  |Identifiant|Description|
  |-----------|------------|
  |[CU01-I1](#cu01-i1-interopérabilité)|N/A | 
  |[CU02-I1](#cu02-i1-interopérabilité)|Ce service est concerné pour toutes les sous-catégories|
  |[CU03-I1](#cu03-i1-interopérabilité)|N/A |
  |[CU04-I1](#cu04-i1-interopérabilité)|Ce service est concerné pour la sous-catégorie "Localiser" |
  |[CU05-I1](#cu05-i1-interopérabilité)|N/A |
  |[CU06-I1](#cu06-i1-interopérabilité)|N/A |
  |[CU07-I1](#cu07-i1-interopérabilité)|N/A |
  |[CU08-I1](#cu08-i1-interopérabilité)|N/A |
  |[CU09-I1](#cu09-i1-interopérabilité)|N/A |
  |[CU10-I1](#cu0-0i1-interopérabilité)|N/A |
### ADD-[Localiser](#rdtq-localiser)
<div class="concept interoperabilite">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Discover Service</li>|<li>Permet de gérer dynamiquement quels services sont disponibles</li>| <li>Augmente le nombre d'appels qui doivent être faits afin de communiquer avec d'autres microservices</li>|H|M|
</div>
<span>Nous avons choisi la tactique "Discover Service" car elle nous permet, dans tous nos microservices, de connaître les autres microservices existants. En effet, surtout dans le cas du microservice de Chaos, il est impératif d'obtenir facilement une liste à jour de tous les microservices déployés.</span>

### ADD-[Gérer les interfaces](#rdtq-gérer-les-ressources)
<div class="concept interoperabilite">

|Concept de design| Pour | Contre| Valeur | Cout|
|-----------------|------|-------|--------|-----|
| <li>Orchestrate</li>|<li>Permet de faire collaborer plusieurs services indépendants afin d'effectuer une action plus complexe</li>|<li>Les actions effectuées par nos microservices ne sont pas assez complexes pour nécessiter l'utilisation de plusieurs petits services indépendants. Cela augmenterait beaucoup la complexité et la latence.</li>|L|H|
| <li>Tailor interface</li>|<li>Permet de configurer certaines interfaces afin d'offrir plus ou moins de fonctionnalités selon certains paramètres, ici le type d'utilisateur (normal ou "poweruser")</li>| <li>Augmente la complexité de l'application et la configuration requise pour faire certains appels</li>|M|M|
</div>
<span>Nous avons choisi la tactique "Tailor interface" car celle-ci nous permet d'offrir des fonctionnalités plus puissantes à certains utilisateurs, ce qui est utile puisque la nature du microservice de Chaos se prête bien à la présence de différents types d'utilisateur. Dans notre cas, nous avons décidé d'offrir une fonctionnalité de "Batching", ou de faire plusieurs appels en un, aux utilisateurs de type "poweruser".</span>

# Réalisation des cas d'utilisation
### [**RDCU-CU01**](#cu01---veux-comparer-les-temps-de-trajet) - Veux comparer les temps de trajet.
![Diagramme](https://github.com/LOG430-MicroServices/LOG430-STM/blob/7171e70fa977ab73ffbbc2199c3a855b0d2a67da/out/doc/plantuml/RDCU_Equipe6/Service_trajet_rdcu/Service_trajet_rdcu.png)
### [**RDCU-CU02**](#cu02---veux-pouvoir-mettre-le-chaos-dans-les-services-en-mode) - Veux pouvoir mettre le chaos dans les services en mode.
![DiagrammeSéquenceChaosMonkey](https://github.com/LOG430-MicroServices/LOG430-STM/blob/db770d083bcb9df3bec865126db4e2f82900424b/out/doc/plantuml/chaos/DiagrammeS%C3%A9quence_CU02/DiagrammeSequenceCU02.png)

### [**RDCU-CU04**](#cu04---veux-pouvoir-s'authentifier) - Veux pouvoir s'authentifier
![DiagrammeSéquenceAuthentification](https://github.com/LOG430-MicroServices/LOG430-STM/blob/6e9ba49ebaee64a86782a90e38347d89530386c0/out/doc/plantuml/auth/DiagrammeS%C3%A9quence_CU04/DiagrammeS%C3%A9quence_CU04.png)
### **RDCU-CU05** - 
![Diagramme](https://github.com/LOG430-MicroServices/LOG430-STM/blob/7171e70fa977ab73ffbbc2199c3a855b0d2a67da/out/doc/plantuml/RDCU_Equipe4/Sercice_discovery_rdcu/Sercice_discovery_rdcu.png)
### **RDCU-CU06** - 
![Diagramme](https://github.com/LOG430-MicroServices/LOG430-STM/blob/7171e70fa977ab73ffbbc2199c3a855b0d2a67da/out/doc/plantuml/RDCU_Equipe8/RDCU_CU6/RDCU_CU6.png)
### **RDCU-CU07** - 
![Diagramme](https://github.com/LOG430-MicroServices/LOG430-STM/blob/41f6aa48c32acf711d49baa6946c14cb283d90a5/out/doc/plantuml/RDCU_Equipe8/RDCU_Service_Monitoring/RDCU_Service_Monitoring.png)
### **RDCU-CU08** - 
![Diagramme](https://github.com/LOG430-MicroServices/LOG430-STM/blob/7171e70fa977ab73ffbbc2199c3a855b0d2a67da/out/doc/plantuml/RDCU_Equipe6/RDCU_CU8/RDCU_CU8.png)
### **RDCU-CU09** - 
![Diagramme](https://github.com/LOG430-MicroServices/LOG430-STM/blob/7171e70fa977ab73ffbbc2199c3a855b0d2a67da/out/doc/plantuml/RDCU_Equipe6/RDCU_CU9/RDCU_CU9.png)

# Réalisation des attributs de qualité

## RDAQ-[Disponibilité](#add-disponibilité) 

  ###  [RDTQ-Détection de faute](#add-détection-de-faute)

  ![Diagramme - Détection de faute](../out/doc/plantuml/auth/Disponibility-DetectFaults/Disponibility-DetectFaults.png)

  <span>La copie principale envoie des messages périodiques à la copie secondaire, appelés Heartbeats, de manière à lui faire savoir qu'elle est toujours disponible.</span>

  ### [RDTQ-Préparation et réparation](#add-préparation-et-réparation)

  ![Diagramme - Préparation et réparation](../out/doc/plantuml/auth/Disponibility-Repair/Disponibility-Repair.png)

  <span>La redondance passive est utilisée afin de toujours avoir une copie de l'application qui est prête à recevoir les appels.</span>

  ### [RDTQ-Réintroduction](#add-réintroduction)

  ![Diagramme - Réintroduction](../out/doc/plantuml/auth/Disponibility-Reintroduce/Disponibility-Reintroduce.png)

  Si la copie secondaire devient principale, elle doit démarrer une autre copie secondaire afin de maintenir deux copies en tout temps.
  
  ### [RDTQ-Prévention des fautes](#add-prévention-des-fautes) 

  ![Diagramme - Prévention des fautes](../out/doc/plantuml/chaos/Disponibility-PreventFaults/RDTQ%20Disponbilit%C3%A9%20%20%20Pr%C3%A9vention%20de%20fautes.png)

  Afin de permettre au Chaosmonkey de fournir des services même si le ServiceDiscovery est indisponible, on garde la liste de services en cache.

  ### Relation entre les éléments architecturaux et les exigences de disponibilité
 |Identifiant|Éléments|Description de la responsabilité|
 |-----------|--------|-------------------------------|
 |[CU02-D1](#cu02-d1-disponibilité) |Chaosmonkey |Doit être disponible même si le Service Registry est hors-ligne|
 |[CU02-D2](#cu02-d2-disponibilité) |Service Registry |Doit donner la liste des services|
 |[CU04-D1](#cu04-d1-disponibilité) |Copie principale|Doit démarrer la copie secondaire et lui envoyer des heartbeats|
 |[CU04-D2](#cu04-d2-disponibilité) |Copie secondaire |Doit s'assurer que la copie principale fonctionne. Sinon, elle devient la copie principale et démarre une nouvelle copie secondaire | 
 |[CU04-D2](#cu04-d2-disponibilité) |Nouvelle copie secondaire |Doit se synchroniser afin de pouvoir être disponible si la copie secondaire arrête de fonctionner |
 |[CU04-D3](#cu04-d3-disponibilité) |Service Registry |Doit être notifié d'un changement de la copie principale |
  
## RDAQ-[Modifiabilité](#add-modifiabilité)

  ###  [RDTQ-Réduire la taille des modules](#add-réduire-la-taille-des-modules)

   ![Diagramme - Réduire la taille des modules](../out/doc/plantuml/auth/Modifiabilite-ReduceModuleSize/Modifiabilite-ReduceModuleSize.png)

  ### [RDTQ-Augmenter la cohésion](#add-augmenter-la-cohésion)
  <span>Increase semantic coherance</span>
  
   ![Diagramme - Augmenter la cohésion](../out/doc/plantuml/auth/Modifiabilite-AugmenteCohesion/Modifiabilite-AugmenteCohesion.png)

  ### [RDTQ-Réduire le couplage](#add-réduire-le-couplage)
  <span >Encapsulation</span>
  
   ![Diagramme - Réduire le couplage](../out/doc/plantuml/auth/Modifiabilite-RéduireCouplage/Modifiabilite-RéduireCouplage.png)

  ### [RDTQ-Defer binding](#add-defer-binding)
  
   ![Diagramme - Defer binding](../out/doc/plantuml/auth/Modifiabilite-DeferBinding/Modifiabilite-DeferBinding.png)

   <span>L'utilisation d'un fichier de configuration permet d'attendre plus longtemps avant d'insérer certaines valeurs dans des variables afin de réduire le couplage.</span>

  ### Relation entre les éléments architecturaux et les exigences de disponibilité
|Identifiant|Éléments|Description de la responsabilité|
|-----------|--------|-------------------------------|  
 |[CU04-M1](#cu04-m1-modifiabilité) |Fichier .env | Contient des informations qui seront utilisées par l'application au moment de l'exécution
  
## RDAQ-[Performance](#add-performance)          

   ### [RDTQ-Contrôler la demande en ressources](#add-contrôler-la-demande-en-ressources)
  
  ![ContrôlerLaDemande](https://github.com/LOG430-MicroServices/LOG430-STM/blob/684a0ccf9cbef2c0dfc56c1feb9fc7fe27e84909/out/doc/plantuml/auth/Performance_ControlerLaDemande/Performance_ControlerLaDemande.png)

  ### [RDTQ-Gérer les ressources](#add-gérer-les-ressources)
  
  ![GérerLesRessources](https://github.com/LOG430-MicroServices/LOG430-STM/blob/684a0ccf9cbef2c0dfc56c1feb9fc7fe27e84909/out/doc/plantuml/auth/Performance-G%C3%A9rerLesRessources/Performance-G%C3%A9rerLesRessources.png)
	
### Relation entre les éléments architecturaux et les exigences de performance
|Identifiant|Éléments|Description de la responsabilité|
|-----------|--------|-------------------------------|
|[CU04-P1](#cu04-p1-performance) | Utilisateur | Attends un service d'authentification performant|
|[CU04-P2](#cu04-p2-performance) | JWTService | Fais les gestion des token d'utilisateurs|
|[CU04-P3](#cu04-p3-performance) | Cache | Garde en mémoire rapide les token|

## RDAQ-[Sécurité](#add-sécurité)

  ### RDTQ-[Détecter les attaques](#add-détecter-les-attaques)
  
  ![DétecterLesAttaques](https://github.com/LOG430-MicroServices/LOG430-STM/blob/684a0ccf9cbef2c0dfc56c1feb9fc7fe27e84909/out/doc/plantuml/auth/S%C3%A9curit%C3%A9-D%C3%A9tecterLesAttaques/RDTQ%20S%C3%A9curit%C3%A9%20%20%20D%C3%A9tecter%20les%20attaques.png)

  ### [RDTQ-Résister aux attaques](#add-résister-aux-attaques)
  
  ![RésisterAuxAttaques](https://github.com/LOG430-MicroServices/LOG430-STM/blob/684a0ccf9cbef2c0dfc56c1feb9fc7fe27e84909/out/doc/plantuml/auth/S%C3%A9curit%C3%A9-R%C3%A9sisterAuxAttaques/RDTQ%20S%C3%A9curit%C3%A9%20%20%20R%C3%A9sister%20aux%20attaques.png)

  ### [RDTQ-Réagir aux attaques](#add-réagir-aux-attaques)
  
  ![RéagirAuxAttaques](https://github.com/LOG430-MicroServices/LOG430-STM/blob/684a0ccf9cbef2c0dfc56c1feb9fc7fe27e84909/out/doc/plantuml/auth/Security-R%C3%A9agirAuxAttaques/RDTQ%20S%C3%A9curit%C3%A9%20%20%20R%C3%A9agir%20aux%20attaques.png)

  ### [RDTQ-Récupérer d'une attaque](#add-récupérer-dune-attaque)
  
  ![RécupérerDesAttaques](https://github.com/LOG430-MicroServices/LOG430-STM/blob/684a0ccf9cbef2c0dfc56c1feb9fc7fe27e84909/out/doc/plantuml/auth/Security-R%C3%A9cup%C3%A9rerDesAttaques/RDTQ%20S%C3%A9curit%C3%A9%20%20%20R%C3%A9cup%C3%A9rer%20des%20attaques.png)

  ### Relation entre les éléments architecturaux et les exigences de sécurité
|Identifiant|Éléments|Description de la responsabilité|
|-----------|--------|-------------------------------|
|[CU04-S1](#cu04-s1-sécurité) | Utilisateur | S'enregistrer et s'authentifier dans le système |
|[CU04-S2](#cu04-s2-sécurité) | Authentification Controller | Gestion de la sécurité dans l'authentification |
  
  
## RDAQ-[Testabilité](#add-testabilité)

  ### [RDTQ-Contrôle et observe l'état du système](#add-controle-and-observe-létat-du-système)[](https://file%2B.vscode-resource.vscode-cdn.net/Users/yvanross/sources/log430/LOG430-STM/doc/documentationArchitecture.md#add-usabilit%C3%A9)
Tactique : Utilisation de Sources de données abstraites
![Controler et observer l'état du systeme](./assets/Testability-ControlObserveSystemState-RDTQ_Testabilité___Controle_et_Observation_de_l_État_du_Systeme__Tactique___Utilisation_de_Sources_de_données_abstraites.png)
  ### [RDTQ-limiter la complexité](#add-limiter-la-complexité)
Tactique: Limiter la Complexité Structurelle
![Diagramme de séquence](./assets/Testability-LimitComplexity-RDTQ_Testabilité___Limiter_la_Complexité_du_Systeme__Tactique__Limiter_la_Complexité_Structurelle.png)
  ### Relation entre les éléments architecturaux et les exigences de testabilité
  |Identifiant| Éléments         | Description de la responsabilité                               |
  |------------------|---------------------------------------------------------------|-------------------------------|
  |[CU04-T1](#cu04-t1-testabilité) | Authentification | Microservice d'authentification et d'autorisation du système |

## RDAQ-[Usabilité](#add-usabilité)

  ### [RDTQ-Supporter l'initiative de l'usager](#add-supporter-linitiative-de-lusager)

  ![Diagramme - Supporter l'initiative de l'usager](../out/doc/plantuml/chaos/Usability-SupportUserInitiative/Convivialit%C3%A9%20%20%20Supporter%20l'initiative%20de%20l'usager.png)
  <span>Afin de faciliter l'utilisation de l'application, on permet à l'usager de combiner plusieurs requêtes.</span>
  
  ### [RDTQ-Supporter l'initiative du système](#add-supporter-linitiative-du-système)

  ![Diagramme - Supporter l'initiative du système](../out/doc/plantuml/chaos/Usability-SupportSystemInitiative/Convivialit%C3%A9%20%20%20Supporter%20l'initiative%20du%20syst%C3%A8me.png)
  <span>On garde l'état d'une tâche afin de pouvoir informer l'utilisateur sur sa progression.</span>

  ### Relation entre les éléments architecturaux et les exigences d'usabilité
|Identifiant|Éléments|Description de la responsabilité|
|-----------|--------|-------------------------------|
  |[CU02-U1](#cu02-u1-usabilité) |Chaosmonkey|Doit permettre à l'utilisateur d'aggréger ses requêtes et de voir l'état d'une requête
  |[CU02-U2](#cu02-u2-usabilité) |Service registry|Doit fournir la liste des services
  |[CU02-U3](#cu02-u3-usabilité) |Utilisateur|Est celui à qui on veut fournir une bonne expérience
  
 ## RDAQ-[Interopérabilité](#add-interopérabilité)

  ### [RDTQ-Localiser](#add-localiser)

  ![Diagramme - Localiser](../out/doc/plantuml/chaos/Interoperability-Locate/RDTQ%20Interop%C3%A9rabilit%C3%A9%20%20%20Localiser.png)
  
  ### [RDTQ-Gérer les interfaces](#add-gérer-les-interfaces)

  ![Diagramme - Gérer les interfaces](../out/doc/plantuml/chaos/Interoperability-ManageInterfaces/RDTQ%20Interop%C3%A9rabilit%C3%A9%20%20%20G%C3%A9rer%20les%20interfaces.png)
  <span>Afin de permettre à différents utilisateurs d'avoir accès à différentes fonctionnalités sur les mêmes routes, on ajoute la fonctionnalité d'aggrégation aux "Powerusers".</span>
  
  ### Relation entre les éléments architecturaux et les exigences d'interopérabilité
|Identifiant|Éléments|Description de la responsabilité|
|-----------|--------|-------------------------------|
  |[CU02-I1](#cu02-i1-interopérabilité) |Utilisateur|N'est pas autorisé à aggréger ses requêtes
  |[CU02-I2](#cu02-i2-interopérabilité) |Poweruser|Est autorisé à aggréger ses requêtes
  |[CU02-I3](#cu02-i3-interopérabilité) |Chaosmonkey|Gère ses interfaces 
  |[CU02-I4](#cu02-i4-interopérabilité) |Service Registry|Fournit la liste des services

# Vues architecturales 
## Vues architecturales de type Module
### Vue #1
>#### Présentation primaire
![Présentation primaire - Vue modules](../out/doc/plantuml/Vues_Architecturales_Modules/Presentation_primaire/Vue%20Modules.png)
>#### Catalogue d'éléments
|Élement|Description|lien vers document d'interfaces|
|-------|-----------|-------------------------------|
|Authentification.AuthController|Contrôleur responsable de générer et des valider les jetons d'authentification|[Document d'interface Authentification](interface-authentification.md)|
|Authentification.AvailibilityController|Contrôleur responsable de gérer les heartbeats entre les différentes copies|[Document d'interface Authentification](interface-authentification.md)|
|Authentification.MonitorController|Contrôleur responsable d'obtenir l'état des microservices (incluant celui-ci) et de simuler les pannes en répondant au Chaosmonkey|[Document d'interface Authentification](interface-authentification.md)|
|Chaosmonkey.ServiceController|Contrôleur responsable d'obtenir la liste des microservices et d'envoyer les requêtes aux autres microservices afin de simuler les pannes|[Document d'interface Chaosmonkey](interface-chaosmonkey.md)|
|Chaosmonkey.TasksController|Contrôleur responsable d'obtenir l'état des tâches prenant beaucoup de temps|[Document d'interface Chaosmonkey](interface-chaosmonkey.md)|
>#### Diagramme de contexte
![Diagramme de contexte - Vue modules](../out/doc/plantuml/Vues_Architecturales_Modules/Contexte/Contexte.png)
>#### Guide de variabilité
Puisque ce diagramme ne présente que les modules présents au niveau de l'implémentation, ils n'ont pas nécessairement de présence au moment de l'exécution. À défaut de modifier les fichiers sources de l'application, il n'y a donc pas de variabilité qui s'applique ici.
>#### Raisonnement
Plusieurs contrôleurs on été développés dans chaque microservice afin de séparer les responsabilités pour les différentes routes de l'application.
Des interfaces internes ont été définies au niveau du Chaosmonkey afin de pouvoir insérer des services "Mock" puisque les autres microservices n'étaient pas disponibles pendant la majorité du temps de développement de l'application.
>#### Vues associées
Tous les diagrammes représentés dans les RDTQ correspondent à des éléments présents dans cette vue.

## Vues architecturales de type composant et connecteur
### Vue #1
>#### Présentation primaire
![VueComposantConnecteurDiagramme](https://github.com/LOG430-MicroServices/LOG430-STM/blob/41f6aa48c32acf711d49baa6946c14cb283d90a5/out/doc/plantuml/Vues_Achitecturales_c&C/Presentation_primaire/Presentation_primaire.png)
>#### Catalogue d'éléments
|Élement|Description|lien vers document d'interfaces|
|-------|-----------|-------------------------------|
 |User | Composant qui initie la requête|
 |Database|Composant qui contient les tokens d’authentification|[Document d'interface Authentification](interface-authentification.md)
 |IDatabase|Interface qui utilise le micro service d’authentification pour vérifier la validité d’un token donné par un user|[Document d'interface Authentification](interface-authentification.md)
 |Authentification_MS_Originale|Microservice qui authentifie qu’un user a le droit d’accéder à un service donné|[Document d'interface Authentification](interface-authentification.md)
 |Authentification_MS_Copie|La copie du micro service originale pour assurer la disponibilité|[Document d'interface Authentification](interface-authentification.md)
 |Chaos|Micro service utiliser pour détruire une instance d’un autre microservice|[Document d'interface Chaosmonkey](interface-chaosmonkey.md)|
 |IserviceDiscovery|Interface à travers laquelle le micro service externe qui intercommunication entre microservices à l’aide d’une source unique de découverte de route est visible|
 |IserviceTrajet|Interface à travers laquelle le micro service externe qui compare les temps de trajet est visible|
 |IserviceMonitoring| Interface à travers laquelle le micro service externe qui informe le mainteneur sur le status de vie des autres microservices est visible|
>#### Diagramme de contexte
![VueComposantConnecteurDiagrammeContexte](https://github.com/LOG430-MicroServices/LOG430-STM/blob/7171e70fa977ab73ffbbc2199c3a855b0d2a67da/out/doc/plantuml/Vues_Achitecturales_c&C/Diagramme_de_contexte/Diagramme_de_contexte.png)

>#### Guide de variabilité
La vue composant connecteur, présente tous les éléments obligatoires pour faire fonctionner le système. Donc nous n’avons pas de variabilité.
>#### Raisonnement
En ce qui concerne la vue composant et connecteur, nous avons pris pour hypothèse qu’on a une seule copie du micro service d’authentification qui reçoit les requetés provenant des utilisateurs et du micro service chaos. Dépendamment de la requête, il va soit interroger la base de données pour vérifier leur authenticité soit transférer la requête vers interface public qui lui connait tous les autres micro services externes associés. 
>#### Vues associées
[Document d'interface Authentification](interface-authentification.md)

## Vues architecturales de type allocation
### Vue #1 - Déploiement pour authentification
>#### Présentation primaire
![VueAllocationDiagramme](https://github.com/LOG430-MicroServices/LOG430-STM/blob/17c5dda7fe515d8109fbdf4878c4a1e98c7a59a8/doc/assets/VueAllocationDigramme.png)
>#### Catalogue d'éléments
|Élement|Description|lien vers document d'interfaces|
|-------|-----------|-------------------------------|
|PC utilisateur (externe)|Élément physique: ordinateur d'un utilisateur qui se connecte au service|[Vue architecturale de contexte](#vue-architecturale-de-contexte)|
|PC utilisateur (interne)|Élément physique: ordinateur d'un utilisateur qui utilise le service sur sa machine|[Vue architecturale de contexte](#vue-architecturale-de-contexte)|
|Serveur|Élément physique: machine qui permet d'exécuter le service|[Vue architecturale de contexte](#vue-architecturale-de-contexte)|
|Application d'authentification|Élément logiciel: service d'authentification|[Vue architecturale de contexte](#vue-architecturale-de-contexte)|
|Base de données|Élément physique: élément qui garde en mémoire les informations des utilisateurs|[Vue architecturale de contexte](#vue-architecturale-de-contexte)|
>#### Diagramme de contexte
![VueAllocationContexte](https://github.com/LOG430-MicroServices/LOG430-STM/blob/d708c2993b83cf90a54987c07ce356bfcbbdd566/doc/assets/Vue%20Allocation%20-%20Contexte.png)
>#### Guide de variabilité
Dans cette vue d'allocation, il n'y a pas de variabilité évidente. Tous les éléments doivent obligatoirement être présents pour le bon fonctionnement du système, ils ne peuvent pas être changés et l'implémentation non plus. 
>#### Raisonnement
En ce qui a trait aux décisions par rapport à la vue allocation, ici, nous avons fait l'hypothèse qu'un seul serveur est suffisant pour supporter les deux microservices et tous les utilisateurs qui voudraient y accéder en même temps. Nous avons aussi assumé qu'étant donnée l'étendue très petite de ce service, une seule copie de la base de donnée serait utile.

>#### Vues associées
[Vue architecturale de contexte](#vue-architecturale-de-contexte)


# Conclusion
Dans ce projet, nous avons eu à développer plusieurs fonctionnalités dans le contexte d'une architecture composée de microservices ayant pour but principal de fournir un service de calcul de temps de trajet. 

Nous avons échangé de la documentation avec d'autres équipes afin d'assurer la compatibilité des différents services, et avons implémenté et intégré plusieurs tactiques architecturales afin d'assurer le respect des différents attributs de qualité.

Nous avons ainsi obtenu deux microservices stables, simples à comprendre, et efficaces.

Ce projet nous a permis de développer une application relativement complexe dans un contexte s'apparentant au développement logiciel dans une grosse entreprise, où différents départements travaillent sur un même projet en échangeant leur documentation publique.


# Documentation des interfaces

| Élement               | Description                                                                                                                                                                                                                                                                                                                                                                                                                            | lien vers document d'interfaces                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| Chaos Monkey          | Ce microservice a été créé pour perturber les autres microservices, en simulant une panne. Il est utilisé pour les tuer, forçant la bonne implémentation du redémarrage ainsi que de s'assurer de la disponibilité du service.                                                                                                                                                                                                        |     [Document d'interface Chaosmonkey](interface-chaosmonkey.md) |                                                                    |
| Authentification      | Ce service d'authentification et d'autorisation sert à verifier que l'utilisation du système par un utilisateur est sincère est justifié. L'utilisateur concerné doit alors s'authentifier dans le système avant de pouvoir effectuer une action, qui devra être autorisée par ce microservice. Les informations essentielles seront stockées dans une base de données afin d'assurer la persistence et la continuité du service. | [Document d'interface Authentification](interface-authentification.md) |

<!--stackedit_data:
eyJoaXN0b3J5IjpbNDU4ODUwNzIwXX0=
-->
