# OpenSSl1.1.1-build
Folder structure:
> E:\
 | --OpensslSrc
 | --OpenSSL_Build
    | --StageXX

In OpenSSL_Build Folder:
## MD - Multi-Threaded Dll
- config
  perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage" --openssldir="E:\DevData\OpenSSL_Build\Stage\SSL" --release
- update makefile:
  remove /Zi
- make
  nmake
  nmake install
  nmake clean'

## MDd
perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage" --openssldir="E:\DevData\OpenSSL_Build\Stage\SSL" --debug
update makefile:
update /Zi -> Z7

## MT
perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage" --openssldir="E:\DevData\OpenSSL_Build\Stage\SSL" --release no-shared
##MTd




