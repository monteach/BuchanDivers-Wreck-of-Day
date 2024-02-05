This short JS routine is used on the BuchanShipwrecks website https://www.buchandivers.com/ it is added in to select a wreck to be published on page 1.
It searches a table for a wreck sunk on the exact day (today), or else finds a randome one.
It displays details of the wreck.  Shows a thumbnail image from the Google Cloud Storage bucket "buchan-shipwrecks-wreck-thumbnails"

It is vital that the thumbnail is stored in exactly "Shipname.jpg", where shipname is the exact name i.e. where ship name is "Cape York" in the table,
the file must be named as "Cape York.jpg" in GC Storage.
