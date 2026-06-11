<script lang="ts">
    import logo from "$lib/assets/lletter-dark.svg";
</script>

<svelte:head>
    <title>Home</title>
    <meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="hero">
    <div class="title">
        <img src={logo} width="120" height="120" alt="Logo" />
        <h1>lletter</h1>
    </div>

    <div class="subtitle">
        <h2>
            We are an indie games studio focused on artistry, craftsmanship, and
            style.
        </h2>
    </div>
</div>

<section class="coming-soon-container">
    <h1>Coming Soon...</h1>

    Are you interested in working in a small indie studio where you'll have the
    independence to work by your own hand, where you'll have the agency to see
    your vision come to life? Do you love well-crafted, polished games that feel
    like they were made by people, not corporations? We're always looking for
    new talent. Please send an email or get in touch using the links below!
</section>

<section class="links">
    <a href="mailto:chrisliu@lletter.net" aria-label="mail">
        <span class="material-symbols--mail"></span>
    </a>
    <a href="https://x.com/clyinko" aria-label="X">
        <span class="logos--x"></span>
    </a>
    <a href="https://bsky.app/profile/chrisliu.dev" aria-label="Bluesky">
        <span class="logos--bluesky"></span>
    </a>
    <a href="https://itch.io/lletter" aria-label="lletter">
        <span class="fa6-brands--itch-io"></span>
    </a>
</section>

<style>
    .hero {
        height: 40vh;
        background: #33212b;
        background: linear-gradient(
            17deg,
            rgba(51, 33, 43, 1) 0%,
            rgba(35, 56, 45, 1) 33%,
            rgba(29, 117, 98, 1) 78%,
            rgba(40, 148, 94, 1) 100%
        );
        display: flex;
        align-items: center;
        justify-content: space-evenly;
        flex-direction: column;
        padding: 80px;

        box-shadow:
            inset 0 0 1px 2px rgba(0, 0, 0, 0.06),
            inset 0 0 2px 4px rgba(0, 0, 0, 0.04),
            inset 0 0 4px 8px rgba(0, 0, 0, 0.02),
            inset 0 0 8px 16px rgba(0, 0, 0, 0.01);

        & h1 {
            font-size: 72pt;
            font-family: "Geom", sans-serif;
            font-weight: 400;
            color: var(--main-accent-color-dark);
        }

        & h2 {
            font-weight: 400;
        }

        & .title {
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: row;
            gap: 12px;
            filter: drop-shadow(2px 2px 0px rgba(0, 0, 0, 0.2));
        }
    }

    .coming-soon-container {
        padding: 48px;
        display: flex;
        align-items: center;
        flex-direction: column;
        max-width: 1200px;
        margin-left: auto;
        margin-right: auto;
        font-size: 1.2em;
        line-height: 1.5em;

        h1 {
            padding-bottom: 1.5em;
        }
    }

    .links {
        width: 100%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        height: 120px;
        color: var(--fg);
        gap: 12px;
        --icon-size: 48px;

        .logos--x {
            display: inline-block;
            color: var(--fg);
            width: var(--icon-size);
            height: var(--icon-size);
            --svg: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 512 512'%3E%3Cpath fill='black' d='M389.2 48h70.6L305.6 224.2L487 464H345L233.7 318.6L106.5 464H35.8l164.9-188.5L26.8 48h145.6l100.5 132.9zm-24.8 373.8h39.1L151.1 88h-42z'/%3E%3C/svg%3E");
            background-color: currentColor;
            -webkit-mask-image: var(--svg);
            mask-image: var(--svg);
            -webkit-mask-repeat: no-repeat;
            mask-repeat: no-repeat;
            -webkit-mask-size: 100% 100%;
            mask-size: 100% 100%;
        }

        .logos--bluesky {
            color: var(--fg);
            display: inline-block;
            width: var(--icon-size);
            height: var(--icon-size);
            --svg: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 640 640'%3E%3Cpath fill='black' d='M439.8 358.7c-3.3-.4-6.7-.8-10-1.3c3.4.4 6.7.9 10 1.3M320 291.1c-26.1-50.7-97.1-145.2-163.1-191.8c-63.3-44.7-87.4-37-103.3-29.8C35.3 77.8 32 105.9 32 122.4S41.1 258 47 277.9c19.5 65.7 89.1 87.9 153.2 80.7c3.3-.5 6.6-.9 10-1.4c-3.3.5-6.6 1-10 1.4c-93.9 14-177.3 48.2-67.9 169.9C252.6 653.1 297.1 501.8 320 425.1c22.9 76.7 49.2 222.5 185.6 103.4c102.4-103.4 28.1-156-65.8-169.9c-3.3-.4-6.7-.8-10-1.3c3.4.4 6.7.9 10 1.3c64.1 7.1 133.6-15.1 153.2-80.7c5.9-19.9 15-138.9 15-155.5s-3.3-44.7-21.6-52.9c-15.8-7.1-40-14.9-103.2 29.8c-66.1 46.6-137.1 141.1-163.2 191.8'/%3E%3C/svg%3E");
            background-color: currentColor;
            -webkit-mask-image: var(--svg);
            mask-image: var(--svg);
            -webkit-mask-repeat: no-repeat;
            mask-repeat: no-repeat;
            -webkit-mask-size: 100% 100%;
            mask-size: 100% 100%;
        }

        .material-symbols--mail {
            color: var(--fg);
            display: inline-block;
            width: var(--icon-size);
            height: var(--icon-size);
            --svg: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 24 24'%3E%3Cpath fill='black' d='M4 20q-.825 0-1.412-.587T2 18V6q0-.825.588-1.412T4 4h16q.825 0 1.413.588T22 6v12q0 .825-.587 1.413T20 20zm8-7L4 8v10h16V8zm0-2l8-5H4zM4 8V6v12z'/%3E%3C/svg%3E");
            background-color: currentcolor;
            -webkit-mask-image: var(--svg);
            mask-image: var(--svg);
            -webkit-mask-repeat: no-repeat;
            mask-repeat: no-repeat;
            -webkit-mask-size: 100% 100%;
            mask-size: 100% 100%;
        }

        .fa6-brands--itch-io {
            color: var(--fg);
            display: inline-block;
            width: var(--icon-size);
            height: var(--icon-size);
            --svg: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 512 512'%3E%3Cpath fill='black' d='M71.92 34.77C50.2 47.67 7.4 96.84 7 109.73v21.34c0 27.06 25.29 50.84 48.25 50.84c27.57 0 50.54-22.85 50.54-50c0 27.12 22.18 50 49.76 50s49-22.85 49-50c0 27.12 23.59 50 51.16 50h.5c27.57 0 51.16-22.85 51.16-50c0 27.12 21.47 50 49 50s49.76-22.85 49.76-50c0 27.12 23 50 50.54 50c23 0 48.25-23.78 48.25-50.84v-21.34c-.4-12.9-43.2-62.07-64.92-75C372.56 32.4 325.76 32 256 32S91.14 33.1 71.92 34.77m132.32 134.39c-22 38.4-77.9 38.71-99.85.25c-13.17 23.14-43.17 32.07-56 27.66c-3.87 40.15-13.67 237.13 17.73 269.15c80 18.67 302.08 18.12 379.76 0c31.65-32.27 21.32-232 17.75-269.15c-12.92 4.44-42.88-4.6-56-27.66c-22 38.52-77.85 38.1-99.85-.24c-7.1 12.49-23.05 28.94-51.76 28.94a57.54 57.54 0 0 1-51.75-28.94zm-41.58 53.77c16.47 0 31.09 0 49.22 19.78a437 437 0 0 1 88.18 0C318.22 223 332.85 223 349.31 223c52.33 0 65.22 77.53 83.87 144.45c17.26 62.15-5.52 63.67-33.95 63.73c-42.15-1.57-65.49-32.18-65.49-62.79c-39.25 6.43-101.93 8.79-155.55 0c0 30.61-23.34 61.22-65.49 62.79c-28.42-.06-51.2-1.58-33.94-63.73c18.67-67 31.56-144.45 83.88-144.45zM256 270.79s-44.38 40.77-52.35 55.21l29-1.17v25.32c0 1.55 21.34.16 23.33.16c11.65.54 23.31 1 23.31-.16v-25.28l29 1.17c-8-14.48-52.35-55.24-52.35-55.24z'/%3E%3C/svg%3E");
            background-color: currentColor;
            -webkit-mask-image: var(--svg);
            mask-image: var(--svg);
            -webkit-mask-repeat: no-repeat;
            mask-repeat: no-repeat;
            -webkit-mask-size: 100% 100%;
            mask-size: 100% 100%;
        }
    }
</style>
