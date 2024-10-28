[[Using variables, Types and Enums]]
[[Getting Started with TypeScript]]


Fundations of functions
Parametres and return values
Sychronous and asynchronous


Specifying Typed Parametres

Ved å bruke Type i variabler gjør det mye raskere og lettere å finne error i koden under utvikling. 

ordet hoisted betyr at vi løfter koden. som et eksempel til dette er at du skriver en funksjon også over denne funksjonen kaller du på funksjonen. 
![[Pasted image 20241025102047.png]]


Defining functions

![[Pasted image 20241025102721.png]]

her vil function være en deklarasjon
mens const er et uttrykk

Med en deklarasjon kan du sette i dette tilfellet consten over funskjonen. mens dersom du bruker const må denne settes opp før du kan bruke variabelen i dette tilfellet i console.log
Dette kommer av at en funksjon er  hoisted altså løftet opp som gjør at det er ok å kalle på den før eller etter funksjonen er satt opp.
Mens Const må deklareres først før du kan kalle på den. Så i tilfellet med den må den settes opp først før du kan gjøre kall til den. 


Return Values and Types

Du kan definere en return type i funksjons kallet ved at du setter en kolon etter parametre og spesifiserer der hvilken return type du ønsker fra denne koden. eks:
* function randomNumberFunction (x: number, y: number): number {  }
* Dette fører til at funksjonen vet at det er et number den skal gi i retur verdi. 

Dersom du ønsker å få et array i retur som en verdi i en funksjon. 
![[Pasted image 20241025104532.png]]

Du kan igjen spesifisere hvilken type array denne funskjonen skal sende i retur ved å legge til dette:

function getProductNames() : string [] { ... };
Denne vil returnere en array med strings.
du kan også gjøre det samme med forskjellige typer data. som f.eks. et objekt.
Dersom du har et array med objekter kan du bruke find funksjonen når du går gjennom arrayet og den ville kunne returnere et objekt fra arrayet.
Du kan igjen spesifisere hva du ønsker ut av funksjonen. 
et eks:
Du har et array kalt sampleProducts av objekter som er productType og du ønsker å få ett av objektene i dette arrayet via id. du vil da kunne spesifisere at id som funksjonen mottar er et number. og at funksjonen skal returnere et ProductType når du mapper gjennom arrayet. du kan også igjen sette | undefined for også å gi funksjonen muligheten til å returnere undefined om den ikke finner noe med den ID. 


Asynchronous functions

![[Pasted image 20241025132010.png]]

Du kan spesifisere denne på denne måten:
![[Pasted image 20241025132055.png]]


Arrow functions

En pil funksjon sier basically 'return whatever this curly braces function does.'

Dette er en kodebit hvor du ikke bruker pil funksjonen. Da må du sette en ny funksjon inne i funksjonen og returne verdien fra den.
![[Pasted image 20241025132759.png]]


Her har du satt pil funksjonen som gjør at du ikke trenger å sette funskjon inn i koden. Dersom koden utfører kunn en linje av kode vil den automatisk sende tilbake verdien. vist ikke vil du sette { } for å utføre flere kodesnutter i denne pil funksjonen. 
![[Pasted image 20241025132856.png]]


Optional Parameters

![[Pasted image 20241025134655.png]]
Du vil kanskje kunne sende inn ikoner med noe du skal laste opp på siden din, men kanskje ikke alle tingene har et ikon, du kan på denne måten sette ikon som en optional parameter. 


Default Parameters

![[Pasted image 20241025134930.png]]
Her setter du en verdi på max number og dette vil bli en default verdi om du ikke spesifiserer noe annet.


Rest Parameters

![[Pasted image 20241025135511.png]]
her er restOfAddress et rest parameter. som settes opp med de tre punktum forran. alle andre argumenter du sender inn etter de to første vil settes inn i dette arrayet. 
![[Pasted image 20241025135910.png]]

Parameter Destructuring

DErsom du har funksjoner eller variabler som har 20-40 argumenter kan det være veldig bra å bruke parameter destructuring. 
Du kan bruke dette ved å sette parameter inn i {   } kan du dra ut enkelte deler av et objekt foreksempel:
![[Pasted image 20241025140458.png]]
Du vil da slippe å måtte skrive i dette tilfellet: product.id, product.name ol. 