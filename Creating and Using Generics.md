[[Creating and Using Classes]]

![[Pasted image 20241028133307.png]]

Ved å bruke Generics vil du kunne gjenbruke koden din mye mer fordi du gir generics istedet for spesifikke verdier. 

![[Pasted image 20241028135348.png]]
I dette eksemplet forteller vi denne funksjonen at vi kommer til å fortelle den hvilken type det kommer til å være, om det er string et nummer eller lingende. Og her er det også satt at den skal returnere T.

![[Pasted image 20241028135530.png]]

Her setter vi at T representer ett nummer. 

![[Pasted image 20241028135748.png]]


Generics and functions

Dersom du har flere lister f.eks med forskjellige ting, som FoodProducts, Customers, orders ol. Istedet for å skrive funksjoner for hver av disse kan du lage en generic funksjon som du da vil kunne bruke med alle de forskjellige listene du har. 
![[Pasted image 20241028140510.png]]

![[Pasted image 20241028140602.png]]


Generics with interfaces

![[Pasted image 20241028141236.png]]

![[Pasted image 20241028141313.png]]

![[Pasted image 20241028141414.png]]

Generics and classes

Du kan sette opp en klasse til å ta in en generic og alle elementene i klassen vil ta i bruk den generice typen du sender inn. 

![[Pasted image 20241028141953.png]]

Generic constraints

![[Pasted image 20241028142723.png]]

Når du lager en generic vil ikke Typescript vite at det f.eks er en id i de forskjellige typene du sender in, du kan da extende den til HasId, som vil da sette en constraint til denne klassen og si at det du sender inn kommer til å ha en id. 
Husk på og sette en interface over som da heter HasId med en id som et nummer. 




