---
title: npm Funding Metadata
date: 2020-05-09T16:56Z
description: point users to your offer page
---

npm version 6.13.0 [added an `npm fund` subcommand for listing funding information about dependencies](https://github.com/npm/cli/releases/tag/v6.13.0).  To leverage that feature for your L0 npm package, edit `package.json` to add a `funding` property:

```json
{
  "funding": {
    "type": "License Zero",
    "url": "https://licensezero.com/offers/562c0ffe-df98-4348-87b7-e60e3c37c534#buy"
  }
}
```

users will see a count of packages within funding metadata when they run `npm install`, as well as a prompt to run `npm fund`.
