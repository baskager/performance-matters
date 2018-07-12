# Performance matters: kager.io

[Klik hier voor een demo](https://test.kager.io)
![Kager.io](http://www.kager.io/uploads/minor/performance-matters/audit/kager/kager-io-screenshot.png)
![Chrome audit](http://www.kager.io/uploads/minor/performance-matters/audit/kager/chrome-audit.png)

## Service worker

Een service worker is in dit project geimplementeerd en krijgt van de google chrome audit een score van 100/100

In deze website cached de service worker alle images en pagina's. De gehele website is offline te gebruiken.

Op mobiele apparaten krijgt je een prompt om de website aan hun homescreen toe te voegen. In dit geval wordt de website een soort 'APP' en krijgt de gebruiker een launcher met een icoontje van mijn logo op zijn homescreen. Bij het openen van de app wordt een splashscreen getoond met mijn logo.

## Server side rendering

De eerste versie van deze app gebruikte wel NodeJS en Express maar er werd bijna niets op de server gerenderd. De komende dingen heb ik verbeterd:

- Projecten in de portfolio worden ingeladen bij het starten bij de server. De projecten staan dus altijd in het geheugen van de server waardoor ze niet elke keer opgehaald moeten worden middels een ajax request.
- Alle pagina's worden server-side gerenderd. In de oude situatie werd alleen de homepage gerenderd en werden andere pagina's dynamisch ingeladen middels ajax requests. Door deze architectuur was de website niet te gebruiken zonder javascript en moest men wachten tot de content opgehaald was middels een ajax request.
- Nginx proxied op de kager.io (Debian Linux) server naar de node webserver waardoor direct gebruik gemaakt wordt van GZIP compressie en een SSL certificaat.

## Gulp

In dit project heb ik gulp geimplementeerd om alle content te minifyen. De volgende media wordt verkleind door de task-runner:

- Afbeeldingen
- CSS
- Javascript

# Performance Audit (slome 3G verbinding)

## Performance voorgaand alle optimalisaties

- 4.35 seconden voor het eerste frame is getoond.
- 7.16 seconden voordat de website leesbaar is (fonts)
- 7.16 seconden voor het laden van de gehele pagina

  ![Voorgaand alle optimalisaties](http://www.kager.io/uploads/minor/performance-matters/audit/kager/homepage-before.png)

### Minifyen van javascript, css en afbeeldingen

### Ondernomen stappen

- Gulp geimplementeerd voor het automatisch minifyen van alle resources

#### Performance verbeteringen

De performance is verbeterd. Het eerste frame wordt nu getoont in 1.12 seconden en de totale laadtijd is verlaagd naar 7.06 seconden

7.06 seconden voordat de website leesbaar is (fonts)
![Minifyen van resources](http://www.kager.io/uploads/minor/performance-matters/audit/kager/homepage%20minify-compress.png)

### Async laden van resources

#### Ondernomen stappen voor de async optimalisatie

- <link> tags met 'rel=preload' voor css en Javascript

#### Performance verbeteringen

Het eerste frame wordt nu getoont in 4.24 seconden en de totale laadtijd is verlaagd naar 7.04 seconden.

Voor het verbeteren van de performance bij het eerste frame kan de 'above the fold' styling inline worden geplaatst.

7.04 seconden voordat de website leesbaar is (fonts)
![Async laden van resources](http://www.kager.io/uploads/minor/performance-matters/audit/kager/async-resources.png)

### Font loading

#### Ondernomen stappen voor de font loading optimalisatie

- Fonts niet meer inladen in inline style
- Local fonts ipv. Google fonts
- 'font-display: swap' stijl op de fonts

#### Performance verbeteringen

Het eerste frame wordt nu getoont in 4.21 seconden en de totale laadtijd is 7.24 seconden

4.21 seconden voordat de website leesbaar is (fonts)
![Voorgaand alle optimalisaties](http://www.kager.io/uploads/minor/performance-matters/audit/kager/font-optimisations.png)

## Samenvatting audit

- De eerste leesbare paint is verlaagd van 7.16 seconden naar 4.21 seconden.
- De gehele laadtijd is niet verbeterd
