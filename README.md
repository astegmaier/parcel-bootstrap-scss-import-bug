# parcel-bootstrap-scss-import-bug

This repo provides a reproduction of [an issue with parcel](https://stackoverflow.com/questions/66536381/cannot-create-property-importer-on-string-scss-bootstrap-scss/69683135#69683135) that can occur if you import `bootstrap.scss` from a `.css` file.

If you try to build the project, you'll see this error:

```
🚨 Build failed.

@parcel/transformer-sass: Cannot create property 'importer' on string 'scss/bootstrap.scss'

  TypeError: Cannot create property 'importer' on string 'scss/bootstrap.scss'
  at loadConfig (/Users/Andrew/Projects/stackoverflow-parcel-bootstrap/node_modules/@parcel/transformer-sass/lib/SassTransformer.js:92:29)
  at async loadPluginConfig (/Users/Andrew/Projects/stackoverflow-parcel-bootstrap/node_modules/@parcel/core/lib/requests/ConfigRequest.js:65:21)
  at async Transformation.loadTransformerConfig
  (/Users/Andrew/Projects/stackoverflow-parcel-bootstrap/node_modules/@parcel/core/lib/Transformation.js:533:5)
  at async Transformation.loadPipeline (/Users/Andrew/Projects/stackoverflow-parcel-bootstrap/node_modules/@parcel/core/lib/Transformation.js:472:20)
  at async Transformation.run (/Users/Andrew/Projects/stackoverflow-parcel-bootstrap/node_modules/@parcel/core/lib/Transformation.js:169:20)
  at async Child.handleRequest (/Users/Andrew/Projects/stackoverflow-parcel-bootstrap/node_modules/@parcel/workers/lib/child.js:217:9)
```