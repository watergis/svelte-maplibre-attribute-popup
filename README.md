# This package was moved into [watergis/svelte-maplibre-components](https://github.com/watergis/svelte-maplibre-components/tree/main/packages/attribute-popup)

# svelte-maplibre-attribute-popup

This is a svelte component to add attribute popup plugin to maplibre.

## Install

```zsh
npm i @watergis/svelte-maplibre-attribute-popup
```

or

```zsh
yarn add @watergis/svelte-maplibre-attribute-popup
```

## Usage

See [Example](./src/example).

```svelte
<script lang="ts">
    import AttributePopupControl from '@watergis/svelte-maplibre-attribute-popup';

  // create maplibre.Map object
  let map = new Map();

  // filter layers to show attribute popup
  // show all layers' attributes if targetLayers is not specified.
  let targetLayers = [
    'meter',
    'flow meter',
    'valve',
    'washout',
  ];

</script>

<AttributePopupControl bind:map={$map} {targetLayers} />

<style>
  @import "https://cdn.jsdelivr.net/npm/bulma@0.9.4/css/bulma.min.css";
</style>
```

This library relies on Bulma CSS. Please import Bulma CSS from either NPM or CDN. For the Bulma CSS, further information can be found [here](https://bulma.io/documentation/overview/start/)

## create-svelte

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte).

### Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# create a new project in the current directory
npm create svelte@latest

# create a new project in my-app
npm create svelte@latest my-app
```

### Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

### Building

To create a production version of your app:

```bash
npm run build
```

You can preview the production build with `npm run preview`.

> To deploy your app, you may need to install an [adapter](https://kit.svelte.dev/docs/adapters) for your target environment.
