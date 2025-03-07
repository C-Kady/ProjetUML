README - Diagramme de séquence du Système : Annulation de réservation
///// Dans le dossier Séquence tous les objets ont été nommées de facon générale, nous n'arivions pas a les nommés de cette facon : ****client004 : Client**** voila pourquoi on les a nommés juste comme ca:  ****Client :****
- le client fait une demande d'annulation de réservation
- le système automatiquement exécute la demande et détruit l'objet de réservation créée
- il initie une demande remboursement si la demande est fait dans les délais sinon le remboursement n'est pas effectuée

Diagramme de séquence du Système : Modification de réservation

- le client veut modifier sa réservation ; seuls les services et certaines prestations peuvent être modifiés 
après réservation
- si le client modifie la période de réservation , le gestionnaire est alors alerté par message et celui-ci
peut valider ou pas la demande du client si l'objet de modification n'est pas disponible
- une fois la modification effectué le système affiche un message de confirmation ou d'erreur

Diagramme de séquence du Système :  Réservation de résidence
- le client une fois sur notre site fait une recherche de résidence
- en fonction de la requête du client, le système affiche une liste des éléments disponibles
- le client fait un choix 
- le système lui affiche un formulaire d'inscription et de réservation
- une fois rempli le système valide la conformité du formulaire puis envoie les infos au gestionnaire
- le gestionnaire reçoit la demande de réservation et peux accepter ou non la demande
- S'il accepte le client reçoit une demande de paiement pour confirmer la réservation 
- Si le gestionnaire refuse, le client peut faire une autre demande sur un autre bien du site

Diagramme de séquence du Système :  Paiement

- le client clique sur le bouton "Payer" qui le redirige vers le système de paiement
- deux cas se présentent :
 - le paiement est validé alors le système informe par un message que la validation est confirmée 
et le client est redigéré vers une page de connexion afin d'accéder à son espace sur le site
 - le paiement est rejeté alors le système redirige le client vers la page de paiement pour qu'il réessaie

Diagramme de séquence du Système :  Donner avis
 
- le client peut laisser un avis sur le site après effectuée une réservation au moins une fois
- une fois l'avis enregistré sur le site ,le système demande validation auprès du gestionnaire
- si celui-ci le valide  le commentaire est alors affiché sur le site sinon il est rejeté et est supprimé

Diagramme de séquence du Système :  Gérer Résidence

- le gestionnaire une fois connecté au site peut utiliser les options pour : 
	- créer , ajouter , modifier ou supprimer des éléments de résidences
	une fois validé le système enregistre les données dans une base à travers les requêtes
	- pendant la création d'une résidence il devra créer aussi les pièces et les contraintes rattachées à ceux-ci

Diagramme de séquence du Système :  Connexion

- l'utilisateur s'il est inscrit peut se connecté sur le site
- il rempli les informations de connexion (login et mot de passe ) puis envoie le formulaire
- le système vérifie les infos reçues du formulaire puis les compare à ceux présents dans la BD récupérés à travers une requête SQL
- si les données sont identiques alors un message de réussite est affiché et la page est redirigée vers l'espace personnel du client
-sinon la page de connexion est retournée avec des messages indiquant les erreurs sur le formulaire


	





