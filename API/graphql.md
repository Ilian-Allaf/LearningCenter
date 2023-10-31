# GraphQL
## Comment ça fonctionne

Les APIs REST et GraphQL sont identiques excepté la couche de routage. Pour rappel le rôle de cette couche dans une API REST (par exemple) est d’appeler les fonctions du métier en fonction du verbe HTTP, de l’url et possiblement des paramètres envoyés. GraphQL agit de même en appelant le métier en fonction de la requête (GraphQL query) envoyée.

GraphQL est en premier lieu un langage de requête.
Le client choisit alors quels champs de chaque Objet (ex: orders) il souhaite et dans quel ordre. La réponse du serveur GraphQL sera alors identique à l’ordre dans lequel a été formulé la requête.

### Schéma
GraphQL est un environnement d’exécution qui interpréte et structure ces requêtes à partir du schéma.
Le schéma est donc un élément central dans la conception d’une API GraphQL. On y définit tous les objets GraphQL, leurs types (string, int, objet précédemment défini… ou encore un tableau des éléments précédents). On y définit aussi toutes les requêtes disponibles dans l’objet global Query, toutes les actions disponibles dans l’objet global Mutation et leurs éventuelles entrées. Enfin il est directement possible de spécifier des règles métier comme par exemple l’ajout d’un point d’exclamation si un champ est obligatoire.

### Resolver
Une fois la requête vérifiée de part sa syntaxe et le schéma du serveur, GraphQL fait appel aux resolvers. Un resolver associe une fonction de l’API (calculs, récupération de données de la base de données, appels à une autre API, etc…) à une requête ou une action définie dans les objets globaux du schéma, Query et Mutation. C’est donc à ce niveau que l’on fait le lien entre les entrées des requêtes et les arguments des fonctions (id dans l’exemple ci-dessous) mais aussi que l’on regroupe les règles de fonctionnement de notre API telle que l’authentification ou la gestion des droits.

## Avantages
- ### Avoid Overfetching & Underfetching 
l’intérêt principal de GraphQL est d’avoir entièrement la main, depuis le front, sur les données retournées par l’API.
En plus d’avoir un flux personnalisé et personnalisable, cela permet surtout d’éviter l’under-fetching et l’over-fetching.

L’over fetching  est le surplus d’informations délivrées par la requête par rapport à la donnée désirée par le client. L’under fetching est le fait de devoir faire plusieurs appels à l’API pour compléter la réponse de notre premier appel qui ne contient pas assez d’informations. Concilier ces deux problématiques peut rapidement devenir un dilemme important dans la conception d’une API avec beaucoup d’informations.

- ### Optimisation des données réseaux
Lorsque l’on développe une application mobile, la consommation des données est un enjeu important à considérer. En effet, notre utilisateur peut se retrouver à tout moment avec une bande passante faible (utilisateurs isolés, transport en commun…) et l’application doit tout de même s’afficher avec le minimum d’appels API, quitte à se compléter par la suite.

Considérons l’exemple ci-dessus. On suppose qu’en général une requête GraphQL est plus longue à arriver à cause de problématique de cache (sur lesquels nous reviendrons) ou du fait d’un temps d’exécution serveur plus important (~+50ms). Donc en temps normal la requête GraphQL sera en général plus lente à arriver (ici par exemple 200ms au lieu de 40ms en temps normal).

## Inconvénients 
- ### Caching
Le plus gros d’entre eux, c’est la complexité de la mise en cache. En effet, avec une API REST qui retourne toujours le même format de données, la mise en cache est très facile


Sources:

https://talks.freelancerepublik.com/introduction-fonctionnement-graphql/
https://blog.octo.com/graphql-et-pourquoi-faire/
