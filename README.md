GitBook Plugin to add Algolia docSearch Plugin

## Installation

```
npm install gitbook-plugin-docsearch
```

## Usage
Gitbook comes with default search option. In order to use this plugin, need to disable the default search plugins and add `docSearch` as bellow :

```
"plugins": [
    "-search",
    "-lunr",
    "docsearch"
  ]
```
add the following plugin configurations in book.json

```
{
   "pluginsConfig": {
     "docSearch": {
       "apiKey" : "replace_with_algolia_doc_search_api_key",
       "index" : "replace_with_algolia_doc_search_index",
        "logo" : "logo.png",
        "brandUrl" : "https://uilicious.com/"
     }
   }
}
```

`logo` and `brandUrl` is optional. So you can choose to leave them empty if you do want want to put your brand logo in Gitbook.

But, if you want to use `logo` then put the logo image into the root directory of your Gitbook project.

In order to customize the styling of your search experience you can supply a css separately as bellow inside book.json

```
"addcssjs": {
   "css": [
        "css/replace_with_your_file_name.css"
        ]
    }
```

#### Known issues

The default behaviour of algolia search result prompt crops out.
See bellow :

![](known-issue.png?raw=true)

In order to fix it, apply the following css with styling

```
.book-summary {
    overflow-y: inherit;
}
```

## License & copyright
Licensed under the [MIT License](LICENSE) 
