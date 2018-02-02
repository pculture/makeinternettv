This is the code for makeinternettv.org

At one point it was a PHP site, but now it's just static code.  The code here
was downloaded from the wayback machine using
https://github.com/hartator/wayback-machine-downloader.  It was then synced to
the s3 bucket makeinternettv.org and is currently served from there.


Updating:

```
aws s3 sync --exclude "*.php" . s3://makeinternettv.org
aws s3 sync --content-type="text/html" --exclude "*" --include "*.php" . s3://makeinternettv.org
```
