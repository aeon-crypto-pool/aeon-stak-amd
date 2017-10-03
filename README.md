### AEON-Stak-AMD - Monero mining software

AEON-Stak is a universal Stratum pool miner. This is the AMD GPU-mining version; there is also an [CPU version](https://github.com/shyba/aeon-stak-cpu) and an [NVIDA GPU version](https://github.com/stoffu/aeon-stak-nvidia)

#### CI
[![Build status](https://ci.appveyor.com/api/projects/status/p21rl7go94wwpm0i?svg=true)](https://ci.appveyor.com/project/RafalSladek/aeon-stak-amd)

#### HTML reports

<img src="https://gist.githubusercontent.com/fireice-uk/2da301131ac01695ff79539a27b81d68/raw/e948641897ba79e5a6ee78e8248cc07779d6eac7/xmr-stak-amd-hashrate.png" width="260"> <img src="https://gist.githubusercontent.com/fireice-uk/2da301131ac01695ff79539a27b81d68/raw/e948641897ba79e5a6ee78e8248cc07779d6eac7/xmr-stak-amd-results.png" width="260"> <img src="https://gist.githubusercontent.com/fireice-uk/2da301131ac01695ff79539a27b81d68/raw/e948641897ba79e5a6ee78e8248cc07779d6eac7/xmr-stak-amd-connection.png" width="260">

The hashrate shown above was generated on a non-modded, non-overclocked RX 480.

#### Usage on Windows 

1) Edit the config.txt file to enter your pool login and password. 
2) Double click the exe file. 

AEON-Stak should compile on any C++11 compliant compiler. Windows compiler is assumed to be MSVC 2015 CE. MSVC build environment is not vendored.
```
-----BEGIN PGP SIGNED MESSAGE-----
Hash: SHA256

Windows binary release checksums

sha1sum
d45ca7cbab2ca9fe994a6c8749be08cc9a13ba69  xmr-stak-amd.exe
4892d4fcb6ef6f6132a90bbb628549eb4b5dc5fd  xmr-stak-amd-notls.exe
d34a0ba0dd7b3b1f900a7e02772e197e974b4a73  libeay32.dll
2ee9966a0fc163da58408d91be36b84fa287c10b  ssleay32.dll
5acb656005a86cad90c6327985c3795d96a96c91  opencl/blake256.cl
9e4e276afd9000945c25f6e5a5259977a29239f4  opencl/cryptonight.cl
c9fb5e4bfb137ff60063978eecd10bffb7c4deb6  opencl/groestl256.cl
361dfce776ee4a89b100d139a879af5d0f0d65e4  opencl/jh.cl
429f559190d1163335847cc08df955234051504b  opencl/wolf-aes.cl
e2862a6d7094aeab21844d3155803e5da99b4a46  opencl/wolf-skein.cl

sha3sum
b5749e46c07793c39a651f41ca8a617f4c3ab2072c50b208734afc6f  xmr-stak-amd.exe
fb29fc2059af15d0bbcd9cb73382d226c7023c22219a6e7edaa07ffc  xmr-stak-amd-notls.exe
133c065d9ef2c93396382e2ba5d8c3ca8c6a57c6beb0159cb9a4b6c5  ssleay32.dll
05003137a87313c81d6c348c9b96411c95d48dc22c35f36c39129747  libeay32.dll
a52b05548fd094e7bbb2367d7922bf19af3ed23ad5df53004fae0825  opencl/blake256.cl
a49c9da554d7b01d091eea56e8b97b943ca33cd2a64a1f3f3169e202  opencl/cryptonight.cl
13315b0a475212c92e10b7627b03a0813132437d4496b6596821b909  opencl/groestl256.cl
89548b917dbe216f5809624ebe350859c1d800048909322049f93d23  opencl/jh.cl
806eb1d4e3d7b6630a422bb42ee00faa76d31143b7c1cbde65e46938  opencl/wolf-aes.cl
052176a740a5a0bc088feea0aa7a72f0e9d96d6b6ffd00844676dd17  opencl/wolf-skein.cl

date
Wed 15 Mar 16:43:43 GMT 2017
-----BEGIN PGP SIGNATURE-----
Version: GnuPG v2

iQEcBAEBCAAGBQJYyW9uAAoJEPsk95p+1Bw0olMIAKCd6SbJqj6mrX4u8GtYAF5X
q0OJc/B27P9BRmP5bjPCJg48iopwe2MYHJN+We6ygw6+y/gn9VNdPnznoxgCaRRp
MEZzg4UYcz3zBlDe5Vfs56PbChky5x9sg02rPzVAX84SakNhRkOcS3638GDL5c20
4gldasMOHyqnM+mjlM8RpOev3SR18hXJAjGam3XxGTFqaI70WdjlwSpCwoQ9Cm6I
BIBsrTn7CK9gYn6RGj71ZDc7azW8GMPe+Aq7X3NP9VmkjmtrkjOrlwECQC20KQ6F
kSRwQQKvgsqFcxoFbmvx59X61qg4amfgEe4VLb8+lh6ZBs5TVRuzJmLZnn2v3dM=
=xYQ1
-----END PGP SIGNATURE-----
```

#### Usage on Linux (Debian-based distros)

**AMD Driver**

http://support.amd.com/en-us/kb-articles/Pages/AMDGPU-PRO-Install.aspx


```
    sudo apt-get install ocl-icd-opencl-dev libmicrohttpd-dev libssl-dev cmake build-essential
    cmake .
    make
```

GCC version 5.1 or higher is required for full C++11 support. CMake release compile scripts, as well as CodeBlocks build environment for debug builds is included.

#### Mining performance 

Mining core is a direct port (except for sercurity fixes) of wolf9466's AMD mining code. Performance is likely to be identical.

#### Default dev donation
By default the miner will donate 1% of the hashpower (1 minute in 100 minutes) to my pool. If you want to change that, edit **donate-level.h** before you build the binaries.

If you want to donate directly to support further development, here is my wallet
```
4581HhZkQHgZrZjKeCfCJxZff9E3xCgHGF25zABZz7oR71TnbbgiS7sK9jveE6Dx6uMs2LwszDuvQJgRZQotdpHt1fTdDhk
```

#### PGP Key
```
-----BEGIN PGP PUBLIC KEY BLOCK-----
Version: GnuPG v2

mQENBFhYUmUBCAC6493W5y1MMs38ApRbI11jWUqNdFm686XLkZWGDfYImzL6pEYk
RdWkyt9ziCyA6NUeWFQYniv/z10RxYKq8ulVVJaKb9qPGMU0ESfdxlFNJkU/pf28
sEVBagGvGw8uFxjQONnBJ7y7iNRWMN7qSRS636wN5ryTHNsmqI4ClXPHkXkDCDUX
QvhXZpG9RRM6jsE3jBGz/LJi3FyZLo/vB60OZBODJ2IA0wSR41RRiOq01OqDueva
9jPoAokNglJfn/CniQ+lqUEXj1vjAZ1D5Mn9fISzA/UPen5Z7Sipaa9aAtsDBOfP
K9iPKOsWa2uTafoyXgiwEVXCCeMMUjCGaoFBABEBAAG0ImZpcmVpY2VfdWsgPGZp
cmVpY2UueG1yQGdtYWlsLmNvbT6JATcEEwEIACEFAlhYUmUCGwMFCwkIBwIGFQgJ
CgsCBBYCAwECHgECF4AACgkQ+yT3mn7UHDTEcQf8CMhqaZ0IOBxeBnsq5HZr2X6z
E5bODp5cPs6ha1tjH3CWpk1AFeykNtXH7kPW9hcDt/e4UQtcHs+lu6YU59X7xLJQ
udOkpWdmooJMXRWS/zeeon4ivT9d69jNnwubh8EJOyw8xm/se6n48BcewfHekW/6
mVrbhLbF1dnuUGXzRN1WxsUZx3uJd2UvrkJhAtHtX92/qIVhT0+3PXV0bmpHURlK
YKhhm8dPLV9jPX8QVRHQXCOHSMqy/KoWEe6CnT0Isbkq3JtS3K4VBVeTX9gkySRc
IFxrNJdXsI9BxKv4O8yajP8DohpoGLMDKZKSO0yq0BRMgMh0cw6Lk22uyulGALkB
DQRYWFJlAQgAqikfViOmIccCZKVMZfNHjnigKtQqNrbJpYZCOImql4FqbZu9F7TD
9HIXA43SPcwziWlyazSy8Pa9nCpc6PuPPO1wxAaNIc5nt+w/x2EGGTIFGjRoubmP
3i5jZzOFYsvR2W3PgVa3/ujeYYJYo1oeVeuGmmJRejs0rp1mbvBSKw1Cq6C4cI0x
GTY1yXFGLIgdfYNMmiLsTy1Qwq8YStbFKeUYAMMG3128SAIaT3Eet911f5Jx4tC8
6kWUr6PX1rQ0LQJqyIsLq9U53XybUksRfJC9IEfgvgBxRBHSD8WfqEhHjhW1VsZG
dcYgr7A1PIneWsCEY+5VUnqTlt2HPaKweQARAQABiQEfBBgBCAAJBQJYWFJlAhsM
AAoJEPsk95p+1Bw0Pr8H/0vZ6U2zaih03jOHOvsrYxRfDXSmgudOp1VS45aHIREd
2nrJ+drleeFVyb14UQqO/6iX9GuDX2yBEHdCg2aljeP98AaMU//RiEtebE6CUWsL
HPVXHIkxwBCBe0YkJINHUQqLz/5f6qLsNUp1uTH2++zhdBWvg+gErTYbx8aFMFYH
0GoOtqE5rtlAh5MTvDZm+UcDwKJCxhrLaN3R3dDoyrDNRTgHQQuX5/opJBiUnVNK
d+vugnxzpMIJQP11yCZkz/KxV8zQ2QPMuZdAoh3znd/vGCJcp0rWphn4pqxA4vDp
c4hC0Yg9Dha1OoE5CJCqVL+ic4vAyB1urAwBlsd/wH8=
=B5I+
-----END PGP PUBLIC KEY BLOCK-----
```

### Common Issues

**msvcp140.dll and vcruntime140.dll not available errors**

Download and install this [runtime package](https://www.microsoft.com/en-us/download/details.aspx?id=48145) from Microsoft.  *Warning: Do NOT use "missing dll" sites - dll's are exe files with another name, and it is a fairly safe bet that any dll on a shady site like that will be trojaned.  Please download offical runtimes from Microsoft above.*

