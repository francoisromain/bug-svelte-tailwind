# Svelte - Tailwind - Prettier : bug

The css classes order is different when formatted on save and when formatted by a script.

To reproduce the bug, in VS Code:

- Clone this repo
- Install the dependencies : `npm i`
- Install the required VS Code extensions : `svelte.svelte-vscode`, `dbaeumer.vscode-eslint`, `esbenp.prettier-vscode` and `bradlc.vscode-tailwindcss`.
- Open the file `src/routes/index.svelte` and save the file. The order of the css classes changes.
- Run `npm run format`. The order of the css classes changes again.

If we remove the `boxShadow` property in `tailwind.config.cjs`, the css order stays the same when formatted on save and by a script.

link to the issue: <https://github.com/tailwindlabs/prettier-plugin-tailwindcss/issues/61>
