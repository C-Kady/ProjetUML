README - Diagramme d'Etat

1- Processus de réservation
 - processus décrivant l'état du système au cours d'une réservation du début à la fin de la location par le client 
ainsi que les évènements intermédiaires

2- Etats paiement
ce diagramme retrace les évènements et les états de paiement au cours d'une demande de paiement de réservation dans notre système
- si un paiement est en attente il peut : échoué, être annulé ou être validé
- si est paiement était validé il peut faire l'objet de remboursement après une demande d'annulation de réservation

3- Etats disponibilité des éléments de résidences

ce diagramme retrace les états possibles des éléments de résidences dans le système
- un élément peut être disponible lors de sa création dans le système puis :
	- peut être disponible puis réservé à la suite d'une demande de réservation
	- peut être en maintenance si le gestionnaire le programme
	- peut être disponible à la suite d'une annulation de réservation ou à la fin d'une maintenance
