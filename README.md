<p align="center">
  <img src="https://github.com/user-attachments/assets/2cc3707f-0e17-481d-b66c-7dabac8f529f">
</p>

# Passphrase Generator

Simple passphrase generator made with Svelte. After the website has been loaded, everything works 100% on the client side. No informattion is ever sent back to the server when generating a passphrase. Words for the passphrase are choosen in a cryptographically secure way from an english dictionary. Settings are randomized when first loading the site.

The app is deployed [here.](https://pw.rafaelbiehler.com)

### Build

1. `npm install`
2. `npm run dev`

### Deploy

1. `npm run build`
2. `npm install -g firebase-tools`
3. `firebase login`
4. `firebase deploy --only hosting`

or just `npm run deploy`, if already logged in.
