# exempel med datainsamling från SCB (Statistiska Central Byrån)

Datat hämtas ifrån följande endpoint: https://api.scb.se/OV0104/v1/doris/en/ssd/BE/BE0101/BE0101A/BefolkningNy

Datat innehåller *"Population by region, marital status, age, sex, observations and year"*

I det här exemplet finns med de filer som genereras när scripten (js-filerna) nedan körs.
Det betyder att du ska kunna köra exemplet "out-of-the-box", bara att "tuta-å-köra".

---

![scb](https://github.com/mattische/exempel-datainsamling/blob/aa0626a5cf7353f9225248551e8034590f64af3d/images/scb_pop_growth.png)

---

Exemplet innehåller följande filer:

**scb-test.js**

ett snabbt litet test som genererar output i terminalen.

**scb-population.js**

hämtar data, från ovan endpoint, för tre regioner och årtalet 2022.
Datat sparas i `population_data_large_cities.json`.

Datat kan ses i diagramform om man öppnar 

**population-chart.html** 

i webbläsaren.

**population_growth_large_cities.js**

hämtar data, från ovan endpoint, och genererar en json-fil (`population_growth_large_cities.json`)
där datat är befolkningsökningen i Sveriges tre största städer 1973-2022.

Datat kan ses i ett linjediagram om man i webbläsare öppnar 

**population_growth.html**

# instruktioner - kör exemplen

axios krävs i node:

`$npm install axios`

internetuppkoppling krävs eftersom Chart.js hämtas via CDN.

generera json-filer så att diagramen kan visas, dvs kör js-filerna med node;

`$node scb-population.js`

`$node scb_population_growth_large_cities.js`

**Nu är json-filer genererade och html-filerna kan öppnas i webbläsare.**

