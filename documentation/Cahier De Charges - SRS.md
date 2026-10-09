# Cahier des charges (SRS léger) — <Turisty>
**Équipe :** Avengers  
**Date :** <2026-10-09>  
**Version :** <v0.1 >

---

---

## 1. Contexte et objectif

- **Contexte :** Les touristes, les nouveaux arrivants et les étudiants peuvent avoir de la difficulté à trouver des activités adaptées à leurs préférences et à leur budget à Montréal. Les informations sont souvent dispersées sur plusieurs plateformes. Il peut également être difficile de rencontrer des personnes avec qui participer à ces activités.

- **Objectif principal :** MTL Complice vise à regrouper des activités, des restaurants et des hébergements afin d’aider les utilisateurs à organiser un séjour ou une sortie à Montréal selon leur budget, leurs intérêts et la durée choisie.

- **Parties prenantes :** Les visiteurs, les membres inscrits, les organisateurs de sorties, les administrateurs de la plateforme et l’équipe responsable du projet.

---

## 2. Portée (Scope)

### 2.1 Inclus (IN)

- IN-1 : Consulter les activités, les restaurants et les hébergements.
- IN-2 : Rechercher et filtrer les lieux selon le budget, la catégorie et les préférences.
- IN-3 : Créer un compte et se connecter.
- IN-4 : Créer un programme personnalisé pour une durée de un à trois jours.
- IN-5 : Calculer le coût estimé du programme et le budget restant.
- IN-6 : Sauvegarder et modifier un programme.
- IN-7 : Créer une sortie liée à une activité.
- IN-8 : Demander à participer à une sortie.
- IN-9 : Signaler un contenu inapproprié.
- IN-10 : Permettre à un administrateur de gérer les lieux, les utilisateurs et les signalements.
- IN-11 : Crée un Chat de groupe pour les différentes sortie collectif
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

- **Membre inscrit :** crée un compte, indique ses préférences, génère un programme, sauvegarde ses choix et demande à participer à une sortie.

- **Organisateur :** crée une sortie, précise la date, l’heure et le nombre de places, puis accepte ou refuse les demandes de participation.

- **Administrateur :** gère les utilisateurs, les lieux, les activités et les contenus signalés.

---

## 4. Exigences fonctionnelles (FR) 
- **FR-1 :** Le système doit permettre aux visiteurs de consulter les activités, les restaurants et les hébergements à Montréal.
- **FR-2 :** Le système doit permettre aux visiteurs de rechercher et de filtrer les lieux selon leur budget, leurs préférences, leur catégorie et la catégorie d’âge.
- **FR-3 :** Le système doit afficher les détails d’un lieu, comme sa description, son adresse, son prix estimé et sa catégorie d’âge recommandée.
- **FR-4 :** Le système doit permettre aux utilisateurs de créer un compte avec un mot de passe securisé et de se connecter.
- **FR-5 :** Le système doit permettre aux membres de sauvegarder et de modifier leur programme.
- **FR-6 :** Le système doit permettre aux membres de créer une sortie liée à une activité en précisant la date, l’heure et le nombre de places disponibles.
- **FR-7 :** Le système doit permettre aux utilisateurs de signaler un contenu inapproprié.

---

## 5. Exigences non fonctionnelles (NFR) 
> Performance / sécurité / disponibilité / UX / maintenabilité…
- **NFR-1 (Performance) :** Le système doit afficher les pages et les résultats de recherche dans un délai de 2 secondes.
- **NFR-2 (Sécurité) :** Le système doit protéger les comptes des utilisateurs en utilisant des mots de passe sécurisés.
- **NFR-3 (UX) :** Le système doit proposer une interface simple et facile à utiliser pour les administrateurs, les visiteurs et les membres.
- **NFR-4 (Qualité) :** Le système doit fonctionner sur les navigateurs web courants, comme Google Chrome, Microsoft Edge et Firefox.

---

## 6. Contraintes 
- **C-1 (Technologie) :** Le projet doit utiliser le langage de programation 'Python'
- **C-2 (Plateforme) :** Le projet doit être développé en forme d’une application web qui est accessible depuis un navigateur.
- **C-3 (Délai) :** Le projet doit être terminé avant la séance 30.
- **C-4 (Outils) :** L’équipe doit utiliser GitHub et Python comme langage de programmation principal.

---

## 7. Le Product Backlog 
- **Epic 1** --> Découvrir Montréal.  
 *US-01 - Consulter les lieux :* En tant que visiteur, je veux consulter les activités, les restaurants et les hébergements afin de découvrir les possibilités offertes à Montréal.  
 *US-02 - Rechercher et filtrer les lieux :* En tant que visiteur, je veux filtrer les lieux selon mon budget, mes préférences, la catégorie et la catégorie d’âge afin d’obtenir des propositions adaptées.  
 *US-03 - Consulter les détails d’un lieu :* En tant que visiteur, je veux consulter les détails d’un lieu afin de connaître sa description, son adresse, son prix estimé et sa catégorie d’âge recommandée.  
  
- **Epic 2** --> Planifier selon son budget.  
 *US-04 - Indiquer ses besoins :* En tant que membre, je veux indiquer mon budget, mes intérêts, la durée de mon séjour, le nombre de personnes et la catégorie d’âge afin d’obtenir un programme adapté.  
 *US-05 - Générer un programme :* En tant que membre, je veux générer un programme personnalisé d’une durée de un à trois jours afin de mieux organiser mon séjour.  
  
- **Epic 3** --> Organiser et rejoindre des sorties.  
 *US-06 - Créer une sortie :* En tant que membre, je veux créer une sortie liée à une activité afin de proposer à d’autres utilisateurs de m’accompagner.  
 *US-07 - Demander à participer à une sortie :* En tant que membre, je veux demander à participer à une sortie afin de rencontrer d’autres personnes et de réaliser l’activité avec elles.  
 *US-08 - Gérer les demandes de participation :* En tant qu’organisateur, je veux accepter ou refuser les demandes afin de gérer les participants à ma sortie.  

---

## 8. Critères d’acceptation globaux
- [ ] Toutes les fonctionnalités prévues sont développées et testées.
- [ ] Des tests unitaires sont présents pour vérifier le fonctionnement des fonctions principales.
- [ ] Les erreurs courantes sont gérées correctement afin d’éviter les problèmes pendant l’utilisation.
- [ ] La documentation du projet est à jour.

## 9. Definition of Done – mini
Une fonctionnalité est considérée comme terminée lorsque :  
- Elle est développée et fonctionne correctement.
- Elle a été testée et les erreurs importantes ont été corrigées.
- Elle respecte les exigences définies dans le cahier des charges.
- La documentation est mise à jour si nécessaire.