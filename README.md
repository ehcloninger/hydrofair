# hydrofair
Website for local non-profit

# building
Build with plain `jekyll` command. Don't use bundle as this project isn't set up for that.
Build on local maching with `jekyll serve --incremental`. Get everything working. 
Then, clear the _site folder with `jekyll clean`. Rebuild with `jekyll build` and use _site folder on the production server.

# deploy

Deploy on AWS S3. Login to account, find hydrofair.org bucket. Delete entire contents. Upload _site folder to bucket. Make
sure you don't upload _site itself, just the contents. Bucket should be public and set to serve a site.
Go into cloudfront and create an invalidation for the site with the root of the S3 bucket. Wait 1-2 minutes and test the site.
