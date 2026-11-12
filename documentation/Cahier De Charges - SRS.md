# Cahier des charges (SRS léger) — Turisty
**Équipe :** The Avengers  
**Date :** 2026-11-11 
**Version :** v0.2

---

---

## 1. Contexte et objectif

- **Contexte :** Les touristes, les nouveaux arrivants et les étudiants ont de la difficulté à trouver des activités adaptées à leurs préférences et à leur budget à Montréal. Les informations sont souvent dispersées sur plusieurs plateformes. Il peut également être difficile de rencontrer des personnes avec qui participer à ces activités.

- **Objectif principal :** Turisty regroupe des activités, des restaurants et des hébergements afin d’aider les utilisateurs à organiser un séjour ou une sortie à Montréal selon leur budget, leurs intérêts et la durée choisie.

- **Parties prenantes :** Les visiteurs, les membres inscrits, les organisateurs de sorties, les administrateurs de la plateforme et l’équipe responsable du projet.

---

## 2. Portée (Scope)

### 2.1 Inclus (IN)

- IN-1 : Consulter les activités, les restaurants et les hébergements.
- IN-2 : Rechercher et filtrer les lieux selon le budget, la catégorie, les préférences et la tranche d'âge.
- IN-3 : Créer un compte et se connecter.
- IN-4 : Créer un programme personnalisé pour une durée de un à trois jours.
- IN-5 : Calculer le coût estimé du programme et le budget restant.
- IN-6 : Sauvegarder et modifier un programme.
- IN-7 : Créer une sortie liée à une activité.
- IN-8 : Demander à participer à une sortie Le membre fait la demande et l'organisateur la traite (accepte ou refuse).
- IN-9 : Signaler un contenu inapproprié.
- IN-10 : Permettre à un administrateur de gérer les lieux, les utilisateurs et les signalements.
- IN-11 : Crée un Chat de groupe pour chaque sortie. Il est limité seulement pour les personnes qui vont participer dans une sortie concrète.
### 2.2 Exclu (OUT)

- OUT-1 : Effectuer des réservations et des paiements directement dans l’application.
- OUT-2 : Afficher les prix et les disponibilités en temps réel.
- OUT-3 : Fournir une messagerie privée générale en dehors des sorties organisées.
- OUT-4 : Développer une application mobile native.
- OUT-5 : Fournir un service de transport ou de covoiturage comparable à Uber.
- OUT-6 : Intégrer un assistant intelligent ou un chatbot dans la première version

---

## 3. Acteurs / profils utilisateurs

- **Visiteur :** consulte les activités, les restaurants et les hébergements sans avoir obligatoirement un compte.

- **Membre inscrit :** garde les droits du visiteur, indique ses préférences, génère un programme, sauvegarde ses choix, crée une sortie, demande à participer à une sortie et discute dans les groupes où il est accepté.

- **Organisateur :** membre inscrit qui a créé une sortie. Il précise la date, l'heure et le nombre de places, puis accepte ou refuse les demandes de participation.

- **Administrateur :** gère les utilisateurs, les lieux, les activités et les contenus signalés.

---

## 4. Exigences fonctionnelles (FR) 
- **FR-1 :** Le système doit permettre aux visiteurs de consulter les activités, les restaurants et les hébergements à Montréal.
- **FR-2 :** Le système doit permettre aux visiteurs de rechercher et de filtrer les lieux selon leur budget, leurs préférences, leur catégorie et la tranche d’âge.
- **FR-3 :** Le système doit afficher les détails d’un lieu, comme sa description, son adresse, son prix estimé et sa tranche d’âge recommandée.
- **FR-4 :** Le système doit permettre aux utilisateurs de créer un compte avec un mot de passe securisé et de se connecter.
- **FR-5 :** Le système doit permettre aux membres de sauvegarder et de modifier leur programme.
- **FR-6 :** Le système doit permettre aux membres de créer une sortie liée à une activité en précisant la date, l’heure et le nombre de places disponibles.
- **FR-7 :** Le système doit permettre à un membre autorisé à lire un message de le signaler.
- **FR-8 :** Le système doit générer pour le membre un programme de 1 à 3 jours selon ses besoins, et afficher le coût estimé et le budget restant.
- **FR-9 :** Un membre connecté doit pouvoir demander à rejoindre une sortie ouverte avec une place disponible. Une deuxième demande pour la même sortie est bloquée.
- **FR-10 :** L’organisateur doit pouvoir accepter ou refuser les demandes de sa sortie. Le système revérifie la capacité au moment de l’acceptation.
- **FR-11 :** L’organisateur et les membres acceptés doivent pouvoir lire et publier des messages dans le groupe de la sortie.
- **FR-12 :** L’administrateur doit pouvoir gérer les lieux, les utilisateurs et les signalements.

---

## 5. Exigences non fonctionnelles (NFR) 
> Performance / sécurité / disponibilité / UX / maintenabilité…
- **NFR-1 (Performance) :** Le système doit afficher les pages et les résultats de recherche dans un délai de 2 secondes. _Vérification future : mesure avec le catalogue fictif, sur un réseau normal, avec Chrome._
- **NFR-2 (Sécurité) :** Le système doit protéger les comptes des utilisateurs en utilisant des mots de passe sécurisés. _Vérification future : revoir la méthode de stockage lors de la conception._
- **NFR-3 (UX) :** Le système doit proposer une interface simple et facile à utiliser pour les administrateurs, les visiteurs et les membres.  _Vérification future : demander à quelques personnes de faire un parcours simple (chercher un lieu, demander une place)._
- **NFR-4 (Qualité) :** Le système doit fonctionner sur les navigateurs web courants, comme Google Chrome, Microsoft Edge et Firefox.  _Vérification future : tester les pages principales sur ces trois navigateurs._

---

## 6. Contraintes 
- **C-1 (Technologie) :** Le projet doit utiliser le langage de programation 'Python'
- **C-2 (Plateforme) :** Le projet doit être développé en forme d’une application web qui est accessible depuis un navigateur.
- **C-3 (Délai) :** Le projet doit être terminé avant la séance 30.
- **C-4 (Outils) :** L'équipe utilise GitHub pour le suivi de la documentation.

### Hypothèses
- Un catalogue de lieux fictifs contient, pour chaque lieu, un prix estimé, son unité (par personne, par groupe ou par nuit) et une tranche d'âge recommandée. La tranche d'âge souhaitée par le membre est comparée à la tranche d'âge recommandée des lieux. Ce n'est pas une interdiction.
- Une API pourrait être une source de données plus tard, mais elle n'est pas nécessaire pour cette remise.
- Une sortie est ouverte tant que sa date et son heure ne sont pas passées. Sa capacité exclut l'organisateur.
- Seules les demandes acceptées comptent dans la capacité d'une sortie.
- Une demande a trois statuts : « En attente », « Acceptée » et « Refusée ». Après un refus, le membre ne peut pas refaire une demande pour la même sortie.
- Turisty ne propose pas de programme qui dépasse le budget du membre.
- Correspondance avec le modèle de données : Lieu = Attraction, Membre = Compte, Programme = program, Étape = Etape. L'organisateur n'est pas un rôle stocké : c'est le membre qui a créé la sortie.

---

## 7. Le Product Backlog 
- **Epic 1** --> Découvrir Montréal.  
 *US-01 - Consulter les lieux :* En tant que visiteur, je veux consulter les activités, les restaurants et les hébergements afin de découvrir les possibilités offertes à Montréal.  
 *US-02 - Rechercher et filtrer les lieux :* En tant que visiteur, je veux filtrer les lieux selon mon budget, mes préférences, la catégorie et la catégorie d’âge afin d’obtenir des propositions adaptées.  
 *US-03 - Consulter les détails d’un lieu :* En tant que visiteur, je veux consulter les détails d’un lieu afin de connaître sa description, son adresse, son prix estimé et sa catégorie d’âge recommandée.  
  
- **Epic 2** --> Planifier selon son budget.  
 *US-04 - Indiquer ses besoins :* En tant que membre, je veux indiquer mon budget, mes intérêts, la durée de mon séjour, le nombre de personnes et la tranche d'âge souhaitée afin d'obtenir un programme adapté.  
 *US-05 - Générer un programme :* En tant que membre, je veux générer un programme personnalisé d’une durée de un à trois jours afin de mieux organiser mon séjour.  
  
- **Epic 3** --> Organiser et rejoindre des sorties.  
 *US-06 - Créer une sortie :* En tant que membre, je veux créer une sortie liée à une activité afin de proposer à d’autres utilisateurs de m’accompagner.  
 *US-07 - Demander à participer à une sortie :* En tant que membre, je veux demander à participer à une sortie afin de rencontrer d’autres personnes et de réaliser l’activité avec elles.  
 *US-08 - Gérer les demandes de participation :* En tant qu’organisateur, je veux accepter ou refuser les demandes afin de gérer les participants à ma sortie.  

- Correspondance entre le backlog et les cas d'utilisation :

- US-01 à US-04 → UC-01 à UC-04 (correspondance directe)
- US-05 → UC-05 et UC-17
- US-06 à US-08 → UC-06 à UC-08 (correspondance directe)
- US-09 → UC-11
- US-10 → UC-12
- US-11 → UC-09 et UC-10
- US-12 → UC-13
- US-13 → UC-14, UC-15 et UC-16

---

## 8. Critères d’acceptation globaux
- US-02 — Rechercher et filtrer
[ ] Étant donné des lieux fictifs de catégories et de prix différents, quand le visiteur choisit « activité », une tranche d’âge et un budget maximal, alors tous les résultats respectent tous les filtres actifs.
[ ] Si aucun lieu ne correspond, Turisty affiche un message de résultat vide clair.
[ ] Si le budget saisi est négatif ou non numérique, Turisty demande de le corriger.

- US-05 — Générer un programme
[ ] Étant donné une durée de 1 à 3 jours et assez de lieux compatibles, le membre obtient un programme pour la durée demandée, avec le coût total estimé et le budget restant.
[ ] Une durée hors de 1 à 3 jours est refusée.
[ ] Si aucun programme ne respecte le budget, Turisty l’indique au lieu de proposer un programme qui le dépasse.

- US-07 — Demander à participer
[ ] Étant donné qu'un membre est connecté, s'il y a une sortie ouverte avec une place disponible et aucune demande existante de ce membre pour cette sortie, quand il fait sa demande, alors Turisty enregistre une seule demande avec le statut « En attente ».
[ ] Si la sortie est complète ou si une demande existe déjà, l’envoi est bloqué et le motif est affiché.
[ ] Une demande « En attente » ne réserve pas de place.

- US-08 — Traiter une demande

[ ] L’organisateur peut accepter ou refuser une demande « En attente » de sa propre sortie. Le membre voit ensuite « Acceptée » ou « Refusée ».
[ ] Si la dernière place a été prise entre-temps, l’acceptation est bloquée et la demande reste « En attente ». L’organisateur peut la refuser.
[ ] Une demande déjà traitée ne peut pas être traitée une deuxième fois.

## 9. Definition of Done 
Une fonctionnalité est considérée comme terminée lorsque :  
- Elle est développée et fonctionne correctement selon le SRS.
- Elle a été testée et les erreurs importantes ont été corrigées.
- La documentation est mise à jour si nécessaire.

## 10. Tâches d'analyse et de conception
- **US-02 :** Préparer 3 fiches de lieux fictifs et détailler UC-02.
- **US-05 :** Définir l'unité des prix (personne / groupe / nuit) et relier le programme à ses étapes dans l'ERD (UC-04, UC-05, UC-17).
- **US-07 :** Écrire UC-07 et dessiner le début du TO-BE.
- **US-08 :** Écrire UC-08 et vérifier la règle de capacité avec l'ERD.

## 11. Ce qui sera fait pour la soumission 3

Class Diagram, Object Diagram, Package Diagram, Sequence Diagrams, Communication Diagram, State Diagram, wireframes et matrice de traçabilité.