
Google Cloud follows its own unique service architecture that we can find in its [documentation](https://cloud.google.com/cdn/docs/overview/). 

Setting up a proper Google Cloud CDN requires four separate services:

1. **Cloud DNS**.  This service involves DNS configuration for a given domain, such as adding A/AAAA records. This allows us to serve assets from a custom domain.
2. **Load Balancer**. It feels a bit excessive, but GCP forces us to handle the routing of a frontend (our DNS) to a backend (Storage bucket) via a load balancer.
3. **Cloud Storage**. This is where we'll be storing to serve our users.
4. **Cloud CDN**. When we configure our load balancer to point to a Cloud Storage bucket, we receive the option to enable "Cloud CDN." This is what tells Google to serve assets from edges in its global network and allows us to set caching policies.

The final architecture looks something like this:







## Cloud CDN LAB

**Source:** https://www.cloudskillsboost.google/focuses/1251?parent=catalog

In this lab, we configure **Google Cloud CDN** (Content Delivery Network) for a backend bucket and verify caching of an image. Cloud CDN uses Google's globally distributed edge points of presence to cache HTTP(S) load balanced content close to our users. Caching content at the edges of Google's network provides faster delivery of content to our users while reducing serving costs.

In this lab, we will learn how to perform the following tasks:
- Create and populate a Cloud Storage bucket.
- Create an HTTP Load Balancer with Cloud CDN.
- Verify the caching of your bucket's content.







## Resources

-  [Cloud CDN overview](https://cloud.google.com/cdn/docs/overview/)
- [Serving Assets via CDN with Google Cloud](https://hackersandslackers.com/cdn-google-cloud/)
- [How to implement Google Cloud CDN](https://geekflare.com/google-cloud-cdn-implementation/)
- https://web.dev/measure/  Measure page quality. Test your page in a lab environment powered by [PageSpeed Insights](https://pagespeed.web.dev/?utm_source=psi&utm_medium=redirect).
- Lab Cloud CDN https://www.cloudskillsboost.google/focuses/1251?parent=catalog 
- [Cache location resource](https://cloud.google.com/cdn/docs/locations)
- 
