<script>

    import Carta from "$lib/carta.svelte";
    import Convite from "../lib/convite.svelte";

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

    const cartas = [new CartaModelo("3", "ouros"), new CartaModelo("3", "ouros"), new CartaModelo("3", "ouros")]

</script>

<!-- App -->
<nav class="h-20 w-[100vw - 1rem] flex justify-between p-4">
    <!-- Logo -->
    <h1 class="font-bold"> Truco Reverso </h1>

    <!-- Ajuda -->
    <div>
        <button
        on:click={() => ajuda() }
        title="Ajuda" class="px-4 py-2 text-white font-bold bg-blue-400 rounded-full shadow-lg transition-all ease-in-out hover:bg-blue-300"> 
        ? 
        </button>
    </div>
        
</nav>

<main>

    <div id="sua-mao" class="flex justify-center gap-2">
        { #each Array(3) as _ }
            <Carta />
        { /each }
    </div>

    <div id="mesa">
        <div id="baralho" class="flex justify-between md:px-12 py-8">
            <div class="absolute mt-6 z-10">
                <Carta />
            </div>

            <!-- Vira -->
            <div class="px-12 rotate-[30deg]">
                <Carta tipo={ 3 } naipe={ "espadas" }/>
            </div>

            <div id="placar">
                <div class="placar-player">
                    { 1 }
                </div>

                <div class="placar-player">
                    { 0 }
                </div>
            </div>
        </div>
    </div>

    <div id="adversario-mao" class="flex justify-center gap-2">
        { #each cartas as carta }
            <Carta { ...carta } />
        { /each }
    </div>

</main>