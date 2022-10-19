<script>
    import {count} from "./stores.js";
    function decrement() {
        //TODO
        count.update(c=>c-1)
    }

</script>

<button on:click={decrement}> - </button>
