<script>
    export let carta = {
        tipo: null,
        naipe: null
    }
</script>


<div class="carta">
    <div>
        <p> { carta.tipo } </p>
    </div>

    <img src={ /* carta.naipe + */ "favicon.png" } alt={ carta.naipe }>

    <div>
        <p> { carta.tipo } </p>
    </div>
</div>


<style>
    
</style>