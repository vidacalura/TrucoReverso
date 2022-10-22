<script>
    export let tipo = null;
    export let naipe = null;

    function jogarCarta(){
        if (naipe){
            
        }
    }

</script>


<div class="{ (naipe == null ? "carta-virada" : "carta") } { naipe }" on:click={ () => jogarCarta() } on:keydown={ () => jogarCarta() }>
    { #if tipo }
        <div>
            <p> { tipo } </p>
        </div>

        <div class="w-full h-[60%] pt-[25%] flex align-middle justify-center">
            <img src={ naipe + ".png" } alt={ naipe }>
        </div>

        <div class="flex justify-end">
            <p> { tipo } </p>
        </div>
    { /if }
</div>