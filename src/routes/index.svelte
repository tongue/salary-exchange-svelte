<script>
  import InfoCard from "../components/InfoCard.svelte";


  
   // JOHAN: Jag har ju jobbat mycket med optimering av Sapper projekt. Och kan säga
   // att det generellt sett inte är bra att ha så mycket text i sina componenter/routes
   // så om du vill få betydligt minder bundle size och snabbare sida så är det värt det
   // att flytta ut allt innehåll i någon form av JSON struktur som du sen laddar så som
   // de gjort här: https://github.com/sveltejs/sapper-template/blob/master/src/routes/blog/%5Bslug%5D.json.js
  
   // En annan grej som jag gör, som gör det lite lättare att skriva kod (tycker jag) är att jag lägger
   // <style /> taggarna efter min html. Det gör det lättare att hoppa mellan script och html. Och html och css.
   // Inte lika mycket skit ivägen :) 
</script>

<style>
  div {
    margin-bottom: 100px;
  }
  h1 {
    text-align: center;
    font-size: 2.8em;
    text-transform: uppercase;
    font-weight: 700;
    margin: 1em 0em 1em 0;
  }

  h2 {
    text-align: center;
  }

</style>

<svelte:head>
  <title>Home</title>
</svelte:head>

<h1>Välkommen</h1>

<div>
  <h2>Vad är löneväxling?</h2>
  <p>
    Löneväxling är en överenskommelse mellan en arbetstagare och en arbetsgivare
    om att avstå en del av sin bruttolön (innan inkomstskatten dras) och
    istället låta arbetsgivaren betala in den summan till den anställdes
    pension. Inkomstskatten dras först när du påbörjar utbetalningen av din
    pension.
  </p>

  <InfoCard
    listItems={['En snöbollseffekt som gör att ditt sparande växer exponentiellt', 'Du får ränta på avkastningen ditt kapital genererat tidigare år', 'Ju högre ränta på ditt sparande desto snabbare kan dina pengar växa']} />
</div>

<div>
  <h2>Få mera i pension.</h2>
  <p>
    Eftersom skatten på pensionssparande idag är ca 6 % lägre än
    arbetsgivaravgiften på lön så brukar arbetsgivaren istället då betala dessa
    6 % extra i den anställdes pensionsfond. Då de varken ska kosta eller vara
    sparsamt för arbetsgivaren att låta den anställde pensionsspara.
  </p>

  <InfoCard
    listItems={['Behöver inte betala skatt på pengarna förrän de betalas ut i pension. Vilket innebär att du får högre ränta på hela beloppet under lång tid samtidigt som inkomstskatten på pengarna antagligen blir lägre när de betalas ut då de flesta får mindre i pension än i lön.', 'Den lön du tjänar över 43 309kr är inte pensionsgrundande i det statliga pensionssystemet, och dessutom betalar du högre skatt på den inkomsten vilket då gör de perfekt att spara den överskjutande delen.']}
    title="Fördelar med löneväxling" />
</div>

<div>

  <h2>Löneväxling passar inte alla.</h2>
  <p>
    Din allmänna pension, sjukpenning, föräldrapenning och a-kasseersättning
    beräknas utifrån den ersättningsgrundande inkomst du har för var och en av
    dessa ersättningar. När din bruttolön sänks påverkas de, dock inte om din
    månadslön eller årslön efter löneväxling ligger över inkomsttaket för de
    olika ersättningsgrundande inkomsterna. Som för den allmänna pensionen 2019
    är 8,07 * inkomstbasbeloppet 2019 (64 400) som är 519 708kr i årsinkomst
    eller 43 309kr i månaden.
  </p>
  <InfoCard
    listItems={['Den lön som du växlar bort sänker din sjuk- och pensionsgrundande inkomst. Det betyder att vissa ersättningar blir lägre både på sikt och i nutid. ', 'Inom kollektivavtalad tjänstepension låser man pengarna till åtminstone 55 års ålder.', 'Din ITP sjukpension som du får vid långvarig sjukdom blir lägre. Om du efter löneväxlingen tjänar under inkomsttaket för respektive förmån, blir sjukpenning, föräldrapenning och tillfällig föräldrapenning lägre. Under vissa förutsättningar kan även den allmänna pensionen bli lägre.']}
    title="Nackdelar med löneväxling" />
</div>
