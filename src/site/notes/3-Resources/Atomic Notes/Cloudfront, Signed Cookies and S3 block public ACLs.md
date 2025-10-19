---
{"dg-publish":true,"permalink":"/3-resources/atomic-notes/cloudfront-signed-cookies-and-s3-block-public-ac-ls/","tags":["aws","cloudfront","☢️"],"updated":"2025-10-18T21:23:28.278-07:00"}
---


Recently, I had to set up Cloudfront with Signed Cookies to serve up S3 content privately.

I had this working when the S3 bucket was public, but the cookies started to be denied when I set the block public ACLs option.

While this seems reasonable in retrospect, it was a big head-scratcher, and I could not find any documentation on debugging why the cookie was being denied.

If you turn on `block public ACLs` it means ANY public access will be denied, including something like Cloudfront, even if you have it configured to allow cloudfront to pull from the s3 bucket.