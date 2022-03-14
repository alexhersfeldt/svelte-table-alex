<script>
export let objectArray = [];
export let headerArray = [];
function isImage(url) {
    return /\.(jpg|jpeg|png|webp|avif|gif|svg)$/.test(url);
}
</script>

{#each objectArray as object}
    <tr>
        {#each headerArray as header}
            {#if (isImage(object[header]))}
                <td><img alt={"avatar"} src={object[header]}/></td>
            {:else}
                <td>{object[header]}</td>
            {/if}
        {/each}
    </tr>
{/each}
