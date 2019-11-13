

  <h1 align="center">Grunnleggende javascript</h1>

  <p align="center">
    Short description
    
  </p>
</p>


## Table of contents

- [Steg 1: Variabler og operasjoner](#Variabler og operasjoner)
- [Steg 2: If-setninger](#If)
- [Steg 3: Funksjoner](#Funksjoner)
- [Linker](#Linker)




## Steg 1: Variabler og operasjoner

En variabel i JavaScript ser slik ut: 

```javascript
var variabelNavn = "verdi";
```

var forteller JavaScript at det er en variabel. En variabel inneholder en verdi, som for
eksempel tall eller tekst :

```javascript
var tall = 7;
var tekst = "Dette er en tekst";
```

F�lg disse instruksjonene: 

- [ ] 1.G� inn p� https://jsfiddle.net/.
- [ ] 2.I JavaScript -vindu skriver du f�lgende:

```javascript
var tall = 9;
var tekst = "Dette er en test";
```

Hver linje i javascript avsluttes med ; eller }, avhengig av om du lager en variabel eller en funskjon. 
varibler avlsuttes med ; , funksjoner med }.

For at vi skal kunne skriv ut noe bruker vi alert();

- [ ] 3.Skriv inn:
 ```javascript
   alert(tekst); 
  ```

- [x] 4.Trykk p� run
- [ ] 5.Vises teksten? hvis ikke sp�r om hjelp. 
- [ ] 6.Lag to nye variabler 

```javascript
var tall1 = 4;
var tall2 = 5;
```

- [ ] 7.N� skal vi ta de to variablene og plusse dem sammen: 

```javascript
alert(tall1 + tall2)
```

- [ ] 8.Trykk run, Fikk du 9?

- [ ] 9.N� som vi vet at vi kan f� JavaScript til � regne for oss, ta � bytt ut + med de andre regneartene vi har og se om JavaScript klarer � regne ut med dem.



<details><summary>tips ulike regnearter</summary>
<p>

#### ulike regnearter i JavaScript!

```javascript
print("hello world!")
```

</p>
</details>


La oss n� se p� hvordan vi kan la en variabel v�re en annen:

- [ ] 10.Legg til enda en variabel

```javascript
var tall3 = tall2;
```


- [ ] 11.hva blir alert(7 * 7)?

<details><summary>svar</summary>
<p>

#### ulike regnearter i JavaScript!

49. Fordi 7 * 7 = 49.

</p>
</details>

- [ ] 12.Skriv ut tall3 og tall2, bruk alert

- [ ] 13.pr�v � endre p� tall2, hva skjer med tall3?

Vi satt jo tall3 til � v�re lik tall2? tall3 blir ikke endret selvom vi endrer p� tall2. Dette er fordi tall-variabler i JavaScript inneholder kun verdier, ikke referanser.

Vi kan ogs� legge til ekstra verdier til en variabel:

```javascript
var tall4 = tall3 + tall1 + 5;
```

- [ ] 14. Bruk alert() til � skrive ut tall4. 

N� har vi f�tt pr�vd ut litt forskjellige variabeler, da skal vi bruke dette sammen med if-setninger for � sjekke om noe er sant eller ikke.

## Steg 2: If -setninger 

En if/else-setning ser slik ut i JavaScript:

```javascript
if(betingelse) {
    // Kj�r koden som blir skrevet her
} else {
    // Kj�r koden som blir skrevet her istedet
}
```

N�r vi bruker if/else sjekker vi om en betingelse er sann eller usann. La oss se p� et eksempel med tall.

- [ ] 1.Skriv inn f�lgende:

```javascript
var tall = 5;
if(tall === 5) {
    alert("Tallet er 5");
} else {
    alert("Tallet er ikke 5");
}

```

Forklaring
Dersom tall har verdien 5 vil den f�rste meldingen skrives ut, dersom tall har en annen verdi, s� vil den andre meldingen skrives ut. For � sjekke om en variabel er lik noe s� bruker vi ===. Endre variabelen tall til andre verdier og se hvilke melding du f�r ut.

La oss se p� et annet eksempel:

```javascript
var alder = 0;
if(alder >= 18) {
    alert("Du er gammel nok til � kj�re bil");
} else if(alder >= 16) {
    alert("Du er gammel nok til � kj�re moped");
} else {
    alert("Du er dessverre ikke gammel nok");
}
```

Kan du tenke deg til hva denne if/else-setningen gj�r? Hvis ikke, sp�r oss! ? 

Pr�v � endre alder slik at du f�r testet om if/else-setningene fungerer.
La oss legge til noe som heter prompt, dette gj�r at du kan ta inn input fra brukeren av nettsiden:

```javascript
var alder = prompt("Hvor gammel er du?");
```

N� skal vi sjekke hva klokken er og skrive en melding ut i fra det. Da bruker vi noe som heter Date i JavaScript, denne inneholder informasjon om dagen i dag. 
Vi lager to variabler, en som er en Date-klasse og en annen som henter timen vi er i n�:


```javascript
var dato = new Date(); // Henter informasjon om dagen i dag
var tid = dato.getHours(); // Henter timen (klokka) vi er i n�
```
 
 - [ ] 2.Bruk alert til � sjekke hva variabelen tid inneholder. 

I en if(betingelse) kan vi sjekke flere ting samtidig ved � bruke && eller ||. && betyr og, || betyr eller. Eksempel:

```javascript
var date = new Date();
var mnd = date.getMonth();
var dato = date.getDate();
if(navn === "Lars" && mnd === 7 && dato === 10) { // mnd = m�ned, dato = dagen i m�neden
    alert("Gratulerer med navnedagen, Lars!");
}
```

For at denne koden skal v�re sann m� navnet v�re Lars og datoen m� v�re 10.8, alts� 10. August. getMonth() leverer ut et tall fra 0-11, derfor er August 7 og ikke 8.
Samme kan du gj�re med || hvis du heller vil sjekke eller:


```javascript
if(mnd === 7 && dato === 10) {
    if(navn === "Lars" || navn === "Lasse") {
        alert("Gratulerer med navnedagen!");
    } else {
        alert("Du har dessverre ikke navnedag i dag.");
    }
}
```

Legg merke til her at hvis datoen er 10.8 s� hopper du inn til en ny if/else som sjekker om navnet ditt enten er Lars eller Lasse. Hvis det er feil dato skjer det ingenting.


## Steg 3: Funksjoner
Til n� har vi bare skrevet linjer med kode i JSfidle. N�r koden kj�res, s� blir den lest fra topp til bunn, linje for linje, s� koden vil kj�re i den rekkef�lgen den st�r i. Men noen ganger �nsker vi at koden skal kj�re n�r en hendelse inntreffer eller noe annet skjer. Ved hjelp av funksjoner kan vi selv bestemme n�r koden skal kj�re eller om den ikke skal kj�re i det hele tatt.

Oppsettet ser slik ut:

```javascript
function funksjonsNavn(parameter1, parameter2) {
    // Kode som utf�res n�r funksjonen kalles
}
funksjonsNavn(paramenter1, parameter2); // Gj�r at funksjonen blir kj�rt
```

En funksjon tar noen ganger inn noen variabler den �nsker � bruk ved hjelp av parameter, men ofte tar man ikke inn noen parameter og da ser en funksjon s�nn ut:

```javascript
function navn() {
    // Kode
}

navn(); //for � kj�re funksjonen
```

En funksjon kalles ofte for en metode. Videre kommer vi til � bruke funksjon og metode litt om hverandre.

 - [ ] 1.Ta n� koden som har med alder � gj�re, og legg den inn i en funksjon. Kall funksjonen for sjekkAlder 
 

<details><summary>Hint</summary>
<p>

```javascript
function sjekkAlder() {
    var alder = prompt("Hvor gammel er du?");

    if(alder >= 18) {
         console.log("Du er gammel nok til � kj�re bil");
    } else if(alder >= 16) {
        console.log("Du er gammel nok til � kj�re moped");
    } else {
        console.log("Du er dessverre ikke gammel nok");
    }
}
```
</p>
</details>


 - [ ] 2.Legg p� kode for at sjekkAlder skal kj�re.

```javascript
sjekkAlder();
```

La oss n� se p� et annet eksempel p� bruk av funksjoner. Vi skal n� lage en funksjon som skal ta inn et paramenter og returnere en verdi.

Vi lager en funksjon som konverterer fahrenheit(temperatur m�l i USA) til Celsius.

 - [ ] 3.Slett det du har i JSfiddle
 
  - [ ] 4.Lag en f�lgende funksjon: 
  
  
  ```javascript
function fahrenheitTilCelsius(fahrenheit) {
    return (5/9) * (fahrenheit - 32);
}
  ```
  
  
Forklaring

   - fahrenheitTilCelsius(fahrenheit) betyr at vi tar inn en variabel som heter fahrenheit. Den kan kun brukes innenfor { } i funksjonen v�r.

   - return (5/9) * (fahrenheit - 32) bruker variabelen fahrenheit og regner sammen mattestykket som st�r der.

   - Men hva betyr return?

   - Return betyr at funksjonen returnerer en verdi til brukeren som brukeren kan se, lagre eller bruke videre. La oss se p� et eksempel:

```javascript
var grader = fahrenheitTilCelsius(77);
```

 - Koden over kj�rer funksjonen fahrenheitTilCelsius med paramenter 77. Funksjonen regner da ut hvor mange celsius 77 fahrenheit er og lagrer denne verdien i variabelen grader.

## Linker

#### ulike regnearter i JavaScript!
* [Gruppeoppgave 1]()
* [Gruppeoppgave 2]()
* [Gruppeoppgave 3]()
* [Gruppeoppgave 4](https://jsfiddle.net/Olav7/ftu3g9xr/42/)