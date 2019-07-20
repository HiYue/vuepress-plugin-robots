# Robots.txt file plugin for Vuepress

## Install
* NPM
```bash
npm install vuepress-plugin-robots
```

## Usage
### Vuepress v0.x
> NOT SUPPORT

### Vuepress v1.x
```javascript
// .vuepress/config.js

module.exports = {
  plugins: {
    'robots': {
        /**
         * @disallowAll
         * Optional: if it's true, all others options are ignored and exclude all robots from the entire server
         */
        disallowAll: false,
        /**
         * @allowAll
         * Optional: if it's true and @disallowAll is false, all others options are ignored and allow all robots complete access
         */
        allowAll: true,      
        /**
         * @sitemap
         * Optional, by default: sitemap.xml
         */ 
        sitemap: "/sitemap.xml",
        /**
         * @host
         * Optional, by default: null
         */   
        host: "https://your-website",
        /**
         * @policies
         * Optional, by default: null
         */ 
        policies: [
            {
                userAgent: '*',
                disallow: [
                    '/admin','/login'
                ],
                allow: [    // Optional: Allowed paths. 
                    'products','blog'
                ]
            }
        ]
    },
  }
}
```

## Thanks
Thanks to [generate-robotstxt](https://github.com/itgalaxy/generate-robotstxt)

## Changelog

## License
MIT