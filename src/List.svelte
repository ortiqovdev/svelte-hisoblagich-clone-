<script lang="ts">
    import { each } from "svelte/internal";


    let value:string = ''
    let array:string[]=[]
    function onAdd(){
        array.push(value)
        array=array
        value= ''
    }
</script>
<div>
    <input type="text" placeholder="text" bind:value={value}>
    <button on:click={onAdd}>Add list</button>
</div>
<ol>
    {#each array as item}
    <li>{item}</li>
    {/each}
</ol>