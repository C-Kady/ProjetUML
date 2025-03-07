README - Diagramme de Classe du Système de Gestion de Résidence

📌 Description Générale

Ce diagramme de classe représente le système de gestion des résidences, permettant aux clients de réserver des logements et aux gestionnaires d’administrer ces résidences. Il définit les entités principales, leurs attributs et leurs relations.

1- Client
Description : Représente un utilisateur qui réserve un logement.

Attributs :

Nom, Prenom : Identité du client.

DateNais : Date de naissance.

Contact : Numéro de contact.

email : Adresse électronique.

Méthodes :

seConnecter(), voirLogement(), reserverLogement(), payerLoyer(), donnerAvis()...

2 -Gestionnaire

Description : Personne en charge de la gestion des résidences.

Attributs : Nom, Prenom, contact, email.

Méthodes :

gererDisponibilites(), gererContrainte(), gererTarif(), gererPiece(), gererResidence().

3- Résidence

Description : Bâtiment contenant plusieurs logements.

Attributs :

Description, nbPieces, adresse, ville.

Relations :

Gérée par 1 Gestionnaire (relation 1..*).

Contient plusieurs Pièces (1..*).

4- Pièce

Description : Une unité (exemple : chambre, studio) dans une résidence.

Attributs :

NomPiece, Tarif, PeriodeDebut, PeriodeFin, disponible, Description.

Relations :

Appartient à une seule Résidence.

Peut avoir plusieurs Contraintes (1..*).

Peut être associée à plusieurs Réservations (1..*).

5- Réservation

Description : Gère la réservation d’un logement par un client.

Attributs : dateDebut, dateFin, coutLoyer.

Relations :

Effectuée par 1 Client (1..*).

Concerne 1 ou plusieurs Pièces (1..*).

Génère 1 ou plusieurs Paiements (1..*).

6- Paiement

Description : Trace les paiements effectués par les clients.

Attributs : Numero, date, montant.

Relations :

Lié à une Réservation (1..*).

7-  Contrainte

Description : Règles associées aux pièces (exemple : durée minimale de séjour, interdiction d’animaux).

Attributs : Type, Description.

Relations :

Client → Réservation

Un client peut effectuer plusieurs réservations (1..*).

Réservation → Pièce

Une réservation peut concerner plusieurs pièces (1..*).

Gestionnaire → Résidence

Un gestionnaire gère plusieurs résidences (1..*).

Résidence → Pièce

Une résidence contient plusieurs pièces (1..*).

Pièce → Contrainte

Une pièce peut avoir plusieurs contraintes (1..*).

Réservation → Paiement

Une réservation génère plusieurs paiements (1..*).