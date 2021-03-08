<template>
  <div class="cover">
    <p>Buongiorno,</p>
    <p>Sono <span>{{ firstName }}</span>, junior Full Stack Web developer che è rimasto particolarmente colpito dalle attività che effettua la vostra azienda. Ho molto apprezzato l'apertura all'innovazione nel portare nei vostri progetti tecnologie sempre più innovative, in particolare la scelta dell’utilizzo di <span>{{ jsPreferFw }}</span> come framework JavaScript.
    </p>

    <p>Da sempre appassionato di programmazione, ho deciso di trasformare questa passione in lavoro.
        Ho fatto formazione nello sviluppo web inizialmente da autodidatta, successivamente frequentando il corso da Full Stack Web Developer di Boolean.careers (corso full time della durata di sei mesi) grazie al quale ho consolidato ed esteso grandemente le mie conoscenze e capacità (<a href="https://www.boolean.careers">www.boolean.careers</a>).</p>

    <p>Curioso di natura. Mi piace provare, sbagliare e affrontare difficoltà, è una forte spinta ad esplorare ciò che mi è ignoto per apprenderne sempre il più possibile.</p>

    <p>Certo che una nostra collaborazione possa essere un'ottima opportunità vi invio il mio curriculum vitae da sottoporre alla vostra attenzione. </p>
    <p>Resto in attesa di un vostro cortese riscontro. <br>
      Cordialmente, <br>
      <span>{{ firstName }} {{ lastName }}</span>
    </p>
  </div>
</template>

<script>
export default {
  name: 'cover',
  props: ['firstName', 'lastName', 'jsPreferFw']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.cover {
  margin: auto;
  p {
    font-size: 1.3rem;
    line-height: 1.5em;
    margin-bottom: 1rem;
  }
  a {
    text-decoration: none;
    color: #fff;
    &:hover {
      text-decoration: underline;
    }
  }
  span {
    color: #000;
    font-size: 1.1em;
    &:hover {
      color: #fff;
    }
  }
}
</style>
