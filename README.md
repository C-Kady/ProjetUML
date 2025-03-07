# ProjetUML
COULIBALY Karidja & KOCORA Roxane

commentaires par rapport aux classes java générées:

*****Relation Client - Reservation******

Dans notre diagramme on a dit :

1 client peut faire 1 ou plusieurs reservations et une reservation est faite par 1 client 
le code Java nous a mis un attribut  public List<Reservation>  = new ArrayList<Reservation> () dans la classe Client, et la classe reservation possede un attribut client de type Client. Cela correspond exactement a notre modelisation. Cet attribut List<Reservation> indique toutes les reservations faites par un client et la reservation a comme reference le client concerné.


1 reservation est faite pour une seule piece pendant un temps donné et 1 piece est reservée a un moment donné. Dans le code Java on retrouve dans Reservation un attribut piece de type Piece et dans Piece un attribut reservation de type Reservation, chacune fait exactement reference a la classe concernée. Cela respecte notre modelisation.


1 reservation peut avoir plusieurs paiements et un paiement concerne une seule reservation, le code Java généré  nous a mis dans la Reservation un attribut de type  public List<Paiement>  = new ArrayList<Paiement> () et dans paiement on a un attribut paiement de type Paiement.
cela est conforme a la modelisation faite au depart (l'attribut List<Paiement> indique tous les paiement seffectués pour une reservation et le paiement a la reference de la reservation qui le concerne).


1 Gestionnaire peut géré plusieurs residences et une residence est gérée par un seul Gestionnaire. Dans le code Java on voit que la classe Gestionnaire poddède un attribut : public List<Residence>  = new ArrayList<Residence> () ce qui montre la liste des residences gérée par le Gestionnaire et dans la classe Residence on a un attribut de type Gestionnaire qui fait reference au gestionnaire qui le gère.


1 residence est constituée de plusieurs pieces et une piece donnée concerne 1 seule résidence. Dans le code java la classe Residence possede un attribut  List<Piece> piece et piece un attribut residence de type Residence. Cele materialise bien notre modelisation


1 piece peut avoir plusieurs contraintes et une contrainte peut concerné plusieurs pieces. Le code java nous fait apparaitre dans la classe Contrainte un attribut public List<Piece>  = new ArrayList<Piece> (); qui correspond au fait qu'un attribut concerne plusieurs pieces  et la classe Piece a un attribut  public List<Contrainte> containte = new ArrayList<Contrainte> (); qui correspond au fait qu'elle puisse avoir plusieurs contraintes. cela respecte notre modélisation.

