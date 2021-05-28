# Cahier des charges

## Présentation du projet

**[ nom du projet ]** est une interface permettant à des clients, des sociétés de services et des prestataires de partager un espace commun. Celle-ci permet la création de projets et des missions qui les composent, l'attribution de ceux-ci à une ou plusieures sociétés de services et, enfin, l'appel ciblé à des prestataires.

## Objectifs du projet

L'objectif principal de ce projet est de fournir aux différents acteurs présents *(client final - société de services - prestataire)* une interface centralisant les outils nécessaires à la satisfaction d'une demande client  tout en fluidifiant le travail des sociétés de services et de leurs prestataires.

# Les fonctionnalités

## Connexion

Cela sera l'unique fonctionnalité accessible depuis la page d'accueil pour assurer la confidentialité du contenu. Les différents acteurs pourront se connecter pour accéder à leurs espaces dédiés.

## [Client] Création/Modification/Suppression de projets

Un client aura la possibilité de créer des projets. Ceux-ci seront alors modifiables ou supprimables en cas de besoin.

> exemple: Un client créé un projet *"Initiation au développement web"* qui aura lieu à Paris.

## [Client] Création/Modification/Suppression de missions

Un client aura la possibilité de créer des missions, suite à la création d'un projet. Celles-ci seront alors modifiables ou supprimables en cas de besoin.

> exemple: Le client créé une mission *"Demi-journée PHP"*, rattachée au projet *"Initiation au développement web"*.

## [Client] Gestion des dates des mission

Un client aura la possibilité de gérer les dates des différentes missions d'un projet.

> exemple: Le client décide que la mission *"Demi-journée PHP"*, initialiement rattachée au projet *"Initiation au développement web"*, se déroulera le 15 Juin 2021.

## [Client] Clonage d'un projet

Un client aura la possibilité de créer une copie d'un projet (et de ses missions).

> exemple: Le client copie le projet *"Initiation au développement web"* *(ainsi que toutes ses missions, ici *"Demi-journée PHP"*)* qui doit se tenir à Paris, mais le situe cette fois-ci à Lyon. Le client a donc deux projets similaires en cours, l'un à Paris, l'autre à Lyon.

## [Client] Attribution d'une société de services/d'un prestataire

Un client aura la possibilité d'attribuer une société de service/un prestataire à un projet donné.

> exemple: Le client décide que seule la société de service "Lyon Coding Company" pourra remplir les missions du projet *"Initiation au développement web"* se tenant à Lyon. Au contraire, il décide que seuls ses propres prestaires/salariés assureront le projet similaire se tenant à Paris.

## [Société de service] Positionnement des prestataires

Une société de service, une fois qu'un projet lui aura été attribué, pourra alors positionner, de façon ciblée, ses prestataires sur les différentes missions proposées.

> exemple: La société *Lyon Coding Company*, ayant la charge du projet *"Initiation au développement web"*, positionne un prestataire, spécialisé dans le langage PHP, sur la mission *"Demi-journée PHP"* qui se tiendra le 15 Juin 2021 à Lyon.

## [Prestataire] Notification des positionnements

Un prestataire se voit notifié par mail toute proposition de positionnement.

> exemple: Le prestataire se voit notifé par mail que la société "Lyon Coding Company" lui propose de remplir la mission *"Demi-journée PHP"* qui se tiendra le 15 Juin 2021 à Lyon.


## [Prestataire] Validation des positionnements

Un prestataire peut décider ou non de valider une proposition de positionnement.

> exemple: Le prestataire accepte le positionnement proposé par "Lyon Coding Company" pour la mission *"Demi-journée PHP"* qui se tiendra le 15 Juin 2021 à Lyon.

## [Prestataire/Société de service] Génération de facture

Un prestataire/une société de service a la possibilité de générer les factures des missions effectuées au cours du mois.

> exemple: Le prestataire a terminé la mission *"Demi-journée PHP"* et récupère la facture après l'avoir générée.

## [Prestataire/Société de service] Rappel d'impayé

Un prestataire/une société de service a la possibilité d'envoyer un email de rappel en cas de dépassement de la date de paiement d'une facture.

> exemple: Le prestaire ayant effectué la mission *"Demi-journée PHP"* n'a toujours pas été payé et décide de relancer par mail la société de services *Lyon Coding Company*.

# User story

| En tant que ...| Je veux...| Afin de ...|
| - | - | - |
| visiteur | une page de connexion | pouvoir acceder aux fonctionnalités du site |
| client - prestataire | une page de déconnexion | pour empecher d'autres personnes d'utiliser mon compte |
| | | |
| client | un espace de gestion | créer/modifier/supprimer des projets |
| client | un espace de gestion | créer/modifier/supprimer des missions |
| client | un bouton | créer une copie d'un projet existant et de ses missions |
| client | un calendrier | gérer les dates des missions |
| client | un espace de gestion | attribuer ou retirer un prestataire/une société de service à une mission |
| | | |
| société de services | un calendrier | proposer un positionnement à des prestataires sur des missions |
| | | |
| prestataire | une notification par email | être prévenu d'une proposition de positionnement |
| prestataire | un calendrier | valider ou non une proposition de positionnement |
| | | |
| société de services - prestataire | bouton | envoyer un email de rappel en cas de dépassement de la date de paiement d'une facture |
| société de services - prestataire | bouton | générer les factures des missions effectuées au cours du mois |
| | | |
| **A COMPLETER** |  |  |  |

# Routes

## FRONT 

|Description|URL|
|---|----------|
|Accueil|/|
|Contacts|/contacts|
|Mentions Légales|/mention-legales|
|||
|Connexion|/login|
|Déconnexion|/logout|
|Inscription|/signup|
|||
|Liste des projets|/projets|
|Création d'un projet|/projet/create|
|Modification d'un projet|/projet/edit|
|Suppression d'un projet|/projet/delete|
|||
|Liste des missions d'un projet|/projet/[id]/missions|
|Création d'une mission|/projet/[id]/mission/create|
|Modification d'une mission|/projet/[id]/mission/[id]/edit|
|Suppression d'une mission|/projet/[id]/mission/[id]/delete|
|||
|**ETC**|**arborescence à confirmer**|

## BACK/API

|Méthode|API route|nom|Description|
|---|----------|----------|----------|
|POST|/api/fauna|index|api route de base pour les requêtes fauna|
|**ETC**|||**a completer au fil du projet**|

# Liste des technologies choisie

- Next.js
- Fauna DB
- GraphQL
- Netlify

# MCD

*à placer*

# Dictionnaire des données

| Nom symbolique | Désignation | Type | Remarque |
| - | - | - | - |
| **User** |  |  |  |
| auth0Id | Numéro d'identification d'un utilisateur | String | Généré par auth0 |
| | | | |
| **Company** |  |  |  |
| name | nom de l'entreprise | String | Peut être client, société de services ou prestataire |
| siret | Numéro SIRET de l'entreprise | Number | - |
| iban | Numéro IBAN de l'entreprise | String | - |
| | | | |
| **Project** |  |  |  |
| name | nom du projet | String | - |
| place | lieu où se déroule le projet | String | - |
| | | | |
| **Mission** |  |  |  |
| name | nom de la mission | String | - |
| rate | tarif de la mission | String | - |
| | | | |
| **MissionUnit** |  |  |  |
| date | date de l'unité de mission | Date | - |
| quantity | quantité d'unité | Number | - |
| | | | |
| **Missionoffer** |  |  |  |
| createdAt | date de création de l'offre | Date | - |
| status | Status de l'offre | String | - |
| | | | |
| **Invoice** |  |  |  |
| number | numéro de la facture | Number | - |
| invoiceDate | date de la facture | Date | - |
| dueDate | date de paiement | Date | - |
| paid | status de la facture | Date | true: payée - false: impayée |
| | | | |




