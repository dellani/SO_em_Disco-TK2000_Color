# SO_em_Disco-TK2000_Color
This repository contains all files used in the digitization of the `Sistema Operacional em Disco - TK2000 Color` user manual. This was included in TKDOS 3.3.x software distribution by the former brazilian militar dictatorship-era "Microsoft" for the Microdigital TK2000 computer series.

![Cover](/scan tailor output.j2k/all pages_page0001.j2k)

Manual pages were scanned with XSane and a multi-function home device (`Canon MX725`) on a Linux System running Fedora 29. TIFF Raw images were processed with `Scan Tailer` and converted to JPEG2000 using the following `Image Magick` command: 

> for i in raw\ input/out/*.tif ; do filename=`basename -s .tif "$i"` ; convert -define jp2:rate=15 "$i" "scan tailor output.j2k/$filename.j2k" ; done

Image Magick was used to create the .PDF file from the JPEG2000 images too:

> convert -adjoin scan\ tailor\ output.j2k/*.j2k "Sistema Operacional em Disco - TK2000 Color.pdf" 
