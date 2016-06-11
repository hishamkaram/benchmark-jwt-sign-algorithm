# Sign Algorithm Benchmark using PyJWT


# Usage
```
pip install -r requirements.txt
python benchmark.py
```

# Result

## MacBook Air (2013)

```
$ python benchmark.py
.............................++++++++++++
.................++++++++++++
writing RSA key
........++++++
..................++++++
writing RSA key
...............................+++
............................+++
writing RSA key
...........................................................++
........................................++
writing RSA key
.........++
.................................................................++
writing RSA key
read EC key
writing EC key
read EC key
writing EC key
read EC key
writing EC key
read EC key
writing EC key
## benchmarker:         release 4.0.1 (for python)
## python version:      3.5.1
## python compiler:     GCC 4.2.1 Compatible Apple LLVM 7.3.0 (clang-703.0.31)
## python platform:     Darwin-15.5.0-x86_64-i386-64bit
## python executable:   /Users/xxx/.pyenv/versions/3.5.1/bin/python
## cpu model:           Intel(R) Core(TM) i5-4250U CPU @ 1.30GHz
## parameters:          loop=1, cycle=1, extra=0

##                                  real    (total    = user    + sys)
encode-hs256-5                    0.5157    0.5100    0.5000    0.0100
decode-hs256-5                    1.0325    1.0000    0.9900    0.0100
encode-hs256-86                   0.6389    0.6300    0.6200    0.0100
decode-hs256-86                   1.0328    0.9900    0.9800    0.0100
encode-rs256-rsa512               5.6488    5.4900    5.2500    0.2400
decode-rs256-rsa512               4.0798    4.0000    3.9500    0.0500
encode-rs256-rsa1024              7.9759    7.9000    7.6100    0.2900
decode-rs256-rsa1024              3.9999    3.9400    3.9000    0.0400
encode-rs256-rsa2048             25.2845   24.9400   24.3500    0.5900
decode-rs256-rsa2048              4.5254    4.4500    4.4100    0.0400
encode-rs256-rsa3072             65.8082   64.0800   62.7500    1.3300
decode-rs256-rsa3072              5.2793    5.2000    5.1600    0.0400
encode-rs256-rsa4096            133.1929  129.6300  127.7200    1.9100
decode-rs256-rsa4096              7.4351    6.7800    6.7100    0.0700
encode-es256-secp224r1            8.7213    8.3500    8.1600    0.1900
decode-es256-secp224r1            7.3140    7.1400    7.0900    0.0500
encode-es256-prime256v1           7.2488    7.2100    7.1000    0.1100
decode-es256-prime256v1           6.9113    6.8100    6.7700    0.0400
encode-es256-secp384r1           18.2934   18.1000   17.8700    0.2300
decode-es256-secp384r1           17.6845   17.5200   17.4100    0.1100
encode-es256-secp521r1           12.6158   12.5500   12.3900    0.1600
decode-es256-secp521r1           16.5139   16.4000   16.3300    0.0700

## Ranking                          real
encode-hs256-5                    0.5157  (100.0) ********************
encode-hs256-86                   0.6389  ( 80.7) ****************
decode-hs256-5                    1.0325  ( 49.9) **********
decode-hs256-86                   1.0328  ( 49.9) **********
decode-rs256-rsa1024              3.9999  ( 12.9) ***
decode-rs256-rsa512               4.0798  ( 12.6) ***
decode-rs256-rsa2048              4.5254  ( 11.4) **
decode-rs256-rsa3072              5.2793  (  9.8) **
encode-rs256-rsa512               5.6488  (  9.1) **
decode-es256-prime256v1           6.9113  (  7.5) *
encode-es256-prime256v1           7.2488  (  7.1) *
decode-es256-secp224r1            7.3140  (  7.1) *
decode-rs256-rsa4096              7.4351  (  6.9) *
encode-rs256-rsa1024              7.9759  (  6.5) *
encode-es256-secp224r1            8.7213  (  5.9) *
encode-es256-secp521r1           12.6158  (  4.1) *
decode-es256-secp521r1           16.5139  (  3.1) *
decode-es256-secp384r1           17.6845  (  2.9) *
encode-es256-secp384r1           18.2934  (  2.8) *
encode-rs256-rsa2048             25.2845  (  2.0)
encode-rs256-rsa3072             65.8082  (  0.8)
encode-rs256-rsa4096            133.1929  (  0.4)

## Matrix                           real    [01]    [02]    [03]    [04]    [05]    [06]    [07]    [08]    [09]    [10]    [11]    [12]    [13]    [14]    [15]    [16]    [17]    [18]    [19]    [20]    [21]    [22]
[01] encode-hs256-5               0.5157   100.0   123.9   200.2   200.3   775.6   791.1   877.5  1023.7  1095.3  1340.1  1405.6  1418.2  1441.7  1546.6  1691.1  2446.3  3202.1  3429.1  3547.2  4902.8 12760.5 25826.7
[02] encode-hs256-86              0.6389    80.7   100.0   161.6   161.7   626.0   638.5   708.3   826.3   884.1  1081.7  1134.5  1144.7  1163.7  1248.3  1365.0  1974.5  2584.6  2767.8  2863.1  3957.3 10299.7 20846.1
[03] decode-hs256-5               1.0325    49.9    61.9   100.0   100.0   387.4   395.1   438.3   511.3   547.1   669.4   702.0   708.4   720.1   772.5   844.7  1221.8  1599.4  1712.7  1771.7  2448.8  6373.5 12899.7
[04] decode-hs256-86              1.0328    49.9    61.9   100.0   100.0   387.3   395.0   438.1   511.1   546.9   669.1   701.8   708.1   719.9   772.2   844.4  1221.5  1598.9  1712.2  1771.2  2448.0  6371.6 12895.7
[05] decode-rs256-rsa1024         3.9999    12.9    16.0    25.8    25.8   100.0   102.0   113.1   132.0   141.2   172.8   181.2   182.9   185.9   199.4   218.0   315.4   412.9   442.1   457.4   632.1  1645.3  3329.9
[06] decode-rs256-rsa512          4.0798    12.6    15.7    25.3    25.3    98.0   100.0   110.9   129.4   138.5   169.4   177.7   179.3   182.2   195.5   213.8   309.2   404.8   433.5   448.4   619.7  1613.0  3264.7
[07] decode-rs256-rsa2048         4.5254    11.4    14.1    22.8    22.8    88.4    90.2   100.0   116.7   124.8   152.7   160.2   161.6   164.3   176.2   192.7   278.8   364.9   390.8   404.2   558.7  1454.2  2943.3
[08] decode-rs256-rsa3072         5.2793     9.8    12.1    19.6    19.6    75.8    77.3    85.7   100.0   107.0   130.9   137.3   138.5   140.8   151.1   165.2   239.0   312.8   335.0   346.5   478.9  1246.5  2522.9
[09] encode-rs256-rsa512          5.6488     9.1    11.3    18.3    18.3    70.8    72.2    80.1    93.5   100.0   122.3   128.3   129.5   131.6   141.2   154.4   223.3   292.3   313.1   323.8   447.6  1165.0  2357.9
[10] decode-es256-prime256v1      6.9113     7.5     9.2    14.9    14.9    57.9    59.0    65.5    76.4    81.7   100.0   104.9   105.8   107.6   115.4   126.2   182.5   238.9   255.9   264.7   365.8   952.2  1927.2
[11] encode-es256-prime256v1      7.2488     7.1     8.8    14.2    14.2    55.2    56.3    62.4    72.8    77.9    95.3   100.0   100.9   102.6   110.0   120.3   174.0   227.8   244.0   252.4   348.8   907.9  1837.5
[12] decode-es256-secp224r1       7.3140     7.1     8.7    14.1    14.1    54.7    55.8    61.9    72.2    77.2    94.5    99.1   100.0   101.7   109.0   119.2   172.5   225.8   241.8   250.1   345.7   899.8  1821.1
[13] decode-rs256-rsa4096         7.4351     6.9     8.6    13.9    13.9    53.8    54.9    60.9    71.0    76.0    93.0    97.5    98.4   100.0   107.3   117.3   169.7   222.1   237.9   246.0   340.1   885.1  1791.4
[14] encode-rs256-rsa1024         7.9759     6.5     8.0    12.9    12.9    50.1    51.2    56.7    66.2    70.8    86.7    90.9    91.7    93.2   100.0   109.3   158.2   207.0   221.7   229.4   317.0   825.1  1669.9
[15] encode-es256-secp224r1       8.7213     5.9     7.3    11.8    11.8    45.9    46.8    51.9    60.5    64.8    79.2    83.1    83.9    85.3    91.5   100.0   144.7   189.4   202.8   209.8   289.9   754.6  1527.2
[16] encode-es256-secp521r1      12.6158     4.1     5.1     8.2     8.2    31.7    32.3    35.9    41.8    44.8    54.8    57.5    58.0    58.9    63.2    69.1   100.0   130.9   140.2   145.0   200.4   521.6  1055.8
[17] decode-es256-secp521r1      16.5139     3.1     3.9     6.3     6.3    24.2    24.7    27.4    32.0    34.2    41.9    43.9    44.3    45.0    48.3    52.8    76.4   100.0   107.1   110.8   153.1   398.5   806.5
[18] decode-es256-secp384r1      17.6845     2.9     3.6     5.8     5.8    22.6    23.1    25.6    29.9    31.9    39.1    41.0    41.4    42.0    45.1    49.3    71.3    93.4   100.0   103.4   143.0   372.1   753.2
[19] encode-es256-secp384r1      18.2934     2.8     3.5     5.6     5.6    21.9    22.3    24.7    28.9    30.9    37.8    39.6    40.0    40.6    43.6    47.7    69.0    90.3    96.7   100.0   138.2   359.7   728.1
[20] encode-rs256-rsa2048        25.2845     2.0     2.5     4.1     4.1    15.8    16.1    17.9    20.9    22.3    27.3    28.7    28.9    29.4    31.5    34.5    49.9    65.3    69.9    72.4   100.0   260.3   526.8
[21] encode-rs256-rsa3072        65.8082     0.8     1.0     1.6     1.6     6.1     6.2     6.9     8.0     8.6    10.5    11.0    11.1    11.3    12.1    13.3    19.2    25.1    26.9    27.8    38.4   100.0   202.4
[22] encode-rs256-rsa4096       133.1929     0.4     0.5     0.8     0.8     3.0     3.1     3.4     4.0     4.2     5.2     5.4     5.5     5.6     6.0     6.5     9.5    12.4    13.3    13.7    19.0    49.4   100.0
```
