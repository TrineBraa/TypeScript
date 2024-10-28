[[TypeScript Fundamentals]]

Introduksjon til TypeScript
Verktøy
Hello World!
Installere Typescript i et prosjekt
Bygging
get the code?
Debugging


Introduksjon til TypeScript:
- Dependable
- Reliable
- consistent JavaScript Code

Hvorfor TypeScript:
- JavaScript med sikkerhets nett
- fremtiden, i dag
- oppdager mer error iløpet av utvikling
- utviklet verktøy
- confidence

Key features
- Strongly Typed
- Classes
- Interfaces
- Generics
- Compiles as JavaScript
- Functions


Tools:
- Node.js
		- Node for LTS (Long term support)
		- Verifiser instalasjonen
			- kjør en terminal og kjør node --version
- Visual Studio Code
		- parameter hint
		- go to definition or symbol
		- peek (den lar deg peeke på annen fil eller kode)
		- renaming
		- tips via lyspæren.

.ts er filnavnet for TypeScript filer. 
Ts filer må også compiles til JavaScript siden browseren ikke kjenner igjen TS.


Bygging:

I tsconfig.json filen: 

caniuse.com - (https://caniuse.com/)
- Du kan sjekke hvile fetures du støtter og velge hvilken type TS du vil ha. Det ebste er å gå for det nyeste du tror kundene støtter. 

sourceMap Settes til True, denne vil kunne mappe kode fra browser til TS slik at du kan gjøre debugging i browser. 

ModuleResolution vil hjelpe å gjøre litt bedre import settings inne i TypeScript.

Debugging:
Når Sourcemapping er slått på vil du kunne se Typescriptet i browseren og bruke denne til debugging, det betyr også at du kan sette breakpoints og gå gjennom koden bit for bit dersom det er behov for det. 