# OpenSSl1.1.1-build
Folder structure:
```
E:\
 | --OpensslSrc
 | --OpenSSL_Build
    | --StageXX
```
In OpenSSL_Build Folder:
## MD - Multi-Threaded Dll
- config
  perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\StageMD32" --openssldir="E:\DevData\OpenSSL_Build\StageMD32\SSL" --release
- update makefile:
  remove /Zi /Fdxxx
- make
  nmake
  nmake install
  nmake clean
## MDd - Multi-Threaded Dll debug
- config
  perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage32\MDd" --openssldir="E:\DevData\OpenSSL_Build\Stage32\MDd\SSL" --debug
- update makefile:
  update /Zi -> Z7, remove /Fdxxx
- make
  nmake
  nmake install
  nmake clean
## MT - Multi-Threaded
- config
  perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage32\MT" --openssldir="E:\DevData\OpenSSL_Build\Stage32\MT\SSL" --release no-shared
- update makefile:
  remove /Zi, /Fdxxx
- make
  nmake
  nmake install
  nmake clean
## MTd - Multi-Threaded
- config
  perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage32\MT" --openssldir="E:\DevData\OpenSSL_Build\Stage32\MT\SSL" -- no-shared
- update makefile:
  update /Zi -> Z7, remove /Fdxxx
- make
  nmake
  nmake install
  nmake clean
  
## MDd
perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage" --openssldir="E:\DevData\OpenSSL_Build\Stage\SSL" --debug
update makefile:
update /Zi -> Z7

## MT
perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage" --openssldir="E:\DevData\OpenSSL_Build\Stage\SSL" --release no-shared
##MTd




