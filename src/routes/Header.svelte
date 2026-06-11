<script lang="ts">
    import logo from "$lib/assets/lletter-dark.svg";
</script>

<header>
    <img src={logo} width="36" height="36" alt="Lletter" />
</header>

<style>
    header {
        display: flex;
        justify-content: flex-start;
        align-items: center;
        width: 100%;
        gap: 4px;
        background-color: var(--bg);
        padding: 8px;
        box-shadow:
            0 1px 2px rgba(0, 0, 0, 0.07),
            0 2px 4px rgba(0, 0, 0, 0.07),
            0 4px 8px rgba(0, 0, 0, 0.07),
            0 8px 16px rgba(0, 0, 0, 0.07);
        z-index: 1;
    }

    img {
        filter: drop-shadow(1px 1px 0px rgba(0, 0, 0, 0.5));
    }
</style>
