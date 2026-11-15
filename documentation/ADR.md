# ADR-01 — Confier la décision de participation à l’organisateur

**Statut :** Proposed  
**Date :** 2026-11-11  
**Décideurs :** Équipe The Avengers  
**Contexte projet :** Turisty — Gestion des demandes de participation aux sorties

---

## 1. Contexte

- **Problème / besoin :** Un membre doit pouvoir demander une place à une sortie. L’organisateur doit pouvoir traiter la demande sans dépasser la capacité de sa sortie.
- **Contraintes :** Un membre ne peut pas envoyer deux demandes pour la même sortie. Seul l’organisateur de la sortie peut accepter ou refuser une demande. Le nombre de places disponibles peut changer entre l’envoi et le traitement.
- **Forces en présence :** Les vérifications automatiques réduisent le travail manuel, mais l’organisateur doit garder le contrôle de sa sortie.

---

## 2. Décision

- **Nous choisissons :** Turisty vérifie que la sortie est ouverte, qu’une place est disponible et qu’il n’existe pas déjà de demande pour le même membre et la même sortie. Si ces conditions sont remplies, la demande passe au statut « En attente ». L’organisateur accepte ou refuse la demande. Avant de confirmer une acceptation, Turisty revérifie les places disponibles.
- **Pour :** Éviter les doublons et les confirmations sans place disponible, tout en laissant la décision finale à l’organisateur.

---

## 3. Alternatives considérées

### Option A — Approver automatiquement les demandes admissibles

- **Avantage :** Le membre peut recevoir une réponse sans attendre l’organisateur.
- **Inconvénient :** L’organisateur ne décide pas de chaque participation. Cette option ne correspond pas à la règle décrite dans le cahier des charges v0.1.

### Option B — Vérification automatique et décision de l’organisateur

- **Avantage :** Turisty bloque les demandes non admissibles et l’organisateur conserve la décision finale.
- **Inconvénient :** Le membre doit attendre que l’organisateur traite sa demande.

---

## 4. Justification

- L’option B respecte les exigences FR-9 et FR-10 du cahier des charges.
- Le système peut vérifier les doublons et les places sans effectuer d’auto-approbation.
- La deuxième vérification évite de confirmer une place qui a été prise entre l’envoi de la demande et son traitement.

---

## 5. Conséquences

### Positives

- Les demandes sont suivies selon trois statuts : « En attente », « Acceptée » et « Refusée ».
- Seule une demande acceptée confirme la participation.

### Négatives / Risques

- Une demande peut rester en attente si l’organisateur ne l’a pas encore traitée.
- Si la dernière place est prise avant l’acceptation, Turisty bloque la confirmation, laisse la demande en attente et informe l’organisateur.

### Impact sur l’architecture / le code

- Le diagramme TO-BE et la fiche UC-08 montrent la vérification des places avant la confirmation.
- Dans l’ERD, `Sortie.NbPlacesMax` indique la capacité et `Demande.StatutDemande` indique l’état de la demande.
- La clé composée (`IdSortie`, `IdCompte`) empêche d’enregistrer deux demandes du même compte pour la même sortie.

---

## 6. Plan d’implémentation

- [ ] Vérifier l’ouverture de la sortie, les places et les doublons au moment de l’envoi.
- [ ] Permettre à l’organisateur de traiter uniquement les demandes de ses propres sorties.
- [ ] Revérifier les places avant de confirmer l’acceptation et communiquer le résultat.

---

## 7. Validation

- **Demande admissible :** elle est enregistrée « En attente », sans confirmation de participation.
- **Demande en double :** aucune deuxième demande n’est enregistrée pour le même compte et la même sortie.
- **Acceptation avec une place disponible :** la demande devient « Acceptée » et le membre reçoit une confirmation.
- **Dernière place déjà prise :** l’acceptation est bloquée, la demande reste en attente et aucune confirmation n’est envoyée.
- **Demande refusée :** son statut devient « Refusée » et le membre reçoit un message de refus.

---

## 8. Liens

- **UML :** [Diagramme d’activité TO-BE](./diagrammes/userstory8_tobe.png)
- **Spécification :** [Fiches de cas d’utilisation — voir UC-08](./diagrammes/Turisty_use%20Case%20Specifications.docx)
- **Référence :** [Cahier des charges v0.2 — FR-9 et FR-10](./Cahier%20De%20Charges%20-%20SRS.md)
- **Issue / Tâche :** Non créée.
