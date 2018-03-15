# Performance Optimaliseren bootstrap documentatie

## Performance voorgaand alle optimalisaties
- 8.07 seconden voor het eerste frame is getoond.
- 11.10 seconden voor het laden van de 'above-the-fold' content.
- 30 seconden voor het laden van de gehele pagina
![Voorgaand alle optimalisaties](http://www.kager.io/uploads/minor/performance-matters/pm-all-before.png)
![Pagespeed mobile](http://www.kager.io/uploads/minor/performance-matters/pm-ps-mobile.png)
![Pagespeed desktop](http://www.kager.io/uploads/minor/performance-matters/pm-ps-desktop.png)

### Critical CSS

#### Ondernomen stappen voor de critical CSS optimalisatie
- 'Above the fold' styling als inline css zodat dit als eerste laadt.

#### Performance verbeteringen
Performance is door het inline stylen alleen niet verbeterd. Dit komt waarschijnlijk omdat de resources (zoals de fonts) nog niet async ingeladen worden


### Async laden van resources

#### Ondernomen stappen voor de async optimalisatie
- 'rel=preload' toegevoegd aan de <link> tags
- JS voor asynchroon laden van de css files

#### Performance verbeteringen
De performance is aanzienlijk verbeterd. De above-the-fold content is in 3.73 seconden geladen.
![Voorgaand alle optimalisaties](http://www.kager.io/uploads/minor/performance-matters/pm-async2.png)

![Pagespeed mobile](http://www.kager.io/uploads/minor/performance-matters/pm-ps-async-mobile2.png)
![Pagespeed desktop](http://www.kager.io/uploads/minor/performance-matters/pm-ps-async-desktop2.png)

### Font loading

#### Ondernomen stappen voor de font loading optimalisatie
- Fonts niet meer inladen in inline style
- 'font-display: swap' stijl op de fonts

#### Performance verbeteringen
De performance is weer aanzienlijk verbeterd. De above-the-fold content is in 738 milliseconden geladen.
![Voorgaand alle optimalisaties](http://www.kager.io/uploads/minor/performance-matters/pm-fonts.png)

![Pagespeed mobile](http://www.kager.io/uploads/minor/performance-matters/pm-ps-fonts-mobile2.png)
![Pagespeed desktop](http://www.kager.io/uploads/minor/performance-matters/pm-ps-fonts-desktop3.png)

### Image optimalisaties

#### Ondernomen stappen voor de image optimalisaties
- Compressie
- Verkleinen van bepaalde afbeeldingen

#### Performance verbeteringen
De gehele pagina is nu in 17 seconden geladen. Dit was eerder 30 seconden.
![Voorgaand alle optimalisaties](http://www.kager.io/uploads/minor/performance-matters/pm-images.png)

![Pagespeed mobile](http://www.kager.io/uploads/minor/performance-matters/pm-ps-images-mobile.png)
![Pagespeed desktop](http://www.kager.io/uploads/minor/performance-matters/pm-ps-images-desktop.png)

### Minify JavaScript en CSS

#### Ondernomen stappen voor de image optimalisaties
- Minify JavaScript
- Minify CSS

#### Performance verbeteringen
De gehele pagina is nu onder 16 seconden geladen.
![Voorgaand alle optimalisaties](http://www.kager.io/uploads/minor/performance-matters/pm-minify.png)

![Pagespeed mobile](http://www.kager.io/uploads/minor/performance-matters/pm-ps-minify-mobile2.png)
![Pagespeed desktop](http://www.kager.io/uploads/minor/performance-matters/pm-ps-minify-desktop.png)


## Samenvatting

### Gehele laadtijd
**Oude situatie:** 30 seconden.

**Nieuwe situatie:** 16 seconden.

**Verbetering in seconden:** 14 seconden.

**Factor:** 2x sneller (afgerond)

### 'Above the fold'
**Oude situatie:** 11.10 seconden

**Nieuwe situatie:** 638 milliseconden

**Verbetering in seconden:** 10.46 seconden

**Factor:** 17x sneller (afgerond)

### Google pagespeed score

**Oude score mobiel:** 54

**Oude score desktop:** 49

**Nieuwe score mobiel:** 97

**Nieuwe score desktop:** 78

**Factor mobiel:** 1.8x beter (afgerond)

**Factor desktop:** 1.6x beter (afgerond)
