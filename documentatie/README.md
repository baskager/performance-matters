# Performance Optimaliseren bootstrap documentatie

## Performance voorgaand alle optimalisaties
8.07 seconden voor het eerste frame is getoond
11.10 seconden voor het laden van de 'above-the-fold' content
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
De performance is aanzienlijk verbeterd. De above-the-fold content is in 627ms geladen.
![Voorgaand alle optimalisaties](http://www.kager.io/uploads/minor/performance-matters/pm-async.png)
![Pagespeed mobile](http://www.kager.io/uploads/minor/performance-matters/pm-ps-async-mobile.png)
![Pagespeed desktop](http://www.kager.io/uploads/minor/performance-matters/pm-ps-async-desktop.png)
