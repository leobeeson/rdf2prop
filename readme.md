### Nodes:
	• ?class rdf:type rdfs:Class
		○ ?instance rdf:type ?class <- Use to instantiate instances, once you have the lists of classes.

### Attributes of Nodes:
	• ?class rdfs:label rdf:literal
		○ ?instance rdfs:comment rdf:literal
	• ?class rdfs:comment rdf:literal
		○ ?instance rdfs:comment rdf:literal
	• ?instance rdf:language rdf:literal
	• ?instance rdfs:seeAlso
		• rdfs:isDefinedBy
	• rdf:value???

### Relationships:
	• Taxonomical relationships between nodes:
		○ ?class rdfs:subClassOf ?class2 .
		○ ?class owl:equivalentClass ?class . <- TODO: reasoning engine
		○ rdfs:member (and suclasses of rdfs:member) <- TODO: reasoning engine
	• Taxonomical relationships between relationships:
		○ ?r1 rdfs:subPropertyOf ?r2 . <- TODO: reasoning engine (#wouldn't a subproperty have been first delcared as a property? If so, we'll have classified it among the properties as either an attribute or a relationship)
		○ ?r1 owl:inverseOf ?r2 . <- TODO: reasoning engine

#### Discenrning attributes from relationships:
	• If ?instance ?property rdf:resource -> ?instance -> ?class -> relationship
	• If ?instance ?property rdf:literal -> ?instance -> ?class -> attribute

### Attributes of Relationships:
	• ?r1 rdf:type owl:SymmetricProperty . <- TODO: reasoning engine
	• ?r1 rdf:type owl:TransitiveProperty . <- TODO: reasoning engine

#### TODO:
• Lines marked with: "TODO: reasoning engine"
• rdfs:domain
• rdfs:range <- TODO: reasoning engine

