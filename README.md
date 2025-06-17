Four custom functions embedded in the Buchan Shipwrecks Google Site (https://www.buchandivers.com/) to handle:

- the table of entries in the blog
- the dynamic, sortable and searchable table of wrecks on the site
- the wreck of the day logic as outlined below
- the wreck map using OpenStreetMap with a marine overlay

The wreck of the day function searches a table for a wreck sunk on the exact day (today), or else finds a random one.
It displays details of the wreck.  Shows a thumbnail image from the Google Cloud Storage bucket "buchan-divers-wreck-thumbnails" which is
in the "Buchan Divers Database" project on the Buchan Divers Google account.

It is vital that the thumbnail is stored in exactly "Shipname.jpg", where shipname is the exact name i.e. where ship name is "Cape York" in the table,
the file must be named as "Cape York.jpg" in GC Storage.

The code runs off two .csv files maintained in this workspace and migrated to the GCP bucket.

**wreckDatabase.csv** holds details of all wrecks on the site and is used for Wreck of the Day, Wreck table and Map.  The name of the wreck is used for hyperlinks and must match the url when spaces and periods are replaced with "-" e.g. "TIC No.8" gives a url of "tic-no-8" and thumbnail of "TIC No.8.jpg" for the map pop-up.  The WotD Comment field is used for wreck of the day. 

Apply updates to the file, save and migrate to cloud with:

gsutil cp wreckDatabase.csv gs://buchan-divers-wreck-database/wreckDatabase.csv

**log.csv** holds log details and can have embedded hyperlinks.  Apply updates to the file, save and migrate to cloud with:

gsutil cp log.csv gs://buchan-divers-wreck-database/log.csv
