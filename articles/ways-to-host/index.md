# Ways to host

* Application hosting
    * Limited
        * [Github pages](https://pages.github.com/) - static only<br />
            It makes sense to use GhP when you want to put some online demos for your repository<br />
            See [gh-pages](https://www.npmjs.com/package/gh-pages)
    * VDS (baremetal or docker)
        * DigitalOcean
        * Vultr
    * Cloud
        * [AWS](https://aws.amazon.com/)
            * EC2 - baremetal
            * S3 - object storage (image, doc, any structure, ...), up to 5gb
            * [Lambda]((https://github.com/awesome1888/tech-insights/blob/master/articles/ways-to-host/amazon-lambda.md)) - function call with built-in scalability
            * CloudFront - CDN
            * DynamoDB - no-sql database with built-in scalability
        * [Cloudflare](https://www.cloudflare.com)
        * Microsoft Azure
        * Google Cloud Platform
    * Other
        * [Netlify](https://www.netlify.com) - connects to your github repo and allows do deploy with CI/CD
* CDN hosting
    * [imgix &#10084;](https://www.imgix.com/)
    * [filestack](https://www.filestack.com/)
* CMS as a service
    * [Contentful](https://www.contentful.com/) - a headless CMS SAAS

