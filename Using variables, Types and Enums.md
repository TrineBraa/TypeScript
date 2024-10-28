[[Getting Started with TypeScript]]

- Benefits of Types
- built-in types
- creating and using typed variables
- creating and using enums

Et sted du kan bruke Typescript fritt for å jobbe med det:
https://www.typescriptlang.org/


Benefits of Types:
TypeScript kan tenkes på som et autovern som holder deg inne på veien så du ikke kjører utfor når du koder. 
Du vil kunne bli varslet mens du koder at det er error i koden.
et eks med JavaScript:
![[Pasted image 20241024134458.png]]
Der vil Javascript la deg ha 2 som tall og 2 som string, den vil ikke gi deg et error og en slik feil kan følge med hele veien til produksjon og erroret kan da bli et problem der ved å gi feil svar.

eks med TypeScript:
![[Pasted image 20241024134612.png]]
Her er variablene merket med hvilken data type som er bestemt for variablene. og når du da setter 2 som string vil det komme som en error og du vil kunne rette opp i dette ved at Typescript varsler deg om denne erroren. 

error til dette eksemplet:
![[Pasted image 20241024134849.png]]


Built-in Types:
- string
- number
- boolean
- array

Det er flere enn disse, men disse er de du vil bruke daglig.

TypeScript types kan brukes på variabler og parametre som følger et mønster som dette:
VariabelNavn : Type
På denne måten kan du sette hvilken data type denne variabelen er beregnet til å ta inn. 

let firstName: string; (Denne variabelen er nå en string. Du vil få error dersom du prøver å sette inn en annen data type inn i denne variabelen.)

function add(x: number, y: number) { funksjons teksten din her}
Her har du definert parametrene med en type. 


Additional Built-in Types:
- undefined (En variabel du aldri bruker, aldri gir en verdi)
- null (en variabel som ikke har noen verdi)
- any (DErsom en variabel skal kunne være hva som helst, denne prøves det å unngå, den slakker på typescript og error kan oppstå som ikke fanges opp fordi variabelen er satt til any. )
- void ( en funksjon kan returnere void, funksjonen gjør noe men gir ikke noe verdi i retur)

Bruk ekstra TypeScript typer som any, void, undefined, null og andra eksisterer i TypeScript. 
I tilfeller hvor variabler kan være en eller flere typer kan en union type brukes. 
Dette er et tilfelle h vor data skal være number, string og eller objekt.

let product : any; (Prøv å unngå dette da det vil gjøre TypeScript ubrukelig.)

let firstName: string | undefined | null;
i dette tilfellet kan firstname være enten en string, undefined eller null. Dette er en union type


Du kan ha funksjoner som ikke returnerer noe, kanskje du har en log funksjon som tar i mot en melding som logges i consollen eller sendes til serveren uten at den gir en verdi tilbake til senderen

function log (msg: string) : void {  }
dette er en funksjon som ikke returnerer noen verdi


Enums:
![[Pasted image 20241025094307.png]]


Create and using Typed Variables:

Let firstName = "Dan"; // Type inference - Den finner automatisk ut hvilken type det er i denne variabelen.


let firstName: string; 
- Dette er bra dersom du skal gi denne variabelen en verdi senere. for den vil vite at det er en String den kan forvente og ikke noe annet. 

let aTestArray: string[] = [];
- Det er veldig lurt å gi et array en verdi slik at du ikke ender opp med et array av masse forskjellige verdier. Dersom du ikke spesifiserer når du setter opp et array vil den få en type av any. 

Dersom du har en string som du vil sette til null vil du måtte sette opp en uniontype som gjøres med |:
let firstName: string | null;
dette betyr da at du kan sette firstName til null.
Dette må gjøres dersom du har strictmode på. Du kan skru dette av for litt mer flexibilitet. 

Creating and using Enums:

Dersom du setter opp en variabel med mange forskjellige verdier, må du huske hva variabelen inneholder samt hvordan casing du har skrevet det i. du kan bli kvitt slike ting ved å bruke Enums.

Du kan samle alle disse verdiene i en Enum, på denne måten når du kaller på den vil koden automatisk kunne gi deg verdiene uten at du selv må huske hvordan du skrev det ol. 

![[Pasted image 20241025100324.png]]

Dersom du setter const enum vil dette føre til at index nummeret blir selv enumen, og du har egentlig ingenmåte å  konvertere dette tilbake til verdien du faktisk hadde satt der. Du vil da bare håndtere index nummeret og ingenting annet. 

