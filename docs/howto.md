# Svelte package

How to make a svelte package ?

- Go into your package folder
- `npm create svelte`
- create your components in `src/lib`
- create a `index.js` with your components with the content below in it

```js
// src/index.js
import YourComponent from './YourComponent.svelte'
export { YourComponent }
```

- Execute `npm run package`
- Your package is build
- Test it with the `src/routes/+page.svelte` file, importing the `$lib/YourComponent.svelte`
- Publish with `npm publish --access=public` since it's private by default
- Register/Login to npm to validate


## Update

- New version
- `npm version patch` 0.0.+1
- `npm version minor` 0.+1.0
- `npm version major` +1.0.0
- publish
- `npm publish`