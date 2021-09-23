<script>
import App from "../App.svelte"
import HamMenu from "./sub-components/HamMenu.svelte"

    $: width = window.innerWidth;
    $: height = window.innerHeight;

    $: navActive = "initial"
    let links = [
        {text: "Home",link: "/#Home",active: false},
        {text: "About",link: "/#About", active: false},
        {text: "History",link: "/#History", active: false},
        {text: "Our Menu",link: "/#OurMenu", active: false},
        {text: "Contact",link: "/#Contact", active: false} 
    ]

    let handleClick = () => {
        if (navActive === "initial") {
            navActive = true
        } else {
            navActive = !navActive
        }
    }

    let handleResize = () => {
        width = window.innerWidth;
        height = window.innerHeight
    }

    window.addEventListener("resize", handleResize)

</script>

<header class="Header_Wrapper">
    {#if width < 1000}
        <div class={`Header_MobNav_Wrapper${navActive === "initial" ? " MobNav_Wrapper_Initial" : navActive ? " MobNav_Wrapper_Active" : " MobNav_Wrapper_Hidden"}`}>
            <div class="Header_MobNav">
                <div class="Header_MobNav_List">
                    {#each links as link} 
                        <li class={`Header_MobNav_Item${link.active ? " MobNavItemActive" : ""}${navActive === "initial" ? " MobNav_Item_Initial" : navActive ? " MobNav_Item_Active" : " MobNav_Item_Hidden"}`} id={`MobNav_Item-${link.text}`}>
                            <a href={link.link} class="Header_MobNav_Item_TextWrapper">
                                <span class="Header_MobNav_Item_Text">{link.text}</span>
                            </a>
                        </li>
                    {/each}
                </div>
            </div>
        </div>
    {/if}
    <div class="Header_Inner">
        <div class="Header_Col1_Wrapper">
            <a href="/" class="Header_Col1 Header_LogoWrapper">
                <span class="Header_Logo">
                    Coffee 
                </span>
            </a>
        </div>
        <div class="Header_Col2_Wrapper">
            {#if width < 1000}
                <HamMenu handleClick={handleClick} />
            {:else}
                <div class="Header_col2 Header_Nav">
                    <div class="Header_Nav_List">
                        {#each links as link} 
                            <li class={`Header_Nav_Item${link.active ? " NavItemActive" : ""}`} id={`item-${link.text}`}>
                                <a href={link.link} class="Header_Nav_Item_TextWrapper">
                                    <span class="Header_Nav_Item_Text">{link.text}</span>
                                </a>
                            </li>
                        {/each}         
                    </div>
                </div>
            {/if}
        </div>
    </div>
</header>


<style>
    
    .Header_Wrapper {
        position: absolute;
        top: 0px;
        width: 100vw;
        z-index: 2;
        display: flex;
        height: fit-content;
        align-items: center;
        justify-content: center;
    }

    .Header_Inner {
        display: flex;
        justify-content: space-between;
        align-items: center;
    
        position: relative;
        width: 92%;
        height: 45px;
        padding-top: 22px;
    }

    .Header_Col1_Wrapper, .Header_Col1 {
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
        width: fit-content;
        height: fit-content;
        text-decoration: none;
    }

    .Header_Logo {
        font-family: "Jost", sans-serif;
        font-style: normal;
        font-weight: 300;
        font-size: 1.7rem;
        color: var(--black);
    }

    .Header_Col2_Wrapper, .Header_Nav {
        width: fit-content;
        height: fit-content;
        display: flex;
        align-items: center;
        justify-content: center;
    }    

    .Header_Nav_List {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
        /* Gap will change depending on the screen width */
        column-gap: 25px; 
    }

    
    .Header_Nav_Item {
        width: fit-content;
        height: fit-content;
        display: flex;
        align-items: center;
        justify-content: center;
        list-style: none;
        position: relative;
    }    
    
    .Header_Nav_Item_TextWrapper {
        text-decoration: none;
        width: fit-content;
        height: fit-content;
        transition: .2s ease opacity;
    }
    
    .Header_Nav_Item:hover{
        opacity: .8;
    }
    
    .Header_Nav_Item_Text {
        font-family: "Jost", sans-serif;
        font-style: normal;
        font-weight: 300;
        font-size: 1.2rem;
        color: var(--black);
    }
    
    .Header_Nav_Item.NavItemActive::after {
        left: 0px;
        right: 0px;
        content: "";
        width: 100%;
        height: 1px;
        bottom: -1px;
        position: absolute;
        background: var(--black);
    }
    
    .Header_MobNav_Wrapper {
        position: absolute;
        top: 0px;
        width: 100%;
        height: 250px;
        background: linear-gradient(to right, var(--white) 0%, var(--white) 50%, var(--white-e) 50%, var(--white-e) 100%);
        padding-top: calc(25px + 67px);
        display: flex;
        justify-content: center;
    }
    
    .Header_MobNav_Wrapper.MobNav_Wrapper_Active {
        animation: .4s ease navActive forwards;
    }
    
    .Header_MobNav_Wrapper.MobNav_Wrapper_Hidden {
        animation: .4s ease navClosed forwards;
    }
    
    .Header_MobNav_Wrapper.MobNav_Wrapper_Initial {
        height: 0px;
        transform: translateY(-340px);
    }
    
    .Header_MobNav {
        position: relative;
        width: 92%;
        height: fit-content;
        background: transparent;
        padding-top: 5px;
    }
    
    .Header_MobNav_List {
        list-style: none;
        display: grid;
        grid-template-rows: 1fr 1fr 1fr 1fr;
        row-gap: 10px;
    }
    
    .Header_MobNav_Item, .Header_MobNav_Item_TextWrapper {
        display: flex;
        align-items: center;
        justify-content: center;
        
        width: fit-content;
        height: fit-content;
        text-decoration: none;
        position: relative;
    }
    
    .Header_MobNav_Item::after {
        content: "";
        position: absolute;
        right: 0px;
        left: 0px;
        top: 0px;
        bottom: 0px; 
        background: var(--white);
    }

    .Header_MobNav_Item.MobNav_Item_Initial::after {
        left: 0px;
    }

    .Header_MobNav_Item.MobNav_Item_Active::after {
        animation: .3s ease itemActive .4s forwards;
    }

    .Header_MobNav_Item_TextWrapper:hover {
        opacity: .8;
    }
    
    .Header_MobNav_Item_Text {
        font-family: "Jost", sans-serif;
        font-size: 20px;
        font-style: normal;
        color: var(--black-b);
    }

    @keyframes itemActive {
        0% {
            left: 0%;
        }
        100% {
            left: 100%;
        }
    }

    @keyframes navClosed {
        0% {
            transform: translateY(0px);
        }

        100% {
            transform: translateY(-340px);
        }
    }

    @keyframes navActive {
        0% {
            transform: translateY(-340px);
        }

        100% {
            transform: translateY(0px);
            height: 250px;
        }
    }

</style>