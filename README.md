## Upgrade

https://docusaurus.io/docs/installation#updating-your-docusaurus-version

```bash
yarn upgrade @docusaurus/core@latest @docusaurus/preset-classic@latest
```

## Local

```bash
cd static
find $VKIT_WEBSITE_RESOURCE -maxdepth 1 -type d -not -path $VKIT_WEBSITE_RESOURCE -not -path '*.git' -exec ln -s {} . \;
cd ..

yarn run start
```

