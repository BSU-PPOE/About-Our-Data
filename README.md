# About-Our-Data
Help understanding the data in this repository.  

## What kind of data is hosted here?

Our collection of repositories currently contains both raw and calibrated images of areas of the night sky in FITS format.  These images were taken with a 14" telescope and a black and white camera (either an Apogee Alta U47 or SBIG STL-6303) with filters to allow only certain types of light through.  Our observatory is located in Bridgewater, MA.

In future, this site will also include helpful instructions for academic collaborators, K-12 teachers, and anyone simply interested in learning how to work with astronomical data, as well as information about the stability of the stars in each area of the sky we image.

## What is a FITS image?

FITS (Flexible Image Transport System) is the standard image format in astronomy and astrophysics.  It's similar to a TIFF file, but it includes a large header (metadata!) with information such as the latitude and longitude of the observatory, the coordinates of the center of the image, the time the image was taken, the size of the camera sensor's pixels, and much more.  The information in the header is meant to help a person work with the data effectively later.

[You can follow this link for the definition of the FITS standard](https://archive.stsci.edu/fits/fits_standard/), but you won't need to know all of that information all at once. The most critical information in that header was already mentioned above!

## What is a data image?

We consider a 'data' image to be any image of an area of the night sky.  It may contain stars, galaxies, nebulae, star clusters, asteroids, planets, comets, etc.  In other words, data images contain things we're interested in studying!

## What is a calibration image?

Calibration images are taken in order to improve the quality of our data images later.  For example, we would like to remove some of the noise (it looks like static!) from our images if we can.  We would also like to remove irregularities in how bright different parts of the picture are.  If we smooth out anything that makes areas in the picture brighter or darker, we can get a better measurement of how bright the stars in the picture really are!  They'll be affected less by other things that have nothing to do with the stars themselves. (That goes for things like nebulae and galaxies, too).

## What are the types of calibration images?

Flats, darks, and biases are all types of calibration images.  At our observatory, we try to use only flats and darks whenever possible.  Needing biases makes the whole process more complicated.

## What is a flat calibration image?

A flat is a picture taken of an evenly-lit surface.  This can be a superbly-lit screen or it can be the twilight sky.  At our observatory, we use the twilight sky.

Flats must be taken with exactly the same equipment setup you use to take your data pictures, through every filter you intend to use to take pictures, with the same binning setting, and at the same camera operating temperature as is used when taking the data images.  In a flat calibration image, you will see large round or donut-shaped dark areas as well as a bright center that gets darker toward the edges of the picture.  That is normal!  The point of flats is to be able to remove those irregularities from the data so there is a nice, smooth background.

At our observatory, we try to take at least 12 flats for each filter we intend to observe in that night.  We take the images just after sunset with our telescope aimed about 45 degrees up on the eastern side of the sky.

## What is a dark calibration image?

A dark is a picture taken with the camera's shutter closed (so no light is coming in from the telescope).  The idea is to capture the noise (static) present even when our camera isn't 'looking' at anything.  At our observatory, we also make sure the lights are off and the lens cap is on the telescope.

Darks look like a staticky old-style TV picture when there's no signal.  The static comes mostly from heat!

Darks must be taken with the same camera, with the same binning setting, and at the same camera operating temperature as is used when taking the data images.  It's strongly preferred to also have the same exposure time as your data images.  (If you don't, you either need to use biases or use darks with a shorter exposure length than the data images).

At our observatory, we take at least 12 darks to match each type of data image as well as each type of flat image we took that night.

Over time, if we take many darks with the same settings (for example, perhaps over the course of a month), we can combine all of those darks into one set of calibration images which work better than a single set.

## What is a bias calibration image?

A bias is an image taken with zero exposure time at all.  This way, all the camera has a chance to do is read the information in each pixel before the camera even begins to collect light.  It will find irregularities - some pixels appear to be brighter than others even though no light was collected.  Some of this comes from the camera's sensor, and some of it comes from the process of downloading the information to the computer.

Taking separate biases is often not necessary since the bias signal is also present in the dark images - so if you use dark calibration, you have already taken the bias signal into account.  However, if you do not have darks of the correct exposure length, you may want to apply biases to everything - including the darks, the flats, and the data - in order to remove that signal separately.

At our observatory, we only take biases about once every six months (or whenever we change the camera operating temperature).  We highly recommend the use of slightly shorter exposure darks as-is rather than using bias correction if darks of the exact exposure length as the data are not available.
