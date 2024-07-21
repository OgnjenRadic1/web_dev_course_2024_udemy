
# Kratki Vodič za HTML Tagove

## 1. Osnovna Struktura

- **`<!DOCTYPE html>`**: Deklaracija HTML verzije.
- **`<html>`**: Koreni element dokumenta.
- **`<head>`**: Sadrži metapodatke i linkove ka spoljašnjim resursima.
- **`<meta>`**: Definiše metapodatke, kao što su karakterna enkodiranost i viewport.
- **`<title>`**: Postavlja naslov dokumenta koji se prikazuje u tabu.
- **`<link>`**: Povezuje dokument sa spoljašnjim resursima, kao što su CSS fajlovi.
- **`<body>`**: Glavni sadržaj dokumenta koji je vidljiv korisnicima.

## 2. Tekstualni Sadržaj

- **`<h1>` to `<h6>`**: Hijerarhijski naslovi (od najvažnijeg do najmanje važnog).
- **`<p>`**: Paragraf teksta.
- **`<ul>`, `<ol>`, `<li>`**: Neuređene i uređene liste i njihove stavke.
- **`<strong>`, `<em>`**: Podebljani i italicizovani tekst.
- **`<blockquote>`**: Blok citata.

## 3. Linkovi i Mediji

- **`<a>`**: Hiperveza ka drugoj stranici.
- **`<img>`**: Umetanje slike.
- **`<audio>`**: Umetanje audio sadržaja.
- **`<video>`**: Umetanje video sadržaja.

## 4. Tabele

- **`<table>`**: Definiše tabelu.
- **`<tr>`**: Definiše red u tabeli.
- **`<th>`**: Ćelija zaglavlja tabele.
- **`<td>`**: Standardna ćelija u tabeli.
- **`<thead>`, `<tbody>`, `<tfoot>`**: Delovi tabele za zaglavlje, telo i podnožje.

## 5. Forme

- **`<form>`**: Kontejner za elemente forme.
- **`<input>`**: Element za unos korisničkih podataka.
- **`<textarea>`**: Višelinijsko polje za unos teksta.
- **`<button>`**: Dugme za slanje forme.
- **`<select>`, `<option>`**: Padajuća lista i opcije za izbor.
- **`<label>`**: Opisuje kontrolu forme.

## 6. Semantički HTML

- **`<header>`, `<nav>`, `<section>`, `<article>`, `<aside>`, `<footer>`**: Elementi za semantičko strukturiranje stranice.
- **`<time>`, `<address>`, `<cite>`, `<q>`, `<abbr>`, `<code>`, `<pre>`, `<em>`, `<strong>`**: Oznake za specifično označavanje delova teksta.

## 7. HTML5 Funkcionalnosti

- **`<datalist>`, `<output>`**: Novi elementi forme.
- **`<progress>`, `<meter>`**: Elementi za prikazivanje napretka.
- **`<canvas>`, `<svg>`**: Elementi za crtanje grafike.

## 8. Globalni Atributi

- **`id`, `class`, `style`, `title`**: Opšti atributi primenjivi na većinu HTML elemenata.
- **`onclick`, `onchange`**: Atributi događaja za JavaScript interakciju.

## 9. Pristupačnost

- **ARIA atributi**: Poboljšavaju pristupačnost dinamičkog sadržaja.
- **Semantički HTML**: Poboljšava čitljivost i interpretaciju stranica od strane čitača ekrana.

## 10. Najbolje Prakse

- **Koristite semantičke oznake**: Poboljšava SEO i pristupačnost.
- **Održavajte čistu strukturu**: Lakše održavanje i razumevanje koda.
- **Komentari u kodu**: Olakšava saradnju i održavanje projekta.


## `<head>` Sekcija

### `<meta>`

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Opis stranice">
<meta name="keywords" content="ključne, reči, za, SEO">
<meta name="author" content="Ime autora">
<meta http-equiv="X-UA-Compatible" content="ie=edge">
```

- **`charset`**: Postavlja karakternu enkodiranost dokumenta na UTF-8.
- **`viewport`**: Kontroliše prikaz na mobilnim uređajima.
- **`description`**: Opisuje sadržaj stranice za pretraživače.
- **`keywords`**: Ključne reči za SEO optimizaciju.
- **`author`**: Ime autora stranice.
- **`X-UA-Compatible`**: Specifičan za IE, određuje verziju kompatibilnosti.

### `<title>`

```html
<title>Naslov Stranice</title>
```

- Definiše naslov koji se prikazuje na tabu pretraživača.

### `<link>`

```html
<link rel="stylesheet" href="styles.css">
<link rel="icon" href="favicon.ico" type="image/x-icon">
<link rel="canonical" href="https://www.example.com/canonical-url">
```

- **`rel="stylesheet"`**: Uvezuje dokument sa CSS fajlom.
- **`rel="icon"`**: Postavlja ikonu taba.
- **`rel="canonical"`**: Definiše kanonički URL stranice.

### `<script>`

```html
<script src="script.js"></script>
<noscript>Your browser does not support JavaScript!</noscript>
```

- **`src`**: Uvozi JavaScript fajl.
- `<noscript>`: Tekst koji se prikazuje kada je JavaScript isključen.

## Forme

### `<form>`

```html
<form action="/submit-form" method="POST" autocomplete="on">
    <label for="username">Username:</label>
    <input type="text" id="username" name="username" required minlength="4" maxlength="20">
    <label for="password">Password:</label>
    <input type="password" id="password" name="password" required>
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    <label for="message">Message:</label>
    <textarea id="message" name="message" rows="4" cols="50" maxlength="500"></textarea>
    <label for="gender">Gender:</label>
    <select id="gender" name="gender" required>
        <option value="male">Male</option>
        <option value="female">Female</option>
    </select>
    <input type="checkbox" id="terms" name="terms" required>
    <label for="terms">I agree to the terms and conditions</label>
    <input type="submit" value="Submit">
    <input type="reset" value="Reset">
</form>
```

- **`action`**: URL za slanje forme.
- **`method`**: HTTP metoda (GET ili POST).
- **`autocomplete`**: Omogućava pretragu za automatsko popunjavanje.
- **`required`**: Zahteva unos polja pre slanja forme.
- **`minlength`, `maxlength`**: Minimalna i maksimalna dužina teksta.
  
### `<input>`

- **`type="text"`**: Jednolinijski unos teksta.
- **`type="password"`**: Polje za unos lozinke.
- **`type="email"`**: Polje za unos email adrese.
- **`type="checkbox"`**: Checkbox za izbor opcija.
- **`type="radio"`**: Radio dugmad za izbor opcija.

### `<textarea>`

- Višelinijsko polje za unos teksta.
- **`rows`**: Broj redova (visina).
- **`cols`**: Broj kolona (širina).

### `<select>` i `<option>`

- **`<select>`**: Padajuća lista za izbor jedne opcije.
- **`<option>`**: Opcije unutar `<select>` elementa.

### `<label>`

- Povezuje kontrolu forme sa opisom.



## Tabele

Tabele su u prošlosti često korišćene za organizaciju podataka i raspored elemenata na web stranicama. Evo detaljnog objašnjenja o tome kako su se koristile:

### Struktura Tabele

```html
<table border="1">
    <caption>Tabela primer</caption>
    <thead>
        <tr>
            <th>Redni broj</th>
            <th>Ime</th>
            <th>Prezime</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1</td>
            <td>Marko</td>
            <td>Marković</td>
        </tr>
        <tr>
            <td>2</td>
            <td>Jovana</td>
            <td>Jovanović</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="3">Ukupno: 2 osobe</td>
        </tr>
    </tfoot>
</table>
```

### Detalji o Tabelama

- **`<table>`**: Definiše tabelu.
- **`<caption>`**: Dodaje naslov tabele.
- **`<thead>`**: Definiše zaglavlje tabele.
- **`<tbody>`**: Definiše telo tabele.
- **`<tfoot>`**: Definiše podnožje tabele.

### Upotreba Tabela

- **Organizacija podataka**: Tabele su koristile za prikazivanje struktuiranih podataka, kao što su raspored ispita, rezultati anketa, itd.
- **Raspored elemenata**: Pre HTML5 i CSS3, tabele su često bile korišćene za kompleksniji raspored elemenata na stranici.

## Putanje (Paths) i Mape u Slikama

### Putanje (Paths)

Putanje se koriste u HTML-u za crtanje složenih oblika kao što su krugovi, pravougaonici, linije itd. Kombinovanjem različitih putanja možete stvoriti kompleksne grafike:

```html
<svg height="150" width="400">
  <path d="M 10 80 Q 95 10 180 80 T 350 80" stroke="black" fill="transparent" />
</svg>
```

- **`<svg>`**: Element za crtanje vektorskih grafika.
- **`<path>`**: Definiše putanju (path).
- **`d` atribut**: Definiše oblik putanje.

### Mape u Slikama

Mape u slikama se koriste za definisanje interaktivnih područja na slici, koja se mogu kliknuti radi navigacije ili drugih akcija:

```html
<img src="planeta.jpg" alt="Planeta" usemap="#planetmap">
<map name="planetmap">
  <area shape="circle" coords="90,58,3" href="informacije.html" alt="Informacije">
  <area shape="rect" coords="110,60,150,80" href="galerija.html" alt="Galerija">
</map>
```

- **`<img>`**: Umetanje slike.
- **`usemap`**: Povezuje mapu sa slikom.
- **`<map>`**: Definiše mapu sa interaktivnim područjima.
- **`<area>`**: Definiše oblast interaktivne mape.

## `<canvas>`

`<canvas>` element omogućava dinamičko crtanje grafike, animacije i interaktivne sadržaje koristeći JavaScript API:

```html
<canvas id="myCanvas" width="200" height="100" style="border:1px solid #000000;"></canvas>
<script>
  var canvas = document.getElementById('myCanvas');
  var ctx = canvas.getContext('2d');
  ctx.fillStyle = 'rgb(200, 0, 0)';
  ctx.fillRect(10, 10, 50, 50);
</script>
```

- **`<canvas>`**: Definiše platno za crtanje.
- **`getContext('2d')`**: Prikazuje dvodimenzionalni kontekst za crtanje.
- **Metode konteksta**: `fillRect`, `strokeRect`, `drawImage`, itd., se koriste za crtanje oblika, linija i slika.

### Primena `<canvas>`

- **Grafike**: Crtanje grafika i animacija.
- **Dinamičke vizualizacije**: Koristi se za dinamičko prikazivanje podataka, kao što su grafikoni i dijagrami.



## Atributi HTML-a koji su služili za stilizovanje pre CSS-a

### 1. `align`

```html
<p align="center">Ovaj tekst je centriran.</p>
```

- **Opis**: Centrira sadržaj u odnosu na roditeljski element.
- **Primena**: Korišćen za centriranje teksta i slika.

### 2. `bgcolor`

```html
<table bgcolor="lightblue">
    <tr>
        <td>Prva ćelija</td>
        <td>Druga ćelija</td>
    </tr>
</table>
```

- **Opis**: Postavlja boju pozadine elementa.
- **Primena**: Korišćen za bojenje pozadine tabele, ćelija ili celog dokumenta.

### 3. `color`

```html
<p color="blue">Ovaj tekst je plave boje.</p>
```

- **Opis**: Postavlja boju teksta.
- **Primena**: Korišćen za definisanje boje teksta unutar elemenata.

### 4. `border`

```html
<table border="1">
    <tr>
        <td>Prva ćelija</td>
        <td>Druga ćelija</td>
    </tr>
</table>
```

- **Opis**: Definiše debljinu i stil granice oko elemenata.
- **Primena**: Korišćen za dodavanje granica oko tabela i drugih elemenata.

### 5. `width`, `height`

```html
<img src="slika.jpg" width="200" height="150">
```

- **Opis**: Postavlja širinu i visinu elementa.
- **Primena**: Korišćen za kontrolu dimenzija slika i drugih elemenata.

### 6. `valign`

```html
<table>
    <tr>
        <td valign="top">Tekst na vrhu</td>
        <td valign="bottom">Tekst na dnu</td>
    </tr>
</table>
```

- **Opis**: Postavlja vertikalno poravnanje sadržaja.
- **Primena**: Korišćen za kontrolu vertikalnog poravnanja teksta u tabelama.

### 7. `nowrap`

```html
<td nowrap>Ne lomi red teksta</td>
```

- **Opis**: Onemogućava prelamanje teksta na više redova.
- **Primena**: Korišćen za sprečavanje automatskog loma teksta u tabelama i drugim elementima.

### 8. `style`

```html
<p style="color: red; font-size: 18px;">Ovaj tekst je crvene boje i veličine fonta 18px.</p>
```

- **Opis**: Inline stilizacija elemenata.
- **Primena**: Omogućava definisanje CSS stilova direktno unutar HTML elemenata.

### 9. `bgcolor`, `text`, `link`, `alink`, `vlink` na `<body>`

```html
<body bgcolor="lightgray" text="black" link="blue" alink="red" vlink="green">
```

- **Opis**: Postavljanje boja pozadine, teksta, linkova u stanju normalnog, aktiviranog i posetjenog stanja na nivou stranice.
- **Primena**: Korišćen za postavljanje globalnih boja na nivou cele stranice.

### 10. `nowrap` na `<td>`, `<th>`

```html
<td nowrap>Ne lomi red teksta</td>
```

- **Opis**: Onemogućava prelamanje teksta na više redova.
- **Primena**: Korišćen za sprečavanje automatskog loma teksta u tabelama i drugim elementima.
