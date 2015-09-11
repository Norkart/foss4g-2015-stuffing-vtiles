# Stuffing your vector tiles full of data

# Mapbox vector tiles in a minute (If you know a bit already)
 - A lot of talks at last years FOSS4G
 - Even ESRI have adopted it
 
# Norwegian maps in a minute (or maybe three)

# "I got an award for Norway"
 - And now some examples. This is Norway.
 
# Far, far away
 - This is Norway!
 
# Seoul gives us an inferiority complex
 - This is Norway.
 
# Modalen
 - And this is Norway. Welcome to Modalen, Norway's least populous municipality.
 - 378 inhabitants and without a road conenction until 1978
 - Their historical main export was sand. These days, it's (rather fittingly) IT services.
 
# Modalen (Google)
 - This is how it looks on Google Maps.
 
# Modalen (OSM)
 - On OSM.
 - Note that OSM is as good as Google even out here, a testament to Norway's strong OSM culture.
 
# Modalen (Norkart)
 - Of course, nothing compares to 242 years worth of the tax-payers money
 - These is our maps, based on the mapping authorities data.
 
# Modalen up close
 - Note the details:
   - Lampposts, manholes, roof angles and hedgerows

# A lot of details!
 - We even have a layer for decommisioned anti-aircraft defence features.
 
# Anyway, vector tiles!
 - Since we're assuming you have some knowledge on vector tiles:
 - It breaks rouglhy itnto two components
 
# The pipeline
 - We took our existing raster pipeline and adapted it
 
# Zoom levels

# Tile size limits

# Never use `SELECT *`
 - This is an example from SQL queries, but the principle is general
 
# Generalisation choices
 - Tippecanoe is a library for generalising features to make nice maps at low zooms
 - We just went with the things we already had, but we could probably just use tippecanoe and our best data.
 
# Keep the originals!
 - A lot of stuff gets thrown out in vector tiles

# The spec vs. best/general practice
 - We could in other words stuff more things in, but it might be bad for speed. Also we'rd lose compatability with Mapbox!
 
# Making Mapbox Studio beg for mercy
 - I think we were doing stuff nobody really expected.
 
# MBTiles Generation times
 - Because of our geography and location on the planet, Norway's bounding box has about twice as much sea and neighbouring countries than it has Norwegian territory. So for us Pyramids worked well!
 
# File sizes
 - I dont have the final data on sizes yet, but the tendency seems clear.
 
# Converting styles from SLD
 - It's amazing what summer interns can get done!
 - Mapbox definitely has a point about making GL styles from scratch, we'll be spending a lot of time on the tweaks.
 
# Original (raster)
 - This is what our raster maps look like
 
# Results (MapboxGL JS)
 - this is the result of our automatic conversion, not bad right?
 - Errors are mainly due to bugs in render order and feature selection, like bridges and tunnels which are modelled as roads with special attributes.

# Results (Mapbox GL Native - Android)
 - The visual fidelity is good in both JS & native
 - The speed is not. 
   - JS needs Chrome and a powerful computer, can lag a fair bit
   - Native works smoothly even on older devices.

# End page
 - So yeah, I have a twitter and this presentation is on GitHub along with some other stuff we've done.
 - Now would be the time for questions and comments!