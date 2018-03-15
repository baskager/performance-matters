# Performance Optimaliseren bootstrap documentatie

## Performance voorgaand alle optimalisaties
8.07 seconden voor het eerste frame is getoond
![Voorgaand alle optimalisaties](http://www.kager.io/uploads/minor/performance-matters/pm-all-before.png)

### Critical CSS

#### Ondernomen stappen voor de critical CSS optimalisatie
- 'Above the fold' styling als inline css zodat dit als eerste laadt.

#### Performance verbeteringen
Performance is door het inline stylen alleen niet verbeterd. Dit komt waarschijnlijk omdat de resources nog niet async ingeladen worden
