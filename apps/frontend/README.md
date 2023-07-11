# Sveltekit with NX

Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte).

```json
{
  "dev": "vite dev --port 3000 --open",
  "build": "vite build",
  "package": "vite package",
  "preview": "vite preview",
  "check": "svelte-check --tsconfig ./tsconfig.json",
  "check:watch": "svelte-check --tsconfig ./tsconfig.json --watch",
  "lint": "prettier --check --ignore-path=../../.prettierignore . && eslint \"src\"",
  "format": "prettier --write --ignore-path=../../.prettierignore ."
}
```

```json
"build": {
    "executor": "@nx/vite:build",
    //...
    //...
    "options": {
        "outputPath": "dist/apps/my-app"
    },
        //...
    }
},
```
