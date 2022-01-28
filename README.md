# Source Code to generate your own NFT"

Inspired from: [Youtube codeStackr](https://github.com/codeSTACKr/video-source-code-create-nft-collection/releases/tag/v0.1.0-alpha)

Base code is from [hashlips_art_engine](https://github.com/HashLips/hashlips_art_engine)

Minting uses [NFTPort](https://nftport.xyz)

## FAQs

### Images not lining up

Be sure that every layer is the same size. If you want the resulting image to be 512x512, then each layer needs to be 512x512. This will ensure that everything lines up properly.

### Only the last image shows up

This is because you are not using `.png` images. `.jpg` or any other type will not work. `.png` has transparency which means there is no background and things behind it will show through.

### ES Module Error \[ERR_REQUIRE_ESM\]

If you are following along with the tutorial you will run into this issue unfortunately.

When the tutorial was created, `node-fetch` was at version 2. It was recently updated to version 3 and no longer supports the `require` syntax.

Fortunately, it's an easy fix. Just type these commands into the terminal:

- `npm uninstall node-fetch`
- `npm install node-fetch@2`

### Any sort of "path" error

Ensure that your layer names in the `config.js` file match exactly to your layer folder names. Also, remove any `-` (hyphens) from your file names.

**To use this code:**

- Clone this repo.
- Run the `yarn install` command.
- Copy your image layers into the `layers` folder.
- Use the `src/config.js` file to set up your layers and NFT information.
- Run the `yarn generate` command.
