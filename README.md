Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
// Creo i componenti per le macrosezioni della pagina e li importo in App.vue; faccio la struttura generale dei macroelementi.

Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
// In data() aggiungo gli array a oggetti con i vari elementi dei menu da visualizzare in pagina tramite v-for.

Per oggi diamo priorità alla struttura: quando è tutto bello solido, passiamo al Sass!
// Stilizzo i vari componenti per riprodurre il layout.

Bonus:
Creare un componente aggiuntivo per gestire la fascia azzurra con le icone.

Create un nuovo componente che rappresenterà le card dei fumetti.
Utilizzate i dati presenti nel file json che trovate in allegato e passateli al componente Card tramite props.
Una volta inseriti tutti i contenuti dinamicamente, completate il vostro layout e rifinite i dettagli con Sass.
// Creo dei componenti separati per il jumbotron, la sezione main-content con il card-wrapper e la singola card. Nella sezione main-content preparo il card-wrapper che verrà popolato con le cards.