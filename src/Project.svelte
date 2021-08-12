<script>
    export let name
    export let link
    export let logo
    export let picture
    export let description
    export let github
    export let technologies
    export let mobileOnly
</script>

<style>
    main {
        background-color: var(--primary);
        color: white;
        box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
        transition: 0.3s;
        min-width: 50%;
    }

    main:hover {
        box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
    }

    .center {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .text {
        padding-bottom: 16px;
        max-width: 80%;
    }

    h1 {
        font-weight: 100;
    }
    
    p {
        padding: 10px
    }

    img {
        max-height: 20vw;
    }

</style>

<main>
    {#if logo !== undefined}
        <img src={logo} alt={name}/>
    {:else}
        <h1>{name}</h1>
        <img src={picture} alt={''} />
    {/if}
    <div class="center">
        <div class="text">
            <p>
                <i class="fas fa-file" /> 
                {description}
            </p>
            <p>
                <i class="fas fa-memory" /> 
                {technologies}
            </p>
            <div>
                <a href={link}>
                    <i class="fas fa-link"></i>
                    {mobileOnly ? 'Site (mobile only)' : 'Site'}
                </a>
            </div>
            <div>
                <a href={github}>
                    <i class="fab fa-github"></i>
                    GitHub
                </a>
            </div>
        </div>
    </div>

</main>