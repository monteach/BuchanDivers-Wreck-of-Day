Three custom functions embedded in the Buchan Shipwrecks Google Site (https://www.buchandivers.com/) to handle:

- the table of entries in the blog
- the dynamic, sortable and searchable table of wrecks on the site
- the wreck of the day logic as outlined below

The wreck of the day function searches a table for a wreck sunk on the exact day (today), or else finds a random one.
It displays details of the wreck.  Shows a thumbnail image from the Google Cloud Storage bucket "buchan-shipwrecks-wreck-thumbnails" which is
in the "BSAC File Uploads" project on Jim's Google account.

It is vital that the thumbnail is stored in exactly "Shipname.jpg", where shipname is the exact name i.e. where ship name is "Cape York" in the table,
the file must be named as "Cape York.jpg" in GC Storage.


gsutil cp wreckDatabase.csv gs://buchan-divers-wreck-database/wreckDatabase.csv
