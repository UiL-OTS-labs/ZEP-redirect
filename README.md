# ZEP-redirect

Package that install a small script meant to redirect non-versioned [zep](http://beexy.org/zep) calls to the correct version.

Assumes that scripts placed in `/usr/local/bin` take priority over those in `/usr/bin`, both are in the `PATH` environment variable, and the latter is the installation location of zep.

# Methodology
In order of priority the zep-redirect checks the following:
* existence of a file _use-zep-x.y.txt_
* a line `requires x.y;` in the zep script being called.

# Exit codes:
* 0 - all is great
* 1 - cannot resolve the zep version
* 2 - resolved zep version does not exist

# Contact:
Chris van Run (C.P.A.vanrun@uu.nl)
