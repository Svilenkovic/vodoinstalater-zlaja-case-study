<a href="https://vodoinstalaterzlaja2015.rs/"><img src="media/cover.jpg" alt="Zlaja 2015, naslovna strana na laptopu i telefonu" width="100%"></a>

# Zlaja 2015

Sajt beogradskog vodoinstalatera i električara u kom sve vodi ka pozivu, uz PWA za radne naloge koja radi i bez mreže.

**[vodoinstalaterzlaja2015.rs](https://vodoinstalaterzlaja2015.rs/)** · [Studija slučaja](https://svilenkovic.rs/radovi/vodoinstalater-zlaja) · [Stranica aplikacije](https://svilenkovic.rs/aplikacija-vodoinstalater) · [English](README.md)

> [!NOTE]
> Klijentski projekat. Izvorni kod pripada klijentu i čuva se u privatnom repozitorijumu. Ova stranica opisuje šta sam uradio i kako.

<table>
  <tr><td><b>Klijent</b></td><td>Zlaja 2015</td></tr>
  <tr><td><b>Delatnost</b></td><td>Vodoinstalaterske i elektro usluge sa hitnim intervencijama 0-24</td></tr>
  <tr><td><b>Lokacija</b></td><td>Beograd</td></tr>
  <tr><td><b>Vrsta</b></td><td>Sajt sa više strana i PWA za radne naloge</td></tr>
  <tr><td><b>Moj deo posla</b></td><td>Dizajn, izrada, SEO, hosting i održavanje</td></tr>
  <tr><td><b>Tehnologije</b></td><td>PHP 8.3, nginx FastCGI cache, MariaDB, PWA, vanilla CSS/JS</td></tr>
</table>

## O projektu

Zlaja 2015 radi vodoinstalaterske i elektro poslove po celom Beogradu, danju i noću: mašinsko odgušenje, čišćenje WOMA sistemom pod visokim pritiskom, septičke jame, bojlere i kompletne elektro instalacije. Posetilac obično ima vodu na podu i traži broj koji radi odmah, pa svaka strana počinje brojem na koji se zove jednim dodirom. Svaka usluga i svaka opština ima i svoju stranu, jer ljudi tako pretražuju.

Sajt ima srpski i engleski bez druge kopije strana. Tekst se piše u paru na elementima sa data-translate, a pre slanja strane PHP-ov izlazni bafer ostavlja polovinu koja odgovara kolačiću sa jezikom. Zamka je bila u nginx FastCGI kešu, koji odgovara bez pokretanja PHP-a, pa bi prvi posetilac narednih deset minuta birao jezik za sve ostale. Kolačić sa jezikom je sada deo ključa keša.

## Šta sam uradio

- PWA za radne naloge koja radi i bez mreže, sa statusom neplaćen pored statusa završen, prioritetom do hitnog i slikama sa terena
- Klijenti kao fizička lica ili firme, troškovi po kategorijama vezani za nalog i izveštaji po mesecu, godini i majstoru; radnik vidi samo svoje nezavršene naloge
- Google Tag Manager se pokreće tek posle prvog skrola, dodira ili klika, ili posle četiri sekunde, i to je donelo najveći deo ubrzanja
- Podskup fonta sa slovima č, š, ž, ć i đ učitava se unapred na svakoj strani, pošto su ta slova pri prvoj poseti padala na sistemski font
- Lightbox bez praznog img src, zbog kog je pregledač celu stranu učitavao po drugi put
- Serverske ispravke: preusmerenje sa www koje čuva putanju, security.txt dostupan uprkos pravilu za skrivene fajlove i slušanje na IPv6

## Merenja

| | Performanse | Pristupačnost | Dobre prakse | SEO |
| :-- | :-: | :-: | :-: | :-: |
| Telefon | 99 | 100 | 100 | 100 |
| Desktop | 95 | 100 | 100 | 100 |

PageSpeed Insights, laboratorijsko merenje živog sajta, septembar 2026. Sigurnosna zaglavlja: 6 od 6. HTML validator: bez grešaka. axe provera pristupačnosti: bez prekršaja. Strukturisani podaci: `BreadcrumbList`, `FAQPage`, `LocalBusiness`, `Plumber`.

## Snimci ekrana

<table>
  <tr>
    <td width="68%" valign="top"><img src="media/desktop.webp" alt="Zlaja 2015, naslovna strana na ekranu širine 1440 px"></td>
    <td width="32%" valign="top"><img src="media/mobile.webp" alt="Zlaja 2015, naslovna strana na telefonu"></td>
  </tr>
</table>

<img src="media/inner-1.webp" alt="Usluge u Beogradu: odgušenje, hitne intervencije, sanitarije i elektro instalacije">
<sub>Usluge u Beogradu: odgušenje, hitne intervencije, sanitarije i elektro instalacije</sub>

<img src="media/inner-2.webp" alt="Elektro popravke i detekcija kvarova, pa razlozi za izbor majstora">
<sub>Elektro popravke i detekcija kvarova, pa razlozi za izbor majstora</sub>

---

<sub>Izrada: [D. Svilenković](https://svilenkovic.rs).</sub>
