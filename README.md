This repository contains the data products and lens modeling results and inputs from Spilker et al. (2018).
If there's anything not posted here that you'd like, just send me an email.

dataproducts
------------

This folder has everything that doesn't involve lensing in any way - a naturally-weighted continuum image of
the ALMA data, an image cube, and a spectrum I extracted from that cube of the OH absorption lines. The 
continuum image and spectrum were used to make Figure 1 in the paper.

lensproducts
------------

This folder has all of the results of the lens modeling in FITS format. There are three sets of FITS files, for
the OH continuum (500km/s of line-free continuum to match the OH reconstructions), the systemic OH absorption, and
the blueshifted wind absorption. Each set has a (dirty) image of the data, model, and residuals, and the reconstructed
source plane. Because the lens modeling is done on the visibilities directly, dirty images are about the closest
approximations that are still useful to inspect. Also included are the continuum-subtracted absorption components. With 
those two files and the continuum source plane reconstruction, you can reproduce Figure 2 in the paper. 

I didn't upload all the MCMC chains from fitting for the lensing deflections (there's a lot), but if you want or need
those for any reason feel free to email me.

lensinputs
----------

This folder has the binary visibility data in the format our lensing code uses, and an XML parameters file showing how
to create the reconstructions from those data inputs. A binary executable of the lensing code is hosted 
[here](https://github.com/yasharhezaveh/Ripple/releases). Note that you'll need a working MPI installation, GSL,
and the [Elemental](http://libelemental.org/) linear algebra library. 
