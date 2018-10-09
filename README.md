# Produce WFI PSF Library

Produces PSF fits files for WFI chips both at native pixel scale 
and at an oversampled pixel-scale. 

This script is executable from the command line (POSIX shell) and 
the functions can be imported/run from the Python interpreter.

Requires the WebbPSF & PySynphot packages plus associated data files.

Usage:

From shell (Change values at line 116-ish first)
```
./wings_psfs.py
```

From interpreter
```
from wings_psfs import write_psf
write_psf(det='SCA01',filt='Z087',pos=(2048,2048),oversample=10,outprefix='WFI')

from wings_psfs import all_psf, chips, filternames
all_psf(chips=[chips[0]],filternames=filternames,grid=5,oversample=10,outprefix='WFI')
```

