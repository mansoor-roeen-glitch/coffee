<script>
    export let handleClick;
</script>

<div on:click={handleClick} class="Header_HamMenu_Wrapper">
    <div class="Header_HamMenu">
        <svg width="40" height="40" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M3 18H21V16H3V18ZM3 13H21V11H3V13ZM3 6V8H21V6H3Z" fill="black"/>
        </svg>      
    </div>
</div>

<style>

    .Header_HamMenu_Wrapper, .Header_HamMenu {
        justify-content: center;
        align-items: center;
        height: fit-content;
        width: fit-content;
        display: flex;
        cursor: pointer;
    }

</style>