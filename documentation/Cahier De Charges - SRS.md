# Cahier des charges (SRS léger) — <Turisty>
**Équipe :** <Noms>  
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
- OUT-6 : Intégrer un assistant intelligent ou un chatbot dans la première version ( Sara:je sais pas trop mais je crois que pour la premiere version c'est trop de travail qu'est ce vous en dite?).

---

## 3. Acteurs / profils utilisateurs

- **Visiteur :** consulte les activités, les restaurants et les hébergements sans avoir obligatoirement un compte.

- **Membre inscrit :** crée un compte, indique ses préférences, génère un programme, sauvegarde ses choix et demande à participer à une sortie.

- **Organisateur :** crée une sortie, précise la date, l’heure et le nombre de places, puis accepte ou refuse les demandes de participation.

- **Administrateur :** gère les utilisateurs, les lieux, les activités et les contenus signalés.

---

## 4. Exigences fonctionnelles (FR)
> Forme recommandée : “Le système doit…”
- **FR-1 :** Le système doit <...>
- **FR-2 :** Le système doit <...>

---

## 5. Exigences non fonctionnelles (NFR)
> Performance / sécurité / disponibilité / UX / maintenabilité…
- **NFR-1 (Performance) :** <ex. temps de réponse < 2s>
- **NFR-2 (Sécurité) :** <ex. authentification requise>
- **NFR-3 (UX) :** <ex. parcours en ≤ 3 clics>
- **NFR-4 (Qualité) :** <ex. couverture minimale de tests>

---

## 6. Contraintes
- **C-1 (Technologie) :** <langage / framework imposé>
- **C-2 (Plateforme) :** <web / mobile / desktop>
- **C-3 (Délai) :** <dates de phases>
- **C-4 (Outils) :** <Git, CI, etc.>

---

## 7. Données & règles métier (si applicable)
- **Entités principales :** <User, Order, ...>
- **Règles métier :** <validation, calculs, permissions, etc.>

---

## 8. Hypothèses & dépendances
### 8.1 Hypothèses
- H-1 : <ex. utilisateurs ont un compte>
- H-2 : <...>

### 8.2 Dépendances
- D-1 : <API externe / BD / service>
- D-2 : <...>

---

## 9. Critères d’acceptation globaux (Definition of Done – mini)
- [ ] Fonctionnalités livrées et testées
- [ ] Tests unitaires présents
- [ ] Gestion d’erreurs minimale
- [ ] Documentation à jour (UML + ADR si requis)
