<script>

import Carta from "$lib/carta.svelte";

class CartaModelo {

    constructor (tipo, naipe){
        this.valor = this.getCartaValor(tipo),
        this.tipo = tipo,
        this.naipe = naipe
    }

    getCartaValor(v){

        let valor = 0;

        switch(v){
            case "3":
                valor++;
            case "2":
                valor++;
            case "A":
                valor++;
            case "K":
                valor++;
            case "J":
                valor++;
            case "Q":
                valor++;
            case "7":
                valor++;
            case "6":
                valor++;
            case "5":
                valor++;
            case "4":
                valor++;
                break;
            default:

        }

        return valor;

    }

}

</script>

<!-- App -->
<nav>
    <!-- Logo -->
    <h1> Truco Reverso </h1>

    <!-- Ajuda -->
    <i> ? </i>
</nav>

<main>

    <div id="sua-mao">
        <Carta />
        <Carta />
        <Carta />
    </div>

    <div id="mesa">
        <div id="baralho">
            <div> </div>

            <!-- Vira -->
            <Carta />
        </div>
    </div>

    <div id="adversario-mao">
        <Carta />
        <Carta />
        <Carta />
    </div>

</main>


<!-- CSS -->
<style>

    * {
        margin: 0;
        padding: 0;
        font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    }

</style>