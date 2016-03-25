# Loading Markdown files in Emberjs

As a developer,

I want to give my users documentation,

Without requiring that non-technical colleagues learn a new programming language

1. `ember install ember-fr-markdown-file`

1. `ember install ember-cli-showdown`

1. `ember generate route mdContent --path /mdContent/:file_name`

1. paste this into app/routes/md-content.js
  - ` model(params) {return params.file_name;}`
1. paste this into app/templates/md-content.hbs
  - `{{markdown-to-html markdown=(fr-markdown-file model)}}`
  
1. link from your templates like:
```handlebars
      {{link-to "Code of Conduct" "mdContent" "code-of-conduct"}}
      {{link-to "Privacy"         "mdContent" "privacy"}}
      {{link-to "Getting Started" "mdContent" "getting-started"}}
```

1. Profit!
