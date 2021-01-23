# OpenSSl1.1.0-build

MT:
perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage" --openssldir="E:\DevData\OpenSSL_Build\Stage\SSL"  --release no-shared

MD
perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage" --openssldir="E:\DevData\OpenSSL_Build\Stage\SSL"  --release

MTd
perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage" --openssldir="E:\DevData\OpenSSL_Build\Stage\SSL"  --debug no-shared

MDd
perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage" --openssldir="E:\DevData\OpenSSL_Build\Stage\SSL"  --debug


// in openssl build folder
## MD - Multi-Threaded Dll
perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage" --openssldir="E:\DevData\OpenSSL_Build\Stage\SSL" --release
update makefile:
remove /Zi
## MDd
perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage" --openssldir="E:\DevData\OpenSSL_Build\Stage\SSL" --debug
update makefile:
update /Zi -> Z7

## MT
perl ..\OpenSSLSrc\Configure VC-WIN32 --prefix="E:\DevData\OpenSSL_Build\Stage" --openssldir="E:\DevData\OpenSSL_Build\Stage\SSL" --release no-shared
##MTd




