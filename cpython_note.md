# CPython Note

A self-guided note based on the book: 'CPython Internals'

01/15/23(S):  cloned CPython 3.9 from GitHub

cloc analysis:
```
cloc cpython
    4223 text files.
    3898 unique files.
     479 files ignored.

github.com/AlDanial/cloc v 1.96  T=5.49 s (709.5 files/s, 379537.9 lines/s)
---------------------------------------------------------------------------------------
Language                             files          blank        comment           code
---------------------------------------------------------------------------------------
Python                                1961         125296         147034         578881
C                                      325          54781          51307         358094
C/C++ Header                           406          15904          10277         179753
reStructuredText                       602         101500         133803         112560
Text                                   131           2734              0          96944
XML                                    189            341            142          44522
Bourne Shell                            16           2968           2653          18512
JSON                                     8              3              0          16266
m4                                       2            567            172           5710
C++                                      5            726            254           3213
YAML                                    40            399            113           2430
HTML                                    10            110             11           1967
WiX source                              51            162             42           1738
DOS Batch                               32            356            101           1735
Visual Studio Solution                   2              1              2           1537
Windows Module Definition                8             23             14           1373
Assembly                                 6            227            384           1365
MSBuild script                          27             40              3            648
Objective-C                              7             98             61            635
Lisp                                     1            109             81            502
diff                                     3              2            201            437
CSV                                      1              0              0            373
Pascal                                   3            116            262            361
PowerShell                               7             86            178            348
make                                     4             87             43            327
Windows Resource File                    7             44             58            303
WiX string localization                 11             20              0            177
INI                                      2             48             27            122
D                                        5              8              1             74
Bourne Again Shell                       2              8              2             46
JavaScript                               1              1              6             46
Markdown                                 4             30             19             45
Fish Shell                               1             13             13             38
IDL                                      2              1              0             35
TOML                                     2              0              0             13
C Shell                                  1              9              5             11
SVG                                      9              0              0              9
XSLT                                     1              0              0              5
DTD                                      1              4              0              2
CSS                                      1              2              4              0
Visual Basic Script                      1              0              1              0
---------------------------------------------------------------------------------------
SUM:                                  3898         306824         347274        1431157
---------------------------------------------------------------------------------------
```
Total **1.4Million Lines of Code!**

## Compiling CPython on MacOS
`xcode-select --install`<br>
`brew install openssl xz zlib gdbm sqlite`
...
```
==> Caveats
==> openssl@3
A CA file has been bootstrapped using certificates from the system
keychain. To add additional certificates, place .pem files in
  /opt/homebrew/etc/openssl@3/certs

and run
  /opt/homebrew/opt/openssl@3/bin/c_rehash

openssl@3 is keg-only, which means it was not symlinked into /opt/homebrew,
because macOS provides LibreSSL.

If you need to have openssl@3 first in your PATH, run:
  echo 'export PATH="/opt/homebrew/opt/openssl@3/bin:$PATH"' >> /Users/younseoroh/.bash_profile

For compilers to find openssl@3 you may need to set:
  export LDFLAGS="-L/opt/homebrew/opt/openssl@3/lib"
  export CPPFLAGS="-I/opt/homebrew/opt/openssl@3/include"

For pkg-config to find openssl@3 you may need to set:
  export PKG_CONFIG_PATH="/opt/homebrew/opt/openssl@3/lib/pkgconfig"

==> zlib
zlib is keg-only, which means it was not symlinked into /opt/homebrew,
because macOS already provides this software and installing another version in
parallel can cause all kinds of trouble.

For compilers to find zlib you may need to set:
  export LDFLAGS="-L/opt/homebrew/opt/zlib/lib"
  export CPPFLAGS="-I/opt/homebrew/opt/zlib/include"

For pkg-config to find zlib you may need to set:
  export PKG_CONFIG_PATH="/opt/homebrew/opt/zlib/lib/pkgconfig"
```
