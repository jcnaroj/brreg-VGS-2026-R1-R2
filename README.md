

  <h1 align="center">Grunnleggende javascript</h1>

  <p align="center">
   

  </p>
</p>


## Table of contents

- [Steg 1 Variabler og operasjoner](#Steg-1-Variabler-og-operasjoner)
- [Steg 2 Valgsetninger](#Valgsetninger)
- [Steg 3 Funksjoner](#Steg-3-Funksjoner)
- [Steg 4 Løkker](#Steg-3-Løkker)
- [Linker](#Linker)




## Steg 1 Variabler og operasjoner

For å forstå hva en variabel er, kan vi tenke på en beholder eller boks som kan inneholde en eneste verdi. Det finnes flere typer slike bokser (dvs. det finnss flere datatyper)


En variabel i JavaScript ser slik ut:

```javascript
let variabelNavn = "verdi";
```

'let' forteller JavaScript at det er en variabel. En variabel inneholder en verdi, som for
eksempel tall eller tekst :

```javascript
let tall = 7;
let tekst = "Dette er en tekst";
```

Følg disse instruksjonene:

- [ ] 1.Gå inn på https://jsfiddle.net/.
- [ ] 2.I JavaScript -vinduet skriver du følgende:

```javascript
let tall = 9;
let tekst = "Dette er en test";
```

Hver linje i javascript avsluttes med ; eller }, avhengig av om du lager en variabel eller en funskjon.
variabler avlsuttes med ; , funksjoner med }.

For at vi skal kunne skrive ut noe kan vi bruke alert(); som lager en pop-up melding på skjermen.

- [ ] 3.Skriv inn:
 ```javascript
   alert(tekst); 
  ```

- [ ] 4.Trykk på run
- [ ] 5.Vises teksten? hvis ikke spør om hjelp.
- [ ] 6.Lag to nye variabler

```javascript
let tall1 = 4;
let tall2 = 5;
```

- [ ] 7.Nå skal vi ta de to variablene og plusse dem sammen:

```javascript
alert(tall1 + tall2)
```

- [ ] 8.Trykk run, Fikk du 9?

- [ ] 9.Nå som vi vet at vi kan få JavaScript til å regne for oss, ta å bytt ut + med de andre regneartene vi har og undersøk om disse støttes av javascript.



<details><summary>tips ulike regnearter</summary>
<p>

#### noen eksempler på regnearter i JavaScript!

```javascript
let tallA = 5 + 1;
let tallB = tallA - 2;
let tallC = 10 * 6;
let tallD = tallC / tallA;
let tallE = 26 / 4; 

// i eksemplene ovenfor vill tallA bli 6 , tallB bli 4, tallC bli 60, tallD bli 10 og tallE bli 6,5
```

</p>
</details>

- [ ] 10.Hva blir alert(7 * 7)?

<details><summary>svar</summary>
<p>

49. Fordi 7 * 7 = 49.

</p>
</details>

La oss nå se på hvordan vi kan la en variabel være en annen:

- [ ] 11.Legg til enda en variabel

```javascript
let tall3 = tall2;
```

- [ ] 12.Skriv ut tall3 og tall2, bruk alert

- [ ] 13.Hva skjer om vi forandrer tall2 etter vi har satt tall3?

Vi satte jo tall3 til å være lik tall2? men tall3 blir ikke endret selvom vi endrer på tall2. Dette er fordi tall-variabler i JavaScript kun leser innhold i andre variable når vi setter eller forandrer de. så tall3 refererer ikke til tall2 den bare leste av verdien tall2 inneholdt.

Vi kan også legge til ekstra verdier til en variabel:

```javascript
let tall4 = tall3 + tall1 + 5;
```

- [ ] 14. Bruk alert() til å skrive ut tall4.

Nå har vi fått prøvd ut litt forskjellige variabeler, da skal vi bruke dette sammen med if-setninger for å sjekke om noe er sant eller ikke.

## Steg 2 Valgsetninger

Tøm innhold i JSFiddel før vi går videre.

En if/else-setning ser slik ut i JavaScript:

```javascript
if(betingelse) {
    // Kjør koden som blir skrevet her
} else {
    // Kjør koden som blir skrevet her istedet
}
```

Når vi bruker if/else sjekker vi om en betingelse er sann eller usann. La oss se på et eksempel med tall.

- [ ] 1.Skriv inn følgende:

```javascript
let tall = 5;
if(tall === 5) {
    alert("Tallet er 5");
} else {
    alert("Tallet er ikke 5");
}

```

Forklaring:
Dersom tall har verdien 5 vil den første meldingen skrives ut, dersom tall har en annen verdi, så vil den andre meldingen skrives ut. For å sjekke om en variabel er lik noe så bruker vi ===. Endre variabelen tall til andre verdier og se hvilken melding du får ut.

La oss se på et annet eksempel:

```javascript
let alder = 0;
if(alder >= 18) {
    alert("Du er gammel nok til å kjøre bil");
} else if(alder >= 16) {
    alert("Du er gammel nok til å kjøre moped");
} else {
    alert("Du er dessverre ikke gammel nok");
}
```

Kan du tenke deg til hva denne if/else-setningen gjør? Hvis ikke, spør oss! ?

Prøv å endre alder slik at du får testet om if/else-setningene fungerer.
La oss legge til noe som heter prompt, dette gjør at du kan ta inn input fra brukeren av nettsiden:

```javascript
let alder = prompt("Hvor gammel er du?");
```

Nå skal vi sjekke hva klokken er og skrive en melding ut i fra det. Da bruker vi noe som heter Date i JavaScript, denne inneholder informasjon om dagen i dag.
Vi lager to variabler, en som er en Date-klasse og en annen som henter timen vi er i nå:


```javascript
let dato = new Date(); // Henter informasjon om dagen i dag
let tid = dato.getHours(); // Henter timen (klokka) vi er i nå
```

- [ ] 2.Bruk alert til å sjekke hva variabelen tid inneholder.

I en if(betingelse) kan vi sjekke flere ting samtidig ved å bruke && eller ||.
-&& betyr "og" som vil si att begge påstander må vere sanne for at hele uttrykket skal bli sant,
-|| betyr "eller" som i enten eller, det betyr at en av påstandene må vere san for at hele uttrykket skal være sant.

Eksempel:
```javascript
let date = new Date();
let mnd = date.getMonth();
let dag = date.getDate();
let navn = "Selma"
if(navn === "Selma" && mnd === 1 && dato === 21) { // mnd = måned, dato = dagen i måneden
    alert("Gratulerer med navnedagen, Selma!");
}
```

For at denne koden skal være sann må navnet være Juliane og datoen må være 16.2, altså 16. Februar.
getMonth() leverer ut et tall fra 0-11, derfor er Januar 0 og ikke 1.
&& betyr som sagt 'og' altså både påstanden på høyre og venstre side av && må vere sann.
på lik linje har vi også || som betyr 'eller' altså påstanden er sann så lenge enten høyre eller venstre side er sann:


```javascript
if(mnd === 1 && dato === 21) {
    if(navn === "Samuel" || navn === "Selma" || navn === "Celine") {
        alert("Gratulerer med navnedagen!");
    } else {
        alert("Du har dessverre ikke navnedag i dag.");
    }
}
```

Legg merke til her at hvis datoen er 16.2 så hopper du inn til en ny if/else som sjekker om navnet ditt enten er Juliane eller Jill. Hvis det er feil dato skjer det ingenting.


## Steg 3 Funksjoner
Til nå har vi bare skrevet linjer med kode i JSFiddle. Når koden kjøres, så blir den lest fra topp til bunn, linje for linje, så koden vil kjøre i den rekkefølgen den står i. Men noen ganger ønsker vi at koden skal kjøre når en hendelse inntreffer eller noe annet skjer. Ved hjelp av funksjoner kan vi selv bestemme når koden skal kjøre eller om den ikke skal kjøre i det hele tatt.

Oppsettet ser slik ut:

```javascript
function funksjonsNavn(parameter1, parameter2) {
    // Kode som utføres når funksjonen kalles
}
funksjonsNavn(paramenter1, parameter2); // Gjør at funksjonen blir kjørt
```

En funksjon tar noen ganger inn noen variabler den ønsker å bruk ved hjelp av parameter, men ofte tar man ikke inn noen parameter og da ser en funksjon sånn ut:

```javascript
function navn() {
    // Kode
}

navn(); //for å kjøre funksjonen
```

En funksjon kalles ofte for en metode. Videre kommer vi til å bruke funksjon og metode litt om hverandre.

- [ ] 1.Ta nå koden som har med alder å gjøre, og legg den inn i en funksjon. Kall funksjonen for sjekkAlder


<details><summary>Hint</summary>
<p>

```javascript
function sjekkAlder() {
    let alder = prompt("Hvor gammel er du?");

    if(alder >= 18) {
        alert("Du er gammel nok til å kjøre bil");
    } else if(alder >= 16) {
        alert("Du er gammel nok til å kjøre moped");
    } else {
        alert("Du er dessverre ikke gammel nok");
    }
}
```
</p>
</details>


- [ ] 2.Legg på kode for at sjekkAlder skal kjøre.

```javascript
sjekkAlder();
```

La oss nå se på et annet eksempel på bruk av funksjoner. Vi skal nå lage en funksjon som skal ta inn et paramenter og returnere en verdi.

Vi lager en funksjon som konverterer fahrenheit(temperatur mål i USA) til Celsius.

- [ ] 3.Slett det du har i JSfiddle

- [ ] 4.Lag en følgende funksjon:


  ```javascript
function fahrenheitTilCelsius(fahrenheit) {
    return (5/9) * (fahrenheit - 32);
}
  ```


Forklaring

- fahrenheitTilCelsius(fahrenheit) betyr at vi tar inn en variabel som heter fahrenheit. Den kan kun brukes innenfor { } i funksjonen vår.

- return (5/9) * (fahrenheit - 32) bruker variabelen fahrenheit og regner sammen mattestykket som står der.

- Men hva betyr return?

- Return betyr at funksjonen returnerer en verdi til brukeren som brukeren kan se, lagre eller bruke videre. La oss se på et eksempel:

```javascript
let grader = fahrenheitTilCelsius(77);
```

- Koden over kjører funksjonen fahrenheitTilCelsius med paramenter 77. Funksjonen regner da ut hvor mange celsius 77 fahrenheit er og lagrer denne verdien i variabelen grader. bruk alert for å skrive ut og se hvor mange celsius dette blir.


## Steg 4 Løkker

Til nå har vi skrevet kode som kjøres én gang fra topp til bunn. Men noen ganger ønsker vi å gjøre **det samme flere ganger**. Da bruker vi **løkker**.

En løkke lar oss gjenta kode flere ganger automatisk.

Den vanligste løkken i JavaScript heter **for-løkke**.

En for-løkke ser slik ut:

```javascript
for(let index = 0; index < 5; index++) {
    // Kode som kjøres flere ganger
}
```

Forklaring:

- `let index = 0` → starter på 0  
- `index < 5` → løkken kjører så lenge dette er sant  
- `index++` → øker tallet med 1 hver gang  

Koden inni `{ }` vil da kjøre flere ganger.

---

### Eksempel 1 – skriv ut tall

1. Gå inn på https://jsfiddle.net/

2. Skriv følgende kode i JavaScript-vinduet:

```javascript
for(let i = 0; i < 5; i++) {
    alert(i);
}
```

3. Trykk **Run**

Hva skjer?

Du vil få opp tallene:

```
0
1
2
3
4
```

Prøv å endre `5` til `10`. Hva skjer nå?

---

### Eksempel 2 – skriv ut alle elever

Vi kan også bruke løkker til å gå gjennom en **liste (array)**.

1. Skriv inn følgende kode:

```javascript
const students = ["Elena", "Baris", "Maria", "Dave"];

for(let index = 0; index < students.length; index++) {
    console.log("Name of student is: " + students[index]);
}
```

Forklaring:

- `students` er en liste med navn
- `students.length` betyr hvor mange navn som finnes i listen
- `students[index]` henter ett navn fra listen

Når koden kjører vil dette skrives i **console**:

```
Name of student is: Elena
Name of student is: Baris
Name of student is: Maria
Name of student is: Dave
```

Hvis du vil se dette i popup i stedet kan du bruke `alert()`:

```javascript
const students = ["Elena", "Baris", "Maria", "Dave"];

for(let index = 0; index < students.length; index++) {
    alert("Name of student is: " + students[index]);
}
```

---

1. Lag en liste med tre navn:

```javascript
let elever = ["Ola", "Kari", "Per"];
```

2. Lag en løkke som skriver ut alle navnene med `alert()`.

Hint:

```javascript
for(let i = 0; i < elever.length; i++) {
    alert(elever[i]);
}
```

## Linker

#### Gruppeoppgaver
Lette oppgaver
* [Intro HTML/CSS](https://jsfiddle.net/Sion17/Luh45kxw/100/)
* [Fibonacci sekvens](https://jsfiddle.net/joakimvu/4dxgcfet/2/)
* [Intro til å hente data](https://jsfiddle.net/joakimvu/fzvan749/21/)
* [The Button](https://jsfiddle.net/dith0510/fkn26zyt/)

Middels oppgaver 
* [Animasjon](https://jsfiddle.net/Sion17/xtpq9dL8/97/)
* [Sammenlign Variable](https://jsfiddle.net/Sion17/796rkwc8/9/)

Vanskelige oppgaver
* [Kalkulatoren](https://jsfiddle.net/Sion17/4ugb05wy/20/)
* [Cubic Tap](https://jsfiddle.net/dith0510/2wn3r7f0/2/)
* [TODO Postit](https://jsfiddle.net/dith0510/0jog1q9h/)
* [Guessing Game](https://jsfiddle.net/dith0510/rs0q2z8g/)
* [Maskify](https://jsfiddle.net/dith0510/mnL5hg8f/)



##### Feedback

*   [Feedback](https://forms.gle/66DKRxUXiTNL8gwR9)
