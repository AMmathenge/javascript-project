<script>
    let name =['']
    let enjoyscoding = true;

    let programmingLanguage =["html","css","javascript"];
    let selected = [''];

</script>
<main>
    <p>Your name is {name}. You {enjoyscoding ? 'enjoy' : "don't enjoy" }coding.</p>
    <hr />
    <input type="text" bind:value={name}/>
    <br />
    <label>
        Do you enjoy coding?<input type="checkbox" bind:checked={enjoyscoding}>
    </label>
    <hr />
    <p>You have selected: {selected.length ? selected.join(', ') : 'nothing'}</p>

    {#each programmingLanguage as language }
        <label >
            <input type="checkbox" bind:group={selected} value={language}/>
        </label>
        <button>{programmingLanguage}</button>
    {/each}
</main>
<style>

</style>