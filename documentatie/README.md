# Performance Optimaliseren bootstrap documentatie
### Critical CSS
De performance verbetering is 6857 milliseconden (6.9 seconden). De 'above the fold content' laadt 9.75x sneller door deze optimalisatie.

#### Ondernomen stappen voor de critical CSS optimalisatie
- Asynchroon inladen van CSS files (Google critical)
- Niet wachten op fonts bij inladen, swappen als ze geladen zijn
- 'Above the fold' styling als inline css zodat dit als eerste laadt. (Google critical)

##### VOOR OPTIMALISATIE
###### Score 50/49
![voor critical css optimalisatie](http://www.kager.io/uploads/minor/performance-matters/critcal-before-ps-mobile.png)
![voor critical css optimalisatie](http://www.kager.io/uploads/minor/performance-matters/critcal-before-ps-desktop.png)

###### 7.56 seconden voordat above-the-fold styling weergeven wordt
![Na critical css optimalisatie](http://www.kager.io/uploads/minor/performance-matters/critical-before.png)

##### NA OPTIMALISATIE
###### Score 96/51
![NA critical css optimalisatie](http://www.kager.io/uploads/minor/performance-matters/critical-after-ps-mobile.png)
![NA critical css optimalisatie](http://www.kager.io/uploads/minor/performance-matters/critcal-after-ps-desktop.png)

###### 703 milliseconden voordat above-the-fold styling weergeven wordt
![Na critical css optimalisatie](http://www.kager.io/uploads/minor/performance-matters/critical-after.png)

