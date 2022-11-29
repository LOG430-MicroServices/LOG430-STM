#### Identité de l'interface
Ceci est le microservice web REST nommé **Chaosmonkey**. Le but principal de ce service est de simuler des pannes dans les différents microservices.
#### Ressources
*Service[] getServices()* \
Fournit la liste des microservices qui peuvent être modifiés par ce micro-service. \
**Pré-conditions**
N/A \
**Post-conditions**
- Le système retourne une liste des microservices qui peuvent être modifiés. \
**Erreurs**
- Le microservice de "Service Registry" n'est pas disponible, donc la route retourne la liste de services sauvegardée en cache.

*void killService(Service service)* \
Envoie une requête à un microservice pour qu'il s'arrête. \
**Pré-conditions** 
- Le microservice à arrêter est disponible. \
**Post-conditions**
- Un appel est envoyé au microservice pour qu'il s'arrête.\
**Chemins alternatifs**
- Si l'utilisateur est un "Poweruser", il peut demander d'arrêter plusieurs microservices à la fois. Dans ce cas, un lien servant à voir l'état de la tâche est retourné.
**Erreurs**
- Le microservice à arrêter n'est pas disponible.
- L'utilisateur essaie d'arrêter plusieurs microservices à la fois dans être un "Poweruser".


*void setLatency(Service service, Number latency)* \
Envoie une requête à un microservice pour qu'il ajoute une latence spécifiée à tous ses appels. \
**Pré-conditions** 
- Le microservice à modifier est disponible. \
**Post-conditions**
- Un appel est envoyé au microservice pour qu'il mette à jour sa latence.\
**Chemins alternatifs**
- Si l'utilisateur est un "Poweruser", il peut demander de modifier plusieurs microservices à la fois. Dans ce cas, un lien servant à voir l'état de la tâche est retourné.
**Erreurs**
- Le microservice à modifier n'est pas disponible.
- L'utilisateur essaie de modifier plusieurs microservices à la fois dans être un "Poweruser".

*Number getTaskStatus(Integer taskId)* \
Retourne l'état d'une tâche. \
**Pré-conditions**
- La tâche existe \
**Post-conditions**
- Le système retourne l'état de la tâche. \
**Erreurs**
- La tâche n'existe pas.


#### Types de données et constantes
**Type Service** \
Ce type représente un microservice pouvant être modifié.
- String name
- String url
#### La gestion des erreurs
- 404 Le service n'existe pas
- 401 L'utilisateur n'a pas l'authorisation d'aggréger ses requêtes

#### Variabilité
Il n'y a pas de variabilité au niveau de cette interface.

#### Caractéristiques des attributs de qualité
Les attributs de qualités suivants sont ici disponibles :
- Disponibilité
- Interopérabilité
- Convivialité
#### Problèmes de justification et de conception
- Les routes kill et setLatency ont également la fonctionnalité d'aggréger des requêtes - cette décision a été de prise afin que tous les utilisateurs aient accès aux mêmes routes et que leur comportement soit plutôt dépendant du type d'utilisateur.
- Un concept de tâches a été implémenté de manière à pouvoir fournir à l'utilisateur une réponse rapide ainsi qu'une manière de consulter l'état de sa requête.
- Ce service de simulation de pannes a été externalisé dans un microservice indépendant afin de respecter la doctrine du "Separation of Concerns".
#### Guide d'utilisation
GET https://portainer.log430-20223-02.logti.etsmtl.ca.nip.io/services

POST https://portainer.log430-20223-02.logti.etsmtl.ca.nip.io/kill \
body : {"name": "Nom", "url": "https://test.microservice.com"}

POST https://portainer.log430-20223-02.logti.etsmtl.ca.nip.io/kill \
body : [{"name": "Nom 1", "url": "https://test1.microservice.com"},{"name": "Nom 2", "url": "https://test2.microservice.com"}]

GET https://portainer.log430-20223-02.logti.etsmtl.ca.nip.io/task/0