# TeX Live-2017 with Python-Pygments

[![TexLive:2017](https://img.shields.io/badge/TeX%20Live-2017-blue.svg)](https://www.tug.org/texlive/acquire.html)
[![](https://images.microbadger.com/badges/image/sumdoc/texlive-2017.svg)](https://microbadger.com/images/sumdoc/texlive-2017 "Get your own image badge on microbadger.com")
[![Build](https://img.shields.io/docker/automated/sumdoc/texlive-2017.svg)](https://hub.docker.com/r/sumdoc/texlive-2017/)
[![Docker Pull](https://img.shields.io/docker/pulls/sumdoc/texlive-2017.svg)](https://hub.docker.com/r/sumdoc/texlive-2017/)
[![License: MIT](https://img.shields.io/github/license/sumandoc/texlive-2017.svg)](https://github.com/sumandoc/TeXLive-2017/blob/master/LICENSE) 
[![Github Stars](https://img.shields.io/github/stars/sumandoc/TeXLive-2017.svg?style=social&label=Github)](https://github.com/sumandoc/TeXLive-2017)



Contains full TeXLive-2017 with additional [python-pygments library](http://pygments.org/) for source code highlighting via [minted package](https://www.ctan.org/pkg/minted).
Also contains [ImageMagick®](https://www.imagemagick.org/script/index.php) for image manipulation to include in TeX files.


## How to get the image?

From the interactive docker shell, pull this image with:

`docker pull sumdoc/texlive-2017`

## Why should you use it?

If you work with Latex documents, this is useful to compile your document **independent of OS and without the need to install anything**.  It contains all the compilers: **pdflatex**, **xelatex** and **lualatex**.

## How to run this image/ How do you use it ?

After you are done with the pull, mount the directory present in your host operating system containing .tex files 
into docker image like this:

`docker run -it -v /c/Users/username/Folder_with_tex:/home -w /home sumdoc/texlive-2017 bin/bash`


You will now have access to the terminal. Your working dir will be `/home` where you will see the .tex files.

Now run:
`pdflatex -shell-escape -synctex=1 -interaction=nonstopmode yourtex.tex` and see your **yourtex.tex** file getting compiled.



**The size of image is 3 GB** which is quite big but
its ***cool*** with all stuff that's available in **CTAN**. :)


