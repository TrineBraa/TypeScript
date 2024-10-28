[[Creating and using functions]]

What is an interface
		An interface is a code contract
		interface definerer formen av data
			det er som en form som brukes til baking.

Ved bruk av interface er det vanskelig å vite hvilken data vi får tilbake fra en funksjon. 
	Det kan være utfordrende og finne ut av typen data i JavaScript
	TypeScript kan hjelpe i dette senarioet siden der setter en data typen og vill kunne få error i koden dersom noe ikke stemmer. 
Hvordan vet du at du sender rett data til en funksjon?

![[Pasted image 20241028093041.png]]

![[Pasted image 20241028093122.png]]

Defining an interface

Dersom du finner deg selv beskrive inholdet i et objekt f.eks. flere ganger vil en interface hjelpe.
interface er et Typescript spesifisert nøkkelord.
Interface er Development time ONLY, den kommer ikke med i produksjonen

![[Pasted image 20241028093425.png]]![[Pasted image 20241028093619.png]]


en funksjon som kaller getProducts, lager en interface til dette. 


![[Pasted image 20241028093541.png]]
Nå vil du kunne legge inn nye aspekter i Product og når denne brukes vil du få error om ikke ting følges opp skikkelig. Dersom du ønsker å ha valgfrie aspekter kan du sette et ? før : når du setter den opp, eks. 
				- Description?: string

Using an interface

'Hva er riktig måte å gi en interface et navn?'
- Gi navn med konsistens
	- Hold deg til en måte å navn gi interfaces på. 

Interface vs. Type

![[Pasted image 20241028095932.png]]

Interface er mye strengere enn type, En Type vil kunne ta en string, mens en interface vil ikke ta noe annet enn et objekt. Dette vil føre til klarere rettningslinjer gjennom development. 

Du kan bruke type for litt mer fleksibilitet, dersom du trenger en string, boolean eller lignende. 
![[Pasted image 20241028103819.png]]

Du kan også gjøre det på denne måten og dermed bruke begge metodene, den vil ta enten et objekt eller en string. 
et annet valg er å bruke enum til product. 
