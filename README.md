# Sistema Operacional em Disco - TK2000 Color
![Capa](/capa.jpg "Sistema Operacional em Disco - TK2000 Color")

This repository contains all files used in the digitization of the `Sistema Operacional em Disco - TK2000 Color` user manual. The manual was part of the TKDOS 3.3.x software distribution by the former brazilian militar dictatorship-era "Microsoft" company. TKDOS 3.3.x was the disk operating system used in the Microdigital TK2000 computer series.

All manual pages were scanned using XSane and a multi-function home device (`Canon MX725`) on a Linux System running Fedora 29. TIFF raw images were processed with `Scan Tailor` and converted to JPEG2000 using the following `Image Magick` command: 

> $ for i in raw\ input/out/*.tif ; do filename=`basename -s .tif "$i"` ; convert -define jp2:rate=15 "$i" "scan tailor output.j2k/$filename.j2k" ; done

Image Magick was used to create the .PDF file from the JPEG2000 images too:

> $ convert -adjoin scan\ tailor\ output.j2k/*.j2k "Sistema Operacional em Disco - TK2000 Color.pdf" 
