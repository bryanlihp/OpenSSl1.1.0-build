# OpenSSl1.1.1-build
Folder structure:
```
E:\
 | --OpensslSrc
 | --OpenSSL_Build
    | --StageXX
```
In OpenSSL_Build Folder:
## WIN32 
Compile using Visual studio X86 native tools.
### MD - Multi-Threaded Dll
- config
  perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage32\MD" --openssldir="E:\DevData\OpenSSL_Build\Stage32\MD\SSL" --release
- update makefile:
  remove /Zi /Fdxxx
- make
  nmake
  nmake install
  nmake clean
### MDd - Multi-Threaded Dll debug
- config
  perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage32\MDd" --openssldir="E:\DevData\OpenSSL_Build\Stage32\MDd\SSL" --debug
- update makefile:
  update /Zi -> Z7, remove /Fdxxx
- make
  nmake
  nmake install
  nmake clean
### MT - Multi-Threaded
- config
  perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage32\MT" --openssldir="E:\DevData\OpenSSL_Build\Stage32\MT\SSL" --release no-shared
- update makefile:
  remove /Zi, /Fdxxx
  remove the line that copies ossl_static.pdb
- make
  nmake
  nmake install
  nmake clean
### MTd - Multi-Threaded
- config
  perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage32\MTd" --openssldir="E:\DevData\OpenSSL_Build\Stage32\MTd\SSL" -- no-shared
- update makefile:
  update /Zi -> Z7, remove /Fdxxx, /MT->/MTd, MDd -> MTd
  remove the line that copies ossl_static.pdb
- make
  nmake
  nmake install
  nmake clean
  
## WIN64
Compile using Visual studio X64 native tools.
### MD - Multi-Threaded Dll
- config
  perl ..\OpenSSLSrc\Configure VC-WIN64 --prefix="E:\DevData\OpenSSL_Build\Stage64\MD" --openssldir="E:\DevData\OpenSSL_Build\Stage64\MD\SSL" --release
- update makefile:
  remove /Zi /Fdxxx
- make
  nmake
  nmake install
  nmake clean
### MDd - Multi-Threaded Dll debug
- config
  perl ..\OpenSSLSrc\Configure VC-WIN64 --prefix="E:\DevData\OpenSSL_Build\Stage64\MDd" --openssldir="E:\DevData\OpenSSL_Build\Stage64\MDd\SSL" --debug
- update makefile:
  update /Zi -> Z7, remove /Fdxxx
- make
  nmake
  nmake install
  nmake clean
### MT - Multi-Threaded
- config
  perl ..\OpenSSLSrc\Configure VC-WIN64 --prefix="E:\DevData\OpenSSL_Build\Stage64\MT" --openssldir="E:\DevData\OpenSSL_Build\Stage64\MT\SSL" --release no-shared
- update makefile:
  remove /Zi, /Fdxxx
- make
  nmake
  nmake install
  nmake clean
### MTd - Multi-Threaded
- config
  perl ..\OpenSSLSrc\Configure VC-WIN64 --prefix="E:\DevData\OpenSSL_Build\Stage64\MTd" --openssldir="E:\DevData\OpenSSL_Build\Stage64\MTd\SSL" -- no-shared
- update makefile:
  update /Zi -> Z7, remove /Fdxxx, /MT->/MTd
- make
  nmake
  nmake install
  nmake clean
  




