# 11ty Liquid Blog Boilerplate

This is a boilerplate based on the tutorial found on [Snipart](https://snipcart.com/blog/11ty-tutorial) for [11ty Templating Framework ](https://www.11ty.dev) using the Liquid templating language.

## Folder layout structure:

```
_data           // data to be used throughout the site
_includes       // site-wide templates
_site           // default 11ty output folder 
posts           // blog posts
style           // CSS styles
.eleventy.js    // project configuration file
index.liquid    // main page
archives.liquid // archives page
```

### Note
Any folder with an underscore at the front (i.e: _data) is the default naming convention and shouldn't be renamed.

.eleventy.js (don't miss the . at the front) is the configuration file for your project.

Feel free to rename other folders to your liking.

## Commands
1. `eleventy` builds into static HTML

2. `eleventy --serve` build into static and hot-reloading via BrowserSync

3. `ctrl+c` to stop BrowserSync local server

## Frontmatter
The content at the top of .md and .liquid
```
---
Content here is called Frontmatter
---
```

### Template
```
---
title:  // HTML page title
---
```


### Pages
```
---
title:  // HTML page title
layout: // name of template file
---
```

### Posts
```
---
title:  // HTML page title
layout: // name of template file
tags:   // any post with the same tags will allow the use of collections
date:   // YYYY-MM-DD
---
```
More information about [collections](https://www.11ty.dev/docs/collections/)

Archives page has [pagination](https://www.11ty.dev/docs/pagination/) which won't be covered in this readme.

## .eleventy.js configuration file
```
module.exports = function(eleventyConfig) {
    eleventyConfig.addPassthroughCopy("style")
    eleventyConfig.addWatchTarget("style")
};
```
Any file in folder named "style" will be watched and updated
