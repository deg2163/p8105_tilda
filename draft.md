Draft
================
Final Project
11/17/2018

Importing data

``` r
load("./data/Wave 1/DS0001/34315-0001-Data.rda")
load("./data/Wave 2/DS0001/37105-0001-Data.rda")
load("./data/Wave 3/DS0001/37106-0001-Data.rda")

wave_1_data = da34315.0001
wave_2_data = da37105.0001
wave_3_data = da37106.0001
```

Creating Graphs

``` r
wave_3_data %>% 
  select(PH001, PH002)
```

    ##               PH001          PH002
    ## 1    (02) Very Good      (04) Fair
    ## 2         (03) Good      (03) Good
    ## 3         (03) Good      (03) Good
    ## 4         (03) Good      (03) Good
    ## 5    (02) Very Good (02) Very Good
    ## 6         (03) Good (02) Very Good
    ## 7    (02) Very Good (02) Very Good
    ## 8    (02) Very Good (02) Very Good
    ## 9         (03) Good      (03) Good
    ## 10        (03) Good      (03) Good
    ## 11   (02) Very Good (02) Very Good
    ## 12   (01) Excellent (01) Excellent
    ## 13        (03) Good (02) Very Good
    ## 14   (02) Very Good (02) Very Good
    ## 15        (04) Fair      (03) Good
    ## 16   (02) Very Good (02) Very Good
    ## 17        (03) Good      (04) Fair
    ## 18        (03) Good      (03) Good
    ## 19        (03) Good (02) Very Good
    ## 20   (02) Very Good (01) Excellent
    ## 21        (03) Good      (03) Good
    ## 22        (03) Good      (03) Good
    ## 23        (03) Good      (03) Good
    ## 24        (03) Good (02) Very Good
    ## 25        (04) Fair (01) Excellent
    ## 26        (03) Good      (03) Good
    ## 27   (02) Very Good (02) Very Good
    ## 28   (02) Very Good (02) Very Good
    ## 29        (05) Poor (02) Very Good
    ## 30   (02) Very Good      (03) Good
    ## 31        (04) Fair (02) Very Good
    ## 32        (03) Good      (03) Good
    ## 33   (02) Very Good (02) Very Good
    ## 34   (01) Excellent (01) Excellent
    ## 35        (03) Good      (03) Good
    ## 36        (03) Good      (03) Good
    ## 37        (04) Fair      (03) Good
    ## 38        (04) Fair      (04) Fair
    ## 39   (02) Very Good (02) Very Good
    ## 40   (01) Excellent (01) Excellent
    ## 41        (04) Fair      (04) Fair
    ## 42   (02) Very Good      (03) Good
    ## 43        (03) Good      (03) Good
    ## 44        (03) Good      (03) Good
    ## 45        (03) Good      (03) Good
    ## 46        (05) Poor      (04) Fair
    ## 47        (04) Fair (02) Very Good
    ## 48        (04) Fair      (03) Good
    ## 49        (03) Good      (03) Good
    ## 50        (05) Poor      (05) Poor
    ## 51        (03) Good      (03) Good
    ## 52        (03) Good      (03) Good
    ## 53   (02) Very Good (02) Very Good
    ## 54        (03) Good      (03) Good
    ## 55        (04) Fair      (04) Fair
    ## 56        (03) Good (02) Very Good
    ## 57   (02) Very Good (02) Very Good
    ## 58        (04) Fair (02) Very Good
    ## 59   (02) Very Good (02) Very Good
    ## 60        (03) Good      (03) Good
    ## 61   (01) Excellent (02) Very Good
    ## 62   (02) Very Good      (03) Good
    ## 63   (02) Very Good (02) Very Good
    ## 64   (02) Very Good (02) Very Good
    ## 65        (04) Fair      (03) Good
    ## 66        (03) Good      (03) Good
    ## 67        (04) Fair      (03) Good
    ## 68   (02) Very Good (02) Very Good
    ## 69        (04) Fair      (04) Fair
    ## 70   (01) Excellent (01) Excellent
    ## 71        (03) Good      (03) Good
    ## 72        (04) Fair (02) Very Good
    ## 73   (02) Very Good (02) Very Good
    ## 74        (03) Good      (03) Good
    ## 75        (03) Good      (03) Good
    ## 76        (03) Good (02) Very Good
    ## 77        (03) Good      (03) Good
    ## 78   (01) Excellent (02) Very Good
    ## 79   (02) Very Good      (03) Good
    ## 80   (01) Excellent (01) Excellent
    ## 81        (04) Fair      (04) Fair
    ## 82        (03) Good (02) Very Good
    ## 83        (03) Good      (03) Good
    ## 84   (01) Excellent (01) Excellent
    ## 85        (03) Good      (03) Good
    ## 86        (03) Good      (03) Good
    ## 87        (03) Good      (03) Good
    ## 88        (03) Good      (03) Good
    ## 89        (03) Good (02) Very Good
    ## 90        (03) Good (02) Very Good
    ## 91        (03) Good      (03) Good
    ## 92   (02) Very Good (02) Very Good
    ## 93        (04) Fair (01) Excellent
    ## 94   (01) Excellent (01) Excellent
    ## 95        (03) Good (02) Very Good
    ## 96        (04) Fair (02) Very Good
    ## 97        (04) Fair      (04) Fair
    ## 98        (03) Good      (03) Good
    ## 99        (04) Fair      (03) Good
    ## 100       (03) Good      (03) Good
    ## 101       (04) Fair      (03) Good
    ## 102  (02) Very Good (02) Very Good
    ## 103       (03) Good      (03) Good
    ## 104       (03) Good      (03) Good
    ## 105       (05) Poor      (04) Fair
    ## 106  (02) Very Good      (03) Good
    ## 107       (04) Fair      (03) Good
    ## 108  (02) Very Good      (03) Good
    ## 109       (04) Fair      (03) Good
    ## 110       (05) Poor      (03) Good
    ## 111       (03) Good      (03) Good
    ## 112  (02) Very Good      (03) Good
    ## 113       (04) Fair (02) Very Good
    ## 114       (04) Fair      (03) Good
    ## 115       (04) Fair      (03) Good
    ## 116  (02) Very Good (02) Very Good
    ## 117       (03) Good      (05) Poor
    ## 118  (02) Very Good      (03) Good
    ## 119       (03) Good      (03) Good
    ## 120  (02) Very Good (02) Very Good
    ## 121       (03) Good (02) Very Good
    ## 122  (02) Very Good (02) Very Good
    ## 123  (02) Very Good (02) Very Good
    ## 124       (04) Fair      (04) Fair
    ## 125       (05) Poor      (03) Good
    ## 126       (03) Good      (03) Good
    ## 127  (02) Very Good (01) Excellent
    ## 128       (03) Good (02) Very Good
    ## 129       (03) Good (02) Very Good
    ## 130       (03) Good      (04) Fair
    ## 131  (01) Excellent (01) Excellent
    ## 132       (04) Fair      (03) Good
    ## 133       (04) Fair (01) Excellent
    ## 134  (02) Very Good (02) Very Good
    ## 135  (02) Very Good (02) Very Good
    ## 136       (04) Fair      (03) Good
    ## 137  (02) Very Good (02) Very Good
    ## 138  (02) Very Good (02) Very Good
    ## 139  (02) Very Good (01) Excellent
    ## 140  (02) Very Good (02) Very Good
    ## 141       (05) Poor (02) Very Good
    ## 142       (03) Good (02) Very Good
    ## 143  (01) Excellent (01) Excellent
    ## 144  (02) Very Good      (03) Good
    ## 145       (03) Good      (03) Good
    ## 146  (02) Very Good      (03) Good
    ## 147       (03) Good      (03) Good
    ## 148       (03) Good      (03) Good
    ## 149  (02) Very Good (02) Very Good
    ## 150       (03) Good      (03) Good
    ## 151       (03) Good      (03) Good
    ## 152       (03) Good      (03) Good
    ## 153       (03) Good      (03) Good
    ## 154  (01) Excellent      (04) Fair
    ## 155       (04) Fair      (04) Fair
    ## 156       (03) Good      (03) Good
    ## 157  (02) Very Good      (04) Fair
    ## 158       (03) Good      (03) Good
    ## 159       (03) Good      (03) Good
    ## 160       (03) Good      (03) Good
    ## 161  (02) Very Good (02) Very Good
    ## 162       (04) Fair      (03) Good
    ## 163  (01) Excellent (02) Very Good
    ## 164  (01) Excellent (01) Excellent
    ## 165  (02) Very Good      (03) Good
    ## 166       (04) Fair      (04) Fair
    ## 167  (02) Very Good (02) Very Good
    ## 168  (02) Very Good (02) Very Good
    ## 169       (03) Good      (03) Good
    ## 170  (02) Very Good      (03) Good
    ## 171  (02) Very Good      (03) Good
    ## 172       (04) Fair      (03) Good
    ## 173       (04) Fair (01) Excellent
    ## 174  (02) Very Good      (03) Good
    ## 175       (03) Good (02) Very Good
    ## 176       (04) Fair      (03) Good
    ## 177  (02) Very Good (02) Very Good
    ## 178  (01) Excellent      (03) Good
    ## 179  (01) Excellent (01) Excellent
    ## 180       (04) Fair      (03) Good
    ## 181       (03) Good      (03) Good
    ## 182  (02) Very Good (02) Very Good
    ## 183       (03) Good (02) Very Good
    ## 184       (04) Fair      (04) Fair
    ## 185       (05) Poor (01) Excellent
    ## 186  (02) Very Good (01) Excellent
    ## 187  (02) Very Good (02) Very Good
    ## 188       (03) Good (02) Very Good
    ## 189       (03) Good      (03) Good
    ## 190  (02) Very Good (02) Very Good
    ## 191       (03) Good (02) Very Good
    ## 192       (03) Good      (03) Good
    ## 193  (01) Excellent (01) Excellent
    ## 194  (02) Very Good (02) Very Good
    ## 195       (04) Fair (01) Excellent
    ## 196  (01) Excellent (01) Excellent
    ## 197  (02) Very Good (01) Excellent
    ## 198       (03) Good      (03) Good
    ## 199  (01) Excellent (01) Excellent
    ## 200  (02) Very Good (02) Very Good
    ## 201       (04) Fair (02) Very Good
    ## 202       (03) Good      (03) Good
    ## 203       (04) Fair (01) Excellent
    ## 204  (02) Very Good      (03) Good
    ## 205       (03) Good (02) Very Good
    ## 206       (04) Fair (02) Very Good
    ## 207  (02) Very Good (02) Very Good
    ## 208  (01) Excellent (01) Excellent
    ## 209       (04) Fair (02) Very Good
    ## 210       (03) Good (02) Very Good
    ## 211  (02) Very Good      (03) Good
    ## 212       (03) Good      (03) Good
    ## 213       (03) Good (02) Very Good
    ## 214       (04) Fair (01) Excellent
    ## 215  (02) Very Good (02) Very Good
    ## 216       (03) Good      (03) Good
    ## 217       (03) Good (02) Very Good
    ## 218       (04) Fair (02) Very Good
    ## 219       (04) Fair      (03) Good
    ## 220  (02) Very Good (02) Very Good
    ## 221       (03) Good      (03) Good
    ## 222  (02) Very Good (02) Very Good
    ## 223       (03) Good (02) Very Good
    ## 224  (02) Very Good (01) Excellent
    ## 225  (02) Very Good      (03) Good
    ## 226       (03) Good (01) Excellent
    ## 227  (02) Very Good (01) Excellent
    ## 228  (02) Very Good (01) Excellent
    ## 229       (04) Fair      (03) Good
    ## 230  (02) Very Good (02) Very Good
    ## 231       (03) Good (02) Very Good
    ## 232       (03) Good      (03) Good
    ## 233       (03) Good (01) Excellent
    ## 234       (03) Good (02) Very Good
    ## 235       (03) Good      (04) Fair
    ## 236       (04) Fair      (03) Good
    ## 237  (02) Very Good      (03) Good
    ## 238       (03) Good      (03) Good
    ## 239  (02) Very Good (01) Excellent
    ## 240       (04) Fair (02) Very Good
    ## 241       (03) Good      (03) Good
    ## 242  (02) Very Good (02) Very Good
    ## 243  (02) Very Good (02) Very Good
    ## 244       (03) Good      (03) Good
    ## 245  (02) Very Good (02) Very Good
    ## 246       (03) Good (02) Very Good
    ## 247       (03) Good      (03) Good
    ## 248       (03) Good      (03) Good
    ## 249       (04) Fair (02) Very Good
    ## 250  (02) Very Good (02) Very Good
    ## 251  (02) Very Good (02) Very Good
    ## 252  (02) Very Good (02) Very Good
    ## 253       (04) Fair      (03) Good
    ## 254  (01) Excellent (01) Excellent
    ## 255  (02) Very Good      (04) Fair
    ## 256       (03) Good      (03) Good
    ## 257  (02) Very Good (01) Excellent
    ## 258  (02) Very Good (02) Very Good
    ## 259       (04) Fair      (03) Good
    ## 260       (04) Fair      (04) Fair
    ## 261       (03) Good      (04) Fair
    ## 262  (02) Very Good      (03) Good
    ## 263  (02) Very Good (01) Excellent
    ## 264  (01) Excellent (01) Excellent
    ## 265  (02) Very Good (02) Very Good
    ## 266       (03) Good (02) Very Good
    ## 267       (03) Good      (03) Good
    ## 268  (02) Very Good (02) Very Good
    ## 269       (04) Fair      (03) Good
    ## 270       (03) Good (02) Very Good
    ## 271  (02) Very Good (02) Very Good
    ## 272       (03) Good      (03) Good
    ## 273  (02) Very Good (02) Very Good
    ## 274  (01) Excellent (02) Very Good
    ## 275  (02) Very Good (02) Very Good
    ## 276  (02) Very Good (02) Very Good
    ## 277  (02) Very Good (02) Very Good
    ## 278  (02) Very Good (02) Very Good
    ## 279  (02) Very Good (02) Very Good
    ## 280       (04) Fair      (03) Good
    ## 281       (03) Good      (03) Good
    ## 282  (02) Very Good (02) Very Good
    ## 283  (02) Very Good      (03) Good
    ## 284  (01) Excellent (01) Excellent
    ## 285  (02) Very Good (02) Very Good
    ## 286  (02) Very Good (02) Very Good
    ## 287  (02) Very Good (02) Very Good
    ## 288       (03) Good      (03) Good
    ## 289  (01) Excellent      (04) Fair
    ## 290       (03) Good      (03) Good
    ## 291  (02) Very Good (02) Very Good
    ## 292  (02) Very Good      (03) Good
    ## 293  (02) Very Good (02) Very Good
    ## 294  (01) Excellent (01) Excellent
    ## 295  (02) Very Good (02) Very Good
    ## 296  (02) Very Good (02) Very Good
    ## 297       (03) Good      (03) Good
    ## 298  (02) Very Good (02) Very Good
    ## 299       (03) Good      (03) Good
    ## 300       (03) Good      (03) Good
    ## 301  (02) Very Good      (04) Fair
    ## 302       (03) Good      (03) Good
    ## 303       (04) Fair (02) Very Good
    ## 304  (02) Very Good      (03) Good
    ## 305       (03) Good (01) Excellent
    ## 306       (03) Good      (03) Good
    ## 307       (03) Good      (03) Good
    ## 308  (02) Very Good (02) Very Good
    ## 309       (03) Good (01) Excellent
    ## 310  (02) Very Good (02) Very Good
    ## 311  (02) Very Good      (03) Good
    ## 312  (01) Excellent      (03) Good
    ## 313       (04) Fair (02) Very Good
    ## 314  (02) Very Good      (04) Fair
    ## 315       (04) Fair      (04) Fair
    ## 316       (03) Good      (03) Good
    ## 317  (02) Very Good (02) Very Good
    ## 318       (03) Good (02) Very Good
    ## 319  (02) Very Good (02) Very Good
    ## 320       (03) Good (02) Very Good
    ## 321       (04) Fair (02) Very Good
    ## 322  (02) Very Good (02) Very Good
    ## 323  (02) Very Good (02) Very Good
    ## 324  (02) Very Good (01) Excellent
    ## 325  (02) Very Good (01) Excellent
    ## 326       (03) Good      (03) Good
    ## 327       (03) Good      (03) Good
    ## 328  (02) Very Good      (03) Good
    ## 329       (04) Fair      (04) Fair
    ## 330       (05) Poor      (04) Fair
    ## 331       (03) Good      (03) Good
    ## 332  (02) Very Good (02) Very Good
    ## 333  (02) Very Good (01) Excellent
    ## 334  (02) Very Good (02) Very Good
    ## 335  (02) Very Good (01) Excellent
    ## 336  (01) Excellent (01) Excellent
    ## 337       (04) Fair (01) Excellent
    ## 338       (03) Good (02) Very Good
    ## 339       (03) Good      (03) Good
    ## 340  (02) Very Good (02) Very Good
    ## 341  (02) Very Good (02) Very Good
    ## 342       (04) Fair      (04) Fair
    ## 343       (04) Fair      (03) Good
    ## 344       (04) Fair (02) Very Good
    ## 345       (04) Fair      (03) Good
    ## 346       (04) Fair      (03) Good
    ## 347       (03) Good (02) Very Good
    ## 348  (01) Excellent (01) Excellent
    ## 349  (01) Excellent (02) Very Good
    ## 350  (02) Very Good      (03) Good
    ## 351  (02) Very Good      (03) Good
    ## 352  (01) Excellent      (03) Good
    ## 353       (03) Good      (03) Good
    ## 354       (03) Good      (03) Good
    ## 355  (01) Excellent (01) Excellent
    ## 356       (04) Fair      (04) Fair
    ## 357  (02) Very Good      (03) Good
    ## 358       (03) Good      (03) Good
    ## 359       (03) Good      (03) Good
    ## 360  (01) Excellent (01) Excellent
    ## 361  (01) Excellent (01) Excellent
    ## 362       (03) Good (02) Very Good
    ## 363       (03) Good (02) Very Good
    ## 364  (02) Very Good      (03) Good
    ## 365       (04) Fair      (04) Fair
    ## 366       (04) Fair      (04) Fair
    ## 367  (02) Very Good      (03) Good
    ## 368       (04) Fair      (04) Fair
    ## 369       (03) Good (01) Excellent
    ## 370       (03) Good      (03) Good
    ## 371       (05) Poor (02) Very Good
    ## 372       (03) Good      (04) Fair
    ## 373  (01) Excellent (01) Excellent
    ## 374       (05) Poor      (03) Good
    ## 375       (04) Fair      (03) Good
    ## 376       (03) Good      (03) Good
    ## 377       (03) Good      (03) Good
    ## 378  (01) Excellent (01) Excellent
    ## 379  (02) Very Good (02) Very Good
    ## 380  (02) Very Good (02) Very Good
    ## 381  (01) Excellent      (03) Good
    ## 382       (03) Good (02) Very Good
    ## 383       (03) Good      (03) Good
    ## 384       (03) Good      (03) Good
    ## 385       (03) Good (02) Very Good
    ## 386       (04) Fair      (03) Good
    ## 387       (03) Good      (03) Good
    ## 388  (02) Very Good (01) Excellent
    ## 389       (03) Good      (03) Good
    ## 390       (03) Good      (03) Good
    ## 391       (03) Good      (03) Good
    ## 392       (04) Fair      (03) Good
    ## 393       (03) Good (01) Excellent
    ## 394       (03) Good      (04) Fair
    ## 395       (03) Good      (03) Good
    ## 396       (03) Good (02) Very Good
    ## 397       (03) Good (02) Very Good
    ## 398       (04) Fair      (04) Fair
    ## 399       (04) Fair      (05) Poor
    ## 400       (05) Poor      (05) Poor
    ## 401  (02) Very Good (02) Very Good
    ## 402       (03) Good      (03) Good
    ## 403       (03) Good      (03) Good
    ## 404       (03) Good      (03) Good
    ## 405  (02) Very Good      (03) Good
    ## 406       (03) Good      (03) Good
    ## 407       (03) Good      (03) Good
    ## 408       (04) Fair      (05) Poor
    ## 409       (04) Fair (02) Very Good
    ## 410       (05) Poor      (04) Fair
    ## 411       (03) Good (02) Very Good
    ## 412  (02) Very Good (02) Very Good
    ## 413  (02) Very Good (02) Very Good
    ## 414       (03) Good      (03) Good
    ## 415       (03) Good      (03) Good
    ## 416  (02) Very Good (02) Very Good
    ## 417       (03) Good      (03) Good
    ## 418  (02) Very Good (02) Very Good
    ## 419       (04) Fair      (03) Good
    ## 420       (04) Fair (02) Very Good
    ## 421       (04) Fair (02) Very Good
    ## 422       (03) Good      (04) Fair
    ## 423       (03) Good      (03) Good
    ## 424       (03) Good      (03) Good
    ## 425  (02) Very Good      (04) Fair
    ## 426       (03) Good (02) Very Good
    ## 427  (02) Very Good (02) Very Good
    ## 428       (03) Good (02) Very Good
    ## 429  (02) Very Good (02) Very Good
    ## 430       (03) Good      (03) Good
    ## 431       (03) Good      (03) Good
    ## 432  (02) Very Good (02) Very Good
    ## 433       (03) Good      (03) Good
    ## 434  (02) Very Good      (03) Good
    ## 435       (03) Good (01) Excellent
    ## 436  (01) Excellent      (03) Good
    ## 437  (02) Very Good (01) Excellent
    ## 438  (02) Very Good (01) Excellent
    ## 439       (03) Good (02) Very Good
    ## 440       (04) Fair (02) Very Good
    ## 441       (04) Fair      (03) Good
    ## 442       (03) Good      (03) Good
    ## 443       (04) Fair (02) Very Good
    ## 444       (03) Good      (03) Good
    ## 445  (01) Excellent (01) Excellent
    ## 446       (03) Good (02) Very Good
    ## 447       (03) Good (01) Excellent
    ## 448       (03) Good      (03) Good
    ## 449  (01) Excellent (01) Excellent
    ## 450       (03) Good (01) Excellent
    ## 451       (03) Good      (03) Good
    ## 452  (02) Very Good (02) Very Good
    ## 453  (01) Excellent (01) Excellent
    ## 454  (02) Very Good (02) Very Good
    ## 455       (03) Good      (03) Good
    ## 456       (03) Good      (03) Good
    ## 457  (02) Very Good        (98) DK
    ## 458  (02) Very Good      (03) Good
    ## 459  (02) Very Good (02) Very Good
    ## 460  (02) Very Good (02) Very Good
    ## 461  (02) Very Good (02) Very Good
    ## 462  (02) Very Good (01) Excellent
    ## 463  (02) Very Good      (03) Good
    ## 464  (01) Excellent (01) Excellent
    ## 465       (05) Poor (02) Very Good
    ## 466  (02) Very Good (02) Very Good
    ## 467  (02) Very Good      (03) Good
    ## 468       (04) Fair (02) Very Good
    ## 469       (03) Good      (03) Good
    ## 470       (05) Poor (02) Very Good
    ## 471       (04) Fair (02) Very Good
    ## 472       (04) Fair      (04) Fair
    ## 473  (02) Very Good (02) Very Good
    ## 474       (03) Good      (04) Fair
    ## 475  (02) Very Good (02) Very Good
    ## 476  (02) Very Good (02) Very Good
    ## 477  (02) Very Good (02) Very Good
    ## 478  (02) Very Good (02) Very Good
    ## 479  (02) Very Good (02) Very Good
    ## 480       (04) Fair      (04) Fair
    ## 481       (03) Good (02) Very Good
    ## 482       (04) Fair (02) Very Good
    ## 483  (02) Very Good (02) Very Good
    ## 484       (03) Good      (03) Good
    ## 485  (02) Very Good (02) Very Good
    ## 486  (02) Very Good (02) Very Good
    ## 487  (02) Very Good (02) Very Good
    ## 488       (03) Good      (03) Good
    ## 489       (03) Good      (03) Good
    ## 490  (02) Very Good (02) Very Good
    ## 491       (03) Good      (03) Good
    ## 492       (04) Fair      (04) Fair
    ## 493       (03) Good (02) Very Good
    ## 494       (03) Good      (03) Good
    ## 495       (03) Good      (03) Good
    ## 496  (01) Excellent (01) Excellent
    ## 497       (04) Fair      (04) Fair
    ## 498       (03) Good      (03) Good
    ## 499       (04) Fair      (04) Fair
    ## 500       (03) Good      (04) Fair
    ## 501  (02) Very Good (02) Very Good
    ## 502  (02) Very Good (02) Very Good
    ## 503       (03) Good      (03) Good
    ## 504       (03) Good      (03) Good
    ## 505  (02) Very Good (01) Excellent
    ## 506       (04) Fair      (03) Good
    ## 507  (02) Very Good      (03) Good
    ## 508  (02) Very Good      (03) Good
    ## 509       (03) Good      (03) Good
    ## 510       (03) Good (02) Very Good
    ## 511       (05) Poor      (03) Good
    ## 512       (03) Good (02) Very Good
    ## 513  (02) Very Good (02) Very Good
    ## 514  (02) Very Good      (03) Good
    ## 515  (02) Very Good (02) Very Good
    ## 516  (01) Excellent (01) Excellent
    ## 517       (03) Good (02) Very Good
    ## 518       (03) Good      (03) Good
    ## 519  (01) Excellent (02) Very Good
    ## 520       (03) Good (02) Very Good
    ## 521       (04) Fair (02) Very Good
    ## 522       (03) Good      (03) Good
    ## 523       (03) Good      (03) Good
    ## 524       (03) Good (01) Excellent
    ## 525  (02) Very Good (02) Very Good
    ## 526       (03) Good      (04) Fair
    ## 527  (02) Very Good (02) Very Good
    ## 528       (03) Good (02) Very Good
    ## 529  (02) Very Good (02) Very Good
    ## 530  (02) Very Good (02) Very Good
    ## 531       (04) Fair (02) Very Good
    ## 532  (01) Excellent (01) Excellent
    ## 533  (02) Very Good (02) Very Good
    ## 534       (03) Good (02) Very Good
    ## 535       (03) Good      (03) Good
    ## 536       (04) Fair (02) Very Good
    ## 537  (02) Very Good (02) Very Good
    ## 538  (02) Very Good (02) Very Good
    ## 539       (04) Fair      (03) Good
    ## 540  (02) Very Good (02) Very Good
    ## 541       (03) Good      (03) Good
    ## 542       (03) Good      (03) Good
    ## 543  (02) Very Good (02) Very Good
    ## 544  (01) Excellent (01) Excellent
    ## 545       (05) Poor      (03) Good
    ## 546       (04) Fair (02) Very Good
    ## 547  (01) Excellent (01) Excellent
    ## 548       (03) Good (02) Very Good
    ## 549       (03) Good      (03) Good
    ## 550  (02) Very Good (02) Very Good
    ## 551  (02) Very Good (02) Very Good
    ## 552       (03) Good      (05) Poor
    ## 553       (03) Good (02) Very Good
    ## 554  (02) Very Good (02) Very Good
    ## 555  (02) Very Good (02) Very Good
    ## 556  (02) Very Good      (03) Good
    ## 557       (04) Fair      (03) Good
    ## 558  (02) Very Good (02) Very Good
    ## 559       (03) Good      (03) Good
    ## 560  (02) Very Good (02) Very Good
    ## 561       (03) Good (02) Very Good
    ## 562  (02) Very Good      (03) Good
    ## 563       (04) Fair      (03) Good
    ## 564       (03) Good      (03) Good
    ## 565  (02) Very Good (01) Excellent
    ## 566  (02) Very Good (02) Very Good
    ## 567  (01) Excellent (01) Excellent
    ## 568  (02) Very Good (02) Very Good
    ## 569       (03) Good      (03) Good
    ## 570  (02) Very Good (02) Very Good
    ## 571       (03) Good      (03) Good
    ## 572  (02) Very Good (02) Very Good
    ## 573       (03) Good (02) Very Good
    ## 574       (03) Good      (03) Good
    ## 575  (02) Very Good (02) Very Good
    ## 576       (05) Poor      (03) Good
    ## 577       (03) Good (02) Very Good
    ## 578  (01) Excellent (01) Excellent
    ## 579       (04) Fair (02) Very Good
    ## 580  (02) Very Good (01) Excellent
    ## 581  (02) Very Good (02) Very Good
    ## 582  (02) Very Good (02) Very Good
    ## 583  (02) Very Good (02) Very Good
    ## 584  (02) Very Good (02) Very Good
    ## 585  (02) Very Good (02) Very Good
    ## 586  (02) Very Good (02) Very Good
    ## 587  (02) Very Good      (03) Good
    ## 588       (03) Good      (03) Good
    ## 589       (03) Good      (03) Good
    ## 590  (02) Very Good (02) Very Good
    ## 591       (04) Fair      (03) Good
    ## 592       (03) Good (02) Very Good
    ## 593       (04) Fair      (03) Good
    ## 594       (03) Good      (03) Good
    ## 595  (01) Excellent (01) Excellent
    ## 596       (03) Good      (03) Good
    ## 597  (02) Very Good      (03) Good
    ## 598  (02) Very Good (01) Excellent
    ## 599  (01) Excellent (01) Excellent
    ## 600  (02) Very Good (02) Very Good
    ## 601       (03) Good (02) Very Good
    ## 602       (03) Good (02) Very Good
    ## 603  (02) Very Good (02) Very Good
    ## 604  (02) Very Good      (03) Good
    ## 605       (03) Good      (04) Fair
    ## 606       (03) Good (02) Very Good
    ## 607       (03) Good      (03) Good
    ## 608  (01) Excellent (01) Excellent
    ## 609  (02) Very Good (02) Very Good
    ## 610  (02) Very Good (02) Very Good
    ## 611       (03) Good      (03) Good
    ## 612  (02) Very Good (02) Very Good
    ## 613  (02) Very Good (02) Very Good
    ## 614  (02) Very Good (02) Very Good
    ## 615       (03) Good (02) Very Good
    ## 616       (03) Good      (03) Good
    ## 617       (04) Fair (02) Very Good
    ## 618       (04) Fair      (03) Good
    ## 619  (02) Very Good (02) Very Good
    ## 620       (04) Fair      (03) Good
    ## 621       (03) Good (02) Very Good
    ## 622  (01) Excellent (01) Excellent
    ## 623  (02) Very Good (02) Very Good
    ## 624       (04) Fair      (03) Good
    ## 625       (03) Good      (03) Good
    ## 626  (02) Very Good (02) Very Good
    ## 627       (04) Fair (02) Very Good
    ## 628       (05) Poor (02) Very Good
    ## 629       (03) Good (02) Very Good
    ## 630  (02) Very Good (02) Very Good
    ## 631       (04) Fair (02) Very Good
    ## 632       (04) Fair (02) Very Good
    ## 633       (04) Fair (02) Very Good
    ## 634       (03) Good      (03) Good
    ## 635       (03) Good      (03) Good
    ## 636  (02) Very Good (01) Excellent
    ## 637       (04) Fair      (04) Fair
    ## 638       (03) Good      (03) Good
    ## 639       (04) Fair (02) Very Good
    ## 640       (03) Good (02) Very Good
    ## 641  (02) Very Good (01) Excellent
    ## 642  (02) Very Good (02) Very Good
    ## 643       (03) Good      (03) Good
    ## 644  (02) Very Good (02) Very Good
    ## 645       (03) Good      (03) Good
    ## 646       (05) Poor      (04) Fair
    ## 647       (03) Good      (03) Good
    ## 648       (03) Good (02) Very Good
    ## 649       (04) Fair      (03) Good
    ## 650       (03) Good (02) Very Good
    ## 651       (03) Good      (03) Good
    ## 652       (03) Good (02) Very Good
    ## 653       (03) Good (02) Very Good
    ## 654  (02) Very Good (02) Very Good
    ## 655  (02) Very Good (02) Very Good
    ## 656  (02) Very Good (02) Very Good
    ## 657       (03) Good (02) Very Good
    ## 658       (04) Fair (02) Very Good
    ## 659       (04) Fair      (03) Good
    ## 660       (03) Good (01) Excellent
    ## 661  (02) Very Good (02) Very Good
    ## 662  (02) Very Good (01) Excellent
    ## 663       (03) Good      (03) Good
    ## 664       (03) Good (02) Very Good
    ## 665       (03) Good        (98) DK
    ## 666  (02) Very Good (02) Very Good
    ## 667  (02) Very Good (02) Very Good
    ## 668  (02) Very Good (02) Very Good
    ## 669  (02) Very Good      (03) Good
    ## 670       (03) Good      (03) Good
    ## 671  (02) Very Good (02) Very Good
    ## 672       (03) Good      (03) Good
    ## 673       (03) Good      (04) Fair
    ## 674       (04) Fair      (03) Good
    ## 675       (03) Good      (03) Good
    ## 676  (02) Very Good (02) Very Good
    ## 677       (03) Good (02) Very Good
    ## 678  (02) Very Good      (03) Good
    ## 679  (02) Very Good      (04) Fair
    ## 680  (02) Very Good      (04) Fair
    ## 681  (02) Very Good (02) Very Good
    ## 682  (02) Very Good (02) Very Good
    ## 683  (02) Very Good (02) Very Good
    ## 684       (03) Good (02) Very Good
    ## 685  (02) Very Good (02) Very Good
    ## 686       (03) Good (01) Excellent
    ## 687       (04) Fair      (04) Fair
    ## 688  (02) Very Good (02) Very Good
    ## 689  (02) Very Good (02) Very Good
    ## 690       (04) Fair      (03) Good
    ## 691       (03) Good      (03) Good
    ## 692       (03) Good (02) Very Good
    ## 693       (03) Good (02) Very Good
    ## 694       (04) Fair      (05) Poor
    ## 695  (02) Very Good (02) Very Good
    ## 696       (03) Good (01) Excellent
    ## 697       (03) Good (02) Very Good
    ## 698  (01) Excellent (01) Excellent
    ## 699       (03) Good      (03) Good
    ## 700  (01) Excellent (01) Excellent
    ## 701  (02) Very Good (02) Very Good
    ## 702  (02) Very Good (02) Very Good
    ## 703  (02) Very Good (02) Very Good
    ## 704  (01) Excellent (01) Excellent
    ## 705  (02) Very Good (02) Very Good
    ## 706       (04) Fair (02) Very Good
    ## 707  (01) Excellent (01) Excellent
    ## 708       (03) Good      (03) Good
    ## 709       (04) Fair      (03) Good
    ## 710  (01) Excellent (01) Excellent
    ## 711  (01) Excellent (01) Excellent
    ## 712  (02) Very Good      (03) Good
    ## 713  (01) Excellent (01) Excellent
    ## 714       (03) Good (02) Very Good
    ## 715       (03) Good (02) Very Good
    ## 716  (02) Very Good (02) Very Good
    ## 717  (02) Very Good (01) Excellent
    ## 718       (03) Good      (04) Fair
    ## 719       (03) Good      (04) Fair
    ## 720       (03) Good (02) Very Good
    ## 721       (03) Good      (03) Good
    ## 722  (02) Very Good (02) Very Good
    ## 723  (01) Excellent (01) Excellent
    ## 724       (03) Good      (03) Good
    ## 725  (02) Very Good (02) Very Good
    ## 726       (04) Fair      (03) Good
    ## 727       (03) Good (01) Excellent
    ## 728  (02) Very Good (01) Excellent
    ## 729       (04) Fair      (04) Fair
    ## 730  (02) Very Good      (04) Fair
    ## 731       (03) Good      (03) Good
    ## 732       (03) Good      (03) Good
    ## 733  (02) Very Good      (03) Good
    ## 734       (03) Good      (03) Good
    ## 735  (01) Excellent (01) Excellent
    ## 736  (01) Excellent (01) Excellent
    ## 737  (02) Very Good (02) Very Good
    ## 738  (01) Excellent (01) Excellent
    ## 739       (04) Fair      (05) Poor
    ## 740  (02) Very Good (02) Very Good
    ## 741  (02) Very Good (02) Very Good
    ## 742       (03) Good      (03) Good
    ## 743       (03) Good (02) Very Good
    ## 744       (03) Good (02) Very Good
    ## 745       (04) Fair (02) Very Good
    ## 746       (03) Good (02) Very Good
    ## 747       (03) Good      (03) Good
    ## 748  (02) Very Good (02) Very Good
    ## 749       (03) Good (02) Very Good
    ## 750  (02) Very Good (02) Very Good
    ## 751  (02) Very Good (02) Very Good
    ## 752  (01) Excellent (02) Very Good
    ## 753       (03) Good (02) Very Good
    ## 754       (05) Poor      (04) Fair
    ## 755       (04) Fair      (04) Fair
    ## 756       (04) Fair      (04) Fair
    ## 757       (03) Good      (04) Fair
    ## 758  (02) Very Good (02) Very Good
    ## 759  (02) Very Good (02) Very Good
    ## 760  (01) Excellent (01) Excellent
    ## 761  (01) Excellent (01) Excellent
    ## 762       (03) Good      (04) Fair
    ## 763       (04) Fair      (03) Good
    ## 764       (03) Good      (03) Good
    ## 765  (01) Excellent (01) Excellent
    ## 766  (02) Very Good (02) Very Good
    ## 767  (02) Very Good (02) Very Good
    ## 768  (01) Excellent (01) Excellent
    ## 769       (03) Good      (03) Good
    ## 770       (03) Good      (03) Good
    ## 771  (02) Very Good (02) Very Good
    ## 772       (03) Good (02) Very Good
    ## 773       (03) Good (02) Very Good
    ## 774       (04) Fair      (03) Good
    ## 775  (02) Very Good (02) Very Good
    ## 776  (02) Very Good (02) Very Good
    ## 777  (02) Very Good (02) Very Good
    ## 778  (02) Very Good (02) Very Good
    ## 779       (04) Fair      (04) Fair
    ## 780       (03) Good (02) Very Good
    ## 781       (03) Good (02) Very Good
    ## 782       (03) Good      (03) Good
    ## 783       (03) Good      (03) Good
    ## 784  (02) Very Good (01) Excellent
    ## 785  (02) Very Good (02) Very Good
    ## 786       (04) Fair (02) Very Good
    ## 787  (02) Very Good (02) Very Good
    ## 788       (03) Good      (03) Good
    ## 789  (02) Very Good (02) Very Good
    ## 790       (03) Good (02) Very Good
    ## 791       (04) Fair (02) Very Good
    ## 792  (02) Very Good (02) Very Good
    ## 793       (03) Good (02) Very Good
    ## 794  (02) Very Good (01) Excellent
    ## 795       (04) Fair (02) Very Good
    ## 796       (03) Good (02) Very Good
    ## 797       (03) Good (02) Very Good
    ## 798  (02) Very Good (02) Very Good
    ## 799       (03) Good (02) Very Good
    ## 800       (03) Good (01) Excellent
    ## 801  (02) Very Good (02) Very Good
    ## 802       (03) Good      (03) Good
    ## 803  (02) Very Good      (03) Good
    ## 804       (03) Good      (03) Good
    ## 805       (03) Good      (03) Good
    ## 806       (04) Fair (02) Very Good
    ## 807  (02) Very Good (02) Very Good
    ## 808       (04) Fair (01) Excellent
    ## 809       (03) Good      (03) Good
    ## 810       (03) Good (02) Very Good
    ## 811       (03) Good (02) Very Good
    ## 812       (03) Good      (03) Good
    ## 813  (02) Very Good (02) Very Good
    ## 814       (03) Good (02) Very Good
    ## 815       (04) Fair      (03) Good
    ## 816  (01) Excellent (01) Excellent
    ## 817       (03) Good (01) Excellent
    ## 818       (03) Good      (04) Fair
    ## 819       (04) Fair      (03) Good
    ## 820       (03) Good (02) Very Good
    ## 821  (02) Very Good (02) Very Good
    ## 822       (03) Good (02) Very Good
    ## 823  (02) Very Good (02) Very Good
    ## 824       (03) Good      (03) Good
    ## 825       (03) Good      (03) Good
    ## 826  (02) Very Good (02) Very Good
    ## 827       (04) Fair      (04) Fair
    ## 828       (03) Good      (03) Good
    ## 829       (04) Fair      (03) Good
    ## 830       (04) Fair      (03) Good
    ## 831       (03) Good      (03) Good
    ## 832       (03) Good      (03) Good
    ## 833  (02) Very Good      (03) Good
    ## 834  (01) Excellent (01) Excellent
    ## 835  (02) Very Good      (03) Good
    ## 836       (03) Good (02) Very Good
    ## 837  (02) Very Good (02) Very Good
    ## 838       (03) Good      (03) Good
    ## 839  (01) Excellent (01) Excellent
    ## 840  (02) Very Good (01) Excellent
    ## 841  (01) Excellent (01) Excellent
    ## 842       (04) Fair      (03) Good
    ## 843  (02) Very Good      (03) Good
    ## 844  (02) Very Good (01) Excellent
    ## 845  (01) Excellent      (03) Good
    ## 846       (03) Good      (03) Good
    ## 847  (01) Excellent (02) Very Good
    ## 848       (03) Good      (03) Good
    ## 849  (02) Very Good (02) Very Good
    ## 850  (02) Very Good (02) Very Good
    ## 851  (02) Very Good (02) Very Good
    ## 852       (04) Fair      (03) Good
    ## 853       (03) Good      (03) Good
    ## 854  (02) Very Good (02) Very Good
    ## 855  (01) Excellent (01) Excellent
    ## 856  (01) Excellent (01) Excellent
    ## 857       (03) Good      (03) Good
    ## 858       (03) Good (02) Very Good
    ## 859       (03) Good      (03) Good
    ## 860       (03) Good      (03) Good
    ## 861       (05) Poor      (03) Good
    ## 862       (04) Fair (02) Very Good
    ## 863       (03) Good      (03) Good
    ## 864  (02) Very Good (02) Very Good
    ## 865       (03) Good      (03) Good
    ## 866  (02) Very Good (02) Very Good
    ## 867       (03) Good      (03) Good
    ## 868       (03) Good      (03) Good
    ## 869  (02) Very Good      (03) Good
    ## 870  (02) Very Good (02) Very Good
    ## 871       (03) Good (02) Very Good
    ## 872  (02) Very Good (01) Excellent
    ## 873  (02) Very Good (01) Excellent
    ## 874  (02) Very Good (01) Excellent
    ## 875  (02) Very Good (02) Very Good
    ## 876       (03) Good      (03) Good
    ## 877       (04) Fair      (03) Good
    ## 878  (02) Very Good (02) Very Good
    ## 879  (02) Very Good (02) Very Good
    ## 880       (04) Fair      (03) Good
    ## 881  (02) Very Good (02) Very Good
    ## 882  (01) Excellent (01) Excellent
    ## 883       (04) Fair      (03) Good
    ## 884       (03) Good      (03) Good
    ## 885       (03) Good      (03) Good
    ## 886  (02) Very Good (02) Very Good
    ## 887  (02) Very Good (02) Very Good
    ## 888       (04) Fair      (03) Good
    ## 889       (03) Good      (03) Good
    ## 890       (03) Good      (03) Good
    ## 891       (03) Good      (03) Good
    ## 892  (01) Excellent (02) Very Good
    ## 893  (02) Very Good      (03) Good
    ## 894  (02) Very Good (02) Very Good
    ## 895  (02) Very Good (01) Excellent
    ## 896  (02) Very Good      (03) Good
    ## 897       (03) Good      (03) Good
    ## 898       (04) Fair      (03) Good
    ## 899       (04) Fair      (04) Fair
    ## 900  (02) Very Good      (03) Good
    ## 901  (02) Very Good (02) Very Good
    ## 902       (03) Good      (03) Good
    ## 903       (03) Good      (04) Fair
    ## 904       (04) Fair (02) Very Good
    ## 905       (04) Fair      (04) Fair
    ## 906       (04) Fair      (04) Fair
    ## 907  (01) Excellent (01) Excellent
    ## 908  (01) Excellent      (03) Good
    ## 909       (04) Fair      (04) Fair
    ## 910  (01) Excellent (01) Excellent
    ## 911  (02) Very Good      (03) Good
    ## 912  (01) Excellent (01) Excellent
    ## 913  (02) Very Good      (03) Good
    ## 914       (04) Fair      (03) Good
    ## 915  (01) Excellent (01) Excellent
    ## 916  (01) Excellent (01) Excellent
    ## 917  (02) Very Good      (03) Good
    ## 918       (03) Good      (03) Good
    ## 919       (03) Good (02) Very Good
    ## 920       (04) Fair      (04) Fair
    ## 921       (03) Good      (03) Good
    ## 922  (02) Very Good (02) Very Good
    ## 923  (02) Very Good      (04) Fair
    ## 924       (04) Fair (02) Very Good
    ## 925       (03) Good      (03) Good
    ## 926  (02) Very Good (02) Very Good
    ## 927  (01) Excellent (01) Excellent
    ## 928       (03) Good (02) Very Good
    ## 929  (01) Excellent (01) Excellent
    ## 930       (03) Good (02) Very Good
    ## 931  (02) Very Good (02) Very Good
    ## 932  (02) Very Good (02) Very Good
    ## 933  (01) Excellent (01) Excellent
    ## 934       (03) Good      (03) Good
    ## 935  (02) Very Good (02) Very Good
    ## 936  (01) Excellent (01) Excellent
    ## 937       (04) Fair      (03) Good
    ## 938       (03) Good      (04) Fair
    ## 939       (03) Good      (03) Good
    ## 940       (03) Good      (03) Good
    ## 941       (03) Good      (03) Good
    ## 942  (02) Very Good (02) Very Good
    ## 943  (02) Very Good (02) Very Good
    ## 944  (02) Very Good      (03) Good
    ## 945       (03) Good      (03) Good
    ## 946  (02) Very Good (02) Very Good
    ## 947       (03) Good      (03) Good
    ## 948  (02) Very Good (02) Very Good
    ## 949       (03) Good      (03) Good
    ## 950  (02) Very Good (02) Very Good
    ## 951       (03) Good (02) Very Good
    ## 952  (01) Excellent (02) Very Good
    ## 953  (01) Excellent (01) Excellent
    ## 954  (01) Excellent (01) Excellent
    ## 955  (01) Excellent (01) Excellent
    ## 956       (03) Good      (03) Good
    ## 957  (01) Excellent (01) Excellent
    ## 958  (01) Excellent (01) Excellent
    ## 959       (03) Good (02) Very Good
    ## 960       (03) Good      (03) Good
    ## 961  (02) Very Good (01) Excellent
    ## 962  (02) Very Good      (03) Good
    ## 963       (05) Poor      (04) Fair
    ## 964       (03) Good (01) Excellent
    ## 965  (02) Very Good (02) Very Good
    ## 966       (04) Fair      (03) Good
    ## 967       (03) Good      (03) Good
    ## 968       (03) Good (02) Very Good
    ## 969       (03) Good (02) Very Good
    ## 970  (02) Very Good (02) Very Good
    ## 971       (03) Good (02) Very Good
    ## 972  (02) Very Good (02) Very Good
    ## 973  (02) Very Good (01) Excellent
    ## 974  (02) Very Good (01) Excellent
    ## 975  (02) Very Good (02) Very Good
    ## 976       (03) Good      (03) Good
    ## 977  (02) Very Good (01) Excellent
    ## 978  (01) Excellent (01) Excellent
    ## 979       (03) Good      (03) Good
    ## 980       (04) Fair (01) Excellent
    ## 981  (01) Excellent (01) Excellent
    ## 982  (01) Excellent (01) Excellent
    ## 983       (04) Fair (01) Excellent
    ## 984  (02) Very Good (02) Very Good
    ## 985       (03) Good (02) Very Good
    ## 986  (02) Very Good (01) Excellent
    ## 987  (02) Very Good (02) Very Good
    ## 988       (04) Fair      (03) Good
    ## 989       (04) Fair (02) Very Good
    ## 990  (02) Very Good (02) Very Good
    ## 991       (03) Good      (03) Good
    ## 992  (01) Excellent (01) Excellent
    ## 993       (03) Good (02) Very Good
    ## 994       (05) Poor      (04) Fair
    ## 995       (04) Fair      (03) Good
    ## 996  (02) Very Good (02) Very Good
    ## 997  (02) Very Good (02) Very Good
    ## 998  (02) Very Good (01) Excellent
    ## 999  (02) Very Good      (03) Good
    ## 1000      (04) Fair      (04) Fair
    ## 1001 (02) Very Good      (03) Good
    ## 1002      (03) Good      (03) Good
    ## 1003      (04) Fair (02) Very Good
    ## 1004      (05) Poor      (04) Fair
    ## 1005      (04) Fair      (03) Good
    ## 1006 (02) Very Good (02) Very Good
    ## 1007 (01) Excellent (01) Excellent
    ## 1008      (03) Good      (03) Good
    ## 1009      (04) Fair      (03) Good
    ## 1010      (04) Fair      (03) Good
    ## 1011      (04) Fair      (04) Fair
    ## 1012 (02) Very Good (02) Very Good
    ## 1013 (02) Very Good (02) Very Good
    ## 1014 (02) Very Good (02) Very Good
    ## 1015 (02) Very Good (02) Very Good
    ## 1016      (03) Good      (03) Good
    ## 1017 (02) Very Good (02) Very Good
    ## 1018      (03) Good      (03) Good
    ## 1019 (02) Very Good (02) Very Good
    ## 1020 (02) Very Good (02) Very Good
    ## 1021      (03) Good (02) Very Good
    ## 1022      (03) Good      (03) Good
    ## 1023 (02) Very Good (01) Excellent
    ## 1024      (03) Good (02) Very Good
    ## 1025      (03) Good (02) Very Good
    ## 1026      (03) Good      (03) Good
    ## 1027 (02) Very Good (02) Very Good
    ## 1028      (03) Good (01) Excellent
    ## 1029      (03) Good (02) Very Good
    ## 1030      (04) Fair      (03) Good
    ## 1031 (02) Very Good (01) Excellent
    ## 1032      (04) Fair      (03) Good
    ## 1033 (02) Very Good (01) Excellent
    ## 1034      (04) Fair (02) Very Good
    ## 1035 (02) Very Good (02) Very Good
    ## 1036      (04) Fair      (04) Fair
    ## 1037 (01) Excellent (01) Excellent
    ## 1038 (02) Very Good (02) Very Good
    ## 1039      (04) Fair      (03) Good
    ## 1040      (04) Fair (02) Very Good
    ## 1041 (02) Very Good (02) Very Good
    ## 1042 (02) Very Good (02) Very Good
    ## 1043 (01) Excellent (02) Very Good
    ## 1044 (02) Very Good (02) Very Good
    ## 1045 (02) Very Good (02) Very Good
    ## 1046      (04) Fair (02) Very Good
    ## 1047 (02) Very Good (02) Very Good
    ## 1048 (02) Very Good (02) Very Good
    ## 1049 (02) Very Good (02) Very Good
    ## 1050      (03) Good (02) Very Good
    ## 1051 (02) Very Good (02) Very Good
    ## 1052 (02) Very Good (02) Very Good
    ## 1053      (03) Good      (03) Good
    ## 1054      (04) Fair      (04) Fair
    ## 1055 (01) Excellent (01) Excellent
    ## 1056      (04) Fair      (03) Good
    ## 1057      (05) Poor      (03) Good
    ## 1058      (03) Good (01) Excellent
    ## 1059      (03) Good      (03) Good
    ## 1060 (02) Very Good (01) Excellent
    ## 1061 (02) Very Good (02) Very Good
    ## 1062 (02) Very Good (02) Very Good
    ## 1063 (01) Excellent (01) Excellent
    ## 1064      (04) Fair (02) Very Good
    ## 1065 (01) Excellent (01) Excellent
    ## 1066      (04) Fair (02) Very Good
    ## 1067 (02) Very Good      (03) Good
    ## 1068      (04) Fair (02) Very Good
    ## 1069      (04) Fair      (04) Fair
    ## 1070      (03) Good      (03) Good
    ## 1071      (04) Fair      (03) Good
    ## 1072 (01) Excellent (01) Excellent
    ## 1073 (01) Excellent      (03) Good
    ## 1074      (03) Good      (03) Good
    ## 1075 (02) Very Good (02) Very Good
    ## 1076 (02) Very Good (02) Very Good
    ## 1077 (01) Excellent (01) Excellent
    ## 1078 (02) Very Good      (04) Fair
    ## 1079 (02) Very Good (02) Very Good
    ## 1080 (02) Very Good (01) Excellent
    ## 1081 (02) Very Good (01) Excellent
    ## 1082 (01) Excellent (01) Excellent
    ## 1083      (04) Fair (02) Very Good
    ## 1084      (04) Fair      (04) Fair
    ## 1085 (02) Very Good (01) Excellent
    ## 1086 (02) Very Good (02) Very Good
    ## 1087      (03) Good (01) Excellent
    ## 1088      (03) Good (02) Very Good
    ## 1089 (01) Excellent (01) Excellent
    ## 1090 (01) Excellent (01) Excellent
    ## 1091      (03) Good      (03) Good
    ## 1092      (05) Poor (01) Excellent
    ## 1093 (02) Very Good      (03) Good
    ## 1094      (03) Good (02) Very Good
    ## 1095      (03) Good (02) Very Good
    ## 1096      (03) Good      (04) Fair
    ## 1097      (03) Good (02) Very Good
    ## 1098 (02) Very Good (02) Very Good
    ## 1099 (01) Excellent (01) Excellent
    ## 1100 (02) Very Good (01) Excellent
    ## 1101 (02) Very Good (02) Very Good
    ## 1102 (02) Very Good (02) Very Good
    ## 1103      (03) Good (01) Excellent
    ## 1104 (02) Very Good (02) Very Good
    ## 1105 (02) Very Good (02) Very Good
    ## 1106      (03) Good (02) Very Good
    ## 1107      (03) Good (02) Very Good
    ## 1108 (02) Very Good (01) Excellent
    ## 1109 (02) Very Good (01) Excellent
    ## 1110 (02) Very Good (02) Very Good
    ## 1111      (04) Fair      (04) Fair
    ## 1112 (02) Very Good      (04) Fair
    ## 1113      (05) Poor      (05) Poor
    ## 1114      (04) Fair (01) Excellent
    ## 1115      (04) Fair      (03) Good
    ## 1116      (04) Fair      (03) Good
    ## 1117 (01) Excellent (01) Excellent
    ## 1118 (01) Excellent (02) Very Good
    ## 1119      (04) Fair (02) Very Good
    ## 1120      (04) Fair (02) Very Good
    ## 1121      (03) Good      (03) Good
    ## 1122      (03) Good (02) Very Good
    ## 1123 (01) Excellent (01) Excellent
    ## 1124      (04) Fair      (03) Good
    ## 1125      (03) Good      (03) Good
    ## 1126 (02) Very Good      (04) Fair
    ## 1127 (02) Very Good (01) Excellent
    ## 1128      (03) Good (02) Very Good
    ## 1129      (03) Good      (03) Good
    ## 1130 (02) Very Good (01) Excellent
    ## 1131 (01) Excellent (01) Excellent
    ## 1132 (01) Excellent (01) Excellent
    ## 1133      (03) Good      (03) Good
    ## 1134 (01) Excellent (01) Excellent
    ## 1135 (02) Very Good      (03) Good
    ## 1136      (03) Good      (03) Good
    ## 1137      (03) Good      (03) Good
    ## 1138 (02) Very Good      (03) Good
    ## 1139 (02) Very Good (02) Very Good
    ## 1140 (02) Very Good (02) Very Good
    ## 1141 (02) Very Good      (03) Good
    ## 1142      (03) Good      (03) Good
    ## 1143      (05) Poor      (05) Poor
    ## 1144      (03) Good      (04) Fair
    ## 1145 (01) Excellent      (03) Good
    ## 1146 (02) Very Good (02) Very Good
    ## 1147      (05) Poor      (05) Poor
    ## 1148 (02) Very Good      (03) Good
    ## 1149      (03) Good      (03) Good
    ## 1150      (04) Fair      (03) Good
    ## 1151      (04) Fair      (04) Fair
    ## 1152 (01) Excellent (02) Very Good
    ## 1153 (02) Very Good      (03) Good
    ## 1154      (03) Good      (03) Good
    ## 1155      (03) Good      (03) Good
    ## 1156      (03) Good      (04) Fair
    ## 1157      (03) Good (02) Very Good
    ## 1158      (03) Good      (03) Good
    ## 1159      (05) Poor      (03) Good
    ## 1160      (04) Fair      (04) Fair
    ## 1161 (02) Very Good      (03) Good
    ## 1162 (02) Very Good (02) Very Good
    ## 1163 (02) Very Good      (03) Good
    ## 1164      (04) Fair      (03) Good
    ## 1165      (03) Good      (03) Good
    ## 1166      (03) Good      (04) Fair
    ## 1167      (04) Fair      (03) Good
    ## 1168 (02) Very Good (01) Excellent
    ## 1169 (01) Excellent (01) Excellent
    ## 1170      (03) Good      (03) Good
    ## 1171      (03) Good      (03) Good
    ## 1172 (02) Very Good (02) Very Good
    ## 1173 (02) Very Good (02) Very Good
    ## 1174      (03) Good (02) Very Good
    ## 1175 (02) Very Good      (03) Good
    ## 1176 (02) Very Good (02) Very Good
    ## 1177 (02) Very Good (02) Very Good
    ## 1178 (02) Very Good (02) Very Good
    ## 1179 (02) Very Good (02) Very Good
    ## 1180 (02) Very Good      (04) Fair
    ## 1181      (03) Good (02) Very Good
    ## 1182 (02) Very Good (02) Very Good
    ## 1183 (01) Excellent (02) Very Good
    ## 1184 (02) Very Good (02) Very Good
    ## 1185      (03) Good      (03) Good
    ## 1186      (04) Fair      (03) Good
    ## 1187      (04) Fair      (03) Good
    ## 1188      (03) Good (02) Very Good
    ## 1189      (03) Good      (03) Good
    ## 1190      (03) Good      (03) Good
    ## 1191 (02) Very Good (02) Very Good
    ## 1192 (01) Excellent (01) Excellent
    ## 1193 (02) Very Good (02) Very Good
    ## 1194 (01) Excellent      (03) Good
    ## 1195 (01) Excellent (01) Excellent
    ## 1196 (02) Very Good (02) Very Good
    ## 1197 (02) Very Good (02) Very Good
    ## 1198      (04) Fair (02) Very Good
    ## 1199 (01) Excellent (01) Excellent
    ## 1200 (02) Very Good (02) Very Good
    ## 1201 (02) Very Good (02) Very Good
    ## 1202      (03) Good      (03) Good
    ## 1203 (02) Very Good (02) Very Good
    ## 1204 (02) Very Good (02) Very Good
    ## 1205      (03) Good      (04) Fair
    ## 1206 (02) Very Good (02) Very Good
    ## 1207      (03) Good      (03) Good
    ## 1208      (03) Good      (03) Good
    ## 1209      (03) Good      (03) Good
    ## 1210 (02) Very Good (01) Excellent
    ## 1211      (04) Fair      (04) Fair
    ## 1212 (01) Excellent (02) Very Good
    ## 1213      (04) Fair      (03) Good
    ## 1214 (02) Very Good (02) Very Good
    ## 1215 (02) Very Good (01) Excellent
    ## 1216      (03) Good      (03) Good
    ## 1217 (02) Very Good (02) Very Good
    ## 1218 (02) Very Good (02) Very Good
    ## 1219 (02) Very Good      (03) Good
    ## 1220      (05) Poor      (03) Good
    ## 1221      (03) Good      (03) Good
    ## 1222 (02) Very Good      (03) Good
    ## 1223      (05) Poor (02) Very Good
    ## 1224 (02) Very Good (02) Very Good
    ## 1225      (04) Fair      (04) Fair
    ## 1226      (03) Good      (03) Good
    ## 1227      (03) Good      (03) Good
    ## 1228      (03) Good      (04) Fair
    ## 1229 (02) Very Good (02) Very Good
    ## 1230 (02) Very Good (02) Very Good
    ## 1231 (02) Very Good (02) Very Good
    ## 1232      (04) Fair (02) Very Good
    ## 1233 (02) Very Good (02) Very Good
    ## 1234      (03) Good      (03) Good
    ## 1235      (03) Good      (04) Fair
    ## 1236 (02) Very Good (02) Very Good
    ## 1237 (02) Very Good (01) Excellent
    ## 1238      (03) Good      (04) Fair
    ## 1239 (02) Very Good (02) Very Good
    ## 1240      (03) Good      (03) Good
    ## 1241 (02) Very Good (02) Very Good
    ## 1242      (03) Good (01) Excellent
    ## 1243      (03) Good      (03) Good
    ## 1244 (02) Very Good (02) Very Good
    ## 1245 (02) Very Good (02) Very Good
    ## 1246 (01) Excellent (01) Excellent
    ## 1247      (03) Good      (03) Good
    ## 1248      (05) Poor      (05) Poor
    ## 1249      (03) Good      (03) Good
    ## 1250      (05) Poor      (03) Good
    ## 1251      (03) Good      (03) Good
    ## 1252 (01) Excellent (01) Excellent
    ## 1253 (02) Very Good (02) Very Good
    ## 1254      (03) Good      (03) Good
    ## 1255 (02) Very Good (02) Very Good
    ## 1256 (02) Very Good      (03) Good
    ## 1257 (02) Very Good (02) Very Good
    ## 1258 (02) Very Good (02) Very Good
    ## 1259      (03) Good      (03) Good
    ## 1260 (01) Excellent (01) Excellent
    ## 1261      (03) Good      (03) Good
    ## 1262      (03) Good      (03) Good
    ## 1263      (04) Fair      (03) Good
    ## 1264 (02) Very Good (02) Very Good
    ## 1265 (02) Very Good (02) Very Good
    ## 1266      (04) Fair      (03) Good
    ## 1267 (02) Very Good      (03) Good
    ## 1268 (02) Very Good      (03) Good
    ## 1269 (01) Excellent (02) Very Good
    ## 1270 (02) Very Good (02) Very Good
    ## 1271 (02) Very Good (02) Very Good
    ## 1272      (04) Fair      (03) Good
    ## 1273 (02) Very Good (02) Very Good
    ## 1274      (03) Good      (03) Good
    ## 1275 (02) Very Good      (03) Good
    ## 1276 (01) Excellent (02) Very Good
    ## 1277      (04) Fair      (03) Good
    ## 1278      (03) Good      (03) Good
    ## 1279      (03) Good      (03) Good
    ## 1280      (04) Fair      (03) Good
    ## 1281      (04) Fair      (03) Good
    ## 1282 (01) Excellent      (03) Good
    ## 1283 (02) Very Good      (03) Good
    ## 1284 (01) Excellent (01) Excellent
    ## 1285 (02) Very Good      (03) Good
    ## 1286 (02) Very Good (02) Very Good
    ## 1287      (03) Good      (03) Good
    ## 1288      (05) Poor      (03) Good
    ## 1289      (04) Fair      (03) Good
    ## 1290      (03) Good      (03) Good
    ## 1291      (03) Good (01) Excellent
    ## 1292      (03) Good (02) Very Good
    ## 1293      (05) Poor      (04) Fair
    ## 1294      (05) Poor      (04) Fair
    ## 1295 (02) Very Good (01) Excellent
    ## 1296      (03) Good      (03) Good
    ## 1297 (02) Very Good (02) Very Good
    ## 1298 (02) Very Good (02) Very Good
    ## 1299      (03) Good      (03) Good
    ## 1300      (03) Good (02) Very Good
    ## 1301 (01) Excellent (01) Excellent
    ## 1302      (04) Fair      (04) Fair
    ## 1303      (03) Good (02) Very Good
    ## 1304 (02) Very Good (02) Very Good
    ## 1305 (02) Very Good      (03) Good
    ## 1306 (01) Excellent (01) Excellent
    ## 1307      (04) Fair      (03) Good
    ## 1308 (02) Very Good (01) Excellent
    ## 1309      (04) Fair      (04) Fair
    ## 1310      (03) Good (02) Very Good
    ## 1311 (01) Excellent (01) Excellent
    ## 1312 (01) Excellent (02) Very Good
    ## 1313      (04) Fair      (03) Good
    ## 1314 (02) Very Good      (03) Good
    ## 1315 (01) Excellent (01) Excellent
    ## 1316      (04) Fair (01) Excellent
    ## 1317      (04) Fair (02) Very Good
    ## 1318 (02) Very Good (02) Very Good
    ## 1319      (03) Good      (03) Good
    ## 1320 (02) Very Good (02) Very Good
    ## 1321      (03) Good (02) Very Good
    ## 1322      (03) Good (02) Very Good
    ## 1323 (02) Very Good (02) Very Good
    ## 1324 (02) Very Good (02) Very Good
    ## 1325 (02) Very Good (01) Excellent
    ## 1326 (01) Excellent (01) Excellent
    ## 1327      (03) Good (01) Excellent
    ## 1328      (04) Fair      (03) Good
    ## 1329      (04) Fair (01) Excellent
    ## 1330 (01) Excellent (02) Very Good
    ## 1331      (03) Good      (03) Good
    ## 1332 (02) Very Good (02) Very Good
    ## 1333 (02) Very Good (01) Excellent
    ## 1334 (01) Excellent (01) Excellent
    ## 1335 (02) Very Good (02) Very Good
    ## 1336 (02) Very Good (02) Very Good
    ## 1337 (02) Very Good      (03) Good
    ## 1338      (03) Good (01) Excellent
    ## 1339      (03) Good      (03) Good
    ## 1340 (02) Very Good (02) Very Good
    ## 1341      (03) Good      (03) Good
    ## 1342      (04) Fair      (03) Good
    ## 1343 (01) Excellent (01) Excellent
    ## 1344 (01) Excellent (01) Excellent
    ## 1345      (03) Good      (03) Good
    ## 1346 (02) Very Good (01) Excellent
    ## 1347      (05) Poor (02) Very Good
    ## 1348 (01) Excellent (01) Excellent
    ## 1349      (04) Fair (02) Very Good
    ## 1350      (03) Good (02) Very Good
    ## 1351 (01) Excellent (02) Very Good
    ## 1352      (03) Good (02) Very Good
    ## 1353      (03) Good (02) Very Good
    ## 1354 (02) Very Good (02) Very Good
    ## 1355      (04) Fair      (03) Good
    ## 1356      (04) Fair      (03) Good
    ## 1357 (02) Very Good (02) Very Good
    ## 1358 (01) Excellent (02) Very Good
    ## 1359 (02) Very Good (02) Very Good
    ## 1360      (03) Good      (03) Good
    ## 1361      (03) Good      (03) Good
    ## 1362      (03) Good      (05) Poor
    ## 1363      (03) Good      (03) Good
    ## 1364      (04) Fair      (03) Good
    ## 1365      (03) Good      (03) Good
    ## 1366 (02) Very Good (02) Very Good
    ## 1367 (01) Excellent (01) Excellent
    ## 1368 (01) Excellent (01) Excellent
    ## 1369 (02) Very Good (02) Very Good
    ## 1370 (02) Very Good (02) Very Good
    ## 1371      (03) Good      (03) Good
    ## 1372      (03) Good      (03) Good
    ## 1373 (02) Very Good (02) Very Good
    ## 1374 (02) Very Good      (04) Fair
    ## 1375      (03) Good      (03) Good
    ## 1376 (02) Very Good      (03) Good
    ## 1377      (04) Fair (02) Very Good
    ## 1378 (02) Very Good (02) Very Good
    ## 1379      (04) Fair      (03) Good
    ## 1380 (02) Very Good      (03) Good
    ## 1381 (02) Very Good (02) Very Good
    ## 1382 (02) Very Good (02) Very Good
    ## 1383 (02) Very Good (02) Very Good
    ## 1384 (02) Very Good (01) Excellent
    ## 1385 (01) Excellent (02) Very Good
    ## 1386      (05) Poor      (04) Fair
    ## 1387      (03) Good      (04) Fair
    ## 1388 (02) Very Good (01) Excellent
    ## 1389 (02) Very Good (02) Very Good
    ## 1390 (02) Very Good      (03) Good
    ## 1391      (03) Good (02) Very Good
    ## 1392 (02) Very Good (01) Excellent
    ## 1393      (03) Good (02) Very Good
    ## 1394      (03) Good (02) Very Good
    ## 1395 (01) Excellent (01) Excellent
    ## 1396      (03) Good      (03) Good
    ## 1397 (02) Very Good (02) Very Good
    ## 1398      (03) Good (01) Excellent
    ## 1399 (02) Very Good (02) Very Good
    ## 1400 (02) Very Good (02) Very Good
    ## 1401 (01) Excellent      (03) Good
    ## 1402 (02) Very Good      (03) Good
    ## 1403      (03) Good (02) Very Good
    ## 1404      (03) Good      (03) Good
    ## 1405 (02) Very Good (02) Very Good
    ## 1406 (02) Very Good (02) Very Good
    ## 1407      (03) Good (02) Very Good
    ## 1408 (01) Excellent (01) Excellent
    ## 1409 (02) Very Good (02) Very Good
    ## 1410 (02) Very Good (02) Very Good
    ## 1411      (03) Good (02) Very Good
    ## 1412      (03) Good      (03) Good
    ## 1413      (04) Fair (02) Very Good
    ## 1414 (01) Excellent (01) Excellent
    ## 1415      (03) Good      (03) Good
    ## 1416      (03) Good (01) Excellent
    ## 1417      (03) Good      (03) Good
    ## 1418 (02) Very Good (02) Very Good
    ## 1419      (04) Fair      (03) Good
    ## 1420 (02) Very Good (01) Excellent
    ## 1421 (01) Excellent (02) Very Good
    ## 1422 (02) Very Good (01) Excellent
    ## 1423 (02) Very Good      (03) Good
    ## 1424 (02) Very Good (02) Very Good
    ## 1425 (02) Very Good      (03) Good
    ## 1426      (04) Fair (02) Very Good
    ## 1427      (03) Good      (03) Good
    ## 1428 (02) Very Good (02) Very Good
    ## 1429 (02) Very Good (01) Excellent
    ## 1430 (01) Excellent (01) Excellent
    ## 1431 (01) Excellent (01) Excellent
    ## 1432      (03) Good      (03) Good
    ## 1433      (03) Good      (03) Good
    ## 1434 (02) Very Good (02) Very Good
    ## 1435 (01) Excellent (01) Excellent
    ## 1436 (02) Very Good (01) Excellent
    ## 1437      (03) Good (02) Very Good
    ## 1438 (02) Very Good (02) Very Good
    ## 1439 (02) Very Good (02) Very Good
    ## 1440 (01) Excellent (01) Excellent
    ## 1441 (02) Very Good      (03) Good
    ## 1442      (03) Good (01) Excellent
    ## 1443 (01) Excellent      (03) Good
    ## 1444      (03) Good      (03) Good
    ## 1445 (02) Very Good (02) Very Good
    ## 1446      (03) Good (02) Very Good
    ## 1447      (04) Fair      (04) Fair
    ## 1448      (03) Good      (03) Good
    ## 1449 (02) Very Good (02) Very Good
    ## 1450      (04) Fair      (03) Good
    ## 1451 (01) Excellent (01) Excellent
    ## 1452 (02) Very Good (01) Excellent
    ## 1453 (02) Very Good (01) Excellent
    ## 1454 (01) Excellent (01) Excellent
    ## 1455 (01) Excellent (01) Excellent
    ## 1456 (02) Very Good (02) Very Good
    ## 1457      (03) Good (02) Very Good
    ## 1458 (02) Very Good      (03) Good
    ## 1459      (04) Fair      (04) Fair
    ## 1460 (02) Very Good (02) Very Good
    ## 1461 (02) Very Good (02) Very Good
    ## 1462 (02) Very Good (02) Very Good
    ## 1463 (02) Very Good (02) Very Good
    ## 1464 (01) Excellent (01) Excellent
    ## 1465 (02) Very Good (02) Very Good
    ## 1466      (04) Fair      (03) Good
    ## 1467      (04) Fair      (03) Good
    ## 1468      (03) Good      (03) Good
    ## 1469      (04) Fair (01) Excellent
    ## 1470 (02) Very Good (02) Very Good
    ## 1471      (03) Good (02) Very Good
    ## 1472      (04) Fair      (03) Good
    ## 1473      (03) Good (02) Very Good
    ## 1474 (02) Very Good (02) Very Good
    ## 1475      (04) Fair (01) Excellent
    ## 1476 (02) Very Good (01) Excellent
    ## 1477 (02) Very Good (01) Excellent
    ## 1478      (03) Good      (03) Good
    ## 1479 (02) Very Good (02) Very Good
    ## 1480 (01) Excellent (01) Excellent
    ## 1481      (04) Fair (01) Excellent
    ## 1482 (01) Excellent (01) Excellent
    ## 1483      (03) Good      (04) Fair
    ## 1484 (02) Very Good (02) Very Good
    ## 1485      (04) Fair      (03) Good
    ## 1486      (04) Fair      (03) Good
    ## 1487 (02) Very Good (02) Very Good
    ## 1488      (03) Good (02) Very Good
    ## 1489      (05) Poor      (04) Fair
    ## 1490 (02) Very Good (02) Very Good
    ## 1491 (01) Excellent (01) Excellent
    ## 1492 (02) Very Good (02) Very Good
    ## 1493 (02) Very Good      (03) Good
    ## 1494      (03) Good      (03) Good
    ## 1495      (03) Good (02) Very Good
    ## 1496      (04) Fair (02) Very Good
    ## 1497 (02) Very Good      (04) Fair
    ## 1498      (04) Fair      (03) Good
    ## 1499      (04) Fair      (03) Good
    ## 1500      (04) Fair (02) Very Good
    ## 1501 (01) Excellent (01) Excellent
    ## 1502 (02) Very Good      (03) Good
    ## 1503 (02) Very Good (02) Very Good
    ## 1504 (02) Very Good (02) Very Good
    ## 1505 (02) Very Good (01) Excellent
    ## 1506      (05) Poor      (04) Fair
    ## 1507      (04) Fair      (03) Good
    ## 1508      (04) Fair      (04) Fair
    ## 1509 (01) Excellent (01) Excellent
    ## 1510 (02) Very Good (01) Excellent
    ## 1511 (02) Very Good (02) Very Good
    ## 1512      (03) Good      (03) Good
    ## 1513 (02) Very Good (02) Very Good
    ## 1514 (02) Very Good (01) Excellent
    ## 1515 (02) Very Good (02) Very Good
    ## 1516      (03) Good (02) Very Good
    ## 1517      (04) Fair (02) Very Good
    ## 1518 (02) Very Good (02) Very Good
    ## 1519 (02) Very Good (01) Excellent
    ## 1520 (02) Very Good (01) Excellent
    ## 1521 (02) Very Good (02) Very Good
    ## 1522 (02) Very Good      (03) Good
    ## 1523 (01) Excellent      (03) Good
    ## 1524      (03) Good      (03) Good
    ## 1525      (03) Good      (03) Good
    ## 1526      (03) Good (01) Excellent
    ## 1527 (02) Very Good      (03) Good
    ## 1528      (03) Good      (03) Good
    ## 1529      (03) Good      (03) Good
    ## 1530      (03) Good      (03) Good
    ## 1531      (03) Good      (03) Good
    ## 1532 (02) Very Good (02) Very Good
    ## 1533 (01) Excellent (01) Excellent
    ## 1534 (02) Very Good (02) Very Good
    ## 1535 (02) Very Good (02) Very Good
    ## 1536 (02) Very Good (01) Excellent
    ## 1537 (02) Very Good (02) Very Good
    ## 1538 (01) Excellent (01) Excellent
    ## 1539      (03) Good (02) Very Good
    ## 1540      (03) Good      (03) Good
    ## 1541 (01) Excellent (01) Excellent
    ## 1542 (02) Very Good (02) Very Good
    ## 1543 (01) Excellent      (03) Good
    ## 1544 (02) Very Good (02) Very Good
    ## 1545 (02) Very Good (02) Very Good
    ## 1546      (03) Good      (03) Good
    ## 1547 (02) Very Good (02) Very Good
    ## 1548      (03) Good      (03) Good
    ## 1549      (03) Good      (03) Good
    ## 1550 (02) Very Good (02) Very Good
    ## 1551 (02) Very Good (02) Very Good
    ## 1552      (03) Good      (03) Good
    ## 1553      (03) Good      (03) Good
    ## 1554 (02) Very Good (01) Excellent
    ## 1555      (03) Good      (03) Good
    ## 1556 (02) Very Good (02) Very Good
    ## 1557 (01) Excellent (02) Very Good
    ## 1558 (02) Very Good (02) Very Good
    ## 1559 (02) Very Good (02) Very Good
    ## 1560 (02) Very Good (02) Very Good
    ## 1561      (03) Good      (03) Good
    ## 1562 (02) Very Good (02) Very Good
    ## 1563 (01) Excellent (01) Excellent
    ## 1564 (01) Excellent (01) Excellent
    ## 1565 (02) Very Good (01) Excellent
    ## 1566 (02) Very Good (02) Very Good
    ## 1567      (05) Poor      (04) Fair
    ## 1568      (03) Good      (03) Good
    ## 1569      (04) Fair      (03) Good
    ## 1570      (03) Good      (03) Good
    ## 1571      (03) Good      (03) Good
    ## 1572      (03) Good (01) Excellent
    ## 1573      (04) Fair      (03) Good
    ## 1574 (02) Very Good      (03) Good
    ## 1575 (01) Excellent (01) Excellent
    ## 1576      (03) Good (01) Excellent
    ## 1577 (02) Very Good (02) Very Good
    ## 1578      (04) Fair      (03) Good
    ## 1579 (02) Very Good      (03) Good
    ## 1580 (02) Very Good (02) Very Good
    ## 1581 (02) Very Good (02) Very Good
    ## 1582 (02) Very Good (01) Excellent
    ## 1583 (01) Excellent      (05) Poor
    ## 1584      (04) Fair      (04) Fair
    ## 1585      (04) Fair      (04) Fair
    ## 1586      (03) Good      (03) Good
    ## 1587      (03) Good      (03) Good
    ## 1588 (02) Very Good (02) Very Good
    ## 1589 (02) Very Good (02) Very Good
    ## 1590      (04) Fair (01) Excellent
    ## 1591 (02) Very Good (02) Very Good
    ## 1592      (03) Good (02) Very Good
    ## 1593 (02) Very Good (02) Very Good
    ## 1594      (05) Poor      (04) Fair
    ## 1595      (04) Fair      (03) Good
    ## 1596 (01) Excellent (01) Excellent
    ## 1597      (03) Good      (03) Good
    ## 1598      (04) Fair      (03) Good
    ## 1599      (05) Poor      (04) Fair
    ## 1600      (03) Good      (03) Good
    ## 1601      (03) Good      (03) Good
    ## 1602      (03) Good      (03) Good
    ## 1603      (05) Poor (02) Very Good
    ## 1604      (04) Fair      (03) Good
    ## 1605      (03) Good (02) Very Good
    ## 1606      (04) Fair      (04) Fair
    ## 1607      (04) Fair      (03) Good
    ## 1608      (05) Poor      (05) Poor
    ## 1609      (04) Fair (02) Very Good
    ## 1610      (03) Good      (03) Good
    ## 1611 (01) Excellent (01) Excellent
    ## 1612 (02) Very Good (02) Very Good
    ## 1613      (05) Poor      (04) Fair
    ## 1614      (04) Fair      (03) Good
    ## 1615 (02) Very Good (02) Very Good
    ## 1616      (03) Good      (03) Good
    ## 1617      (03) Good      (03) Good
    ## 1618      (04) Fair      (04) Fair
    ## 1619 (02) Very Good (02) Very Good
    ## 1620 (02) Very Good (02) Very Good
    ## 1621      (03) Good (02) Very Good
    ## 1622      (03) Good      (03) Good
    ## 1623 (01) Excellent (01) Excellent
    ## 1624 (02) Very Good (02) Very Good
    ## 1625      (05) Poor      (03) Good
    ## 1626 (01) Excellent (01) Excellent
    ## 1627 (02) Very Good      (03) Good
    ## 1628      (04) Fair      (03) Good
    ## 1629      (04) Fair      (03) Good
    ## 1630 (02) Very Good (02) Very Good
    ## 1631      (03) Good (02) Very Good
    ## 1632      (03) Good      (03) Good
    ## 1633 (01) Excellent (01) Excellent
    ## 1634 (02) Very Good (02) Very Good
    ## 1635 (02) Very Good (02) Very Good
    ## 1636 (02) Very Good (02) Very Good
    ## 1637      (04) Fair      (04) Fair
    ## 1638      (03) Good      (03) Good
    ## 1639      (03) Good      (03) Good
    ## 1640      (03) Good      (03) Good
    ## 1641      (03) Good      (03) Good
    ## 1642      (03) Good (02) Very Good
    ## 1643      (03) Good      (03) Good
    ## 1644      (05) Poor (02) Very Good
    ## 1645      (03) Good      (03) Good
    ## 1646 (01) Excellent (01) Excellent
    ## 1647 (02) Very Good (02) Very Good
    ## 1648      (04) Fair      (04) Fair
    ## 1649      (03) Good (02) Very Good
    ## 1650 (01) Excellent (01) Excellent
    ## 1651 (02) Very Good (01) Excellent
    ## 1652      (03) Good      (03) Good
    ## 1653 (02) Very Good (01) Excellent
    ## 1654 (02) Very Good (02) Very Good
    ## 1655      (03) Good      (03) Good
    ## 1656      (04) Fair      (03) Good
    ## 1657      (04) Fair      (04) Fair
    ## 1658      (04) Fair      (04) Fair
    ## 1659 (02) Very Good      (03) Good
    ## 1660 (02) Very Good (02) Very Good
    ## 1661      (05) Poor      (05) Poor
    ## 1662 (02) Very Good (02) Very Good
    ## 1663      (03) Good      (03) Good
    ## 1664 (02) Very Good (02) Very Good
    ## 1665      (03) Good (02) Very Good
    ## 1666      (04) Fair (02) Very Good
    ## 1667 (01) Excellent (01) Excellent
    ## 1668      (04) Fair      (03) Good
    ## 1669      (03) Good      (03) Good
    ## 1670      (04) Fair      (03) Good
    ## 1671      (03) Good      (03) Good
    ## 1672      (03) Good      (03) Good
    ## 1673      (03) Good      (03) Good
    ## 1674      (03) Good (02) Very Good
    ## 1675 (02) Very Good (02) Very Good
    ## 1676 (01) Excellent (01) Excellent
    ## 1677 (02) Very Good (02) Very Good
    ## 1678      (03) Good      (03) Good
    ## 1679      (04) Fair      (03) Good
    ## 1680 (02) Very Good (02) Very Good
    ## 1681 (02) Very Good (02) Very Good
    ## 1682 (02) Very Good (02) Very Good
    ## 1683      (03) Good (02) Very Good
    ## 1684      (03) Good      (03) Good
    ## 1685      (04) Fair      (03) Good
    ## 1686      (04) Fair      (04) Fair
    ## 1687      (03) Good      (04) Fair
    ## 1688 (01) Excellent (01) Excellent
    ## 1689 (02) Very Good (02) Very Good
    ## 1690      (04) Fair (02) Very Good
    ## 1691 (02) Very Good (02) Very Good
    ## 1692      (03) Good      (03) Good
    ## 1693      (03) Good      (03) Good
    ## 1694      (03) Good      (03) Good
    ## 1695 (02) Very Good (02) Very Good
    ## 1696 (02) Very Good      (03) Good
    ## 1697      (04) Fair      (03) Good
    ## 1698      (03) Good      (03) Good
    ## 1699      (03) Good (02) Very Good
    ## 1700 (02) Very Good (02) Very Good
    ## 1701 (01) Excellent (01) Excellent
    ## 1702 (01) Excellent (01) Excellent
    ## 1703 (02) Very Good (02) Very Good
    ## 1704      (03) Good (02) Very Good
    ## 1705      (04) Fair      (04) Fair
    ## 1706      (04) Fair      (03) Good
    ## 1707 (02) Very Good (02) Very Good
    ## 1708      (04) Fair (02) Very Good
    ## 1709 (02) Very Good (02) Very Good
    ## 1710      (03) Good      (03) Good
    ## 1711      (03) Good      (03) Good
    ## 1712      (04) Fair      (04) Fair
    ## 1713      (03) Good (02) Very Good
    ## 1714      (05) Poor      (05) Poor
    ## 1715      (03) Good      (03) Good
    ## 1716      (04) Fair (01) Excellent
    ## 1717 (02) Very Good      (03) Good
    ## 1718 (02) Very Good      (03) Good
    ## 1719 (02) Very Good (02) Very Good
    ## 1720      (03) Good      (03) Good
    ## 1721 (02) Very Good      (03) Good
    ## 1722      (03) Good (02) Very Good
    ## 1723      (03) Good      (03) Good
    ## 1724      (03) Good      (03) Good
    ## 1725      (03) Good      (03) Good
    ## 1726      (04) Fair      (03) Good
    ## 1727      (03) Good (02) Very Good
    ## 1728 (02) Very Good      (03) Good
    ## 1729 (02) Very Good (01) Excellent
    ## 1730 (02) Very Good      (03) Good
    ## 1731 (01) Excellent (01) Excellent
    ## 1732 (02) Very Good (02) Very Good
    ## 1733 (01) Excellent (01) Excellent
    ## 1734      (03) Good      (03) Good
    ## 1735      (03) Good      (03) Good
    ## 1736 (02) Very Good (02) Very Good
    ## 1737      (04) Fair      (03) Good
    ## 1738      (03) Good      (04) Fair
    ## 1739 (02) Very Good (01) Excellent
    ## 1740 (02) Very Good (02) Very Good
    ## 1741 (02) Very Good (02) Very Good
    ## 1742      (03) Good      (03) Good
    ## 1743      (03) Good      (03) Good
    ## 1744 (02) Very Good (02) Very Good
    ## 1745      (03) Good      (03) Good
    ## 1746 (02) Very Good      (03) Good
    ## 1747 (01) Excellent (01) Excellent
    ## 1748 (01) Excellent (01) Excellent
    ## 1749      (03) Good      (03) Good
    ## 1750      (03) Good      (03) Good
    ## 1751 (02) Very Good (02) Very Good
    ## 1752 (01) Excellent (01) Excellent
    ## 1753 (01) Excellent (01) Excellent
    ## 1754 (02) Very Good (02) Very Good
    ## 1755 (02) Very Good (02) Very Good
    ## 1756 (02) Very Good (02) Very Good
    ## 1757      (03) Good (01) Excellent
    ## 1758 (02) Very Good (02) Very Good
    ## 1759      (05) Poor      (04) Fair
    ## 1760      (04) Fair      (03) Good
    ## 1761      (03) Good      (03) Good
    ## 1762      (03) Good      (03) Good
    ## 1763 (02) Very Good (02) Very Good
    ## 1764      (04) Fair      (04) Fair
    ## 1765 (02) Very Good (02) Very Good
    ## 1766      (03) Good      (03) Good
    ## 1767 (02) Very Good (01) Excellent
    ## 1768      (04) Fair      (03) Good
    ## 1769      (03) Good      (03) Good
    ## 1770      (04) Fair      (04) Fair
    ## 1771      (03) Good      (03) Good
    ## 1772      (03) Good      (03) Good
    ## 1773      (03) Good      (03) Good
    ## 1774      (04) Fair      (03) Good
    ## 1775 (02) Very Good (02) Very Good
    ## 1776      (03) Good      (03) Good
    ## 1777 (02) Very Good      (03) Good
    ## 1778 (01) Excellent (01) Excellent
    ## 1779 (02) Very Good (02) Very Good
    ## 1780 (02) Very Good (02) Very Good
    ## 1781      (03) Good      (03) Good
    ## 1782      (03) Good (02) Very Good
    ## 1783      (04) Fair (01) Excellent
    ## 1784      (03) Good      (03) Good
    ## 1785      (03) Good      (03) Good
    ## 1786      (03) Good (02) Very Good
    ## 1787      (04) Fair      (04) Fair
    ## 1788      (03) Good      (03) Good
    ## 1789 (02) Very Good (01) Excellent
    ## 1790 (02) Very Good      (03) Good
    ## 1791      (03) Good      (03) Good
    ## 1792      (03) Good      (03) Good
    ## 1793      (04) Fair      (03) Good
    ## 1794 (02) Very Good (02) Very Good
    ## 1795 (02) Very Good (02) Very Good
    ## 1796 (02) Very Good (02) Very Good
    ## 1797      (03) Good      (03) Good
    ## 1798 (02) Very Good (02) Very Good
    ## 1799 (02) Very Good (02) Very Good
    ## 1800 (02) Very Good (02) Very Good
    ## 1801      (04) Fair      (03) Good
    ## 1802      (03) Good      (03) Good
    ## 1803      (04) Fair      (04) Fair
    ## 1804 (01) Excellent (02) Very Good
    ## 1805      (03) Good      (03) Good
    ## 1806      (03) Good (02) Very Good
    ## 1807      (03) Good      (03) Good
    ## 1808      (04) Fair (01) Excellent
    ## 1809      (04) Fair      (03) Good
    ## 1810 (02) Very Good (02) Very Good
    ## 1811 (02) Very Good      (03) Good
    ## 1812 (02) Very Good      (03) Good
    ## 1813      (03) Good      (03) Good
    ## 1814      (04) Fair      (03) Good
    ## 1815 (02) Very Good (02) Very Good
    ## 1816      (04) Fair      (03) Good
    ## 1817      (03) Good      (03) Good
    ## 1818 (01) Excellent (01) Excellent
    ## 1819      (03) Good      (03) Good
    ## 1820      (03) Good (02) Very Good
    ## 1821      (03) Good (02) Very Good
    ## 1822      (03) Good      (03) Good
    ## 1823 (02) Very Good      (03) Good
    ## 1824 (02) Very Good (02) Very Good
    ## 1825 (01) Excellent (02) Very Good
    ## 1826      (03) Good      (03) Good
    ## 1827 (01) Excellent (01) Excellent
    ## 1828      (03) Good (02) Very Good
    ## 1829      (03) Good      (03) Good
    ## 1830      (03) Good (02) Very Good
    ## 1831      (03) Good      (03) Good
    ## 1832 (02) Very Good (02) Very Good
    ## 1833      (04) Fair      (03) Good
    ## 1834 (01) Excellent (02) Very Good
    ## 1835      (03) Good      (03) Good
    ## 1836      (04) Fair      (03) Good
    ## 1837      (04) Fair (02) Very Good
    ## 1838      (03) Good      (03) Good
    ## 1839      (03) Good      (03) Good
    ## 1840 (02) Very Good (02) Very Good
    ## 1841 (02) Very Good (02) Very Good
    ## 1842      (03) Good      (03) Good
    ## 1843 (02) Very Good (01) Excellent
    ## 1844      (03) Good (02) Very Good
    ## 1845      (03) Good      (03) Good
    ## 1846      (03) Good      (03) Good
    ## 1847 (02) Very Good (02) Very Good
    ## 1848      (05) Poor      (03) Good
    ## 1849 (02) Very Good (02) Very Good
    ## 1850      (03) Good      (03) Good
    ## 1851      (03) Good      (03) Good
    ## 1852 (02) Very Good (02) Very Good
    ## 1853      (03) Good (02) Very Good
    ## 1854 (01) Excellent (01) Excellent
    ## 1855 (02) Very Good (02) Very Good
    ## 1856      (04) Fair      (03) Good
    ## 1857      (04) Fair (02) Very Good
    ## 1858 (02) Very Good      (03) Good
    ## 1859      (05) Poor      (05) Poor
    ## 1860      (03) Good      (03) Good
    ## 1861      (04) Fair      (04) Fair
    ## 1862 (02) Very Good (02) Very Good
    ## 1863 (02) Very Good (02) Very Good
    ## 1864      (03) Good      (03) Good
    ## 1865      (04) Fair      (04) Fair
    ## 1866 (02) Very Good (02) Very Good
    ## 1867 (02) Very Good (02) Very Good
    ## 1868 (02) Very Good (02) Very Good
    ## 1869 (02) Very Good      (03) Good
    ## 1870 (02) Very Good      (03) Good
    ## 1871 (02) Very Good (02) Very Good
    ## 1872 (01) Excellent (02) Very Good
    ## 1873      (04) Fair (01) Excellent
    ## 1874 (02) Very Good (02) Very Good
    ## 1875 (02) Very Good      (03) Good
    ## 1876 (01) Excellent (01) Excellent
    ## 1877      (03) Good      (03) Good
    ## 1878      (03) Good      (03) Good
    ## 1879      (03) Good      (03) Good
    ## 1880      (03) Good (02) Very Good
    ## 1881 (01) Excellent      (03) Good
    ## 1882 (01) Excellent (01) Excellent
    ## 1883 (01) Excellent (01) Excellent
    ## 1884      (04) Fair      (03) Good
    ## 1885      (03) Good      (03) Good
    ## 1886      (04) Fair (02) Very Good
    ## 1887 (01) Excellent (01) Excellent
    ## 1888      (03) Good (02) Very Good
    ## 1889      (03) Good      (03) Good
    ## 1890 (02) Very Good (02) Very Good
    ## 1891      (03) Good      (03) Good
    ## 1892      (05) Poor      (04) Fair
    ## 1893      (03) Good      (03) Good
    ## 1894      (03) Good      (03) Good
    ## 1895 (02) Very Good (02) Very Good
    ## 1896      (03) Good (02) Very Good
    ## 1897 (01) Excellent (01) Excellent
    ## 1898 (01) Excellent (01) Excellent
    ## 1899      (04) Fair      (03) Good
    ## 1900 (01) Excellent (01) Excellent
    ## 1901 (01) Excellent (02) Very Good
    ## 1902      (04) Fair (02) Very Good
    ## 1903      (04) Fair      (04) Fair
    ## 1904 (01) Excellent (01) Excellent
    ## 1905      (03) Good (02) Very Good
    ## 1906      (03) Good      (04) Fair
    ## 1907      (03) Good      (03) Good
    ## 1908 (02) Very Good (02) Very Good
    ## 1909 (02) Very Good (02) Very Good
    ## 1910      (04) Fair      (03) Good
    ## 1911 (02) Very Good (02) Very Good
    ## 1912 (01) Excellent (01) Excellent
    ## 1913      (03) Good      (03) Good
    ## 1914      (03) Good (02) Very Good
    ## 1915      (03) Good      (03) Good
    ## 1916      (04) Fair      (04) Fair
    ## 1917      (03) Good (02) Very Good
    ## 1918      (03) Good      (03) Good
    ## 1919      (04) Fair      (04) Fair
    ## 1920      (03) Good      (03) Good
    ## 1921      (03) Good      (03) Good
    ## 1922      (03) Good      (03) Good
    ## 1923      (03) Good (02) Very Good
    ## 1924      (03) Good      (04) Fair
    ## 1925      (03) Good      (03) Good
    ## 1926 (01) Excellent (01) Excellent
    ## 1927 (01) Excellent (01) Excellent
    ## 1928      (04) Fair      (04) Fair
    ## 1929 (02) Very Good (01) Excellent
    ## 1930 (01) Excellent (01) Excellent
    ## 1931 (01) Excellent (01) Excellent
    ## 1932      (03) Good      (03) Good
    ## 1933 (02) Very Good (01) Excellent
    ## 1934      (03) Good (02) Very Good
    ## 1935 (02) Very Good (01) Excellent
    ## 1936 (01) Excellent (02) Very Good
    ## 1937 (01) Excellent      (03) Good
    ## 1938      (04) Fair (01) Excellent
    ## 1939 (02) Very Good (01) Excellent
    ## 1940      (03) Good      (03) Good
    ## 1941      (05) Poor      (04) Fair
    ## 1942 (02) Very Good      (03) Good
    ## 1943      (03) Good      (03) Good
    ## 1944 (02) Very Good (02) Very Good
    ## 1945      (03) Good      (03) Good
    ## 1946      (03) Good (02) Very Good
    ## 1947      (04) Fair (02) Very Good
    ## 1948 (02) Very Good      (03) Good
    ## 1949 (02) Very Good      (03) Good
    ## 1950      (03) Good      (03) Good
    ## 1951      (03) Good      (03) Good
    ## 1952      (03) Good      (03) Good
    ## 1953      (03) Good      (03) Good
    ## 1954      (03) Good (02) Very Good
    ## 1955      (03) Good (01) Excellent
    ## 1956      (04) Fair      (04) Fair
    ## 1957 (02) Very Good      (03) Good
    ## 1958      (03) Good (01) Excellent
    ## 1959 (01) Excellent (02) Very Good
    ## 1960 (02) Very Good (02) Very Good
    ## 1961      (04) Fair      (04) Fair
    ## 1962 (02) Very Good (02) Very Good
    ## 1963      (04) Fair      (03) Good
    ## 1964      (03) Good      (03) Good
    ## 1965 (02) Very Good (02) Very Good
    ## 1966      (03) Good      (03) Good
    ## 1967      (03) Good (02) Very Good
    ## 1968      (03) Good (02) Very Good
    ## 1969      (03) Good (02) Very Good
    ## 1970 (02) Very Good (02) Very Good
    ## 1971      (03) Good      (03) Good
    ## 1972 (01) Excellent (01) Excellent
    ## 1973      (03) Good      (03) Good
    ## 1974      (04) Fair      (04) Fair
    ## 1975 (02) Very Good      (03) Good
    ## 1976 (01) Excellent (01) Excellent
    ## 1977 (01) Excellent (01) Excellent
    ## 1978      (04) Fair      (03) Good
    ## 1979      (03) Good      (03) Good
    ## 1980      (04) Fair      (04) Fair
    ## 1981      (03) Good (02) Very Good
    ## 1982      (05) Poor      (04) Fair
    ## 1983      (04) Fair      (03) Good
    ## 1984 (02) Very Good (02) Very Good
    ## 1985      (04) Fair (02) Very Good
    ## 1986      (04) Fair      (04) Fair
    ## 1987 (02) Very Good (02) Very Good
    ## 1988 (01) Excellent (01) Excellent
    ## 1989      (03) Good (02) Very Good
    ## 1990      (03) Good (01) Excellent
    ## 1991      (04) Fair      (04) Fair
    ## 1992 (02) Very Good (02) Very Good
    ## 1993      (04) Fair      (03) Good
    ## 1994      (05) Poor      (05) Poor
    ## 1995 (02) Very Good (02) Very Good
    ## 1996 (02) Very Good      (03) Good
    ## 1997 (02) Very Good      (03) Good
    ## 1998 (02) Very Good (02) Very Good
    ## 1999      (04) Fair (02) Very Good
    ## 2000      (03) Good (01) Excellent
    ## 2001      (03) Good (02) Very Good
    ## 2002      (05) Poor      (04) Fair
    ## 2003 (02) Very Good (02) Very Good
    ## 2004      (03) Good      (03) Good
    ## 2005      (03) Good (01) Excellent
    ## 2006      (03) Good      (03) Good
    ## 2007 (02) Very Good (02) Very Good
    ## 2008 (02) Very Good (01) Excellent
    ## 2009      (03) Good      (03) Good
    ## 2010      (03) Good      (03) Good
    ## 2011 (02) Very Good      (03) Good
    ## 2012 (02) Very Good (02) Very Good
    ## 2013      (04) Fair (02) Very Good
    ## 2014      (03) Good      (03) Good
    ## 2015      (05) Poor      (03) Good
    ## 2016 (02) Very Good (02) Very Good
    ## 2017 (02) Very Good (02) Very Good
    ## 2018 (02) Very Good (02) Very Good
    ## 2019      (04) Fair      (03) Good
    ## 2020      (03) Good (01) Excellent
    ## 2021 (01) Excellent (01) Excellent
    ## 2022 (01) Excellent (02) Very Good
    ## 2023      (03) Good      (04) Fair
    ## 2024      (04) Fair      (03) Good
    ## 2025 (02) Very Good      (03) Good
    ## 2026 (02) Very Good (02) Very Good
    ## 2027      (04) Fair      (04) Fair
    ## 2028 (02) Very Good      (03) Good
    ## 2029 (01) Excellent (01) Excellent
    ## 2030      (04) Fair      (04) Fair
    ## 2031      (03) Good      (03) Good
    ## 2032 (01) Excellent (02) Very Good
    ## 2033      (03) Good      (04) Fair
    ## 2034 (02) Very Good (02) Very Good
    ## 2035      (05) Poor      (04) Fair
    ## 2036 (02) Very Good (02) Very Good
    ## 2037 (02) Very Good      (03) Good
    ## 2038      (04) Fair (02) Very Good
    ## 2039 (02) Very Good (02) Very Good
    ## 2040 (02) Very Good (01) Excellent
    ## 2041 (01) Excellent (01) Excellent
    ## 2042      (03) Good      (03) Good
    ## 2043      (03) Good      (03) Good
    ## 2044      (03) Good (02) Very Good
    ## 2045 (02) Very Good (01) Excellent
    ## 2046      (04) Fair      (04) Fair
    ## 2047      (05) Poor      (04) Fair
    ## 2048      (04) Fair      (04) Fair
    ## 2049      (03) Good (01) Excellent
    ## 2050      (04) Fair (02) Very Good
    ## 2051 (01) Excellent (01) Excellent
    ## 2052 (01) Excellent (01) Excellent
    ## 2053 (02) Very Good (02) Very Good
    ## 2054      (03) Good      (03) Good
    ## 2055      (03) Good      (03) Good
    ## 2056 (02) Very Good (02) Very Good
    ## 2057      (03) Good      (03) Good
    ## 2058 (02) Very Good (02) Very Good
    ## 2059 (02) Very Good (02) Very Good
    ## 2060      (03) Good      (03) Good
    ## 2061      (03) Good      (03) Good
    ## 2062 (02) Very Good (02) Very Good
    ## 2063      (03) Good      (03) Good
    ## 2064      (03) Good (01) Excellent
    ## 2065      (04) Fair      (03) Good
    ## 2066      (03) Good      (03) Good
    ## 2067      (04) Fair      (03) Good
    ## 2068      (04) Fair      (04) Fair
    ## 2069      (03) Good (01) Excellent
    ## 2070 (02) Very Good (02) Very Good
    ## 2071 (02) Very Good (02) Very Good
    ## 2072 (02) Very Good      (03) Good
    ## 2073      (03) Good      (03) Good
    ## 2074      (04) Fair      (03) Good
    ## 2075      (03) Good      (03) Good
    ## 2076 (02) Very Good (02) Very Good
    ## 2077      (03) Good      (03) Good
    ## 2078      (03) Good      (03) Good
    ## 2079      (03) Good      (03) Good
    ## 2080      (04) Fair      (04) Fair
    ## 2081      (03) Good      (03) Good
    ## 2082      (03) Good      (03) Good
    ## 2083      (03) Good      (03) Good
    ## 2084      (04) Fair      (04) Fair
    ## 2085      (03) Good (02) Very Good
    ## 2086 (02) Very Good      (03) Good
    ## 2087 (02) Very Good (02) Very Good
    ## 2088      (03) Good (02) Very Good
    ## 2089      (04) Fair      (03) Good
    ## 2090      (03) Good      (03) Good
    ## 2091      (03) Good      (03) Good
    ## 2092      (03) Good      (03) Good
    ## 2093      (03) Good      (03) Good
    ## 2094      (04) Fair (02) Very Good
    ## 2095      (03) Good      (03) Good
    ## 2096 (02) Very Good (02) Very Good
    ## 2097 (01) Excellent (01) Excellent
    ## 2098      (03) Good (02) Very Good
    ## 2099 (02) Very Good (02) Very Good
    ## 2100 (02) Very Good (02) Very Good
    ## 2101      (03) Good      (03) Good
    ## 2102      (03) Good      (03) Good
    ## 2103      (04) Fair      (03) Good
    ## 2104      (05) Poor      (05) Poor
    ## 2105      (04) Fair      (03) Good
    ## 2106 (02) Very Good (02) Very Good
    ## 2107 (02) Very Good (02) Very Good
    ## 2108 (01) Excellent (01) Excellent
    ## 2109 (02) Very Good (02) Very Good
    ## 2110      (03) Good      (03) Good
    ## 2111      (05) Poor      (04) Fair
    ## 2112 (01) Excellent (02) Very Good
    ## 2113      (03) Good      (03) Good
    ## 2114 (01) Excellent (02) Very Good
    ## 2115      (04) Fair      (03) Good
    ## 2116 (01) Excellent      (03) Good
    ## 2117 (02) Very Good      (03) Good
    ## 2118 (02) Very Good (02) Very Good
    ## 2119 (02) Very Good (02) Very Good
    ## 2120 (02) Very Good (02) Very Good
    ## 2121      (03) Good      (03) Good
    ## 2122 (02) Very Good (02) Very Good
    ## 2123      (04) Fair      (04) Fair
    ## 2124 (02) Very Good (02) Very Good
    ## 2125 (02) Very Good (02) Very Good
    ## 2126      (03) Good      (03) Good
    ## 2127      (03) Good      (03) Good
    ## 2128      (04) Fair      (03) Good
    ## 2129 (02) Very Good      (03) Good
    ## 2130      (03) Good      (03) Good
    ## 2131 (01) Excellent (01) Excellent
    ## 2132      (03) Good      (03) Good
    ## 2133      (04) Fair (01) Excellent
    ## 2134 (02) Very Good (02) Very Good
    ## 2135 (01) Excellent (01) Excellent
    ## 2136      (03) Good (02) Very Good
    ## 2137      (04) Fair      (03) Good
    ## 2138      (03) Good      (03) Good
    ## 2139 (02) Very Good (02) Very Good
    ## 2140      (03) Good      (03) Good
    ## 2141      (03) Good      (03) Good
    ## 2142 (02) Very Good (02) Very Good
    ## 2143 (01) Excellent      (03) Good
    ## 2144      (04) Fair      (04) Fair
    ## 2145      (03) Good      (03) Good
    ## 2146 (02) Very Good (02) Very Good
    ## 2147 (02) Very Good (02) Very Good
    ## 2148      (03) Good      (03) Good
    ## 2149      (03) Good      (03) Good
    ## 2150 (01) Excellent (01) Excellent
    ## 2151      (04) Fair      (03) Good
    ## 2152      (03) Good      (03) Good
    ## 2153 (01) Excellent (01) Excellent
    ## 2154      (03) Good      (03) Good
    ## 2155 (02) Very Good      (03) Good
    ## 2156 (02) Very Good (02) Very Good
    ## 2157 (02) Very Good (02) Very Good
    ## 2158 (02) Very Good      (03) Good
    ## 2159 (01) Excellent (01) Excellent
    ## 2160 (02) Very Good (02) Very Good
    ## 2161 (02) Very Good (02) Very Good
    ## 2162 (01) Excellent (02) Very Good
    ## 2163      (03) Good      (03) Good
    ## 2164      (03) Good      (03) Good
    ## 2165 (01) Excellent (02) Very Good
    ## 2166      (03) Good      (03) Good
    ## 2167 (02) Very Good (02) Very Good
    ## 2168 (02) Very Good (02) Very Good
    ## 2169      (03) Good      (03) Good
    ## 2170 (02) Very Good (02) Very Good
    ## 2171 (01) Excellent (01) Excellent
    ## 2172      (03) Good      (03) Good
    ## 2173 (02) Very Good (02) Very Good
    ## 2174 (02) Very Good (02) Very Good
    ## 2175      (03) Good (02) Very Good
    ## 2176      (03) Good      (03) Good
    ## 2177      (03) Good (01) Excellent
    ## 2178      (04) Fair      (04) Fair
    ## 2179 (02) Very Good (02) Very Good
    ## 2180      (03) Good      (03) Good
    ## 2181      (03) Good      (03) Good
    ## 2182      (03) Good      (03) Good
    ## 2183 (02) Very Good (02) Very Good
    ## 2184      (03) Good      (03) Good
    ## 2185      (03) Good      (03) Good
    ## 2186 (01) Excellent (02) Very Good
    ## 2187      (03) Good (02) Very Good
    ## 2188 (02) Very Good (02) Very Good
    ## 2189 (02) Very Good (02) Very Good
    ## 2190      (05) Poor (01) Excellent
    ## 2191      (05) Poor      (04) Fair
    ## 2192      (03) Good (01) Excellent
    ## 2193 (02) Very Good (02) Very Good
    ## 2194 (02) Very Good      (03) Good
    ## 2195      (04) Fair (02) Very Good
    ## 2196      (04) Fair      (04) Fair
    ## 2197      (03) Good      (03) Good
    ## 2198 (01) Excellent (01) Excellent
    ## 2199      (03) Good (02) Very Good
    ## 2200 (02) Very Good      (03) Good
    ## 2201      (03) Good      (03) Good
    ## 2202 (02) Very Good (02) Very Good
    ## 2203      (04) Fair      (03) Good
    ## 2204 (01) Excellent (01) Excellent
    ## 2205 (01) Excellent (01) Excellent
    ## 2206 (01) Excellent (01) Excellent
    ## 2207 (02) Very Good      (04) Fair
    ## 2208      (03) Good      (03) Good
    ## 2209      (03) Good (01) Excellent
    ## 2210 (02) Very Good (02) Very Good
    ## 2211 (02) Very Good (02) Very Good
    ## 2212      (03) Good      (03) Good
    ## 2213      (03) Good      (03) Good
    ## 2214 (02) Very Good (02) Very Good
    ## 2215 (02) Very Good (02) Very Good
    ## 2216      (04) Fair      (03) Good
    ## 2217 (01) Excellent (01) Excellent
    ## 2218      (03) Good (01) Excellent
    ## 2219      (03) Good      (03) Good
    ## 2220      (04) Fair      (04) Fair
    ## 2221 (02) Very Good (02) Very Good
    ## 2222 (01) Excellent (01) Excellent
    ## 2223      (03) Good      (03) Good
    ## 2224      (03) Good      (03) Good
    ## 2225 (01) Excellent (02) Very Good
    ## 2226      (03) Good      (03) Good
    ## 2227      (03) Good      (03) Good
    ## 2228 (02) Very Good      (04) Fair
    ## 2229      (04) Fair      (04) Fair
    ## 2230 (02) Very Good (02) Very Good
    ## 2231 (02) Very Good (02) Very Good
    ## 2232      (04) Fair      (03) Good
    ## 2233      (03) Good (01) Excellent
    ## 2234 (02) Very Good (02) Very Good
    ## 2235 (02) Very Good (02) Very Good
    ## 2236      (03) Good      (03) Good
    ## 2237      (03) Good      (03) Good
    ## 2238 (01) Excellent (01) Excellent
    ## 2239 (02) Very Good (02) Very Good
    ## 2240      (03) Good      (03) Good
    ## 2241      (03) Good      (03) Good
    ## 2242      (03) Good      (03) Good
    ## 2243 (01) Excellent (01) Excellent
    ## 2244 (01) Excellent (01) Excellent
    ## 2245      (03) Good      (03) Good
    ## 2246      (04) Fair      (04) Fair
    ## 2247      (03) Good      (03) Good
    ## 2248      (04) Fair      (03) Good
    ## 2249      (03) Good      (04) Fair
    ## 2250 (02) Very Good (02) Very Good
    ## 2251 (02) Very Good (02) Very Good
    ## 2252      (04) Fair      (04) Fair
    ## 2253 (02) Very Good      (03) Good
    ## 2254      (03) Good (02) Very Good
    ## 2255      (03) Good (02) Very Good
    ## 2256 (02) Very Good      (03) Good
    ## 2257      (05) Poor (02) Very Good
    ## 2258      (05) Poor      (03) Good
    ## 2259      (03) Good      (03) Good
    ## 2260 (01) Excellent      (03) Good
    ## 2261      (03) Good      (03) Good
    ## 2262      (04) Fair      (03) Good
    ## 2263      (03) Good (01) Excellent
    ## 2264      (03) Good      (03) Good
    ## 2265      (03) Good      (03) Good
    ## 2266      (03) Good      (03) Good
    ## 2267      (04) Fair (02) Very Good
    ## 2268 (01) Excellent (01) Excellent
    ## 2269      (03) Good      (03) Good
    ## 2270 (02) Very Good (02) Very Good
    ## 2271      (03) Good      (03) Good
    ## 2272      (03) Good      (03) Good
    ## 2273      (03) Good (01) Excellent
    ## 2274 (02) Very Good      (03) Good
    ## 2275      (04) Fair      (03) Good
    ## 2276      (03) Good      (03) Good
    ## 2277      (03) Good      (03) Good
    ## 2278      (03) Good      (03) Good
    ## 2279      (03) Good      (03) Good
    ## 2280 (02) Very Good (02) Very Good
    ## 2281      (03) Good      (03) Good
    ## 2282      (03) Good      (03) Good
    ## 2283      (03) Good (02) Very Good
    ## 2284 (02) Very Good (02) Very Good
    ## 2285      (03) Good      (03) Good
    ## 2286 (02) Very Good (02) Very Good
    ## 2287      (04) Fair      (03) Good
    ## 2288      (03) Good (02) Very Good
    ## 2289      (04) Fair      (04) Fair
    ## 2290      (03) Good      (03) Good
    ## 2291      (04) Fair      (03) Good
    ## 2292 (02) Very Good      (03) Good
    ## 2293      (05) Poor      (05) Poor
    ## 2294 (02) Very Good (02) Very Good
    ## 2295      (03) Good      (03) Good
    ## 2296 (02) Very Good (02) Very Good
    ## 2297 (02) Very Good      (03) Good
    ## 2298      (04) Fair      (03) Good
    ## 2299 (02) Very Good      (03) Good
    ## 2300      (03) Good      (03) Good
    ## 2301      (03) Good      (03) Good
    ## 2302 (02) Very Good (01) Excellent
    ## 2303 (02) Very Good (02) Very Good
    ## 2304      (03) Good      (03) Good
    ## 2305 (02) Very Good (02) Very Good
    ## 2306      (03) Good (01) Excellent
    ## 2307 (02) Very Good (02) Very Good
    ## 2308 (01) Excellent (01) Excellent
    ## 2309 (01) Excellent (01) Excellent
    ## 2310 (02) Very Good (02) Very Good
    ## 2311      (03) Good (01) Excellent
    ## 2312 (02) Very Good (02) Very Good
    ## 2313      (03) Good      (03) Good
    ## 2314      (04) Fair      (03) Good
    ## 2315 (02) Very Good (01) Excellent
    ## 2316      (03) Good      (03) Good
    ## 2317 (02) Very Good (01) Excellent
    ## 2318      (03) Good      (03) Good
    ## 2319 (01) Excellent (01) Excellent
    ## 2320      (04) Fair      (03) Good
    ## 2321 (02) Very Good (02) Very Good
    ## 2322      (03) Good      (03) Good
    ## 2323 (02) Very Good (02) Very Good
    ## 2324 (02) Very Good (02) Very Good
    ## 2325      (03) Good      (03) Good
    ## 2326      (04) Fair      (03) Good
    ## 2327 (01) Excellent (01) Excellent
    ## 2328      (03) Good      (03) Good
    ## 2329      (03) Good      (03) Good
    ## 2330      (04) Fair      (04) Fair
    ## 2331      (03) Good      (03) Good
    ## 2332 (01) Excellent (02) Very Good
    ## 2333      (03) Good (02) Very Good
    ## 2334 (01) Excellent (01) Excellent
    ## 2335 (02) Very Good (02) Very Good
    ## 2336      (04) Fair      (04) Fair
    ## 2337      (03) Good      (03) Good
    ## 2338      (04) Fair      (03) Good
    ## 2339      (04) Fair      (04) Fair
    ## 2340      (04) Fair      (04) Fair
    ## 2341      (05) Poor      (04) Fair
    ## 2342 (01) Excellent      (03) Good
    ## 2343 (02) Very Good (01) Excellent
    ## 2344 (01) Excellent (01) Excellent
    ## 2345 (02) Very Good (01) Excellent
    ## 2346 (02) Very Good (02) Very Good
    ## 2347      (03) Good      (03) Good
    ## 2348 (02) Very Good      (03) Good
    ## 2349      (03) Good      (03) Good
    ## 2350      (05) Poor (02) Very Good
    ## 2351 (02) Very Good      (03) Good
    ## 2352 (02) Very Good (02) Very Good
    ## 2353      (03) Good      (03) Good
    ## 2354      (04) Fair      (03) Good
    ## 2355      (03) Good      (03) Good
    ## 2356 (01) Excellent (01) Excellent
    ## 2357 (01) Excellent (01) Excellent
    ## 2358      (03) Good      (03) Good
    ## 2359 (01) Excellent (01) Excellent
    ## 2360 (01) Excellent (01) Excellent
    ## 2361 (02) Very Good      (03) Good
    ## 2362 (01) Excellent (01) Excellent
    ## 2363 (01) Excellent      (03) Good
    ## 2364 (02) Very Good (02) Very Good
    ## 2365      (03) Good      (03) Good
    ## 2366 (02) Very Good (02) Very Good
    ## 2367 (02) Very Good      (03) Good
    ## 2368      (03) Good      (04) Fair
    ## 2369      (03) Good      (03) Good
    ## 2370 (02) Very Good (02) Very Good
    ## 2371 (02) Very Good (02) Very Good
    ## 2372 (01) Excellent (01) Excellent
    ## 2373 (01) Excellent (01) Excellent
    ## 2374      (04) Fair      (04) Fair
    ## 2375 (02) Very Good (02) Very Good
    ## 2376 (02) Very Good      (03) Good
    ## 2377      (03) Good      (03) Good
    ## 2378 (02) Very Good (02) Very Good
    ## 2379 (02) Very Good      (03) Good
    ## 2380      (03) Good      (03) Good
    ## 2381 (01) Excellent (02) Very Good
    ## 2382      (03) Good (02) Very Good
    ## 2383      (03) Good (02) Very Good
    ## 2384 (01) Excellent (01) Excellent
    ## 2385      (04) Fair (02) Very Good
    ## 2386 (01) Excellent (01) Excellent
    ## 2387 (01) Excellent      (03) Good
    ## 2388      (04) Fair      (05) Poor
    ## 2389      (03) Good (02) Very Good
    ## 2390      (03) Good      (03) Good
    ## 2391      (03) Good      (03) Good
    ## 2392 (01) Excellent (02) Very Good
    ## 2393 (02) Very Good      (04) Fair
    ## 2394      (05) Poor (02) Very Good
    ## 2395 (02) Very Good      (03) Good
    ## 2396 (01) Excellent (01) Excellent
    ## 2397 (02) Very Good      (03) Good
    ## 2398      (04) Fair (01) Excellent
    ## 2399 (01) Excellent (01) Excellent
    ## 2400      (03) Good      (04) Fair
    ## 2401      (04) Fair      (03) Good
    ## 2402 (02) Very Good (02) Very Good
    ## 2403      (04) Fair      (04) Fair
    ## 2404      (03) Good (02) Very Good
    ## 2405      (03) Good      (03) Good
    ## 2406      (03) Good      (03) Good
    ## 2407      (04) Fair (02) Very Good
    ## 2408 (02) Very Good      (03) Good
    ## 2409 (02) Very Good (02) Very Good
    ## 2410      (03) Good      (03) Good
    ## 2411      (03) Good (02) Very Good
    ## 2412      (03) Good      (03) Good
    ## 2413 (01) Excellent      (03) Good
    ## 2414 (02) Very Good (02) Very Good
    ## 2415 (01) Excellent (01) Excellent
    ## 2416      (03) Good (02) Very Good
    ## 2417      (03) Good      (04) Fair
    ## 2418      (03) Good (02) Very Good
    ## 2419      (04) Fair      (03) Good
    ## 2420      (03) Good (02) Very Good
    ## 2421 (01) Excellent (01) Excellent
    ## 2422      (03) Good      (03) Good
    ## 2423 (02) Very Good      (03) Good
    ## 2424      (03) Good      (03) Good
    ## 2425 (02) Very Good (02) Very Good
    ## 2426      (04) Fair      (03) Good
    ## 2427 (01) Excellent (01) Excellent
    ## 2428 (02) Very Good (02) Very Good
    ## 2429      (03) Good (02) Very Good
    ## 2430 (02) Very Good (02) Very Good
    ## 2431 (02) Very Good (02) Very Good
    ## 2432 (02) Very Good      (04) Fair
    ## 2433      (04) Fair      (04) Fair
    ## 2434      (03) Good      (03) Good
    ## 2435      (03) Good (02) Very Good
    ## 2436 (02) Very Good (01) Excellent
    ## 2437      (04) Fair (02) Very Good
    ## 2438      (03) Good (01) Excellent
    ## 2439 (02) Very Good      (03) Good
    ## 2440 (01) Excellent (01) Excellent
    ## 2441 (02) Very Good (01) Excellent
    ## 2442 (02) Very Good (02) Very Good
    ## 2443 (02) Very Good (02) Very Good
    ## 2444      (04) Fair (01) Excellent
    ## 2445 (02) Very Good (02) Very Good
    ## 2446 (02) Very Good      (04) Fair
    ## 2447      (03) Good      (03) Good
    ## 2448      (03) Good      (03) Good
    ## 2449 (02) Very Good      (03) Good
    ## 2450 (01) Excellent (02) Very Good
    ## 2451      (03) Good (02) Very Good
    ## 2452 (01) Excellent (01) Excellent
    ## 2453      (03) Good      (04) Fair
    ## 2454 (02) Very Good (02) Very Good
    ## 2455 (02) Very Good (01) Excellent
    ## 2456      (04) Fair      (03) Good
    ## 2457 (02) Very Good (02) Very Good
    ## 2458      (03) Good (02) Very Good
    ## 2459 (01) Excellent (01) Excellent
    ## 2460      (03) Good      (03) Good
    ## 2461 (02) Very Good      (03) Good
    ## 2462      (03) Good      (03) Good
    ## 2463      (05) Poor      (03) Good
    ## 2464      (05) Poor (01) Excellent
    ## 2465 (02) Very Good (02) Very Good
    ## 2466 (02) Very Good (02) Very Good
    ## 2467      (04) Fair      (03) Good
    ## 2468 (02) Very Good (02) Very Good
    ## 2469        (98) DK      (03) Good
    ## 2470      (03) Good (01) Excellent
    ## 2471      (04) Fair      (04) Fair
    ## 2472      (03) Good      (03) Good
    ## 2473      (03) Good      (03) Good
    ## 2474      (04) Fair      (05) Poor
    ## 2475      (03) Good      (03) Good
    ## 2476      (03) Good (02) Very Good
    ## 2477      (04) Fair (01) Excellent
    ## 2478 (02) Very Good (02) Very Good
    ## 2479      (04) Fair      (03) Good
    ## 2480      (03) Good      (03) Good
    ## 2481      (04) Fair (02) Very Good
    ## 2482 (02) Very Good      (03) Good
    ## 2483 (01) Excellent (02) Very Good
    ## 2484      (03) Good (02) Very Good
    ## 2485      (03) Good      (03) Good
    ## 2486 (02) Very Good      (03) Good
    ## 2487      (03) Good      (03) Good
    ## 2488 (01) Excellent (02) Very Good
    ## 2489      (04) Fair      (04) Fair
    ## 2490 (02) Very Good (02) Very Good
    ## 2491      (03) Good      (03) Good
    ## 2492      (03) Good      (03) Good
    ## 2493 (02) Very Good (01) Excellent
    ## 2494      (03) Good (02) Very Good
    ## 2495      (03) Good (02) Very Good
    ## 2496      (03) Good      (03) Good
    ## 2497 (02) Very Good (01) Excellent
    ## 2498 (02) Very Good      (03) Good
    ## 2499 (02) Very Good      (03) Good
    ## 2500      (03) Good      (04) Fair
    ## 2501      (03) Good      (03) Good
    ## 2502 (01) Excellent (02) Very Good
    ## 2503 (01) Excellent (01) Excellent
    ## 2504 (01) Excellent (01) Excellent
    ## 2505      (03) Good      (03) Good
    ## 2506 (02) Very Good (01) Excellent
    ## 2507      (03) Good      (03) Good
    ## 2508      (03) Good      (03) Good
    ## 2509 (02) Very Good (01) Excellent
    ## 2510 (01) Excellent (01) Excellent
    ## 2511 (01) Excellent (02) Very Good
    ## 2512      (03) Good (02) Very Good
    ## 2513 (01) Excellent      (03) Good
    ## 2514 (02) Very Good (02) Very Good
    ## 2515 (01) Excellent (01) Excellent
    ## 2516      (03) Good      (04) Fair
    ## 2517 (02) Very Good      (03) Good
    ## 2518 (02) Very Good (02) Very Good
    ## 2519 (02) Very Good (01) Excellent
    ## 2520      (03) Good      (03) Good
    ## 2521 (02) Very Good (02) Very Good
    ## 2522      (03) Good (02) Very Good
    ## 2523 (01) Excellent (01) Excellent
    ## 2524 (01) Excellent (01) Excellent
    ## 2525      (03) Good      (04) Fair
    ## 2526 (01) Excellent (02) Very Good
    ## 2527      (03) Good (02) Very Good
    ## 2528 (01) Excellent (02) Very Good
    ## 2529 (02) Very Good (02) Very Good
    ## 2530 (01) Excellent (01) Excellent
    ## 2531 (01) Excellent (01) Excellent
    ## 2532 (02) Very Good      (03) Good
    ## 2533 (01) Excellent (01) Excellent
    ## 2534      (04) Fair (02) Very Good
    ## 2535 (02) Very Good (02) Very Good
    ## 2536      (03) Good      (03) Good
    ## 2537      (03) Good (02) Very Good
    ## 2538 (02) Very Good (01) Excellent
    ## 2539      (03) Good      (03) Good
    ## 2540 (02) Very Good (02) Very Good
    ## 2541 (02) Very Good (02) Very Good
    ## 2542 (02) Very Good      (04) Fair
    ## 2543      (04) Fair      (03) Good
    ## 2544 (02) Very Good      (03) Good
    ## 2545 (01) Excellent (01) Excellent
    ## 2546 (01) Excellent (01) Excellent
    ## 2547 (01) Excellent (02) Very Good
    ## 2548 (02) Very Good (02) Very Good
    ## 2549 (01) Excellent (01) Excellent
    ## 2550      (03) Good      (03) Good
    ## 2551 (02) Very Good      (04) Fair
    ## 2552 (01) Excellent (01) Excellent
    ## 2553 (02) Very Good (01) Excellent
    ## 2554      (03) Good      (03) Good
    ## 2555 (02) Very Good (02) Very Good
    ## 2556 (02) Very Good      (03) Good
    ## 2557      (04) Fair      (03) Good
    ## 2558      (04) Fair (02) Very Good
    ## 2559 (02) Very Good (02) Very Good
    ## 2560 (02) Very Good      (03) Good
    ## 2561      (04) Fair      (04) Fair
    ## 2562      (05) Poor      (04) Fair
    ## 2563      (03) Good (01) Excellent
    ## 2564      (03) Good      (03) Good
    ## 2565      (03) Good (02) Very Good
    ## 2566 (02) Very Good (02) Very Good
    ## 2567 (01) Excellent (02) Very Good
    ## 2568 (02) Very Good (01) Excellent
    ## 2569 (01) Excellent (01) Excellent
    ## 2570      (04) Fair (02) Very Good
    ## 2571 (02) Very Good (02) Very Good
    ## 2572 (02) Very Good (02) Very Good
    ## 2573 (01) Excellent (01) Excellent
    ## 2574 (01) Excellent (01) Excellent
    ## 2575      (03) Good      (03) Good
    ## 2576 (02) Very Good (02) Very Good
    ## 2577 (02) Very Good (02) Very Good
    ## 2578      (03) Good (02) Very Good
    ## 2579 (02) Very Good (02) Very Good
    ## 2580 (02) Very Good (01) Excellent
    ## 2581 (02) Very Good (02) Very Good
    ## 2582 (01) Excellent (02) Very Good
    ## 2583 (01) Excellent (01) Excellent
    ## 2584      (03) Good      (03) Good
    ## 2585 (01) Excellent (02) Very Good
    ## 2586 (01) Excellent (01) Excellent
    ## 2587      (04) Fair (02) Very Good
    ## 2588 (02) Very Good (02) Very Good
    ## 2589 (02) Very Good (02) Very Good
    ## 2590 (01) Excellent (02) Very Good
    ## 2591 (02) Very Good (01) Excellent
    ## 2592      (04) Fair      (03) Good
    ## 2593      (03) Good (02) Very Good
    ## 2594      (03) Good      (03) Good
    ## 2595 (02) Very Good (02) Very Good
    ## 2596 (02) Very Good      (03) Good
    ## 2597 (02) Very Good (01) Excellent
    ## 2598      (04) Fair      (04) Fair
    ## 2599      (03) Good      (03) Good
    ## 2600 (01) Excellent (01) Excellent
    ## 2601      (03) Good      (03) Good
    ## 2602 (02) Very Good (01) Excellent
    ## 2603      (03) Good      (03) Good
    ## 2604 (01) Excellent (01) Excellent
    ## 2605 (01) Excellent (01) Excellent
    ## 2606 (01) Excellent      (03) Good
    ## 2607 (02) Very Good (01) Excellent
    ## 2608 (02) Very Good (02) Very Good
    ## 2609 (01) Excellent (02) Very Good
    ## 2610 (01) Excellent (02) Very Good
    ## 2611 (01) Excellent (01) Excellent
    ## 2612      (03) Good      (04) Fair
    ## 2613 (01) Excellent (02) Very Good
    ## 2614      (03) Good      (03) Good
    ## 2615 (01) Excellent (01) Excellent
    ## 2616      (03) Good (01) Excellent
    ## 2617      (03) Good      (03) Good
    ## 2618      (04) Fair (02) Very Good
    ## 2619 (02) Very Good      (05) Poor
    ## 2620 (02) Very Good      (03) Good
    ## 2621 (01) Excellent (02) Very Good
    ## 2622 (02) Very Good (02) Very Good
    ## 2623      (03) Good      (04) Fair
    ## 2624      (04) Fair      (03) Good
    ## 2625      (05) Poor      (03) Good
    ## 2626      (03) Good (02) Very Good
    ## 2627 (02) Very Good      (03) Good
    ## 2628 (02) Very Good (02) Very Good
    ## 2629      (03) Good (01) Excellent
    ## 2630      (03) Good (02) Very Good
    ## 2631      (03) Good      (04) Fair
    ## 2632      (03) Good      (03) Good
    ## 2633 (01) Excellent (01) Excellent
    ## 2634      (04) Fair      (03) Good
    ## 2635      (04) Fair (01) Excellent
    ## 2636 (02) Very Good      (03) Good
    ## 2637 (02) Very Good (02) Very Good
    ## 2638      (03) Good      (03) Good
    ## 2639 (02) Very Good (02) Very Good
    ## 2640      (03) Good      (03) Good
    ## 2641      (03) Good (01) Excellent
    ## 2642 (02) Very Good (02) Very Good
    ## 2643 (02) Very Good (02) Very Good
    ## 2644      (04) Fair      (04) Fair
    ## 2645 (02) Very Good (02) Very Good
    ## 2646 (02) Very Good (02) Very Good
    ## 2647      (03) Good      (03) Good
    ## 2648      (03) Good      (03) Good
    ## 2649 (01) Excellent (02) Very Good
    ## 2650 (01) Excellent (01) Excellent
    ## 2651 (02) Very Good (01) Excellent
    ## 2652      (03) Good (01) Excellent
    ## 2653      (03) Good      (03) Good
    ## 2654 (01) Excellent (01) Excellent
    ## 2655      (04) Fair (01) Excellent
    ## 2656      (03) Good      (03) Good
    ## 2657 (02) Very Good (02) Very Good
    ## 2658 (01) Excellent      (03) Good
    ## 2659 (02) Very Good (01) Excellent
    ## 2660 (02) Very Good (02) Very Good
    ## 2661 (02) Very Good (02) Very Good
    ## 2662      (03) Good      (03) Good
    ## 2663 (02) Very Good (02) Very Good
    ## 2664 (02) Very Good (01) Excellent
    ## 2665 (02) Very Good (02) Very Good
    ## 2666 (02) Very Good (01) Excellent
    ## 2667      (03) Good (02) Very Good
    ## 2668 (01) Excellent (02) Very Good
    ## 2669 (02) Very Good      (03) Good
    ## 2670 (02) Very Good (02) Very Good
    ## 2671 (02) Very Good (01) Excellent
    ## 2672 (02) Very Good (02) Very Good
    ## 2673 (02) Very Good (02) Very Good
    ## 2674      (03) Good (02) Very Good
    ## 2675      (03) Good      (03) Good
    ## 2676 (01) Excellent (01) Excellent
    ## 2677 (02) Very Good (02) Very Good
    ## 2678 (01) Excellent (01) Excellent
    ## 2679 (01) Excellent (01) Excellent
    ## 2680 (02) Very Good      (03) Good
    ## 2681 (01) Excellent (02) Very Good
    ## 2682 (02) Very Good      (03) Good
    ## 2683      (03) Good (02) Very Good
    ## 2684 (01) Excellent (01) Excellent
    ## 2685 (02) Very Good (02) Very Good
    ## 2686      (03) Good (01) Excellent
    ## 2687 (01) Excellent (01) Excellent
    ## 2688 (01) Excellent (01) Excellent
    ## 2689      (03) Good      (03) Good
    ## 2690      (03) Good      (03) Good
    ## 2691      (03) Good (01) Excellent
    ## 2692      (04) Fair (01) Excellent
    ## 2693      (03) Good (02) Very Good
    ## 2694      (03) Good (02) Very Good
    ## 2695 (01) Excellent (02) Very Good
    ## 2696 (02) Very Good (02) Very Good
    ## 2697 (02) Very Good (02) Very Good
    ## 2698 (01) Excellent (01) Excellent
    ## 2699 (01) Excellent (01) Excellent
    ## 2700      (03) Good (02) Very Good
    ## 2701 (02) Very Good (02) Very Good
    ## 2702 (02) Very Good (02) Very Good
    ## 2703 (01) Excellent (01) Excellent
    ## 2704 (02) Very Good (02) Very Good
    ## 2705 (01) Excellent (01) Excellent
    ## 2706 (02) Very Good (01) Excellent
    ## 2707 (02) Very Good (01) Excellent
    ## 2708 (01) Excellent (01) Excellent
    ## 2709      (03) Good      (03) Good
    ## 2710      (03) Good (02) Very Good
    ## 2711      (04) Fair      (05) Poor
    ## 2712      (03) Good (02) Very Good
    ## 2713      (03) Good      (03) Good
    ## 2714      (03) Good      (03) Good
    ## 2715 (01) Excellent (01) Excellent
    ## 2716      (03) Good (02) Very Good
    ## 2717      (04) Fair      (03) Good
    ## 2718      (03) Good      (03) Good
    ## 2719 (02) Very Good (01) Excellent
    ## 2720      (03) Good      (03) Good
    ## 2721 (01) Excellent (01) Excellent
    ## 2722 (02) Very Good (02) Very Good
    ## 2723      (04) Fair (01) Excellent
    ## 2724 (02) Very Good (02) Very Good
    ## 2725      (03) Good      (03) Good
    ## 2726 (01) Excellent (02) Very Good
    ## 2727 (02) Very Good (02) Very Good
    ## 2728      (05) Poor (02) Very Good
    ## 2729 (02) Very Good      (03) Good
    ## 2730 (02) Very Good (02) Very Good
    ## 2731 (01) Excellent (01) Excellent
    ## 2732      (04) Fair      (04) Fair
    ## 2733      (03) Good      (04) Fair
    ## 2734      (04) Fair      (04) Fair
    ## 2735      (03) Good (02) Very Good
    ## 2736      (03) Good      (03) Good
    ## 2737      (05) Poor      (03) Good
    ## 2738      (03) Good      (04) Fair
    ## 2739 (02) Very Good      (03) Good
    ## 2740 (01) Excellent (01) Excellent
    ## 2741 (02) Very Good (02) Very Good
    ## 2742      (03) Good      (03) Good
    ## 2743 (02) Very Good      (03) Good
    ## 2744 (02) Very Good (02) Very Good
    ## 2745      (03) Good      (03) Good
    ## 2746 (02) Very Good (01) Excellent
    ## 2747      (04) Fair      (03) Good
    ## 2748 (01) Excellent (01) Excellent
    ## 2749 (02) Very Good      (03) Good
    ## 2750 (02) Very Good (01) Excellent
    ## 2751 (02) Very Good (02) Very Good
    ## 2752      (03) Good      (03) Good
    ## 2753      (04) Fair (02) Very Good
    ## 2754 (02) Very Good (02) Very Good
    ## 2755      (03) Good (02) Very Good
    ## 2756 (01) Excellent (01) Excellent
    ## 2757      (03) Good      (03) Good
    ## 2758 (01) Excellent (01) Excellent
    ## 2759      (03) Good (01) Excellent
    ## 2760 (02) Very Good      (03) Good
    ## 2761      (03) Good      (03) Good
    ## 2762      (03) Good      (03) Good
    ## 2763      (04) Fair      (03) Good
    ## 2764 (02) Very Good      (03) Good
    ## 2765 (02) Very Good (02) Very Good
    ## 2766 (02) Very Good (02) Very Good
    ## 2767      (03) Good      (04) Fair
    ## 2768      (03) Good      (03) Good
    ## 2769      (03) Good (02) Very Good
    ## 2770      (03) Good      (03) Good
    ## 2771      (03) Good (02) Very Good
    ## 2772      (03) Good      (03) Good
    ## 2773 (01) Excellent (01) Excellent
    ## 2774 (02) Very Good (02) Very Good
    ## 2775 (02) Very Good (02) Very Good
    ## 2776 (02) Very Good (02) Very Good
    ## 2777      (03) Good      (03) Good
    ## 2778 (01) Excellent (01) Excellent
    ## 2779 (02) Very Good (02) Very Good
    ## 2780      (03) Good      (03) Good
    ## 2781      (03) Good      (03) Good
    ## 2782 (02) Very Good (01) Excellent
    ## 2783      (03) Good      (04) Fair
    ## 2784      (04) Fair      (03) Good
    ## 2785 (02) Very Good      (03) Good
    ## 2786      (03) Good      (03) Good
    ## 2787 (02) Very Good (02) Very Good
    ## 2788 (02) Very Good (01) Excellent
    ## 2789 (02) Very Good (02) Very Good
    ## 2790      (03) Good      (03) Good
    ## 2791 (02) Very Good (02) Very Good
    ## 2792      (03) Good      (03) Good
    ## 2793      (04) Fair      (03) Good
    ## 2794 (02) Very Good (02) Very Good
    ## 2795 (01) Excellent (02) Very Good
    ## 2796      (03) Good      (03) Good
    ## 2797      (03) Good      (03) Good
    ## 2798      (03) Good      (03) Good
    ## 2799      (03) Good      (03) Good
    ## 2800 (02) Very Good (02) Very Good
    ## 2801      (03) Good      (03) Good
    ## 2802      (03) Good      (03) Good
    ## 2803      (03) Good (02) Very Good
    ## 2804      (03) Good      (03) Good
    ## 2805      (04) Fair      (03) Good
    ## 2806 (02) Very Good (02) Very Good
    ## 2807 (02) Very Good (01) Excellent
    ## 2808 (02) Very Good      (03) Good
    ## 2809      (04) Fair      (03) Good
    ## 2810      (03) Good      (03) Good
    ## 2811      (03) Good      (03) Good
    ## 2812 (02) Very Good (02) Very Good
    ## 2813 (02) Very Good (02) Very Good
    ## 2814      (05) Poor      (04) Fair
    ## 2815 (02) Very Good (01) Excellent
    ## 2816 (02) Very Good (02) Very Good
    ## 2817      (04) Fair      (03) Good
    ## 2818 (02) Very Good      (03) Good
    ## 2819 (02) Very Good      (04) Fair
    ## 2820 (01) Excellent (01) Excellent
    ## 2821 (01) Excellent (01) Excellent
    ## 2822 (02) Very Good (02) Very Good
    ## 2823 (02) Very Good (02) Very Good
    ## 2824      (03) Good      (03) Good
    ## 2825 (02) Very Good      (03) Good
    ## 2826 (02) Very Good (01) Excellent
    ## 2827      (03) Good (02) Very Good
    ## 2828      (03) Good (02) Very Good
    ## 2829      (03) Good      (03) Good
    ## 2830 (01) Excellent (01) Excellent
    ## 2831 (01) Excellent (02) Very Good
    ## 2832      (03) Good      (03) Good
    ## 2833      (03) Good      (03) Good
    ## 2834      (03) Good (02) Very Good
    ## 2835 (02) Very Good (01) Excellent
    ## 2836 (02) Very Good      (03) Good
    ## 2837 (01) Excellent (01) Excellent
    ## 2838 (02) Very Good      (03) Good
    ## 2839 (01) Excellent      (03) Good
    ## 2840      (04) Fair      (03) Good
    ## 2841      (03) Good (02) Very Good
    ## 2842 (02) Very Good (02) Very Good
    ## 2843 (02) Very Good (02) Very Good
    ## 2844 (02) Very Good (02) Very Good
    ## 2845 (01) Excellent (01) Excellent
    ## 2846 (02) Very Good (02) Very Good
    ## 2847 (01) Excellent (01) Excellent
    ## 2848      (03) Good      (03) Good
    ## 2849 (02) Very Good (02) Very Good
    ## 2850 (01) Excellent (01) Excellent
    ## 2851 (01) Excellent (01) Excellent
    ## 2852 (02) Very Good (02) Very Good
    ## 2853      (03) Good      (04) Fair
    ## 2854 (02) Very Good (01) Excellent
    ## 2855 (01) Excellent (01) Excellent
    ## 2856 (02) Very Good      (03) Good
    ## 2857 (02) Very Good (02) Very Good
    ## 2858      (03) Good      (03) Good
    ## 2859      (04) Fair (02) Very Good
    ## 2860      (03) Good      (03) Good
    ## 2861 (02) Very Good      (03) Good
    ## 2862 (02) Very Good (02) Very Good
    ## 2863      (03) Good      (03) Good
    ## 2864 (01) Excellent      (03) Good
    ## 2865 (02) Very Good (02) Very Good
    ## 2866 (01) Excellent (02) Very Good
    ## 2867      (03) Good      (03) Good
    ## 2868 (02) Very Good      (03) Good
    ## 2869      (03) Good      (03) Good
    ## 2870 (01) Excellent (01) Excellent
    ## 2871 (02) Very Good (02) Very Good
    ## 2872      (03) Good (01) Excellent
    ## 2873 (02) Very Good (01) Excellent
    ## 2874      (03) Good      (03) Good
    ## 2875 (02) Very Good      (03) Good
    ## 2876 (02) Very Good (02) Very Good
    ## 2877 (02) Very Good (02) Very Good
    ## 2878 (01) Excellent (01) Excellent
    ## 2879 (02) Very Good (02) Very Good
    ## 2880 (02) Very Good (02) Very Good
    ## 2881      (04) Fair (02) Very Good
    ## 2882 (02) Very Good (02) Very Good
    ## 2883 (01) Excellent (01) Excellent
    ## 2884 (02) Very Good      (03) Good
    ## 2885 (02) Very Good      (03) Good
    ## 2886      (04) Fair      (03) Good
    ## 2887      (04) Fair (02) Very Good
    ## 2888      (03) Good      (03) Good
    ## 2889      (03) Good      (03) Good
    ## 2890 (01) Excellent (01) Excellent
    ## 2891      (04) Fair      (05) Poor
    ## 2892      (03) Good      (03) Good
    ## 2893      (03) Good (01) Excellent
    ## 2894      (04) Fair      (04) Fair
    ## 2895      (04) Fair (02) Very Good
    ## 2896      (03) Good      (03) Good
    ## 2897      (04) Fair      (05) Poor
    ## 2898 (02) Very Good (02) Very Good
    ## 2899 (02) Very Good (02) Very Good
    ## 2900      (05) Poor      (04) Fair
    ## 2901      (03) Good      (04) Fair
    ## 2902      (03) Good (01) Excellent
    ## 2903      (03) Good      (04) Fair
    ## 2904 (02) Very Good (02) Very Good
    ## 2905      (03) Good      (03) Good
    ## 2906      (03) Good      (03) Good
    ## 2907      (04) Fair      (04) Fair
    ## 2908 (02) Very Good (02) Very Good
    ## 2909 (02) Very Good      (03) Good
    ## 2910 (02) Very Good (02) Very Good
    ## 2911 (02) Very Good (01) Excellent
    ## 2912 (02) Very Good (02) Very Good
    ## 2913 (02) Very Good (02) Very Good
    ## 2914 (01) Excellent      (03) Good
    ## 2915 (02) Very Good (02) Very Good
    ## 2916 (01) Excellent (01) Excellent
    ## 2917 (02) Very Good (02) Very Good
    ## 2918 (02) Very Good (02) Very Good
    ## 2919 (02) Very Good (02) Very Good
    ## 2920      (04) Fair (02) Very Good
    ## 2921      (05) Poor (02) Very Good
    ## 2922      (04) Fair      (04) Fair
    ## 2923 (01) Excellent (02) Very Good
    ## 2924 (02) Very Good (01) Excellent
    ## 2925 (02) Very Good      (03) Good
    ## 2926 (02) Very Good (02) Very Good
    ## 2927      (03) Good      (03) Good
    ## 2928      (03) Good (01) Excellent
    ## 2929 (02) Very Good      (03) Good
    ## 2930 (02) Very Good (02) Very Good
    ## 2931      (03) Good      (03) Good
    ## 2932      (03) Good (01) Excellent
    ## 2933 (02) Very Good      (03) Good
    ## 2934      (03) Good (02) Very Good
    ## 2935 (01) Excellent (01) Excellent
    ## 2936 (01) Excellent (01) Excellent
    ## 2937      (03) Good (02) Very Good
    ## 2938 (02) Very Good (01) Excellent
    ## 2939 (01) Excellent (01) Excellent
    ## 2940 (02) Very Good (02) Very Good
    ## 2941      (04) Fair      (03) Good
    ## 2942 (02) Very Good (02) Very Good
    ## 2943 (02) Very Good (02) Very Good
    ## 2944      (03) Good (02) Very Good
    ## 2945 (02) Very Good      (03) Good
    ## 2946      (03) Good (02) Very Good
    ## 2947 (02) Very Good      (03) Good
    ## 2948 (02) Very Good (02) Very Good
    ## 2949 (02) Very Good      (03) Good
    ## 2950 (02) Very Good      (03) Good
    ## 2951 (02) Very Good (02) Very Good
    ## 2952 (02) Very Good (02) Very Good
    ## 2953      (05) Poor      (03) Good
    ## 2954 (02) Very Good (02) Very Good
    ## 2955      (03) Good      (03) Good
    ## 2956 (02) Very Good      (03) Good
    ## 2957 (02) Very Good      (03) Good
    ## 2958 (02) Very Good (01) Excellent
    ## 2959 (02) Very Good (01) Excellent
    ## 2960      (04) Fair      (04) Fair
    ## 2961 (02) Very Good      (04) Fair
    ## 2962      (03) Good      (03) Good
    ## 2963 (01) Excellent (01) Excellent
    ## 2964 (02) Very Good      (03) Good
    ## 2965      (03) Good (02) Very Good
    ## 2966 (02) Very Good (02) Very Good
    ## 2967 (01) Excellent (02) Very Good
    ## 2968 (02) Very Good (02) Very Good
    ## 2969 (02) Very Good      (03) Good
    ## 2970 (01) Excellent (01) Excellent
    ## 2971      (03) Good (02) Very Good
    ## 2972      (04) Fair (02) Very Good
    ## 2973 (02) Very Good (02) Very Good
    ## 2974 (02) Very Good (02) Very Good
    ## 2975 (02) Very Good (02) Very Good
    ## 2976      (03) Good (01) Excellent
    ## 2977      (04) Fair      (03) Good
    ## 2978      (03) Good      (03) Good
    ## 2979 (02) Very Good (02) Very Good
    ## 2980 (02) Very Good (02) Very Good
    ## 2981 (01) Excellent (01) Excellent
    ## 2982 (02) Very Good (02) Very Good
    ## 2983 (02) Very Good (02) Very Good
    ## 2984 (02) Very Good (02) Very Good
    ## 2985 (02) Very Good (01) Excellent
    ## 2986 (02) Very Good      (03) Good
    ## 2987      (03) Good      (03) Good
    ## 2988      (03) Good      (03) Good
    ## 2989      (04) Fair      (04) Fair
    ## 2990      (03) Good      (03) Good
    ## 2991      (04) Fair      (04) Fair
    ## 2992      (03) Good      (03) Good
    ## 2993 (02) Very Good (02) Very Good
    ## 2994      (03) Good      (03) Good
    ## 2995      (03) Good      (03) Good
    ## 2996      (03) Good      (03) Good
    ## 2997 (02) Very Good (02) Very Good
    ## 2998 (02) Very Good (02) Very Good
    ## 2999 (02) Very Good (01) Excellent
    ## 3000      (04) Fair (02) Very Good
    ## 3001      (04) Fair (02) Very Good
    ## 3002 (01) Excellent (02) Very Good
    ## 3003      (05) Poor      (03) Good
    ## 3004 (02) Very Good (02) Very Good
    ## 3005      (04) Fair      (03) Good
    ## 3006 (02) Very Good      (03) Good
    ## 3007 (02) Very Good (02) Very Good
    ## 3008      (03) Good      (04) Fair
    ## 3009      (03) Good      (03) Good
    ## 3010      (04) Fair      (03) Good
    ## 3011 (01) Excellent (01) Excellent
    ## 3012      (03) Good      (03) Good
    ## 3013      (04) Fair (02) Very Good
    ## 3014 (02) Very Good (02) Very Good
    ## 3015      (03) Good (02) Very Good
    ## 3016      (03) Good (01) Excellent
    ## 3017 (02) Very Good (01) Excellent
    ## 3018      (03) Good (02) Very Good
    ## 3019      (03) Good (02) Very Good
    ## 3020 (02) Very Good      (03) Good
    ## 3021      (03) Good      (05) Poor
    ## 3022      (03) Good      (04) Fair
    ## 3023      (04) Fair      (03) Good
    ## 3024      (03) Good      (04) Fair
    ## 3025      (03) Good      (04) Fair
    ## 3026      (03) Good (02) Very Good
    ## 3027      (05) Poor (01) Excellent
    ## 3028      (03) Good      (03) Good
    ## 3029      (03) Good      (04) Fair
    ## 3030      (04) Fair (02) Very Good
    ## 3031 (01) Excellent (01) Excellent
    ## 3032 (02) Very Good (02) Very Good
    ## 3033      (04) Fair (02) Very Good
    ## 3034 (01) Excellent (01) Excellent
    ## 3035      (03) Good (02) Very Good
    ## 3036 (02) Very Good (01) Excellent
    ## 3037      (03) Good (02) Very Good
    ## 3038      (04) Fair      (03) Good
    ## 3039      (03) Good (02) Very Good
    ## 3040      (03) Good      (03) Good
    ## 3041      (04) Fair      (03) Good
    ## 3042      (04) Fair (02) Very Good
    ## 3043      (04) Fair (01) Excellent
    ## 3044      (05) Poor      (04) Fair
    ## 3045 (01) Excellent (01) Excellent
    ## 3046 (02) Very Good (02) Very Good
    ## 3047      (04) Fair      (04) Fair
    ## 3048      (03) Good (01) Excellent
    ## 3049      (03) Good      (04) Fair
    ## 3050      (04) Fair (01) Excellent
    ## 3051      (04) Fair      (03) Good
    ## 3052      (04) Fair      (03) Good
    ## 3053      (03) Good (02) Very Good
    ## 3054      (04) Fair      (03) Good
    ## 3055 (02) Very Good (02) Very Good
    ## 3056      (03) Good      (03) Good
    ## 3057 (01) Excellent (02) Very Good
    ## 3058 (02) Very Good      (05) Poor
    ## 3059      (04) Fair      (04) Fair
    ## 3060      (03) Good (02) Very Good
    ## 3061      (04) Fair (01) Excellent
    ## 3062      (04) Fair      (05) Poor
    ## 3063 (02) Very Good (01) Excellent
    ## 3064      (03) Good      (04) Fair
    ## 3065      (03) Good      (03) Good
    ## 3066      (03) Good (02) Very Good
    ## 3067 (01) Excellent (01) Excellent
    ## 3068      (03) Good      (03) Good
    ## 3069      (03) Good (02) Very Good
    ## 3070      (03) Good      (03) Good
    ## 3071 (02) Very Good (02) Very Good
    ## 3072 (01) Excellent (01) Excellent
    ## 3073 (02) Very Good (02) Very Good
    ## 3074      (03) Good (02) Very Good
    ## 3075      (03) Good      (03) Good
    ## 3076 (01) Excellent (02) Very Good
    ## 3077      (04) Fair      (04) Fair
    ## 3078 (02) Very Good      (03) Good
    ## 3079 (01) Excellent (02) Very Good
    ## 3080      (03) Good      (03) Good
    ## 3081      (04) Fair (02) Very Good
    ## 3082 (02) Very Good (02) Very Good
    ## 3083      (05) Poor (01) Excellent
    ## 3084 (02) Very Good      (04) Fair
    ## 3085      (03) Good (02) Very Good
    ## 3086      (03) Good      (03) Good
    ## 3087 (02) Very Good (02) Very Good
    ## 3088 (02) Very Good      (03) Good
    ## 3089      (03) Good      (03) Good
    ## 3090 (01) Excellent (02) Very Good
    ## 3091 (01) Excellent (01) Excellent
    ## 3092 (01) Excellent (01) Excellent
    ## 3093 (01) Excellent (02) Very Good
    ## 3094 (02) Very Good (01) Excellent
    ## 3095 (02) Very Good      (03) Good
    ## 3096 (01) Excellent (01) Excellent
    ## 3097 (02) Very Good      (04) Fair
    ## 3098      (03) Good      (03) Good
    ## 3099 (02) Very Good (02) Very Good
    ## 3100      (03) Good      (03) Good
    ## 3101 (02) Very Good (02) Very Good
    ## 3102 (01) Excellent (01) Excellent
    ## 3103      (03) Good      (03) Good
    ## 3104 (02) Very Good (02) Very Good
    ## 3105 (01) Excellent (01) Excellent
    ## 3106 (02) Very Good (02) Very Good
    ## 3107      (05) Poor      (04) Fair
    ## 3108      (03) Good      (03) Good
    ## 3109 (01) Excellent (01) Excellent
    ## 3110      (04) Fair      (04) Fair
    ## 3111 (02) Very Good (02) Very Good
    ## 3112      (03) Good (02) Very Good
    ## 3113 (02) Very Good      (03) Good
    ## 3114      (03) Good      (03) Good
    ## 3115      (04) Fair      (03) Good
    ## 3116      (04) Fair      (04) Fair
    ## 3117 (02) Very Good      (03) Good
    ## 3118 (01) Excellent (02) Very Good
    ## 3119      (03) Good      (03) Good
    ## 3120      (03) Good (02) Very Good
    ## 3121      (03) Good      (03) Good
    ## 3122 (02) Very Good (02) Very Good
    ## 3123 (01) Excellent (01) Excellent
    ## 3124 (02) Very Good (02) Very Good
    ## 3125 (02) Very Good (02) Very Good
    ## 3126 (02) Very Good (02) Very Good
    ## 3127 (01) Excellent (02) Very Good
    ## 3128 (02) Very Good (02) Very Good
    ## 3129 (01) Excellent (01) Excellent
    ## 3130 (02) Very Good (02) Very Good
    ## 3131 (01) Excellent (01) Excellent
    ## 3132 (02) Very Good (02) Very Good
    ## 3133      (04) Fair      (03) Good
    ## 3134      (03) Good      (03) Good
    ## 3135 (02) Very Good      (03) Good
    ## 3136 (02) Very Good      (03) Good
    ## 3137 (01) Excellent (01) Excellent
    ## 3138      (03) Good      (03) Good
    ## 3139      (03) Good      (03) Good
    ## 3140      (03) Good (01) Excellent
    ## 3141 (02) Very Good (02) Very Good
    ## 3142 (01) Excellent (01) Excellent
    ## 3143      (04) Fair      (03) Good
    ## 3144      (04) Fair (01) Excellent
    ## 3145 (01) Excellent (01) Excellent
    ## 3146 (02) Very Good (02) Very Good
    ## 3147      (03) Good      (03) Good
    ## 3148      (03) Good      (03) Good
    ## 3149 (02) Very Good      (03) Good
    ## 3150 (02) Very Good (02) Very Good
    ## 3151 (02) Very Good      (03) Good
    ## 3152 (02) Very Good (02) Very Good
    ## 3153 (01) Excellent (01) Excellent
    ## 3154 (02) Very Good (02) Very Good
    ## 3155 (02) Very Good (01) Excellent
    ## 3156 (01) Excellent (01) Excellent
    ## 3157      (03) Good      (03) Good
    ## 3158 (02) Very Good (02) Very Good
    ## 3159 (01) Excellent (02) Very Good
    ## 3160 (02) Very Good (02) Very Good
    ## 3161      (03) Good      (04) Fair
    ## 3162 (02) Very Good (01) Excellent
    ## 3163      (03) Good (02) Very Good
    ## 3164      (03) Good      (03) Good
    ## 3165      (03) Good (02) Very Good
    ## 3166 (02) Very Good (01) Excellent
    ## 3167      (03) Good      (03) Good
    ## 3168      (03) Good (01) Excellent
    ## 3169 (02) Very Good      (03) Good
    ## 3170      (04) Fair (02) Very Good
    ## 3171 (01) Excellent (02) Very Good
    ## 3172      (04) Fair      (04) Fair
    ## 3173 (01) Excellent (02) Very Good
    ## 3174 (02) Very Good      (03) Good
    ## 3175      (03) Good (02) Very Good
    ## 3176 (02) Very Good (02) Very Good
    ## 3177 (01) Excellent (01) Excellent
    ## 3178 (02) Very Good (02) Very Good
    ## 3179 (01) Excellent (01) Excellent
    ## 3180 (01) Excellent (01) Excellent
    ## 3181 (02) Very Good (02) Very Good
    ## 3182 (01) Excellent (02) Very Good
    ## 3183      (04) Fair      (03) Good
    ## 3184      (03) Good      (03) Good
    ## 3185      (03) Good (02) Very Good
    ## 3186      (03) Good      (03) Good
    ## 3187      (03) Good      (03) Good
    ## 3188 (02) Very Good      (03) Good
    ## 3189 (02) Very Good (02) Very Good
    ## 3190      (04) Fair      (04) Fair
    ## 3191 (02) Very Good (02) Very Good
    ## 3192 (01) Excellent (02) Very Good
    ## 3193 (02) Very Good (02) Very Good
    ## 3194      (03) Good (02) Very Good
    ## 3195 (02) Very Good      (03) Good
    ## 3196      (03) Good      (03) Good
    ## 3197      (03) Good      (04) Fair
    ## 3198 (01) Excellent (01) Excellent
    ## 3199 (02) Very Good (01) Excellent
    ## 3200      (04) Fair (02) Very Good
    ## 3201 (01) Excellent (02) Very Good
    ## 3202      (04) Fair      (03) Good
    ## 3203      (03) Good (02) Very Good
    ## 3204      (03) Good      (03) Good
    ## 3205 (02) Very Good (02) Very Good
    ## 3206      (03) Good (02) Very Good
    ## 3207 (02) Very Good      (03) Good
    ## 3208      (03) Good (02) Very Good
    ## 3209 (02) Very Good (02) Very Good
    ## 3210 (02) Very Good (01) Excellent
    ## 3211 (01) Excellent (02) Very Good
    ## 3212 (02) Very Good (02) Very Good
    ## 3213 (02) Very Good (02) Very Good
    ## 3214 (01) Excellent (01) Excellent
    ## 3215 (02) Very Good      (04) Fair
    ## 3216      (03) Good      (04) Fair
    ## 3217 (02) Very Good (01) Excellent
    ## 3218 (01) Excellent (01) Excellent
    ## 3219 (02) Very Good (01) Excellent
    ## 3220      (04) Fair      (04) Fair
    ## 3221 (02) Very Good (02) Very Good
    ## 3222      (04) Fair (01) Excellent
    ## 3223      (04) Fair      (03) Good
    ## 3224 (02) Very Good (02) Very Good
    ## 3225 (02) Very Good (02) Very Good
    ## 3226 (02) Very Good (01) Excellent
    ## 3227      (04) Fair (02) Very Good
    ## 3228 (01) Excellent      (04) Fair
    ## 3229 (01) Excellent (01) Excellent
    ## 3230 (01) Excellent (01) Excellent
    ## 3231 (02) Very Good (02) Very Good
    ## 3232 (01) Excellent (02) Very Good
    ## 3233 (02) Very Good (02) Very Good
    ## 3234 (02) Very Good (02) Very Good
    ## 3235      (04) Fair      (04) Fair
    ## 3236      (04) Fair      (04) Fair
    ## 3237 (01) Excellent (02) Very Good
    ## 3238      (03) Good      (03) Good
    ## 3239 (02) Very Good      (03) Good
    ## 3240 (01) Excellent      (03) Good
    ## 3241 (01) Excellent (01) Excellent
    ## 3242      (03) Good (01) Excellent
    ## 3243      (03) Good      (03) Good
    ## 3244      (03) Good      (04) Fair
    ## 3245      (03) Good (02) Very Good
    ## 3246      (03) Good      (04) Fair
    ## 3247      (03) Good      (03) Good
    ## 3248      (03) Good      (03) Good
    ## 3249      (03) Good      (04) Fair
    ## 3250 (02) Very Good (02) Very Good
    ## 3251      (03) Good      (03) Good
    ## 3252 (01) Excellent (01) Excellent
    ## 3253 (02) Very Good (02) Very Good
    ## 3254 (01) Excellent (02) Very Good
    ## 3255      (05) Poor      (04) Fair
    ## 3256 (02) Very Good (02) Very Good
    ## 3257 (02) Very Good (02) Very Good
    ## 3258 (02) Very Good      (03) Good
    ## 3259 (02) Very Good (02) Very Good
    ## 3260      (03) Good (01) Excellent
    ## 3261      (03) Good (02) Very Good
    ## 3262      (03) Good (02) Very Good
    ## 3263 (02) Very Good (02) Very Good
    ## 3264      (03) Good      (03) Good
    ## 3265 (01) Excellent (01) Excellent
    ## 3266 (01) Excellent (01) Excellent
    ## 3267 (02) Very Good      (04) Fair
    ## 3268 (01) Excellent (01) Excellent
    ## 3269 (01) Excellent (01) Excellent
    ## 3270 (02) Very Good      (03) Good
    ## 3271      (03) Good      (03) Good
    ## 3272 (02) Very Good      (03) Good
    ## 3273 (01) Excellent (01) Excellent
    ## 3274      (03) Good (02) Very Good
    ## 3275      (04) Fair      (03) Good
    ## 3276 (02) Very Good      (03) Good
    ## 3277      (03) Good      (03) Good
    ## 3278      (03) Good (01) Excellent
    ## 3279      (03) Good      (03) Good
    ## 3280 (02) Very Good      (03) Good
    ## 3281      (03) Good      (03) Good
    ## 3282 (02) Very Good (01) Excellent
    ## 3283 (02) Very Good      (03) Good
    ## 3284      (03) Good (02) Very Good
    ## 3285      (03) Good      (03) Good
    ## 3286 (02) Very Good (02) Very Good
    ## 3287      (03) Good      (03) Good
    ## 3288      (03) Good (02) Very Good
    ## 3289      (05) Poor      (03) Good
    ## 3290      (03) Good (02) Very Good
    ## 3291 (01) Excellent (01) Excellent
    ## 3292 (02) Very Good (02) Very Good
    ## 3293 (01) Excellent (01) Excellent
    ## 3294      (03) Good      (03) Good
    ## 3295 (02) Very Good (02) Very Good
    ## 3296 (01) Excellent (01) Excellent
    ## 3297 (02) Very Good (01) Excellent
    ## 3298 (01) Excellent      (03) Good
    ## 3299 (01) Excellent (01) Excellent
    ## 3300 (01) Excellent (01) Excellent
    ## 3301      (03) Good (01) Excellent
    ## 3302      (03) Good (02) Very Good
    ## 3303      (04) Fair      (04) Fair
    ## 3304 (02) Very Good      (03) Good
    ## 3305      (03) Good      (03) Good
    ## 3306 (01) Excellent (01) Excellent
    ## 3307 (01) Excellent (01) Excellent
    ## 3308 (02) Very Good (02) Very Good
    ## 3309      (04) Fair      (04) Fair
    ## 3310      (03) Good      (03) Good
    ## 3311      (03) Good      (03) Good
    ## 3312 (02) Very Good (01) Excellent
    ## 3313 (02) Very Good (02) Very Good
    ## 3314      (03) Good      (03) Good
    ## 3315 (02) Very Good (02) Very Good
    ## 3316      (05) Poor      (03) Good
    ## 3317 (01) Excellent (01) Excellent
    ## 3318      (03) Good (02) Very Good
    ## 3319      (04) Fair      (04) Fair
    ## 3320 (02) Very Good      (03) Good
    ## 3321 (02) Very Good (02) Very Good
    ## 3322 (02) Very Good (02) Very Good
    ## 3323      (03) Good      (03) Good
    ## 3324 (02) Very Good      (03) Good
    ## 3325 (02) Very Good (02) Very Good
    ## 3326      (03) Good      (04) Fair
    ## 3327      (03) Good      (04) Fair
    ## 3328      (03) Good      (03) Good
    ## 3329 (01) Excellent (01) Excellent
    ## 3330 (02) Very Good (01) Excellent
    ## 3331 (02) Very Good (02) Very Good
    ## 3332      (03) Good      (03) Good
    ## 3333      (04) Fair      (04) Fair
    ## 3334 (02) Very Good      (04) Fair
    ## 3335      (03) Good (02) Very Good
    ## 3336 (02) Very Good (02) Very Good
    ## 3337      (03) Good      (03) Good
    ## 3338      (03) Good      (03) Good
    ## 3339 (02) Very Good (02) Very Good
    ## 3340 (01) Excellent (01) Excellent
    ## 3341      (03) Good      (03) Good
    ## 3342 (01) Excellent (01) Excellent
    ## 3343 (02) Very Good (02) Very Good
    ## 3344 (02) Very Good      (03) Good
    ## 3345 (02) Very Good (02) Very Good
    ## 3346 (01) Excellent (02) Very Good
    ## 3347      (04) Fair      (04) Fair
    ## 3348 (01) Excellent (01) Excellent
    ## 3349 (02) Very Good (02) Very Good
    ## 3350 (02) Very Good (02) Very Good
    ## 3351 (01) Excellent (02) Very Good
    ## 3352 (02) Very Good (02) Very Good
    ## 3353 (01) Excellent      (03) Good
    ## 3354      (04) Fair (01) Excellent
    ## 3355 (01) Excellent (02) Very Good
    ## 3356 (01) Excellent (02) Very Good
    ## 3357      (04) Fair      (04) Fair
    ## 3358      (05) Poor      (03) Good
    ## 3359      (03) Good      (03) Good
    ## 3360 (01) Excellent (01) Excellent
    ## 3361 (02) Very Good (01) Excellent
    ## 3362 (01) Excellent (01) Excellent
    ## 3363      (04) Fair (02) Very Good
    ## 3364      (03) Good      (04) Fair
    ## 3365 (01) Excellent (01) Excellent
    ## 3366      (03) Good      (03) Good
    ## 3367      (05) Poor      (05) Poor
    ## 3368 (02) Very Good (02) Very Good
    ## 3369      (03) Good      (03) Good
    ## 3370      (05) Poor      (05) Poor
    ## 3371      (03) Good      (03) Good
    ## 3372      (03) Good      (03) Good
    ## 3373 (02) Very Good      (03) Good
    ## 3374      (03) Good (02) Very Good
    ## 3375      (05) Poor      (05) Poor
    ## 3376      (05) Poor      (05) Poor
    ## 3377 (02) Very Good      (04) Fair
    ## 3378      (04) Fair      (04) Fair
    ## 3379 (02) Very Good (02) Very Good
    ## 3380 (02) Very Good (02) Very Good
    ## 3381 (02) Very Good (02) Very Good
    ## 3382 (02) Very Good      (03) Good
    ## 3383 (02) Very Good (02) Very Good
    ## 3384 (02) Very Good      (05) Poor
    ## 3385      (04) Fair (02) Very Good
    ## 3386      (04) Fair      (04) Fair
    ## 3387 (02) Very Good (02) Very Good
    ## 3388      (04) Fair      (03) Good
    ## 3389      (03) Good (02) Very Good
    ## 3390      (03) Good (02) Very Good
    ## 3391 (02) Very Good (02) Very Good
    ## 3392 (02) Very Good (02) Very Good
    ## 3393      (03) Good (02) Very Good
    ## 3394      (03) Good      (03) Good
    ## 3395 (01) Excellent      (03) Good
    ## 3396      (03) Good      (03) Good
    ## 3397 (01) Excellent (02) Very Good
    ## 3398      (04) Fair      (04) Fair
    ## 3399 (01) Excellent (01) Excellent
    ## 3400 (02) Very Good (02) Very Good
    ## 3401      (03) Good (02) Very Good
    ## 3402      (03) Good      (03) Good
    ## 3403      (03) Good (02) Very Good
    ## 3404 (02) Very Good      (03) Good
    ## 3405 (02) Very Good (01) Excellent
    ## 3406 (02) Very Good (02) Very Good
    ## 3407      (04) Fair (02) Very Good
    ## 3408      (04) Fair      (04) Fair
    ## 3409 (02) Very Good (02) Very Good
    ## 3410 (01) Excellent (01) Excellent
    ## 3411      (03) Good (02) Very Good
    ## 3412      (03) Good      (03) Good
    ## 3413      (03) Good      (03) Good
    ## 3414 (02) Very Good      (03) Good
    ## 3415      (05) Poor (02) Very Good
    ## 3416      (04) Fair (01) Excellent
    ## 3417 (02) Very Good (02) Very Good
    ## 3418      (03) Good (02) Very Good
    ## 3419 (02) Very Good (02) Very Good
    ## 3420 (01) Excellent (01) Excellent
    ## 3421 (01) Excellent (01) Excellent
    ## 3422 (02) Very Good (02) Very Good
    ## 3423      (03) Good      (03) Good
    ## 3424 (02) Very Good (02) Very Good
    ## 3425      (03) Good      (03) Good
    ## 3426      (03) Good (01) Excellent
    ## 3427      (03) Good (02) Very Good
    ## 3428      (03) Good      (03) Good
    ## 3429 (02) Very Good (02) Very Good
    ## 3430      (03) Good      (03) Good
    ## 3431      (03) Good      (03) Good
    ## 3432 (02) Very Good (02) Very Good
    ## 3433 (02) Very Good (01) Excellent
    ## 3434      (04) Fair (02) Very Good
    ## 3435 (01) Excellent (02) Very Good
    ## 3436 (02) Very Good (01) Excellent
    ## 3437 (02) Very Good      (03) Good
    ## 3438      (03) Good (02) Very Good
    ## 3439 (01) Excellent (01) Excellent
    ## 3440 (01) Excellent (01) Excellent
    ## 3441      (03) Good (02) Very Good
    ## 3442      (03) Good      (03) Good
    ## 3443      (04) Fair      (03) Good
    ## 3444 (01) Excellent (01) Excellent
    ## 3445      (05) Poor      (03) Good
    ## 3446 (01) Excellent (02) Very Good
    ## 3447      (04) Fair (02) Very Good
    ## 3448      (05) Poor      (05) Poor
    ## 3449      (05) Poor (02) Very Good
    ## 3450      (03) Good      (03) Good
    ## 3451      (03) Good (02) Very Good
    ## 3452 (02) Very Good      (04) Fair
    ## 3453      (04) Fair      (03) Good
    ## 3454      (03) Good      (03) Good
    ## 3455 (02) Very Good (02) Very Good
    ## 3456      (04) Fair (02) Very Good
    ## 3457      (03) Good      (03) Good
    ## 3458 (02) Very Good      (03) Good
    ## 3459      (05) Poor      (05) Poor
    ## 3460      (04) Fair (01) Excellent
    ## 3461 (02) Very Good (01) Excellent
    ## 3462 (02) Very Good (02) Very Good
    ## 3463      (03) Good (01) Excellent
    ## 3464      (04) Fair      (04) Fair
    ## 3465      (05) Poor      (04) Fair
    ## 3466      (03) Good      (03) Good
    ## 3467 (02) Very Good (01) Excellent
    ## 3468      (03) Good (01) Excellent
    ## 3469      (03) Good (02) Very Good
    ## 3470      (03) Good (02) Very Good
    ## 3471      (03) Good      (04) Fair
    ## 3472 (02) Very Good (02) Very Good
    ## 3473      (04) Fair (02) Very Good
    ## 3474      (04) Fair      (04) Fair
    ## 3475      (03) Good (02) Very Good
    ## 3476 (01) Excellent (01) Excellent
    ## 3477 (01) Excellent (01) Excellent
    ## 3478      (03) Good      (03) Good
    ## 3479 (02) Very Good (01) Excellent
    ## 3480      (04) Fair (01) Excellent
    ## 3481      (05) Poor (01) Excellent
    ## 3482      (03) Good      (03) Good
    ## 3483 (02) Very Good      (04) Fair
    ## 3484      (03) Good      (03) Good
    ## 3485 (02) Very Good (02) Very Good
    ## 3486 (01) Excellent (01) Excellent
    ## 3487 (02) Very Good (01) Excellent
    ## 3488 (02) Very Good (02) Very Good
    ## 3489 (02) Very Good (02) Very Good
    ## 3490      (04) Fair      (04) Fair
    ## 3491      (04) Fair (02) Very Good
    ## 3492      (04) Fair (02) Very Good
    ## 3493 (02) Very Good      (03) Good
    ## 3494      (04) Fair      (03) Good
    ## 3495 (02) Very Good (02) Very Good
    ## 3496 (02) Very Good (01) Excellent
    ## 3497 (02) Very Good (02) Very Good
    ## 3498      (03) Good      (03) Good
    ## 3499 (02) Very Good (02) Very Good
    ## 3500      (03) Good (01) Excellent
    ## 3501 (02) Very Good      (03) Good
    ## 3502 (02) Very Good (02) Very Good
    ## 3503 (02) Very Good      (03) Good
    ## 3504 (02) Very Good      (04) Fair
    ## 3505 (02) Very Good (02) Very Good
    ## 3506      (04) Fair      (03) Good
    ## 3507 (02) Very Good      (03) Good
    ## 3508      (03) Good (02) Very Good
    ## 3509      (04) Fair (02) Very Good
    ## 3510      (04) Fair      (03) Good
    ## 3511 (02) Very Good (02) Very Good
    ## 3512 (01) Excellent (01) Excellent
    ## 3513      (03) Good      (03) Good
    ## 3514      (04) Fair      (05) Poor
    ## 3515 (02) Very Good (02) Very Good
    ## 3516      (03) Good      (03) Good
    ## 3517      (03) Good (02) Very Good
    ## 3518 (02) Very Good (01) Excellent
    ## 3519 (01) Excellent (01) Excellent
    ## 3520      (03) Good (02) Very Good
    ## 3521      (03) Good      (03) Good
    ## 3522      (03) Good (02) Very Good
    ## 3523 (02) Very Good (02) Very Good
    ## 3524 (01) Excellent      (03) Good
    ## 3525      (05) Poor      (04) Fair
    ## 3526 (02) Very Good (02) Very Good
    ## 3527 (02) Very Good (02) Very Good
    ## 3528      (03) Good      (03) Good
    ## 3529 (01) Excellent (01) Excellent
    ## 3530 (02) Very Good (02) Very Good
    ## 3531 (02) Very Good (02) Very Good
    ## 3532 (02) Very Good (02) Very Good
    ## 3533      (03) Good      (03) Good
    ## 3534 (01) Excellent (01) Excellent
    ## 3535      (04) Fair      (03) Good
    ## 3536 (01) Excellent (01) Excellent
    ## 3537 (01) Excellent (02) Very Good
    ## 3538      (03) Good (02) Very Good
    ## 3539      (03) Good (02) Very Good
    ## 3540 (02) Very Good (02) Very Good
    ## 3541 (01) Excellent (01) Excellent
    ## 3542 (02) Very Good (02) Very Good
    ## 3543      (03) Good      (03) Good
    ## 3544 (02) Very Good (01) Excellent
    ## 3545 (02) Very Good      (03) Good
    ## 3546 (01) Excellent (01) Excellent
    ## 3547      (04) Fair (01) Excellent
    ## 3548 (02) Very Good (02) Very Good
    ## 3549 (02) Very Good (02) Very Good
    ## 3550      (03) Good      (03) Good
    ## 3551 (01) Excellent (02) Very Good
    ## 3552 (01) Excellent (01) Excellent
    ## 3553      (03) Good (01) Excellent
    ## 3554      (04) Fair (01) Excellent
    ## 3555 (02) Very Good (02) Very Good
    ## 3556 (01) Excellent (01) Excellent
    ## 3557      (03) Good (02) Very Good
    ## 3558 (02) Very Good (02) Very Good
    ## 3559 (02) Very Good      (03) Good
    ## 3560 (02) Very Good (01) Excellent
    ## 3561      (04) Fair (02) Very Good
    ## 3562      (03) Good (02) Very Good
    ## 3563      (04) Fair      (04) Fair
    ## 3564      (03) Good      (03) Good
    ## 3565 (02) Very Good      (03) Good
    ## 3566      (03) Good      (04) Fair
    ## 3567      (04) Fair (02) Very Good
    ## 3568 (02) Very Good (02) Very Good
    ## 3569      (04) Fair      (03) Good
    ## 3570 (02) Very Good (02) Very Good
    ## 3571      (05) Poor      (04) Fair
    ## 3572      (03) Good (02) Very Good
    ## 3573 (02) Very Good (01) Excellent
    ## 3574 (01) Excellent (02) Very Good
    ## 3575      (03) Good      (03) Good
    ## 3576 (02) Very Good (02) Very Good
    ## 3577 (02) Very Good (02) Very Good
    ## 3578      (03) Good      (04) Fair
    ## 3579 (02) Very Good (02) Very Good
    ## 3580      (03) Good      (03) Good
    ## 3581      (03) Good      (03) Good
    ## 3582      (03) Good      (03) Good
    ## 3583 (02) Very Good (02) Very Good
    ## 3584 (01) Excellent (01) Excellent
    ## 3585      (03) Good      (04) Fair
    ## 3586 (02) Very Good (02) Very Good
    ## 3587      (03) Good      (04) Fair
    ## 3588      (04) Fair      (04) Fair
    ## 3589 (02) Very Good      (03) Good
    ## 3590      (05) Poor      (04) Fair
    ## 3591 (02) Very Good (02) Very Good
    ## 3592 (02) Very Good (02) Very Good
    ## 3593 (02) Very Good (01) Excellent
    ## 3594 (02) Very Good (01) Excellent
    ## 3595 (02) Very Good (01) Excellent
    ## 3596 (01) Excellent (01) Excellent
    ## 3597 (02) Very Good (02) Very Good
    ## 3598 (01) Excellent (01) Excellent
    ## 3599 (02) Very Good (01) Excellent
    ## 3600      (05) Poor (02) Very Good
    ## 3601      (03) Good      (03) Good
    ## 3602      (03) Good      (03) Good
    ## 3603 (02) Very Good (02) Very Good
    ## 3604 (02) Very Good (01) Excellent
    ## 3605 (01) Excellent (01) Excellent
    ## 3606 (02) Very Good      (03) Good
    ## 3607 (01) Excellent (01) Excellent
    ## 3608 (02) Very Good (02) Very Good
    ## 3609      (03) Good (01) Excellent
    ## 3610      (05) Poor (02) Very Good
    ## 3611 (02) Very Good (02) Very Good
    ## 3612 (01) Excellent (01) Excellent
    ## 3613 (02) Very Good (02) Very Good
    ## 3614 (02) Very Good (02) Very Good
    ## 3615 (01) Excellent (01) Excellent
    ## 3616      (04) Fair (02) Very Good
    ## 3617      (03) Good (01) Excellent
    ## 3618 (02) Very Good (01) Excellent
    ## 3619      (04) Fair      (03) Good
    ## 3620      (03) Good      (04) Fair
    ## 3621      (03) Good      (04) Fair
    ## 3622 (01) Excellent (01) Excellent
    ## 3623      (03) Good (02) Very Good
    ## 3624 (02) Very Good (02) Very Good
    ## 3625 (01) Excellent (02) Very Good
    ## 3626      (03) Good      (03) Good
    ## 3627 (02) Very Good (01) Excellent
    ## 3628      (03) Good      (03) Good
    ## 3629 (02) Very Good (02) Very Good
    ## 3630 (01) Excellent (02) Very Good
    ## 3631      (03) Good      (03) Good
    ## 3632 (02) Very Good (01) Excellent
    ## 3633      (03) Good      (03) Good
    ## 3634      (04) Fair      (03) Good
    ## 3635      (04) Fair (02) Very Good
    ## 3636      (03) Good (02) Very Good
    ## 3637      (03) Good (01) Excellent
    ## 3638      (04) Fair      (03) Good
    ## 3639 (02) Very Good (02) Very Good
    ## 3640      (03) Good      (03) Good
    ## 3641      (03) Good (02) Very Good
    ## 3642 (01) Excellent (02) Very Good
    ## 3643      (03) Good      (03) Good
    ## 3644      (04) Fair      (03) Good
    ## 3645      (04) Fair      (03) Good
    ## 3646 (01) Excellent (01) Excellent
    ## 3647      (03) Good (02) Very Good
    ## 3648 (01) Excellent (01) Excellent
    ## 3649 (02) Very Good      (03) Good
    ## 3650      (03) Good (01) Excellent
    ## 3651 (02) Very Good (02) Very Good
    ## 3652      (03) Good (02) Very Good
    ## 3653 (01) Excellent      (03) Good
    ## 3654      (03) Good (02) Very Good
    ## 3655 (02) Very Good (01) Excellent
    ## 3656 (02) Very Good (01) Excellent
    ## 3657 (02) Very Good (02) Very Good
    ## 3658 (01) Excellent (02) Very Good
    ## 3659 (02) Very Good (02) Very Good
    ## 3660 (01) Excellent (02) Very Good
    ## 3661      (03) Good (01) Excellent
    ## 3662      (03) Good (02) Very Good
    ## 3663 (02) Very Good (01) Excellent
    ## 3664 (02) Very Good (02) Very Good
    ## 3665 (01) Excellent (01) Excellent
    ## 3666      (04) Fair      (04) Fair
    ## 3667 (02) Very Good (02) Very Good
    ## 3668      (03) Good      (03) Good
    ## 3669      (03) Good      (03) Good
    ## 3670      (04) Fair (02) Very Good
    ## 3671      (03) Good      (03) Good
    ## 3672 (01) Excellent (02) Very Good
    ## 3673      (03) Good      (03) Good
    ## 3674 (02) Very Good (02) Very Good
    ## 3675 (01) Excellent      (03) Good
    ## 3676      (03) Good      (04) Fair
    ## 3677 (02) Very Good (02) Very Good
    ## 3678 (02) Very Good (02) Very Good
    ## 3679 (01) Excellent (01) Excellent
    ## 3680      (03) Good      (03) Good
    ## 3681 (01) Excellent (01) Excellent
    ## 3682      (04) Fair      (03) Good
    ## 3683      (03) Good (02) Very Good
    ## 3684      (04) Fair      (03) Good
    ## 3685      (03) Good      (03) Good
    ## 3686 (02) Very Good (02) Very Good
    ## 3687      (05) Poor      (05) Poor
    ## 3688      (05) Poor      (03) Good
    ## 3689      (05) Poor      (03) Good
    ## 3690      (03) Good      (04) Fair
    ## 3691      (03) Good      (03) Good
    ## 3692 (02) Very Good      (04) Fair
    ## 3693      (03) Good (02) Very Good
    ## 3694      (03) Good (01) Excellent
    ## 3695      (03) Good (02) Very Good
    ## 3696      (04) Fair      (03) Good
    ## 3697 (02) Very Good      (03) Good
    ## 3698 (02) Very Good (01) Excellent
    ## 3699 (01) Excellent (01) Excellent
    ## 3700      (05) Poor      (04) Fair
    ## 3701      (04) Fair (02) Very Good
    ## 3702      (04) Fair      (04) Fair
    ## 3703 (02) Very Good (02) Very Good
    ## 3704 (02) Very Good      (03) Good
    ## 3705 (02) Very Good (02) Very Good
    ## 3706 (01) Excellent (01) Excellent
    ## 3707      (03) Good (02) Very Good
    ## 3708 (02) Very Good (02) Very Good
    ## 3709      (05) Poor      (03) Good
    ## 3710      (03) Good      (03) Good
    ## 3711      (04) Fair      (04) Fair
    ## 3712      (04) Fair      (03) Good
    ## 3713      (03) Good      (03) Good
    ## 3714      (04) Fair (01) Excellent
    ## 3715      (04) Fair      (04) Fair
    ## 3716 (02) Very Good (02) Very Good
    ## 3717      (05) Poor (01) Excellent
    ## 3718 (02) Very Good (02) Very Good
    ## 3719      (04) Fair      (04) Fair
    ## 3720      (03) Good      (03) Good
    ## 3721      (03) Good (02) Very Good
    ## 3722      (04) Fair (01) Excellent
    ## 3723 (02) Very Good (02) Very Good
    ## 3724      (05) Poor      (03) Good
    ## 3725      (04) Fair      (04) Fair
    ## 3726      (03) Good      (03) Good
    ## 3727 (01) Excellent (01) Excellent
    ## 3728 (02) Very Good (02) Very Good
    ## 3729 (02) Very Good (02) Very Good
    ## 3730      (04) Fair      (05) Poor
    ## 3731      (04) Fair      (04) Fair
    ## 3732 (02) Very Good (02) Very Good
    ## 3733      (03) Good      (03) Good
    ## 3734      (03) Good (02) Very Good
    ## 3735 (02) Very Good (02) Very Good
    ## 3736      (05) Poor      (05) Poor
    ## 3737      (04) Fair      (03) Good
    ## 3738      (03) Good      (03) Good
    ## 3739 (01) Excellent (01) Excellent
    ## 3740      (04) Fair      (04) Fair
    ## 3741      (03) Good      (03) Good
    ## 3742 (02) Very Good (02) Very Good
    ## 3743      (04) Fair      (03) Good
    ## 3744      (03) Good      (03) Good
    ## 3745      (03) Good      (03) Good
    ## 3746      (03) Good      (03) Good
    ## 3747 (02) Very Good      (03) Good
    ## 3748 (02) Very Good      (03) Good
    ## 3749 (02) Very Good (01) Excellent
    ## 3750      (03) Good      (03) Good
    ## 3751 (01) Excellent (01) Excellent
    ## 3752 (02) Very Good      (03) Good
    ## 3753 (02) Very Good (02) Very Good
    ## 3754 (02) Very Good (02) Very Good
    ## 3755 (02) Very Good (01) Excellent
    ## 3756      (04) Fair      (04) Fair
    ## 3757      (04) Fair (02) Very Good
    ## 3758      (03) Good      (03) Good
    ## 3759      (03) Good      (03) Good
    ## 3760      (04) Fair      (04) Fair
    ## 3761 (02) Very Good      (04) Fair
    ## 3762 (01) Excellent (02) Very Good
    ## 3763      (04) Fair      (03) Good
    ## 3764      (03) Good (01) Excellent
    ## 3765 (02) Very Good (02) Very Good
    ## 3766 (02) Very Good (02) Very Good
    ## 3767 (01) Excellent (01) Excellent
    ## 3768      (03) Good (02) Very Good
    ## 3769 (02) Very Good (02) Very Good
    ## 3770      (03) Good (02) Very Good
    ## 3771 (02) Very Good (02) Very Good
    ## 3772 (01) Excellent (02) Very Good
    ## 3773      (03) Good (02) Very Good
    ## 3774 (02) Very Good (02) Very Good
    ## 3775      (03) Good (02) Very Good
    ## 3776      (03) Good      (04) Fair
    ## 3777      (05) Poor      (05) Poor
    ## 3778 (02) Very Good (02) Very Good
    ## 3779 (01) Excellent (02) Very Good
    ## 3780      (03) Good      (03) Good
    ## 3781      (04) Fair      (03) Good
    ## 3782 (01) Excellent (02) Very Good
    ## 3783 (02) Very Good      (04) Fair
    ## 3784 (02) Very Good (02) Very Good
    ## 3785      (03) Good (02) Very Good
    ## 3786      (03) Good (01) Excellent
    ## 3787      (03) Good      (03) Good
    ## 3788      (03) Good      (03) Good
    ## 3789 (02) Very Good      (03) Good
    ## 3790 (02) Very Good (02) Very Good
    ## 3791      (03) Good      (03) Good
    ## 3792      (03) Good      (03) Good
    ## 3793      (04) Fair (02) Very Good
    ## 3794      (03) Good      (03) Good
    ## 3795      (04) Fair      (05) Poor
    ## 3796      (03) Good      (03) Good
    ## 3797 (02) Very Good (02) Very Good
    ## 3798 (02) Very Good (02) Very Good
    ## 3799 (02) Very Good      (03) Good
    ## 3800      (03) Good      (03) Good
    ## 3801      (03) Good      (05) Poor
    ## 3802      (03) Good (02) Very Good
    ## 3803 (02) Very Good      (03) Good
    ## 3804      (04) Fair (02) Very Good
    ## 3805      (03) Good (02) Very Good
    ## 3806 (01) Excellent (01) Excellent
    ## 3807      (04) Fair      (03) Good
    ## 3808 (02) Very Good (02) Very Good
    ## 3809      (03) Good      (03) Good
    ## 3810 (02) Very Good (01) Excellent
    ## 3811 (02) Very Good      (03) Good
    ## 3812 (02) Very Good (02) Very Good
    ## 3813      (04) Fair      (04) Fair
    ## 3814 (02) Very Good (02) Very Good
    ## 3815 (02) Very Good (02) Very Good
    ## 3816 (02) Very Good (02) Very Good
    ## 3817 (01) Excellent      (03) Good
    ## 3818      (03) Good (02) Very Good
    ## 3819      (03) Good      (03) Good
    ## 3820 (02) Very Good      (03) Good
    ## 3821      (03) Good      (03) Good
    ## 3822 (02) Very Good (01) Excellent
    ## 3823      (03) Good (02) Very Good
    ## 3824 (01) Excellent (01) Excellent
    ## 3825 (01) Excellent (01) Excellent
    ## 3826 (02) Very Good (02) Very Good
    ## 3827 (01) Excellent (02) Very Good
    ## 3828      (03) Good      (03) Good
    ## 3829 (02) Very Good (01) Excellent
    ## 3830 (01) Excellent (01) Excellent
    ## 3831 (02) Very Good (02) Very Good
    ## 3832 (02) Very Good (02) Very Good
    ## 3833 (02) Very Good (02) Very Good
    ## 3834 (02) Very Good (02) Very Good
    ## 3835 (01) Excellent (01) Excellent
    ## 3836 (01) Excellent (01) Excellent
    ## 3837 (02) Very Good      (03) Good
    ## 3838      (04) Fair      (04) Fair
    ## 3839      (04) Fair      (04) Fair
    ## 3840 (01) Excellent (02) Very Good
    ## 3841 (02) Very Good      (03) Good
    ## 3842      (05) Poor      (04) Fair
    ## 3843      (04) Fair      (03) Good
    ## 3844 (02) Very Good (02) Very Good
    ## 3845      (03) Good (01) Excellent
    ## 3846      (03) Good (01) Excellent
    ## 3847 (02) Very Good (02) Very Good
    ## 3848 (02) Very Good (01) Excellent
    ## 3849      (04) Fair      (03) Good
    ## 3850      (03) Good (02) Very Good
    ## 3851      (05) Poor      (04) Fair
    ## 3852      (03) Good      (03) Good
    ## 3853 (02) Very Good      (03) Good
    ## 3854      (03) Good      (03) Good
    ## 3855 (02) Very Good      (04) Fair
    ## 3856      (03) Good      (04) Fair
    ## 3857 (02) Very Good      (03) Good
    ## 3858      (03) Good      (03) Good
    ## 3859      (05) Poor      (05) Poor
    ## 3860 (01) Excellent (02) Very Good
    ## 3861      (03) Good      (03) Good
    ## 3862      (03) Good (02) Very Good
    ## 3863      (03) Good      (03) Good
    ## 3864 (02) Very Good (02) Very Good
    ## 3865 (02) Very Good      (03) Good
    ## 3866 (01) Excellent (01) Excellent
    ## 3867 (02) Very Good (01) Excellent
    ## 3868      (03) Good      (03) Good
    ## 3869 (01) Excellent (01) Excellent
    ## 3870      (03) Good      (03) Good
    ## 3871      (03) Good      (03) Good
    ## 3872      (03) Good      (03) Good
    ## 3873 (02) Very Good      (03) Good
    ## 3874 (01) Excellent (01) Excellent
    ## 3875 (02) Very Good      (03) Good
    ## 3876 (02) Very Good (01) Excellent
    ## 3877      (03) Good      (03) Good
    ## 3878 (01) Excellent (02) Very Good
    ## 3879      (03) Good      (03) Good
    ## 3880      (03) Good (02) Very Good
    ## 3881 (02) Very Good (02) Very Good
    ## 3882      (03) Good (02) Very Good
    ## 3883 (02) Very Good (02) Very Good
    ## 3884      (04) Fair (02) Very Good
    ## 3885      (03) Good      (03) Good
    ## 3886      (03) Good (02) Very Good
    ## 3887 (02) Very Good (01) Excellent
    ## 3888      (03) Good      (03) Good
    ## 3889 (02) Very Good (02) Very Good
    ## 3890 (02) Very Good      (03) Good
    ## 3891      (03) Good (02) Very Good
    ## 3892      (05) Poor      (05) Poor
    ## 3893      (03) Good (02) Very Good
    ## 3894 (02) Very Good (01) Excellent
    ## 3895      (05) Poor      (04) Fair
    ## 3896      (03) Good (02) Very Good
    ## 3897 (02) Very Good (01) Excellent
    ## 3898      (03) Good      (03) Good
    ## 3899 (01) Excellent (01) Excellent
    ## 3900      (03) Good      (03) Good
    ## 3901 (01) Excellent (02) Very Good
    ## 3902 (02) Very Good      (03) Good
    ## 3903 (02) Very Good      (03) Good
    ## 3904      (03) Good      (03) Good
    ## 3905      (03) Good      (03) Good
    ## 3906      (03) Good (02) Very Good
    ## 3907 (02) Very Good      (03) Good
    ## 3908      (03) Good      (03) Good
    ## 3909 (01) Excellent (01) Excellent
    ## 3910      (03) Good (02) Very Good
    ## 3911 (01) Excellent (01) Excellent
    ## 3912      (03) Good (02) Very Good
    ## 3913      (04) Fair      (03) Good
    ## 3914 (02) Very Good (02) Very Good
    ## 3915      (05) Poor (02) Very Good
    ## 3916      (04) Fair (02) Very Good
    ## 3917      (03) Good (02) Very Good
    ## 3918      (04) Fair      (03) Good
    ## 3919      (03) Good (01) Excellent
    ## 3920      (03) Good      (03) Good
    ## 3921      (03) Good (02) Very Good
    ## 3922      (03) Good      (03) Good
    ## 3923 (01) Excellent (02) Very Good
    ## 3924      (05) Poor (01) Excellent
    ## 3925      (03) Good      (03) Good
    ## 3926      (03) Good (01) Excellent
    ## 3927 (02) Very Good (02) Very Good
    ## 3928 (02) Very Good (02) Very Good
    ## 3929 (02) Very Good (01) Excellent
    ## 3930      (03) Good      (04) Fair
    ## 3931 (02) Very Good (02) Very Good
    ## 3932      (03) Good (01) Excellent
    ## 3933 (02) Very Good (02) Very Good
    ## 3934 (01) Excellent      (03) Good
    ## 3935 (01) Excellent (01) Excellent
    ## 3936      (04) Fair (02) Very Good
    ## 3937 (02) Very Good (02) Very Good
    ## 3938 (01) Excellent      (03) Good
    ## 3939 (02) Very Good (02) Very Good
    ## 3940      (03) Good      (03) Good
    ## 3941 (02) Very Good      (03) Good
    ## 3942 (02) Very Good (01) Excellent
    ## 3943      (03) Good      (03) Good
    ## 3944 (01) Excellent (02) Very Good
    ## 3945 (02) Very Good (01) Excellent
    ## 3946 (01) Excellent (01) Excellent
    ## 3947      (04) Fair      (03) Good
    ## 3948 (01) Excellent (01) Excellent
    ## 3949 (02) Very Good      (03) Good
    ## 3950 (02) Very Good (02) Very Good
    ## 3951      (03) Good (02) Very Good
    ## 3952      (04) Fair      (03) Good
    ## 3953 (02) Very Good (01) Excellent
    ## 3954      (03) Good      (03) Good
    ## 3955      (03) Good (01) Excellent
    ## 3956      (03) Good (02) Very Good
    ## 3957 (02) Very Good (01) Excellent
    ## 3958      (03) Good      (03) Good
    ## 3959 (01) Excellent (01) Excellent
    ## 3960      (03) Good      (03) Good
    ## 3961 (02) Very Good (02) Very Good
    ## 3962      (03) Good      (03) Good
    ## 3963      (03) Good      (03) Good
    ## 3964      (04) Fair (02) Very Good
    ## 3965 (02) Very Good (01) Excellent
    ## 3966 (02) Very Good (01) Excellent
    ## 3967      (03) Good (02) Very Good
    ## 3968 (02) Very Good      (03) Good
    ## 3969      (03) Good      (03) Good
    ## 3970 (02) Very Good (02) Very Good
    ## 3971 (02) Very Good (02) Very Good
    ## 3972 (02) Very Good      (03) Good
    ## 3973 (01) Excellent (01) Excellent
    ## 3974      (03) Good      (03) Good
    ## 3975      (03) Good (02) Very Good
    ## 3976 (02) Very Good (02) Very Good
    ## 3977 (02) Very Good (02) Very Good
    ## 3978 (02) Very Good (01) Excellent
    ## 3979 (02) Very Good (02) Very Good
    ## 3980      (03) Good      (03) Good
    ## 3981      (04) Fair (01) Excellent
    ## 3982 (01) Excellent (02) Very Good
    ## 3983      (03) Good      (03) Good
    ## 3984      (04) Fair      (03) Good
    ## 3985      (03) Good      (03) Good
    ## 3986      (04) Fair      (04) Fair
    ## 3987      (03) Good      (03) Good
    ## 3988      (03) Good      (04) Fair
    ## 3989      (04) Fair      (03) Good
    ## 3990 (02) Very Good (02) Very Good
    ## 3991      (05) Poor      (05) Poor
    ## 3992      (03) Good      (03) Good
    ## 3993 (02) Very Good      (03) Good
    ## 3994      (03) Good (01) Excellent
    ## 3995      (03) Good      (03) Good
    ## 3996 (02) Very Good (02) Very Good
    ## 3997      (03) Good (01) Excellent
    ## 3998      (04) Fair      (03) Good
    ## 3999      (03) Good (02) Very Good
    ## 4000 (02) Very Good (02) Very Good
    ## 4001 (02) Very Good (02) Very Good
    ## 4002 (01) Excellent (01) Excellent
    ## 4003      (04) Fair      (03) Good
    ## 4004 (02) Very Good (02) Very Good
    ## 4005      (04) Fair      (03) Good
    ## 4006      (05) Poor      (05) Poor
    ## 4007      (04) Fair      (03) Good
    ## 4008 (02) Very Good (02) Very Good
    ## 4009 (02) Very Good (02) Very Good
    ## 4010 (02) Very Good      (03) Good
    ## 4011      (03) Good      (03) Good
    ## 4012 (02) Very Good      (04) Fair
    ## 4013      (03) Good (02) Very Good
    ## 4014 (02) Very Good (02) Very Good
    ## 4015 (02) Very Good (01) Excellent
    ## 4016      (03) Good      (03) Good
    ## 4017 (01) Excellent (01) Excellent
    ## 4018      (03) Good (01) Excellent
    ## 4019 (01) Excellent (02) Very Good
    ## 4020      (04) Fair      (03) Good
    ## 4021      (03) Good (01) Excellent
    ## 4022 (01) Excellent (01) Excellent
    ## 4023 (02) Very Good      (03) Good
    ## 4024      (03) Good      (03) Good
    ## 4025 (01) Excellent (01) Excellent
    ## 4026      (03) Good      (03) Good
    ## 4027      (03) Good      (03) Good
    ## 4028 (01) Excellent (01) Excellent
    ## 4029 (02) Very Good (01) Excellent
    ## 4030 (02) Very Good      (03) Good
    ## 4031      (03) Good (02) Very Good
    ## 4032 (01) Excellent (01) Excellent
    ## 4033      (03) Good (02) Very Good
    ## 4034 (01) Excellent (02) Very Good
    ## 4035 (02) Very Good      (03) Good
    ## 4036 (02) Very Good (02) Very Good
    ## 4037 (02) Very Good (01) Excellent
    ## 4038      (03) Good      (03) Good
    ## 4039 (02) Very Good (02) Very Good
    ## 4040      (03) Good (01) Excellent
    ## 4041      (04) Fair      (03) Good
    ## 4042      (03) Good      (03) Good
    ## 4043      (04) Fair      (03) Good
    ## 4044 (02) Very Good      (03) Good
    ## 4045 (02) Very Good      (03) Good
    ## 4046 (01) Excellent (01) Excellent
    ## 4047 (02) Very Good (02) Very Good
    ## 4048      (03) Good      (03) Good
    ## 4049 (02) Very Good (01) Excellent
    ## 4050      (04) Fair (02) Very Good
    ## 4051 (02) Very Good (02) Very Good
    ## 4052      (03) Good (02) Very Good
    ## 4053      (04) Fair      (05) Poor
    ## 4054 (01) Excellent (01) Excellent
    ## 4055 (01) Excellent (01) Excellent
    ## 4056 (01) Excellent (01) Excellent
    ## 4057 (02) Very Good (02) Very Good
    ## 4058 (01) Excellent (01) Excellent
    ## 4059      (05) Poor (01) Excellent
    ## 4060 (02) Very Good (02) Very Good
    ## 4061 (02) Very Good (02) Very Good
    ## 4062 (02) Very Good (02) Very Good
    ## 4063      (04) Fair      (04) Fair
    ## 4064      (05) Poor      (04) Fair
    ## 4065      (03) Good      (03) Good
    ## 4066      (03) Good      (03) Good
    ## 4067 (02) Very Good (02) Very Good
    ## 4068 (01) Excellent (01) Excellent
    ## 4069      (03) Good (02) Very Good
    ## 4070 (02) Very Good (02) Very Good
    ## 4071      (03) Good      (03) Good
    ## 4072 (02) Very Good (01) Excellent
    ## 4073      (04) Fair      (04) Fair
    ## 4074 (02) Very Good (02) Very Good
    ## 4075 (02) Very Good (02) Very Good
    ## 4076 (01) Excellent (01) Excellent
    ## 4077 (02) Very Good (02) Very Good
    ## 4078      (03) Good      (03) Good
    ## 4079      (03) Good      (03) Good
    ## 4080 (02) Very Good (02) Very Good
    ## 4081      (03) Good      (03) Good
    ## 4082      (03) Good      (04) Fair
    ## 4083 (02) Very Good      (03) Good
    ## 4084      (04) Fair      (04) Fair
    ## 4085      (03) Good      (04) Fair
    ## 4086      (03) Good      (03) Good
    ## 4087      (03) Good      (03) Good
    ## 4088 (01) Excellent (02) Very Good
    ## 4089      (03) Good      (03) Good
    ## 4090 (02) Very Good (02) Very Good
    ## 4091 (02) Very Good (02) Very Good
    ## 4092      (03) Good      (03) Good
    ## 4093 (02) Very Good (02) Very Good
    ## 4094 (01) Excellent (02) Very Good
    ## 4095 (02) Very Good (02) Very Good
    ## 4096 (01) Excellent (01) Excellent
    ## 4097 (01) Excellent      (03) Good
    ## 4098      (04) Fair      (03) Good
    ## 4099      (03) Good      (03) Good
    ## 4100      (03) Good      (04) Fair
    ## 4101 (02) Very Good (02) Very Good
    ## 4102 (01) Excellent (01) Excellent
    ## 4103      (03) Good      (03) Good
    ## 4104      (03) Good      (03) Good
    ## 4105 (02) Very Good      (03) Good
    ## 4106      (03) Good      (03) Good
    ## 4107 (02) Very Good (02) Very Good
    ## 4108      (03) Good      (03) Good
    ## 4109      (03) Good      (03) Good
    ## 4110 (01) Excellent (01) Excellent
    ## 4111 (01) Excellent (01) Excellent
    ## 4112      (03) Good (01) Excellent
    ## 4113      (04) Fair      (04) Fair
    ## 4114      (04) Fair      (03) Good
    ## 4115 (02) Very Good (01) Excellent
    ## 4116      (03) Good      (03) Good
    ## 4117      (04) Fair      (04) Fair
    ## 4118 (02) Very Good (02) Very Good
    ## 4119 (02) Very Good (02) Very Good
    ## 4120      (03) Good      (03) Good
    ## 4121      (03) Good      (03) Good
    ## 4122 (01) Excellent (01) Excellent
    ## 4123      (04) Fair      (03) Good
    ## 4124      (04) Fair      (03) Good
    ## 4125      (04) Fair (02) Very Good
    ## 4126 (02) Very Good (02) Very Good
    ## 4127 (02) Very Good (02) Very Good
    ## 4128      (03) Good      (03) Good
    ## 4129      (03) Good      (03) Good
    ## 4130      (03) Good (01) Excellent
    ## 4131      (03) Good      (03) Good
    ## 4132      (03) Good      (04) Fair
    ## 4133      (04) Fair      (03) Good
    ## 4134 (01) Excellent (01) Excellent
    ## 4135      (03) Good      (03) Good
    ## 4136      (03) Good (01) Excellent
    ## 4137      (03) Good      (03) Good
    ## 4138      (04) Fair      (04) Fair
    ## 4139 (02) Very Good (02) Very Good
    ## 4140 (01) Excellent (02) Very Good
    ## 4141 (02) Very Good (02) Very Good
    ## 4142 (02) Very Good (02) Very Good
    ## 4143 (01) Excellent (01) Excellent
    ## 4144 (02) Very Good (02) Very Good
    ## 4145      (03) Good      (03) Good
    ## 4146      (03) Good      (03) Good
    ## 4147 (02) Very Good      (03) Good
    ## 4148 (02) Very Good      (03) Good
    ## 4149      (03) Good      (03) Good
    ## 4150 (02) Very Good      (03) Good
    ## 4151      (04) Fair (01) Excellent
    ## 4152 (02) Very Good (02) Very Good
    ## 4153 (02) Very Good (02) Very Good
    ## 4154      (03) Good      (03) Good
    ## 4155 (02) Very Good (02) Very Good
    ## 4156      (03) Good (02) Very Good
    ## 4157      (03) Good      (03) Good
    ## 4158 (02) Very Good (02) Very Good
    ## 4159      (03) Good (01) Excellent
    ## 4160      (03) Good (02) Very Good
    ## 4161      (05) Poor      (05) Poor
    ## 4162      (05) Poor      (03) Good
    ## 4163      (04) Fair      (03) Good
    ## 4164 (02) Very Good (01) Excellent
    ## 4165      (03) Good      (04) Fair
    ## 4166      (03) Good      (04) Fair
    ## 4167      (04) Fair (02) Very Good
    ## 4168 (02) Very Good (02) Very Good
    ## 4169      (04) Fair      (04) Fair
    ## 4170 (02) Very Good (02) Very Good
    ## 4171 (02) Very Good      (03) Good
    ## 4172 (02) Very Good      (03) Good
    ## 4173 (01) Excellent (02) Very Good
    ## 4174      (03) Good      (03) Good
    ## 4175      (05) Poor      (04) Fair
    ## 4176 (02) Very Good (02) Very Good
    ## 4177      (04) Fair (01) Excellent
    ## 4178      (03) Good      (03) Good
    ## 4179 (02) Very Good (02) Very Good
    ## 4180      (04) Fair      (04) Fair
    ## 4181 (01) Excellent (01) Excellent
    ## 4182 (02) Very Good      (03) Good
    ## 4183      (03) Good      (03) Good
    ## 4184 (01) Excellent (01) Excellent
    ## 4185 (02) Very Good      (03) Good
    ## 4186      (03) Good      (03) Good
    ## 4187 (02) Very Good      (03) Good
    ## 4188      (03) Good (02) Very Good
    ## 4189      (03) Good (02) Very Good
    ## 4190      (03) Good      (03) Good
    ## 4191      (03) Good      (03) Good
    ## 4192 (02) Very Good (02) Very Good
    ## 4193 (02) Very Good (02) Very Good
    ## 4194      (03) Good (01) Excellent
    ## 4195 (02) Very Good (01) Excellent
    ## 4196 (02) Very Good      (03) Good
    ## 4197 (02) Very Good (02) Very Good
    ## 4198 (02) Very Good (02) Very Good
    ## 4199      (04) Fair      (04) Fair
    ## 4200 (01) Excellent (02) Very Good
    ## 4201      (04) Fair      (04) Fair
    ## 4202      (03) Good      (03) Good
    ## 4203 (02) Very Good (02) Very Good
    ## 4204      (03) Good      (04) Fair
    ## 4205 (02) Very Good (01) Excellent
    ## 4206 (01) Excellent (01) Excellent
    ## 4207      (04) Fair (02) Very Good
    ## 4208 (02) Very Good (02) Very Good
    ## 4209      (04) Fair (02) Very Good
    ## 4210 (02) Very Good (02) Very Good
    ## 4211      (03) Good      (03) Good
    ## 4212 (02) Very Good (02) Very Good
    ## 4213 (02) Very Good      (03) Good
    ## 4214      (03) Good      (03) Good
    ## 4215      (03) Good      (03) Good
    ## 4216      (03) Good      (03) Good
    ## 4217 (02) Very Good (01) Excellent
    ## 4218      (03) Good      (03) Good
    ## 4219 (01) Excellent (01) Excellent
    ## 4220      (03) Good (02) Very Good
    ## 4221 (02) Very Good (02) Very Good
    ## 4222      (03) Good      (03) Good
    ## 4223 (02) Very Good (01) Excellent
    ## 4224      (03) Good      (03) Good
    ## 4225 (02) Very Good (02) Very Good
    ## 4226      (03) Good (02) Very Good
    ## 4227      (03) Good      (03) Good
    ## 4228      (03) Good      (03) Good
    ## 4229      (04) Fair      (03) Good
    ## 4230 (02) Very Good (02) Very Good
    ## 4231 (02) Very Good (02) Very Good
    ## 4232      (03) Good (02) Very Good
    ## 4233      (05) Poor      (04) Fair
    ## 4234      (03) Good      (03) Good
    ## 4235      (04) Fair      (03) Good
    ## 4236 (02) Very Good      (03) Good
    ## 4237 (01) Excellent (02) Very Good
    ## 4238 (02) Very Good (02) Very Good
    ## 4239      (04) Fair      (04) Fair
    ## 4240      (04) Fair (01) Excellent
    ## 4241 (02) Very Good (02) Very Good
    ## 4242      (05) Poor      (04) Fair
    ## 4243 (02) Very Good (02) Very Good
    ## 4244 (01) Excellent (01) Excellent
    ## 4245      (03) Good      (03) Good
    ## 4246      (03) Good      (04) Fair
    ## 4247      (04) Fair      (03) Good
    ## 4248      (03) Good      (03) Good
    ## 4249      (03) Good      (04) Fair
    ## 4250      (04) Fair      (03) Good
    ## 4251 (02) Very Good      (03) Good
    ## 4252      (04) Fair      (03) Good
    ## 4253 (02) Very Good (02) Very Good
    ## 4254 (02) Very Good (02) Very Good
    ## 4255 (02) Very Good (02) Very Good
    ## 4256 (01) Excellent (01) Excellent
    ## 4257 (02) Very Good (02) Very Good
    ## 4258 (02) Very Good      (03) Good
    ## 4259 (02) Very Good (02) Very Good
    ## 4260 (01) Excellent (02) Very Good
    ## 4261      (04) Fair (01) Excellent
    ## 4262 (02) Very Good (01) Excellent
    ## 4263 (01) Excellent (02) Very Good
    ## 4264      (03) Good      (03) Good
    ## 4265 (02) Very Good (02) Very Good
    ## 4266 (02) Very Good (02) Very Good
    ## 4267 (01) Excellent (01) Excellent
    ## 4268 (01) Excellent (01) Excellent
    ## 4269      (03) Good (02) Very Good
    ## 4270      (03) Good (02) Very Good
    ## 4271 (01) Excellent (01) Excellent
    ## 4272 (02) Very Good (02) Very Good
    ## 4273      (03) Good      (03) Good
    ## 4274      (03) Good      (03) Good
    ## 4275 (01) Excellent (01) Excellent
    ## 4276      (03) Good      (03) Good
    ## 4277      (05) Poor (02) Very Good
    ## 4278      (03) Good (01) Excellent
    ## 4279 (02) Very Good (02) Very Good
    ## 4280      (04) Fair      (03) Good
    ## 4281 (02) Very Good      (05) Poor
    ## 4282      (04) Fair (02) Very Good
    ## 4283 (01) Excellent (02) Very Good
    ## 4284      (03) Good      (04) Fair
    ## 4285      (03) Good (01) Excellent
    ## 4286      (03) Good      (03) Good
    ## 4287      (03) Good      (04) Fair
    ## 4288 (02) Very Good      (03) Good
    ## 4289 (02) Very Good      (03) Good
    ## 4290      (03) Good      (03) Good
    ## 4291 (01) Excellent (01) Excellent
    ## 4292 (02) Very Good (02) Very Good
    ## 4293 (02) Very Good (01) Excellent
    ## 4294      (03) Good      (03) Good
    ## 4295 (01) Excellent (02) Very Good
    ## 4296      (04) Fair (02) Very Good
    ## 4297 (02) Very Good (02) Very Good
    ## 4298 (02) Very Good (02) Very Good
    ## 4299 (02) Very Good (02) Very Good
    ## 4300 (01) Excellent (01) Excellent
    ## 4301 (02) Very Good      (03) Good
    ## 4302      (04) Fair      (04) Fair
    ## 4303 (02) Very Good (02) Very Good
    ## 4304 (02) Very Good (02) Very Good
    ## 4305      (03) Good (02) Very Good
    ## 4306      (03) Good      (03) Good
    ## 4307 (02) Very Good (02) Very Good
    ## 4308 (01) Excellent (02) Very Good
    ## 4309      (04) Fair      (04) Fair
    ## 4310      (03) Good      (03) Good
    ## 4311 (02) Very Good (02) Very Good
    ## 4312 (02) Very Good (02) Very Good
    ## 4313 (02) Very Good (02) Very Good
    ## 4314 (02) Very Good      (03) Good
    ## 4315 (02) Very Good (02) Very Good
    ## 4316 (02) Very Good (02) Very Good
    ## 4317 (02) Very Good (02) Very Good
    ## 4318 (02) Very Good      (03) Good
    ## 4319      (03) Good      (03) Good
    ## 4320 (02) Very Good (02) Very Good
    ## 4321      (04) Fair      (04) Fair
    ## 4322      (04) Fair      (03) Good
    ## 4323 (02) Very Good      (03) Good
    ## 4324 (01) Excellent (01) Excellent
    ## 4325 (02) Very Good (02) Very Good
    ## 4326      (03) Good      (03) Good
    ## 4327 (02) Very Good (02) Very Good
    ## 4328 (02) Very Good (02) Very Good
    ## 4329      (03) Good      (03) Good
    ## 4330      (03) Good      (03) Good
    ## 4331      (03) Good      (03) Good
    ## 4332      (05) Poor      (03) Good
    ## 4333      (03) Good (02) Very Good
    ## 4334      (03) Good      (03) Good
    ## 4335 (02) Very Good (02) Very Good
    ## 4336      (03) Good      (03) Good
    ## 4337      (03) Good      (03) Good
    ## 4338      (04) Fair      (03) Good
    ## 4339      (03) Good      (03) Good
    ## 4340 (02) Very Good      (03) Good
    ## 4341 (02) Very Good (02) Very Good
    ## 4342      (03) Good      (03) Good
    ## 4343 (02) Very Good      (04) Fair
    ## 4344 (02) Very Good      (03) Good
    ## 4345      (03) Good (02) Very Good
    ## 4346 (02) Very Good (02) Very Good
    ## 4347      (03) Good      (03) Good
    ## 4348      (04) Fair (02) Very Good
    ## 4349      (04) Fair      (03) Good
    ## 4350      (04) Fair      (03) Good
    ## 4351      (03) Good      (03) Good
    ## 4352      (03) Good (02) Very Good
    ## 4353 (02) Very Good      (03) Good
    ## 4354      (03) Good      (03) Good
    ## 4355      (03) Good      (03) Good
    ## 4356 (02) Very Good      (03) Good
    ## 4357 (02) Very Good (02) Very Good
    ## 4358      (03) Good      (03) Good
    ## 4359 (02) Very Good      (03) Good
    ## 4360      (04) Fair      (04) Fair
    ## 4361 (02) Very Good (02) Very Good
    ## 4362 (02) Very Good (02) Very Good
    ## 4363 (02) Very Good (02) Very Good
    ## 4364 (02) Very Good (01) Excellent
    ## 4365      (03) Good      (03) Good
    ## 4366      (04) Fair (02) Very Good
    ## 4367      (04) Fair (02) Very Good
    ## 4368 (01) Excellent      (04) Fair
    ## 4369      (04) Fair      (04) Fair
    ## 4370 (01) Excellent (01) Excellent
    ## 4371      (03) Good      (03) Good
    ## 4372 (01) Excellent (01) Excellent
    ## 4373 (02) Very Good      (03) Good
    ## 4374      (04) Fair      (04) Fair
    ## 4375 (02) Very Good (02) Very Good
    ## 4376 (02) Very Good (01) Excellent
    ## 4377 (01) Excellent (01) Excellent
    ## 4378 (02) Very Good (02) Very Good
    ## 4379 (02) Very Good (02) Very Good
    ## 4380      (03) Good      (03) Good
    ## 4381      (03) Good      (03) Good
    ## 4382      (03) Good      (04) Fair
    ## 4383 (01) Excellent      (03) Good
    ## 4384      (04) Fair      (04) Fair
    ## 4385 (02) Very Good (02) Very Good
    ## 4386      (05) Poor      (03) Good
    ## 4387 (01) Excellent (01) Excellent
    ## 4388      (04) Fair (02) Very Good
    ## 4389 (01) Excellent (01) Excellent
    ## 4390 (02) Very Good (02) Very Good
    ## 4391 (02) Very Good      (03) Good
    ## 4392 (02) Very Good (02) Very Good
    ## 4393 (01) Excellent (02) Very Good
    ## 4394 (02) Very Good (02) Very Good
    ## 4395 (02) Very Good (02) Very Good
    ## 4396 (02) Very Good      (03) Good
    ## 4397 (02) Very Good (02) Very Good
    ## 4398      (03) Good (02) Very Good
    ## 4399 (02) Very Good (02) Very Good
    ## 4400 (01) Excellent (02) Very Good
    ## 4401      (04) Fair      (04) Fair
    ## 4402      (03) Good (02) Very Good
    ## 4403      (03) Good      (04) Fair
    ## 4404      (04) Fair      (03) Good
    ## 4405      (03) Good      (03) Good
    ## 4406      (04) Fair      (03) Good
    ## 4407 (02) Very Good (02) Very Good
    ## 4408 (02) Very Good (02) Very Good
    ## 4409 (01) Excellent (02) Very Good
    ## 4410      (03) Good (02) Very Good
    ## 4411      (03) Good      (03) Good
    ## 4412      (04) Fair      (03) Good
    ## 4413 (02) Very Good (02) Very Good
    ## 4414      (03) Good (01) Excellent
    ## 4415 (01) Excellent (02) Very Good
    ## 4416 (02) Very Good      (03) Good
    ## 4417      (04) Fair      (04) Fair
    ## 4418 (02) Very Good (02) Very Good
    ## 4419 (02) Very Good      (03) Good
    ## 4420      (03) Good (02) Very Good
    ## 4421 (02) Very Good (02) Very Good
    ## 4422 (02) Very Good      (03) Good
    ## 4423      (03) Good      (03) Good
    ## 4424 (01) Excellent (02) Very Good
    ## 4425      (03) Good      (03) Good
    ## 4426 (02) Very Good      (03) Good
    ## 4427 (02) Very Good      (03) Good
    ## 4428 (02) Very Good (01) Excellent
    ## 4429 (01) Excellent (02) Very Good
    ## 4430      (03) Good      (03) Good
    ## 4431 (02) Very Good (02) Very Good
    ## 4432 (02) Very Good (01) Excellent
    ## 4433 (02) Very Good (02) Very Good
    ## 4434      (03) Good      (03) Good
    ## 4435      (03) Good      (05) Poor
    ## 4436 (01) Excellent      (03) Good
    ## 4437 (02) Very Good (02) Very Good
    ## 4438      (03) Good      (03) Good
    ## 4439      (03) Good      (03) Good
    ## 4440      (03) Good      (03) Good
    ## 4441      (05) Poor (02) Very Good
    ## 4442      (03) Good      (03) Good
    ## 4443 (01) Excellent (02) Very Good
    ## 4444      (04) Fair      (03) Good
    ## 4445 (01) Excellent      (04) Fair
    ## 4446      (03) Good      (03) Good
    ## 4447 (02) Very Good (02) Very Good
    ## 4448 (02) Very Good (02) Very Good
    ## 4449 (01) Excellent (02) Very Good
    ## 4450 (02) Very Good (02) Very Good
    ## 4451      (03) Good (02) Very Good
    ## 4452      (03) Good      (03) Good
    ## 4453 (02) Very Good (02) Very Good
    ## 4454 (02) Very Good      (04) Fair
    ## 4455      (03) Good      (03) Good
    ## 4456 (02) Very Good (02) Very Good
    ## 4457      (03) Good (02) Very Good
    ## 4458 (02) Very Good (02) Very Good
    ## 4459 (02) Very Good (01) Excellent
    ## 4460 (02) Very Good (02) Very Good
    ## 4461 (02) Very Good (02) Very Good
    ## 4462      (03) Good (02) Very Good
    ## 4463      (03) Good      (03) Good
    ## 4464 (02) Very Good      (03) Good
    ## 4465      (03) Good      (03) Good
    ## 4466      (03) Good      (03) Good
    ## 4467      (03) Good (02) Very Good
    ## 4468 (02) Very Good (01) Excellent
    ## 4469 (02) Very Good (02) Very Good
    ## 4470      (03) Good      (03) Good
    ## 4471      (03) Good (01) Excellent
    ## 4472      (03) Good      (03) Good
    ## 4473      (03) Good      (03) Good
    ## 4474      (03) Good      (04) Fair
    ## 4475      (03) Good      (03) Good
    ## 4476 (02) Very Good      (03) Good
    ## 4477      (03) Good      (04) Fair
    ## 4478      (03) Good      (03) Good
    ## 4479 (01) Excellent (01) Excellent
    ## 4480      (04) Fair      (03) Good
    ## 4481 (02) Very Good (02) Very Good
    ## 4482      (03) Good      (03) Good
    ## 4483 (02) Very Good      (03) Good
    ## 4484      (05) Poor      (04) Fair
    ## 4485 (01) Excellent (01) Excellent
    ## 4486      (04) Fair      (03) Good
    ## 4487      (03) Good      (03) Good
    ## 4488      (04) Fair      (03) Good
    ## 4489      (03) Good      (03) Good
    ## 4490      (03) Good (02) Very Good
    ## 4491      (03) Good      (03) Good
    ## 4492      (03) Good      (03) Good
    ## 4493      (03) Good      (04) Fair
    ## 4494      (05) Poor (02) Very Good
    ## 4495      (03) Good      (03) Good
    ## 4496 (02) Very Good (02) Very Good
    ## 4497 (01) Excellent (01) Excellent
    ## 4498      (03) Good      (03) Good
    ## 4499 (02) Very Good (02) Very Good
    ## 4500      (04) Fair      (04) Fair
    ## 4501      (03) Good      (03) Good
    ## 4502 (02) Very Good (01) Excellent
    ## 4503      (05) Poor      (04) Fair
    ## 4504      (03) Good      (03) Good
    ## 4505      (05) Poor (02) Very Good
    ## 4506      (04) Fair      (03) Good
    ## 4507 (02) Very Good      (03) Good
    ## 4508      (04) Fair      (03) Good
    ## 4509 (02) Very Good (01) Excellent
    ## 4510 (02) Very Good (02) Very Good
    ## 4511      (03) Good      (03) Good
    ## 4512      (03) Good      (03) Good
    ## 4513 (02) Very Good      (03) Good
    ## 4514 (02) Very Good (02) Very Good
    ## 4515      (03) Good      (03) Good
    ## 4516 (02) Very Good      (03) Good
    ## 4517      (04) Fair      (03) Good
    ## 4518      (03) Good      (03) Good
    ## 4519 (01) Excellent (02) Very Good
    ## 4520      (03) Good      (03) Good
    ## 4521 (02) Very Good (02) Very Good
    ## 4522      (05) Poor (02) Very Good
    ## 4523 (02) Very Good (02) Very Good
    ## 4524      (03) Good      (03) Good
    ## 4525      (03) Good      (03) Good
    ## 4526      (03) Good      (03) Good
    ## 4527      (03) Good (01) Excellent
    ## 4528      (03) Good      (04) Fair
    ## 4529      (04) Fair      (04) Fair
    ## 4530      (03) Good      (03) Good
    ## 4531      (04) Fair      (03) Good
    ## 4532      (05) Poor      (05) Poor
    ## 4533      (03) Good      (03) Good
    ## 4534      (04) Fair      (03) Good
    ## 4535      (04) Fair      (04) Fair
    ## 4536      (03) Good      (03) Good
    ## 4537      (03) Good      (03) Good
    ## 4538 (02) Very Good      (03) Good
    ## 4539      (03) Good      (03) Good
    ## 4540      (03) Good      (03) Good
    ## 4541      (03) Good      (03) Good
    ## 4542      (03) Good      (03) Good
    ## 4543      (03) Good      (04) Fair
    ## 4544      (04) Fair      (03) Good
    ## 4545      (03) Good      (04) Fair
    ## 4546      (05) Poor      (03) Good
    ## 4547      (03) Good      (03) Good
    ## 4548      (04) Fair      (04) Fair
    ## 4549      (03) Good      (03) Good
    ## 4550      (05) Poor      (04) Fair
    ## 4551 (01) Excellent (01) Excellent
    ## 4552      (04) Fair      (03) Good
    ## 4553      (03) Good      (03) Good
    ## 4554 (02) Very Good (02) Very Good
    ## 4555 (02) Very Good (02) Very Good
    ## 4556      (04) Fair      (04) Fair
    ## 4557 (01) Excellent (01) Excellent
    ## 4558 (01) Excellent      (03) Good
    ## 4559      (04) Fair      (04) Fair
    ## 4560 (02) Very Good (02) Very Good
    ## 4561 (02) Very Good      (04) Fair
    ## 4562      (03) Good      (03) Good
    ## 4563      (03) Good      (03) Good
    ## 4564 (01) Excellent (01) Excellent
    ## 4565      (03) Good (01) Excellent
    ## 4566      (03) Good      (03) Good
    ## 4567 (01) Excellent (02) Very Good
    ## 4568 (01) Excellent (02) Very Good
    ## 4569 (02) Very Good (02) Very Good
    ## 4570      (03) Good      (03) Good
    ## 4571 (02) Very Good (02) Very Good
    ## 4572      (03) Good      (03) Good
    ## 4573 (02) Very Good (02) Very Good
    ## 4574      (03) Good      (03) Good
    ## 4575      (03) Good (01) Excellent
    ## 4576      (03) Good (02) Very Good
    ## 4577 (02) Very Good (01) Excellent
    ## 4578      (04) Fair      (03) Good
    ## 4579      (04) Fair      (04) Fair
    ## 4580      (03) Good (02) Very Good
    ## 4581 (02) Very Good (02) Very Good
    ## 4582 (01) Excellent (02) Very Good
    ## 4583      (03) Good      (03) Good
    ## 4584 (01) Excellent (02) Very Good
    ## 4585      (03) Good      (03) Good
    ## 4586      (03) Good      (03) Good
    ## 4587 (02) Very Good (02) Very Good
    ## 4588 (02) Very Good      (03) Good
    ## 4589      (03) Good      (03) Good
    ## 4590      (03) Good      (03) Good
    ## 4591 (01) Excellent (01) Excellent
    ## 4592      (03) Good (02) Very Good
    ## 4593 (01) Excellent (01) Excellent
    ## 4594 (02) Very Good (01) Excellent
    ## 4595 (02) Very Good      (03) Good
    ## 4596 (02) Very Good (02) Very Good
    ## 4597      (04) Fair      (03) Good
    ## 4598      (03) Good      (03) Good
    ## 4599      (03) Good      (03) Good
    ## 4600 (01) Excellent (01) Excellent
    ## 4601 (02) Very Good (02) Very Good
    ## 4602      (04) Fair (02) Very Good
    ## 4603      (03) Good (02) Very Good
    ## 4604      (04) Fair      (04) Fair
    ## 4605      (03) Good      (03) Good
    ## 4606 (02) Very Good (02) Very Good
    ## 4607 (01) Excellent (01) Excellent
    ## 4608      (03) Good      (04) Fair
    ## 4609 (01) Excellent      (03) Good
    ## 4610 (02) Very Good      (03) Good
    ## 4611 (02) Very Good      (03) Good
    ## 4612      (03) Good      (03) Good
    ## 4613 (01) Excellent (01) Excellent
    ## 4614      (03) Good      (03) Good
    ## 4615      (03) Good      (03) Good
    ## 4616 (02) Very Good (02) Very Good
    ## 4617      (03) Good (02) Very Good
    ## 4618 (02) Very Good      (03) Good
    ## 4619      (03) Good      (03) Good
    ## 4620      (05) Poor      (04) Fair
    ## 4621 (02) Very Good      (03) Good
    ## 4622      (03) Good      (03) Good
    ## 4623      (03) Good      (03) Good
    ## 4624      (04) Fair      (04) Fair
    ## 4625      (03) Good      (03) Good
    ## 4626      (03) Good (02) Very Good
    ## 4627      (04) Fair      (04) Fair
    ## 4628      (03) Good      (03) Good
    ## 4629 (02) Very Good (02) Very Good
    ## 4630      (04) Fair      (04) Fair
    ## 4631      (03) Good      (03) Good
    ## 4632      (03) Good      (03) Good
    ## 4633      (03) Good (02) Very Good
    ## 4634      (03) Good      (03) Good
    ## 4635      (04) Fair      (03) Good
    ## 4636      (05) Poor (01) Excellent
    ## 4637      (03) Good      (03) Good
    ## 4638      (03) Good      (03) Good
    ## 4639 (02) Very Good      (03) Good
    ## 4640 (02) Very Good (02) Very Good
    ## 4641 (02) Very Good      (03) Good
    ## 4642      (03) Good      (03) Good
    ## 4643      (03) Good (01) Excellent
    ## 4644 (02) Very Good (02) Very Good
    ## 4645      (03) Good (02) Very Good
    ## 4646 (01) Excellent (01) Excellent
    ## 4647      (03) Good      (04) Fair
    ## 4648 (02) Very Good (02) Very Good
    ## 4649      (04) Fair      (04) Fair
    ## 4650      (05) Poor      (03) Good
    ## 4651 (01) Excellent (01) Excellent
    ## 4652      (05) Poor      (03) Good
    ## 4653 (02) Very Good      (03) Good
    ## 4654      (03) Good (02) Very Good
    ## 4655      (04) Fair      (03) Good
    ## 4656 (01) Excellent (01) Excellent
    ## 4657      (03) Good (02) Very Good
    ## 4658      (03) Good      (03) Good
    ## 4659      (04) Fair      (03) Good
    ## 4660      (03) Good      (03) Good
    ## 4661      (03) Good      (03) Good
    ## 4662 (01) Excellent (02) Very Good
    ## 4663      (04) Fair      (03) Good
    ## 4664 (01) Excellent (01) Excellent
    ## 4665      (03) Good      (03) Good
    ## 4666      (04) Fair      (03) Good
    ## 4667 (02) Very Good (02) Very Good
    ## 4668      (04) Fair      (04) Fair
    ## 4669      (04) Fair      (04) Fair
    ## 4670      (03) Good      (03) Good
    ## 4671      (03) Good (02) Very Good
    ## 4672 (02) Very Good      (03) Good
    ## 4673      (04) Fair (02) Very Good
    ## 4674      (05) Poor      (03) Good
    ## 4675 (02) Very Good      (03) Good
    ## 4676      (03) Good (02) Very Good
    ## 4677 (02) Very Good      (03) Good
    ## 4678      (03) Good      (03) Good
    ## 4679      (03) Good      (03) Good
    ## 4680 (02) Very Good (02) Very Good
    ## 4681      (04) Fair      (04) Fair
    ## 4682      (03) Good      (03) Good
    ## 4683 (02) Very Good (02) Very Good
    ## 4684      (03) Good (02) Very Good
    ## 4685      (03) Good      (03) Good
    ## 4686      (03) Good      (04) Fair
    ## 4687      (03) Good      (04) Fair
    ## 4688      (03) Good      (03) Good
    ## 4689      (04) Fair      (03) Good
    ## 4690 (01) Excellent (01) Excellent
    ## 4691 (01) Excellent (02) Very Good
    ## 4692      (03) Good      (03) Good
    ## 4693      (03) Good (02) Very Good
    ## 4694      (04) Fair (01) Excellent
    ## 4695 (01) Excellent (02) Very Good
    ## 4696 (02) Very Good (02) Very Good
    ## 4697 (02) Very Good (02) Very Good
    ## 4698      (03) Good (02) Very Good
    ## 4699 (02) Very Good (02) Very Good
    ## 4700 (01) Excellent (01) Excellent
    ## 4701 (01) Excellent (01) Excellent
    ## 4702      (03) Good (02) Very Good
    ## 4703 (02) Very Good (02) Very Good
    ## 4704 (01) Excellent      (03) Good
    ## 4705 (02) Very Good (01) Excellent
    ## 4706      (04) Fair      (04) Fair
    ## 4707      (03) Good (02) Very Good
    ## 4708      (03) Good (02) Very Good
    ## 4709      (04) Fair      (03) Good
    ## 4710 (01) Excellent (01) Excellent
    ## 4711 (02) Very Good (02) Very Good
    ## 4712      (03) Good      (03) Good
    ## 4713      (03) Good      (03) Good
    ## 4714 (02) Very Good      (03) Good
    ## 4715      (04) Fair (02) Very Good
    ## 4716 (01) Excellent      (03) Good
    ## 4717 (01) Excellent (01) Excellent
    ## 4718      (03) Good      (03) Good
    ## 4719      (04) Fair      (04) Fair
    ## 4720      (03) Good (01) Excellent
    ## 4721      (03) Good      (03) Good
    ## 4722 (02) Very Good (02) Very Good
    ## 4723 (02) Very Good (02) Very Good
    ## 4724 (02) Very Good (01) Excellent
    ## 4725      (04) Fair      (04) Fair
    ## 4726      (03) Good      (03) Good
    ## 4727      (03) Good      (03) Good
    ## 4728 (02) Very Good (02) Very Good
    ## 4729      (03) Good (02) Very Good
    ## 4730      (03) Good      (03) Good
    ## 4731 (01) Excellent (01) Excellent
    ## 4732      (03) Good      (03) Good
    ## 4733      (03) Good      (03) Good
    ## 4734 (01) Excellent (02) Very Good
    ## 4735      (03) Good      (03) Good
    ## 4736 (02) Very Good (01) Excellent
    ## 4737      (04) Fair      (03) Good
    ## 4738 (02) Very Good (01) Excellent
    ## 4739 (02) Very Good (02) Very Good
    ## 4740      (03) Good      (03) Good
    ## 4741      (03) Good (02) Very Good
    ## 4742      (03) Good      (03) Good
    ## 4743 (02) Very Good      (03) Good
    ## 4744      (04) Fair (02) Very Good
    ## 4745      (03) Good      (03) Good
    ## 4746      (05) Poor      (04) Fair
    ## 4747      (03) Good (02) Very Good
    ## 4748 (02) Very Good (02) Very Good
    ## 4749      (03) Good (02) Very Good
    ## 4750 (02) Very Good (02) Very Good
    ## 4751      (03) Good (02) Very Good
    ## 4752 (02) Very Good (01) Excellent
    ## 4753 (02) Very Good      (03) Good
    ## 4754      (04) Fair      (03) Good
    ## 4755 (02) Very Good (01) Excellent
    ## 4756      (03) Good (02) Very Good
    ## 4757 (02) Very Good (02) Very Good
    ## 4758 (02) Very Good (02) Very Good
    ## 4759      (03) Good (02) Very Good
    ## 4760      (04) Fair      (03) Good
    ## 4761 (01) Excellent (02) Very Good
    ## 4762      (03) Good (01) Excellent
    ## 4763 (01) Excellent (02) Very Good
    ## 4764 (02) Very Good (01) Excellent
    ## 4765 (02) Very Good      (03) Good
    ## 4766 (01) Excellent (01) Excellent
    ## 4767 (02) Very Good (02) Very Good
    ## 4768      (03) Good      (03) Good
    ## 4769      (04) Fair      (03) Good
    ## 4770 (02) Very Good (02) Very Good
    ## 4771 (01) Excellent (01) Excellent
    ## 4772      (03) Good      (04) Fair
    ## 4773      (03) Good (02) Very Good
    ## 4774 (02) Very Good (01) Excellent
    ## 4775      (03) Good      (03) Good
    ## 4776      (04) Fair      (03) Good
    ## 4777 (02) Very Good (02) Very Good
    ## 4778 (01) Excellent (02) Very Good
    ## 4779      (03) Good (02) Very Good
    ## 4780      (03) Good      (03) Good
    ## 4781 (02) Very Good      (03) Good
    ## 4782      (03) Good      (03) Good
    ## 4783 (02) Very Good      (03) Good
    ## 4784 (02) Very Good (02) Very Good
    ## 4785 (02) Very Good (02) Very Good
    ## 4786 (02) Very Good (02) Very Good
    ## 4787 (02) Very Good (02) Very Good
    ## 4788 (01) Excellent (01) Excellent
    ## 4789 (02) Very Good      (04) Fair
    ## 4790      (03) Good (02) Very Good
    ## 4791      (04) Fair      (03) Good
    ## 4792 (01) Excellent (01) Excellent
    ## 4793 (02) Very Good (01) Excellent
    ## 4794      (03) Good      (03) Good
    ## 4795      (03) Good (02) Very Good
    ## 4796      (03) Good      (03) Good
    ## 4797      (04) Fair      (04) Fair
    ## 4798      (05) Poor      (04) Fair
    ## 4799 (01) Excellent (01) Excellent
    ## 4800 (02) Very Good (01) Excellent
    ## 4801 (01) Excellent      (03) Good
    ## 4802 (01) Excellent (01) Excellent
    ## 4803      (04) Fair      (03) Good
    ## 4804 (02) Very Good (01) Excellent
    ## 4805 (02) Very Good (02) Very Good
    ## 4806      (03) Good      (03) Good
    ## 4807      (03) Good      (03) Good
    ## 4808      (04) Fair      (04) Fair
    ## 4809 (01) Excellent (01) Excellent
    ## 4810 (02) Very Good (01) Excellent
    ## 4811      (04) Fair      (03) Good
    ## 4812      (04) Fair (02) Very Good
    ## 4813 (01) Excellent (01) Excellent
    ## 4814 (01) Excellent (01) Excellent
    ## 4815 (01) Excellent (01) Excellent
    ## 4816 (01) Excellent (02) Very Good
    ## 4817 (02) Very Good (02) Very Good
    ## 4818      (03) Good      (03) Good
    ## 4819      (03) Good      (03) Good
    ## 4820      (03) Good      (03) Good
    ## 4821      (03) Good      (03) Good
    ## 4822      (03) Good (02) Very Good
    ## 4823      (03) Good (01) Excellent
    ## 4824      (03) Good      (03) Good
    ## 4825 (02) Very Good (01) Excellent
    ## 4826      (03) Good      (03) Good
    ## 4827      (03) Good (02) Very Good
    ## 4828 (02) Very Good (02) Very Good
    ## 4829 (01) Excellent (02) Very Good
    ## 4830 (01) Excellent (02) Very Good
    ## 4831      (03) Good (02) Very Good
    ## 4832 (02) Very Good (01) Excellent
    ## 4833      (03) Good      (03) Good
    ## 4834 (02) Very Good (02) Very Good
    ## 4835      (03) Good (02) Very Good
    ## 4836 (02) Very Good (02) Very Good
    ## 4837 (02) Very Good (02) Very Good
    ## 4838 (02) Very Good (02) Very Good
    ## 4839      (03) Good      (03) Good
    ## 4840      (03) Good      (05) Poor
    ## 4841 (02) Very Good (02) Very Good
    ## 4842 (02) Very Good (02) Very Good
    ## 4843      (03) Good (02) Very Good
    ## 4844      (04) Fair      (04) Fair
    ## 4845 (02) Very Good      (03) Good
    ## 4846      (03) Good      (03) Good
    ## 4847      (04) Fair      (03) Good
    ## 4848 (01) Excellent (01) Excellent
    ## 4849      (03) Good (02) Very Good
    ## 4850 (02) Very Good (02) Very Good
    ## 4851      (03) Good (01) Excellent
    ## 4852      (03) Good      (04) Fair
    ## 4853 (02) Very Good (02) Very Good
    ## 4854 (01) Excellent (01) Excellent
    ## 4855 (02) Very Good (02) Very Good
    ## 4856 (02) Very Good (02) Very Good
    ## 4857 (01) Excellent (01) Excellent
    ## 4858      (04) Fair      (04) Fair
    ## 4859 (01) Excellent (01) Excellent
    ## 4860      (04) Fair      (04) Fair
    ## 4861      (03) Good      (03) Good
    ## 4862 (02) Very Good (02) Very Good
    ## 4863 (02) Very Good (01) Excellent
    ## 4864 (02) Very Good      (04) Fair
    ## 4865 (01) Excellent      (05) Poor
    ## 4866 (01) Excellent (01) Excellent
    ## 4867 (01) Excellent (01) Excellent
    ## 4868 (02) Very Good (02) Very Good
    ## 4869      (04) Fair      (03) Good
    ## 4870      (03) Good      (03) Good
    ## 4871 (02) Very Good (02) Very Good
    ## 4872 (01) Excellent (01) Excellent
    ## 4873      (04) Fair      (04) Fair
    ## 4874 (02) Very Good      (03) Good
    ## 4875      (04) Fair      (04) Fair
    ## 4876      (03) Good      (03) Good
    ## 4877      (03) Good      (05) Poor
    ## 4878      (03) Good      (03) Good
    ## 4879      (03) Good      (03) Good
    ## 4880      (03) Good      (03) Good
    ## 4881      (05) Poor      (04) Fair
    ## 4882 (02) Very Good      (03) Good
    ## 4883      (04) Fair      (03) Good
    ## 4884 (01) Excellent (01) Excellent
    ## 4885 (01) Excellent (01) Excellent
    ## 4886      (03) Good (02) Very Good
    ## 4887      (03) Good      (03) Good
    ## 4888      (03) Good      (04) Fair
    ## 4889      (03) Good      (03) Good
    ## 4890 (02) Very Good      (03) Good
    ## 4891      (04) Fair      (03) Good
    ## 4892 (02) Very Good      (03) Good
    ## 4893 (01) Excellent (02) Very Good
    ## 4894      (03) Good (02) Very Good
    ## 4895 (02) Very Good      (03) Good
    ## 4896      (04) Fair      (03) Good
    ## 4897      (03) Good      (03) Good
    ## 4898      (03) Good      (03) Good
    ## 4899      (03) Good      (03) Good
    ## 4900      (05) Poor      (04) Fair
    ## 4901 (02) Very Good (02) Very Good
    ## 4902      (03) Good      (03) Good
    ## 4903 (01) Excellent      (03) Good
    ## 4904      (03) Good      (03) Good
    ## 4905      (04) Fair      (03) Good
    ## 4906      (04) Fair      (04) Fair
    ## 4907 (01) Excellent (01) Excellent
    ## 4908      (03) Good      (03) Good
    ## 4909      (03) Good (02) Very Good
    ## 4910      (04) Fair      (03) Good
    ## 4911      (04) Fair      (03) Good
    ## 4912 (01) Excellent (02) Very Good
    ## 4913      (03) Good (02) Very Good
    ## 4914 (01) Excellent (02) Very Good
    ## 4915      (03) Good      (03) Good
    ## 4916      (03) Good      (03) Good
    ## 4917      (03) Good      (03) Good
    ## 4918      (03) Good      (03) Good
    ## 4919 (01) Excellent (01) Excellent
    ## 4920 (02) Very Good (02) Very Good
    ## 4921 (02) Very Good (02) Very Good
    ## 4922      (03) Good (01) Excellent
    ## 4923 (01) Excellent (01) Excellent
    ## 4924      (03) Good      (03) Good
    ## 4925      (03) Good      (03) Good
    ## 4926 (02) Very Good      (03) Good
    ## 4927 (02) Very Good      (03) Good
    ## 4928 (02) Very Good      (03) Good
    ## 4929      (03) Good      (03) Good
    ## 4930      (03) Good      (03) Good
    ## 4931 (02) Very Good (02) Very Good
    ## 4932 (02) Very Good (02) Very Good
    ## 4933      (03) Good      (03) Good
    ## 4934      (03) Good      (03) Good
    ## 4935      (03) Good (02) Very Good
    ## 4936      (03) Good (02) Very Good
    ## 4937      (04) Fair      (03) Good
    ## 4938 (02) Very Good (01) Excellent
    ## 4939      (03) Good      (03) Good
    ## 4940 (01) Excellent (01) Excellent
    ## 4941 (02) Very Good (02) Very Good
    ## 4942      (03) Good (02) Very Good
    ## 4943      (03) Good      (03) Good
    ## 4944      (03) Good      (03) Good
    ## 4945      (03) Good      (03) Good
    ## 4946 (02) Very Good      (03) Good
    ## 4947      (03) Good      (03) Good
    ## 4948      (03) Good      (03) Good
    ## 4949      (03) Good      (03) Good
    ## 4950 (01) Excellent (01) Excellent
    ## 4951      (03) Good      (03) Good
    ## 4952      (03) Good      (03) Good
    ## 4953      (03) Good      (03) Good
    ## 4954      (04) Fair      (03) Good
    ## 4955      (03) Good      (03) Good
    ## 4956      (03) Good      (03) Good
    ## 4957      (03) Good      (03) Good
    ## 4958      (03) Good      (03) Good
    ## 4959      (03) Good      (03) Good
    ## 4960      (03) Good      (03) Good
    ## 4961      (03) Good      (03) Good
    ## 4962      (03) Good      (03) Good
    ## 4963      (03) Good      (03) Good
    ## 4964 (02) Very Good      (03) Good
    ## 4965      (03) Good      (04) Fair
    ## 4966      (05) Poor      (04) Fair
    ## 4967 (02) Very Good (01) Excellent
    ## 4968 (01) Excellent (01) Excellent
    ## 4969      (03) Good (01) Excellent
    ## 4970      (03) Good      (03) Good
    ## 4971      (03) Good      (03) Good
    ## 4972      (04) Fair      (03) Good
    ## 4973      (03) Good      (03) Good
    ## 4974      (03) Good      (03) Good
    ## 4975 (02) Very Good (02) Very Good
    ## 4976 (02) Very Good (02) Very Good
    ## 4977 (02) Very Good      (03) Good
    ## 4978      (04) Fair      (04) Fair
    ## 4979      (04) Fair      (04) Fair
    ## 4980 (01) Excellent (01) Excellent
    ## 4981 (02) Very Good (01) Excellent
    ## 4982      (03) Good      (03) Good
    ## 4983      (03) Good      (03) Good
    ## 4984 (01) Excellent (01) Excellent
    ## 4985 (01) Excellent (01) Excellent
    ## 4986 (01) Excellent (01) Excellent
    ## 4987      (03) Good      (03) Good
    ## 4988      (05) Poor      (05) Poor
    ## 4989 (01) Excellent (01) Excellent
    ## 4990      (05) Poor      (03) Good
    ## 4991      (05) Poor (02) Very Good
    ## 4992      (04) Fair      (03) Good
    ## 4993      (03) Good      (03) Good
    ## 4994      (03) Good      (04) Fair
    ## 4995 (01) Excellent (02) Very Good
    ## 4996      (03) Good      (03) Good
    ## 4997 (02) Very Good (02) Very Good
    ## 4998      (04) Fair (02) Very Good
    ## 4999      (03) Good      (03) Good
    ## 5000      (03) Good      (03) Good
    ## 5001      (04) Fair      (05) Poor
    ## 5002      (04) Fair      (03) Good
    ## 5003 (02) Very Good (02) Very Good
    ## 5004 (02) Very Good (01) Excellent
    ## 5005      (04) Fair (02) Very Good
    ## 5006      (03) Good (01) Excellent
    ## 5007      (04) Fair      (03) Good
    ## 5008      (04) Fair      (04) Fair
    ## 5009      (04) Fair      (04) Fair
    ## 5010 (02) Very Good (02) Very Good
    ## 5011 (02) Very Good (01) Excellent
    ## 5012      (03) Good      (03) Good
    ## 5013 (02) Very Good (02) Very Good
    ## 5014 (01) Excellent (01) Excellent
    ## 5015      (04) Fair (02) Very Good
    ## 5016 (02) Very Good (01) Excellent
    ## 5017 (02) Very Good (01) Excellent
    ## 5018 (02) Very Good (02) Very Good
    ## 5019 (02) Very Good (02) Very Good
    ## 5020 (01) Excellent (01) Excellent
    ## 5021      (03) Good      (03) Good
    ## 5022      (04) Fair (02) Very Good
    ## 5023      (04) Fair (02) Very Good
    ## 5024      (03) Good (02) Very Good
    ## 5025      (03) Good      (03) Good
    ## 5026      (04) Fair      (03) Good
    ## 5027      (03) Good      (03) Good
    ## 5028 (02) Very Good (02) Very Good
    ## 5029 (02) Very Good (01) Excellent
    ## 5030      (03) Good      (03) Good
    ## 5031      (03) Good      (03) Good
    ## 5032 (01) Excellent (01) Excellent
    ## 5033      (03) Good      (03) Good
    ## 5034      (03) Good      (03) Good
    ## 5035 (01) Excellent (02) Very Good
    ## 5036      (03) Good      (03) Good
    ## 5037      (04) Fair      (03) Good
    ## 5038 (02) Very Good (01) Excellent
    ## 5039      (04) Fair (01) Excellent
    ## 5040      (04) Fair      (04) Fair
    ## 5041      (03) Good (02) Very Good
    ## 5042 (02) Very Good      (03) Good
    ## 5043 (01) Excellent (01) Excellent
    ## 5044 (02) Very Good (01) Excellent
    ## 5045 (02) Very Good (01) Excellent
    ## 5046      (03) Good (01) Excellent
    ## 5047      (03) Good (02) Very Good
    ## 5048 (02) Very Good (01) Excellent
    ## 5049      (04) Fair (01) Excellent
    ## 5050      (03) Good (01) Excellent
    ## 5051 (02) Very Good (01) Excellent
    ## 5052      (03) Good (01) Excellent
    ## 5053      (03) Good      (04) Fair
    ## 5054      (03) Good      (03) Good
    ## 5055 (01) Excellent (01) Excellent
    ## 5056      (03) Good (01) Excellent
    ## 5057      (03) Good      (03) Good
    ## 5058 (02) Very Good (02) Very Good
    ## 5059      (03) Good      (03) Good
    ## 5060 (02) Very Good (01) Excellent
    ## 5061      (04) Fair      (04) Fair
    ## 5062      (04) Fair      (03) Good
    ## 5063      (03) Good      (03) Good
    ## 5064      (05) Poor      (03) Good
    ## 5065      (03) Good      (03) Good
    ## 5066      (03) Good      (03) Good
    ## 5067      (04) Fair      (04) Fair
    ## 5068 (01) Excellent (01) Excellent
    ## 5069 (02) Very Good      (03) Good
    ## 5070      (03) Good      (04) Fair
    ## 5071      (03) Good      (03) Good
    ## 5072      (03) Good (01) Excellent
    ## 5073      (04) Fair      (04) Fair
    ## 5074      (03) Good      (03) Good
    ## 5075      (03) Good      (03) Good
    ## 5076      (03) Good      (03) Good
    ## 5077 (02) Very Good (01) Excellent
    ## 5078 (01) Excellent (01) Excellent
    ## 5079      (04) Fair      (03) Good
    ## 5080 (02) Very Good (02) Very Good
    ## 5081 (02) Very Good      (03) Good
    ## 5082      (04) Fair      (04) Fair
    ## 5083      (04) Fair      (04) Fair
    ## 5084 (02) Very Good (01) Excellent
    ## 5085      (03) Good      (03) Good
    ## 5086 (02) Very Good (01) Excellent
    ## 5087      (03) Good (02) Very Good
    ## 5088 (02) Very Good (02) Very Good
    ## 5089      (03) Good (02) Very Good
    ## 5090 (02) Very Good (01) Excellent
    ## 5091 (02) Very Good (01) Excellent
    ## 5092      (03) Good (02) Very Good
    ## 5093      (05) Poor (02) Very Good
    ## 5094      (03) Good (02) Very Good
    ## 5095 (01) Excellent (01) Excellent
    ## 5096 (01) Excellent      (03) Good
    ## 5097 (01) Excellent (01) Excellent
    ## 5098 (02) Very Good (02) Very Good
    ## 5099 (02) Very Good (02) Very Good
    ## 5100 (01) Excellent (01) Excellent
    ## 5101 (01) Excellent (01) Excellent
    ## 5102 (02) Very Good (02) Very Good
    ## 5103 (01) Excellent (02) Very Good
    ## 5104 (02) Very Good (02) Very Good
    ## 5105 (02) Very Good (02) Very Good
    ## 5106      (04) Fair      (04) Fair
    ## 5107      (05) Poor      (05) Poor
    ## 5108 (02) Very Good (02) Very Good
    ## 5109 (01) Excellent (01) Excellent
    ## 5110 (02) Very Good (02) Very Good
    ## 5111 (01) Excellent (01) Excellent
    ## 5112 (01) Excellent (01) Excellent
    ## 5113 (01) Excellent (01) Excellent
    ## 5114 (01) Excellent (01) Excellent
    ## 5115 (02) Very Good (01) Excellent
    ## 5116 (02) Very Good (01) Excellent
    ## 5117      (03) Good (02) Very Good
    ## 5118 (01) Excellent (01) Excellent
    ## 5119      (04) Fair      (04) Fair
    ## 5120 (01) Excellent (01) Excellent
    ## 5121      (03) Good (01) Excellent
    ## 5122 (01) Excellent (01) Excellent
    ## 5123 (01) Excellent (01) Excellent
    ## 5124 (02) Very Good (01) Excellent
    ## 5125      (04) Fair      (03) Good
    ## 5126      (03) Good (01) Excellent
    ## 5127 (02) Very Good (01) Excellent
    ## 5128 (02) Very Good (02) Very Good
    ## 5129      (03) Good      (03) Good
    ## 5130      (03) Good (02) Very Good
    ## 5131 (01) Excellent (01) Excellent
    ## 5132 (01) Excellent (02) Very Good
    ## 5133      (03) Good      (03) Good
    ## 5134 (02) Very Good (02) Very Good
    ## 5135      (03) Good (02) Very Good
    ## 5136      (03) Good      (03) Good
    ## 5137      (03) Good (02) Very Good
    ## 5138 (02) Very Good (01) Excellent
    ## 5139      (03) Good (01) Excellent
    ## 5140      (03) Good (02) Very Good
    ## 5141      (04) Fair (02) Very Good
    ## 5142 (02) Very Good (02) Very Good
    ## 5143 (01) Excellent (01) Excellent
    ## 5144      (03) Good (01) Excellent
    ## 5145 (02) Very Good (02) Very Good
    ## 5146 (02) Very Good (02) Very Good
    ## 5147 (02) Very Good (02) Very Good
    ## 5148 (01) Excellent (02) Very Good
    ## 5149 (02) Very Good (02) Very Good
    ## 5150 (01) Excellent (01) Excellent
    ## 5151 (02) Very Good (02) Very Good
    ## 5152 (02) Very Good (02) Very Good
    ## 5153 (02) Very Good (02) Very Good
    ## 5154 (01) Excellent (01) Excellent
    ## 5155 (01) Excellent (01) Excellent
    ## 5156 (02) Very Good (02) Very Good
    ## 5157 (01) Excellent (02) Very Good
    ## 5158 (02) Very Good (02) Very Good
    ## 5159      (03) Good      (04) Fair
    ## 5160 (02) Very Good (02) Very Good
    ## 5161      (03) Good      (03) Good
    ## 5162      (03) Good      (04) Fair
    ## 5163      (03) Good      (03) Good
    ## 5164 (01) Excellent      (03) Good
    ## 5165      (04) Fair (02) Very Good
    ## 5166      (04) Fair (02) Very Good
    ## 5167      (03) Good (01) Excellent
    ## 5168 (02) Very Good (02) Very Good
    ## 5169      (03) Good      (03) Good
    ## 5170 (02) Very Good (02) Very Good
    ## 5171      (03) Good (01) Excellent
    ## 5172      (04) Fair (01) Excellent
    ## 5173      (03) Good (02) Very Good
    ## 5174      (03) Good (01) Excellent
    ## 5175      (03) Good (01) Excellent
    ## 5176      (03) Good (01) Excellent
    ## 5177      (03) Good (01) Excellent
    ## 5178 (01) Excellent (01) Excellent
    ## 5179      (03) Good (02) Very Good
    ## 5180      (03) Good (01) Excellent
    ## 5181 (02) Very Good (01) Excellent
    ## 5182 (01) Excellent (01) Excellent
    ## 5183 (02) Very Good (02) Very Good
    ## 5184 (01) Excellent (01) Excellent
    ## 5185 (01) Excellent (01) Excellent
    ## 5186 (02) Very Good (01) Excellent
    ## 5187 (02) Very Good (02) Very Good
    ## 5188 (02) Very Good      (03) Good
    ## 5189      (03) Good      (03) Good
    ## 5190      (03) Good      (03) Good
    ## 5191      (03) Good (02) Very Good
    ## 5192      (04) Fair      (03) Good
    ## 5193 (01) Excellent (01) Excellent
    ## 5194 (01) Excellent (02) Very Good
    ## 5195 (02) Very Good (02) Very Good
    ## 5196      (03) Good (02) Very Good
    ## 5197      (04) Fair      (04) Fair
    ## 5198      (05) Poor (02) Very Good
    ## 5199 (01) Excellent (01) Excellent
    ## 5200 (02) Very Good (01) Excellent
    ## 5201      (03) Good (01) Excellent
    ## 5202 (01) Excellent (01) Excellent
    ## 5203 (02) Very Good (02) Very Good
    ## 5204      (03) Good      (03) Good
    ## 5205 (01) Excellent (01) Excellent
    ## 5206 (01) Excellent (01) Excellent
    ## 5207      (03) Good (02) Very Good
    ## 5208      (03) Good (02) Very Good
    ## 5209 (02) Very Good (02) Very Good
    ## 5210      (03) Good (02) Very Good
    ## 5211      (03) Good      (03) Good
    ## 5212 (02) Very Good (02) Very Good
    ## 5213 (02) Very Good (02) Very Good
    ## 5214 (02) Very Good (02) Very Good
    ## 5215 (02) Very Good (02) Very Good
    ## 5216 (02) Very Good (02) Very Good
    ## 5217      (04) Fair      (03) Good
    ## 5218 (01) Excellent (01) Excellent
    ## 5219      (03) Good      (03) Good
    ## 5220      (03) Good (02) Very Good
    ## 5221 (02) Very Good      (03) Good
    ## 5222 (02) Very Good (02) Very Good
    ## 5223      (05) Poor (02) Very Good
    ## 5224      (03) Good (01) Excellent
    ## 5225 (02) Very Good (02) Very Good
    ## 5226      (03) Good (02) Very Good
    ## 5227 (01) Excellent (02) Very Good
    ## 5228 (02) Very Good (02) Very Good
    ## 5229      (03) Good      (03) Good
    ## 5230      (03) Good (02) Very Good
    ## 5231 (02) Very Good (02) Very Good
    ## 5232 (01) Excellent (01) Excellent
    ## 5233      (03) Good      (03) Good
    ## 5234 (02) Very Good (02) Very Good
    ## 5235 (02) Very Good (02) Very Good
    ## 5236 (01) Excellent (02) Very Good
    ## 5237 (01) Excellent (01) Excellent
    ## 5238      (04) Fair (01) Excellent
    ## 5239      (03) Good (02) Very Good
    ## 5240 (02) Very Good (02) Very Good
    ## 5241      (03) Good (02) Very Good
    ## 5242 (02) Very Good (01) Excellent
    ## 5243      (03) Good      (03) Good
    ## 5244      (04) Fair      (03) Good
    ## 5245 (02) Very Good (02) Very Good
    ## 5246      (03) Good (02) Very Good
    ## 5247      (03) Good (02) Very Good
    ## 5248      (03) Good (02) Very Good
    ## 5249      (03) Good (02) Very Good
    ## 5250      (04) Fair      (04) Fair
    ## 5251 (02) Very Good (02) Very Good
    ## 5252 (01) Excellent (01) Excellent
    ## 5253 (02) Very Good (01) Excellent
    ## 5254      (04) Fair      (03) Good
    ## 5255      (03) Good      (03) Good
    ## 5256 (02) Very Good (02) Very Good
    ## 5257      (04) Fair      (03) Good
    ## 5258 (01) Excellent (01) Excellent
    ## 5259      (03) Good (02) Very Good
    ## 5260 (02) Very Good (02) Very Good
    ## 5261 (02) Very Good (02) Very Good
    ## 5262      (03) Good      (03) Good
    ## 5263 (01) Excellent (02) Very Good
    ## 5264      (03) Good      (03) Good
    ## 5265 (01) Excellent (01) Excellent
    ## 5266      (03) Good (02) Very Good
    ## 5267 (02) Very Good (01) Excellent
    ## 5268 (02) Very Good      (03) Good
    ## 5269 (02) Very Good (02) Very Good
    ## 5270      (03) Good      (03) Good
    ## 5271      (04) Fair (01) Excellent
    ## 5272      (05) Poor      (03) Good
    ## 5273 (02) Very Good (01) Excellent
    ## 5274 (02) Very Good (02) Very Good
    ## 5275      (03) Good (02) Very Good
    ## 5276 (02) Very Good (01) Excellent
    ## 5277 (01) Excellent (01) Excellent
    ## 5278      (04) Fair (02) Very Good
    ## 5279      (03) Good (02) Very Good
    ## 5280      (04) Fair      (03) Good
    ## 5281 (01) Excellent (01) Excellent
    ## 5282      (03) Good      (03) Good
    ## 5283      (03) Good      (03) Good
    ## 5284 (02) Very Good (02) Very Good
    ## 5285 (02) Very Good (02) Very Good
    ## 5286 (02) Very Good (02) Very Good
    ## 5287 (02) Very Good (01) Excellent
    ## 5288 (01) Excellent (01) Excellent
    ## 5289 (02) Very Good      (03) Good
    ## 5290      (04) Fair      (04) Fair
    ## 5291 (02) Very Good      (03) Good
    ## 5292 (02) Very Good      (03) Good
    ## 5293 (02) Very Good (02) Very Good
    ## 5294 (01) Excellent (01) Excellent
    ## 5295      (04) Fair      (03) Good
    ## 5296 (02) Very Good (02) Very Good
    ## 5297 (01) Excellent (01) Excellent
    ## 5298      (03) Good      (03) Good
    ## 5299      (04) Fair      (04) Fair
    ## 5300      (03) Good      (03) Good
    ## 5301 (01) Excellent (01) Excellent
    ## 5302      (04) Fair (02) Very Good
    ## 5303 (02) Very Good (02) Very Good
    ## 5304      (04) Fair      (03) Good
    ## 5305 (02) Very Good      (03) Good
    ## 5306 (02) Very Good (02) Very Good
    ## 5307      (03) Good      (03) Good
    ## 5308      (03) Good      (03) Good
    ## 5309 (02) Very Good (02) Very Good
    ## 5310 (02) Very Good (02) Very Good
    ## 5311 (01) Excellent (01) Excellent
    ## 5312      (03) Good (01) Excellent
    ## 5313 (01) Excellent (01) Excellent
    ## 5314 (02) Very Good (02) Very Good
    ## 5315 (01) Excellent (01) Excellent
    ## 5316 (01) Excellent (01) Excellent
    ## 5317      (03) Good      (04) Fair
    ## 5318      (03) Good      (03) Good
    ## 5319 (01) Excellent      (03) Good
    ## 5320      (03) Good (02) Very Good
    ## 5321      (03) Good      (03) Good
    ## 5322      (05) Poor      (04) Fair
    ## 5323      (03) Good (02) Very Good
    ## 5324      (03) Good      (03) Good
    ## 5325      (03) Good      (03) Good
    ## 5326 (02) Very Good (02) Very Good
    ## 5327 (02) Very Good (02) Very Good
    ## 5328      (04) Fair      (03) Good
    ## 5329      (04) Fair      (04) Fair
    ## 5330 (02) Very Good (02) Very Good
    ## 5331 (02) Very Good (02) Very Good
    ## 5332 (02) Very Good (02) Very Good
    ## 5333 (01) Excellent (01) Excellent
    ## 5334      (03) Good      (04) Fair
    ## 5335 (01) Excellent (01) Excellent
    ## 5336 (02) Very Good (01) Excellent
    ## 5337 (01) Excellent (01) Excellent
    ## 5338 (02) Very Good (02) Very Good
    ## 5339 (02) Very Good (02) Very Good
    ## 5340      (05) Poor      (05) Poor
    ## 5341      (03) Good      (03) Good
    ## 5342 (02) Very Good (02) Very Good
    ## 5343      (03) Good      (03) Good
    ## 5344      (03) Good (01) Excellent
    ## 5345      (03) Good (01) Excellent
    ## 5346      (03) Good      (03) Good
    ## 5347 (02) Very Good (02) Very Good
    ## 5348      (03) Good (02) Very Good
    ## 5349      (03) Good (01) Excellent
    ## 5350 (02) Very Good (02) Very Good
    ## 5351 (02) Very Good (02) Very Good
    ## 5352      (03) Good      (04) Fair
    ## 5353 (02) Very Good (02) Very Good
    ## 5354 (01) Excellent (01) Excellent
    ## 5355 (02) Very Good (02) Very Good
    ## 5356 (01) Excellent (01) Excellent
    ## 5357 (02) Very Good (01) Excellent
    ## 5358 (02) Very Good (01) Excellent
    ## 5359 (02) Very Good (02) Very Good
    ## 5360 (02) Very Good (01) Excellent
    ## 5361 (02) Very Good (02) Very Good
    ## 5362 (01) Excellent      (03) Good
    ## 5363      (05) Poor (02) Very Good
    ## 5364      (03) Good (01) Excellent
    ## 5365 (02) Very Good (01) Excellent
    ## 5366      (04) Fair (01) Excellent
    ## 5367 (02) Very Good (02) Very Good
    ## 5368      (04) Fair (01) Excellent
    ## 5369 (02) Very Good (01) Excellent
    ## 5370      (04) Fair      (04) Fair
    ## 5371      (04) Fair      (03) Good
    ## 5372 (02) Very Good (01) Excellent
    ## 5373 (02) Very Good (01) Excellent
    ## 5374 (02) Very Good (01) Excellent
    ## 5375 (02) Very Good (01) Excellent
    ## 5376      (05) Poor      (03) Good
    ## 5377 (01) Excellent (01) Excellent
    ## 5378 (02) Very Good (02) Very Good
    ## 5379 (01) Excellent (02) Very Good
    ## 5380      (03) Good      (04) Fair
    ## 5381 (01) Excellent (01) Excellent
    ## 5382 (01) Excellent (01) Excellent
    ## 5383      (03) Good (01) Excellent
    ## 5384      (04) Fair      (03) Good
    ## 5385      (03) Good      (04) Fair
    ## 5386      (03) Good      (03) Good
    ## 5387      (03) Good      (03) Good
    ## 5388 (02) Very Good (02) Very Good
    ## 5389      (05) Poor (01) Excellent
    ## 5390 (02) Very Good (02) Very Good
    ## 5391 (01) Excellent (01) Excellent
    ## 5392      (03) Good (02) Very Good
    ## 5393      (03) Good      (03) Good
    ## 5394      (03) Good (01) Excellent
    ## 5395 (02) Very Good (02) Very Good
    ## 5396      (03) Good      (03) Good
    ## 5397      (03) Good      (03) Good
    ## 5398      (03) Good (02) Very Good
    ## 5399 (02) Very Good (01) Excellent
    ## 5400 (01) Excellent (01) Excellent
    ## 5401 (01) Excellent (01) Excellent
    ## 5402      (04) Fair (02) Very Good
    ## 5403      (03) Good (02) Very Good
    ## 5404 (01) Excellent (01) Excellent
    ## 5405 (01) Excellent (01) Excellent
    ## 5406      (03) Good (01) Excellent
    ## 5407 (02) Very Good (02) Very Good
    ## 5408 (01) Excellent (01) Excellent
    ## 5409 (02) Very Good (02) Very Good
    ## 5410 (02) Very Good (02) Very Good
    ## 5411 (02) Very Good (02) Very Good
    ## 5412 (02) Very Good      (03) Good
    ## 5413 (02) Very Good      (03) Good
    ## 5414      (04) Fair (02) Very Good
    ## 5415 (02) Very Good      (03) Good
    ## 5416      (05) Poor (02) Very Good
    ## 5417 (01) Excellent (01) Excellent
    ## 5418 (02) Very Good (01) Excellent
    ## 5419      (04) Fair (02) Very Good
    ## 5420      (03) Good (01) Excellent
    ## 5421      (04) Fair      (03) Good
    ## 5422      (03) Good (02) Very Good
    ## 5423      (04) Fair      (04) Fair
    ## 5424      (04) Fair      (04) Fair
    ## 5425 (01) Excellent (01) Excellent
    ## 5426      (04) Fair (01) Excellent
    ## 5427 (02) Very Good (01) Excellent
    ## 5428      (03) Good (02) Very Good
    ## 5429 (01) Excellent (01) Excellent
    ## 5430      (03) Good      (03) Good
    ## 5431 (02) Very Good (02) Very Good
    ## 5432 (02) Very Good (02) Very Good
    ## 5433 (02) Very Good (02) Very Good
    ## 5434      (03) Good (02) Very Good
    ## 5435 (02) Very Good (01) Excellent
    ## 5436 (02) Very Good (01) Excellent
    ## 5437      (03) Good      (03) Good
    ## 5438 (01) Excellent (01) Excellent
    ## 5439      (03) Good      (03) Good
    ## 5440 (02) Very Good (02) Very Good
    ## 5441      (04) Fair      (03) Good
    ## 5442      (04) Fair (01) Excellent
    ## 5443 (02) Very Good      (03) Good
    ## 5444 (02) Very Good      (03) Good
    ## 5445      (05) Poor      (03) Good
    ## 5446      (03) Good      (03) Good
    ## 5447 (02) Very Good (02) Very Good
    ## 5448      (03) Good (02) Very Good
    ## 5449 (01) Excellent (02) Very Good
    ## 5450 (02) Very Good (02) Very Good
    ## 5451      (04) Fair      (03) Good
    ## 5452      (03) Good      (03) Good
    ## 5453 (01) Excellent (01) Excellent
    ## 5454      (04) Fair (02) Very Good
    ## 5455      (04) Fair      (04) Fair
    ## 5456      (04) Fair      (03) Good
    ## 5457      (03) Good (02) Very Good
    ## 5458      (03) Good      (03) Good
    ## 5459 (01) Excellent (01) Excellent
    ## 5460      (03) Good (02) Very Good
    ## 5461      (03) Good (02) Very Good
    ## 5462 (02) Very Good (02) Very Good
    ## 5463      (04) Fair (02) Very Good
    ## 5464 (02) Very Good (01) Excellent
    ## 5465      (03) Good      (03) Good
    ## 5466 (02) Very Good (01) Excellent
    ## 5467 (01) Excellent (01) Excellent
    ## 5468      (03) Good (01) Excellent
    ## 5469 (01) Excellent (01) Excellent
    ## 5470 (02) Very Good (01) Excellent
    ## 5471      (03) Good      (03) Good
    ## 5472      (03) Good (01) Excellent
    ## 5473      (04) Fair (02) Very Good
    ## 5474 (02) Very Good (02) Very Good
    ## 5475 (02) Very Good (01) Excellent
    ## 5476 (02) Very Good (01) Excellent
    ## 5477      (03) Good (02) Very Good
    ## 5478      (03) Good      (03) Good
    ## 5479 (02) Very Good (02) Very Good
    ## 5480      (03) Good (02) Very Good
    ## 5481      (03) Good      (03) Good
    ## 5482 (02) Very Good (01) Excellent
    ## 5483 (01) Excellent (01) Excellent
    ## 5484 (01) Excellent (01) Excellent
    ## 5485      (04) Fair (02) Very Good
    ## 5486 (02) Very Good      (03) Good
    ## 5487 (02) Very Good      (03) Good
    ## 5488 (02) Very Good (02) Very Good
    ## 5489 (01) Excellent (01) Excellent
    ## 5490 (01) Excellent (02) Very Good
    ## 5491      (03) Good (02) Very Good
    ## 5492      (03) Good      (04) Fair
    ## 5493 (02) Very Good (01) Excellent
    ## 5494 (01) Excellent (01) Excellent
    ## 5495 (01) Excellent (01) Excellent
    ## 5496 (02) Very Good (01) Excellent
    ## 5497 (01) Excellent (01) Excellent
    ## 5498 (02) Very Good (02) Very Good
    ## 5499      (03) Good (02) Very Good
    ## 5500 (02) Very Good (01) Excellent
    ## 5501 (02) Very Good      (03) Good
    ## 5502 (01) Excellent (01) Excellent
    ## 5503 (01) Excellent (02) Very Good
    ## 5504 (01) Excellent (01) Excellent
    ## 5505 (01) Excellent (01) Excellent
    ## 5506 (02) Very Good (01) Excellent
    ## 5507 (02) Very Good (02) Very Good
    ## 5508 (02) Very Good (02) Very Good
    ## 5509      (04) Fair (02) Very Good
    ## 5510 (02) Very Good (01) Excellent
    ## 5511 (02) Very Good (01) Excellent
    ## 5512      (04) Fair      (03) Good
    ## 5513      (04) Fair (02) Very Good
    ## 5514 (01) Excellent (01) Excellent
    ## 5515 (02) Very Good (01) Excellent
    ## 5516      (03) Good (02) Very Good
    ## 5517 (01) Excellent (02) Very Good
    ## 5518 (02) Very Good (02) Very Good
    ## 5519      (03) Good      (04) Fair
    ## 5520 (02) Very Good      (03) Good
    ## 5521 (01) Excellent (01) Excellent
    ## 5522      (04) Fair (02) Very Good
    ## 5523 (01) Excellent (01) Excellent
    ## 5524 (01) Excellent (01) Excellent
    ## 5525      (03) Good      (03) Good
    ## 5526      (03) Good      (03) Good
    ## 5527 (02) Very Good (02) Very Good
    ## 5528 (01) Excellent (01) Excellent
    ## 5529 (02) Very Good (01) Excellent
    ## 5530      (04) Fair (02) Very Good
    ## 5531 (02) Very Good (02) Very Good
    ## 5532 (02) Very Good (01) Excellent
    ## 5533 (02) Very Good (01) Excellent
    ## 5534 (01) Excellent (01) Excellent
    ## 5535 (02) Very Good (02) Very Good
    ## 5536      (03) Good (01) Excellent
    ## 5537      (04) Fair (02) Very Good
    ## 5538      (03) Good (01) Excellent
    ## 5539      (03) Good (01) Excellent
    ## 5540 (02) Very Good (01) Excellent
    ## 5541 (01) Excellent (01) Excellent
    ## 5542 (01) Excellent (01) Excellent
    ## 5543 (02) Very Good (01) Excellent
    ## 5544 (02) Very Good      (04) Fair
    ## 5545 (01) Excellent (01) Excellent
    ## 5546 (01) Excellent (01) Excellent
    ## 5547 (02) Very Good (02) Very Good
    ## 5548 (02) Very Good      (04) Fair
    ## 5549 (01) Excellent (01) Excellent
    ## 5550      (04) Fair (02) Very Good
    ## 5551      (04) Fair      (03) Good
    ## 5552      (03) Good      (03) Good
    ## 5553 (02) Very Good (01) Excellent
    ## 5554 (01) Excellent      (03) Good
    ## 5555      (03) Good (02) Very Good
    ## 5556 (02) Very Good (02) Very Good
    ## 5557 (02) Very Good (02) Very Good
    ## 5558 (02) Very Good (02) Very Good
    ## 5559      (03) Good (02) Very Good
    ## 5560 (02) Very Good (02) Very Good
    ## 5561      (03) Good      (03) Good
    ## 5562 (02) Very Good (01) Excellent
    ## 5563 (02) Very Good      (03) Good
    ## 5564      (03) Good      (04) Fair
    ## 5565 (02) Very Good (02) Very Good
    ## 5566 (02) Very Good (02) Very Good
    ## 5567 (01) Excellent (01) Excellent
    ## 5568 (02) Very Good (02) Very Good
    ## 5569 (02) Very Good (02) Very Good
    ## 5570 (02) Very Good (01) Excellent
    ## 5571      (04) Fair (02) Very Good
    ## 5572 (01) Excellent (01) Excellent
    ## 5573      (03) Good (01) Excellent
    ## 5574      (04) Fair      (04) Fair
    ## 5575      (03) Good (01) Excellent
    ## 5576 (02) Very Good (02) Very Good
    ## 5577      (04) Fair      (04) Fair
    ## 5578      (03) Good      (03) Good
    ## 5579 (01) Excellent (01) Excellent
    ## 5580 (01) Excellent      (03) Good
    ## 5581      (03) Good      (03) Good
    ## 5582 (01) Excellent (01) Excellent
    ## 5583      (03) Good      (03) Good
    ## 5584      (03) Good      (03) Good
    ## 5585      (03) Good      (03) Good
    ## 5586      (03) Good      (03) Good
    ## 5587 (02) Very Good      (03) Good
    ## 5588 (02) Very Good (02) Very Good
    ## 5589      (03) Good      (03) Good
    ## 5590      (05) Poor      (04) Fair
    ## 5591 (02) Very Good (02) Very Good
    ## 5592 (01) Excellent      (03) Good
    ## 5593      (03) Good      (04) Fair
    ## 5594 (02) Very Good (02) Very Good
    ## 5595      (03) Good      (03) Good
    ## 5596 (02) Very Good (02) Very Good
    ## 5597 (02) Very Good (02) Very Good
    ## 5598      (04) Fair      (04) Fair
    ## 5599 (02) Very Good (02) Very Good
    ## 5600 (01) Excellent (01) Excellent
    ## 5601      (03) Good      (03) Good
    ## 5602      (04) Fair      (03) Good
    ## 5603 (02) Very Good (02) Very Good
    ## 5604      (03) Good      (03) Good
    ## 5605      (04) Fair      (04) Fair
    ## 5606 (01) Excellent (01) Excellent
    ## 5607      (04) Fair      (04) Fair
    ## 5608      (04) Fair (02) Very Good
    ## 5609 (02) Very Good (02) Very Good
    ## 5610 (01) Excellent (01) Excellent
    ## 5611 (01) Excellent (01) Excellent
    ## 5612 (02) Very Good      (03) Good
    ## 5613      (03) Good      (03) Good
    ## 5614 (01) Excellent (01) Excellent
    ## 5615 (01) Excellent (01) Excellent
    ## 5616      (04) Fair      (03) Good
    ## 5617 (01) Excellent (01) Excellent
    ## 5618 (02) Very Good (02) Very Good
    ## 5619      (03) Good (02) Very Good
    ## 5620 (02) Very Good (02) Very Good
    ## 5621      (03) Good      (03) Good
    ## 5622 (02) Very Good (02) Very Good
    ## 5623      (03) Good (02) Very Good
    ## 5624 (01) Excellent (01) Excellent
    ## 5625 (02) Very Good (02) Very Good
    ## 5626 (01) Excellent (01) Excellent
    ## 5627 (02) Very Good      (03) Good
    ## 5628      (04) Fair      (03) Good
    ## 5629 (02) Very Good (02) Very Good
    ## 5630 (02) Very Good (02) Very Good
    ## 5631      (03) Good      (03) Good
    ## 5632      (03) Good      (03) Good
    ## 5633 (02) Very Good (02) Very Good
    ## 5634 (01) Excellent (01) Excellent
    ## 5635      (03) Good      (03) Good
    ## 5636 (02) Very Good (02) Very Good
    ## 5637 (01) Excellent (01) Excellent
    ## 5638 (01) Excellent (01) Excellent
    ## 5639      (03) Good (02) Very Good
    ## 5640 (01) Excellent (01) Excellent
    ## 5641      (03) Good      (03) Good
    ## 5642 (02) Very Good (02) Very Good
    ## 5643 (02) Very Good (02) Very Good
    ## 5644      (03) Good      (03) Good
    ## 5645 (02) Very Good (01) Excellent
    ## 5646 (02) Very Good (02) Very Good
    ## 5647      (03) Good      (03) Good
    ## 5648 (02) Very Good (02) Very Good
    ## 5649 (02) Very Good (01) Excellent
    ## 5650      (04) Fair (02) Very Good
    ## 5651      (04) Fair      (03) Good
    ## 5652      (05) Poor      (05) Poor
    ## 5653 (02) Very Good (02) Very Good
    ## 5654      (04) Fair      (03) Good
    ## 5655 (01) Excellent (02) Very Good
    ## 5656      (03) Good      (03) Good
    ## 5657 (02) Very Good      (03) Good
    ## 5658 (02) Very Good (02) Very Good
    ## 5659      (03) Good      (04) Fair
    ## 5660 (02) Very Good (02) Very Good
    ## 5661 (02) Very Good (02) Very Good
    ## 5662      (03) Good      (03) Good
    ## 5663      (05) Poor      (04) Fair
    ## 5664      (04) Fair      (04) Fair
    ## 5665      (03) Good      (04) Fair
    ## 5666 (02) Very Good (02) Very Good
    ## 5667 (01) Excellent (02) Very Good
    ## 5668      (04) Fair      (03) Good
    ## 5669      (04) Fair (02) Very Good
    ## 5670 (01) Excellent (01) Excellent
    ## 5671 (02) Very Good (02) Very Good
    ## 5672 (02) Very Good (02) Very Good
    ## 5673 (02) Very Good (02) Very Good
    ## 5674      (03) Good (02) Very Good
    ## 5675 (02) Very Good      (03) Good
    ## 5676 (02) Very Good (02) Very Good
    ## 5677      (04) Fair (02) Very Good
    ## 5678      (03) Good      (03) Good
    ## 5679      (04) Fair      (04) Fair
    ## 5680 (01) Excellent (01) Excellent
    ## 5681 (02) Very Good (02) Very Good
    ## 5682 (01) Excellent (01) Excellent
    ## 5683      (03) Good      (04) Fair
    ## 5684      (04) Fair      (04) Fair
    ## 5685 (02) Very Good (02) Very Good
    ## 5686 (02) Very Good (02) Very Good
    ## 5687      (04) Fair      (03) Good
    ## 5688      (03) Good      (03) Good
    ## 5689      (04) Fair      (03) Good
    ## 5690 (02) Very Good      (04) Fair
    ## 5691      (03) Good      (03) Good
    ## 5692 (02) Very Good (02) Very Good
    ## 5693      (03) Good (02) Very Good
    ## 5694      (04) Fair      (05) Poor
    ## 5695      (05) Poor      (03) Good
    ## 5696 (02) Very Good      (03) Good
    ## 5697      (03) Good      (03) Good
    ## 5698      (05) Poor      (04) Fair
    ## 5699      (04) Fair      (04) Fair
    ## 5700      (03) Good      (03) Good
    ## 5701      (03) Good      (03) Good
    ## 5702 (02) Very Good (02) Very Good
    ## 5703 (02) Very Good (02) Very Good
    ## 5704      (04) Fair      (03) Good
    ## 5705      (03) Good      (03) Good
    ## 5706      (05) Poor      (04) Fair
    ## 5707      (04) Fair      (04) Fair
    ## 5708      (05) Poor      (03) Good
    ## 5709 (02) Very Good      (03) Good
    ## 5710 (02) Very Good (02) Very Good
    ## 5711      (03) Good (02) Very Good
    ## 5712 (02) Very Good (02) Very Good
    ## 5713      (04) Fair      (03) Good
    ## 5714      (03) Good      (03) Good
    ## 5715 (02) Very Good (02) Very Good
    ## 5716 (01) Excellent (01) Excellent
    ## 5717      (04) Fair      (04) Fair
    ## 5718      (03) Good      (03) Good
    ## 5719 (02) Very Good      (03) Good
    ## 5720      (03) Good (02) Very Good
    ## 5721 (02) Very Good (02) Very Good
    ## 5722 (02) Very Good (02) Very Good
    ## 5723 (02) Very Good (02) Very Good
    ## 5724 (02) Very Good (01) Excellent
    ## 5725 (02) Very Good      (03) Good
    ## 5726 (02) Very Good (02) Very Good
    ## 5727      (03) Good (02) Very Good
    ## 5728      (03) Good (02) Very Good
    ## 5729      (03) Good      (03) Good
    ## 5730 (02) Very Good      (03) Good
    ## 5731 (02) Very Good (02) Very Good
    ## 5732      (03) Good      (03) Good
    ## 5733      (05) Poor      (03) Good
    ## 5734      (03) Good      (03) Good
    ## 5735      (03) Good      (04) Fair
    ## 5736      (03) Good      (03) Good
    ## 5737      (03) Good      (03) Good
    ## 5738 (01) Excellent (01) Excellent
    ## 5739      (03) Good      (04) Fair
    ## 5740 (02) Very Good (02) Very Good
    ## 5741      (03) Good      (04) Fair
    ## 5742      (05) Poor (01) Excellent
    ## 5743      (03) Good      (03) Good
    ## 5744      (03) Good      (04) Fair
    ## 5745      (03) Good (02) Very Good
    ## 5746      (03) Good      (03) Good
    ## 5747      (04) Fair (01) Excellent
    ## 5748      (03) Good      (03) Good
    ## 5749 (02) Very Good      (03) Good
    ## 5750      (04) Fair (01) Excellent
    ## 5751      (04) Fair (02) Very Good
    ## 5752      (04) Fair      (03) Good
    ## 5753      (04) Fair      (04) Fair
    ## 5754      (03) Good      (03) Good
    ## 5755      (04) Fair      (03) Good
    ## 5756      (03) Good      (03) Good
    ## 5757 (01) Excellent (01) Excellent
    ## 5758      (03) Good      (03) Good
    ## 5759      (03) Good      (03) Good
    ## 5760      (03) Good      (03) Good
    ## 5761      (03) Good      (03) Good
    ## 5762      (03) Good      (03) Good
    ## 5763 (02) Very Good      (03) Good
    ## 5764 (02) Very Good (02) Very Good
    ## 5765 (02) Very Good      (03) Good
    ## 5766      (03) Good      (03) Good
    ## 5767 (02) Very Good      (03) Good
    ## 5768 (01) Excellent (01) Excellent
    ## 5769 (02) Very Good (01) Excellent
    ## 5770      (03) Good (01) Excellent
    ## 5771      (03) Good (02) Very Good
    ## 5772 (01) Excellent      (04) Fair
    ## 5773      (04) Fair (01) Excellent
    ## 5774      (04) Fair (02) Very Good
    ## 5775 (01) Excellent (02) Very Good
    ## 5776 (01) Excellent      (03) Good
    ## 5777 (02) Very Good      (05) Poor
    ## 5778      (03) Good      (03) Good
    ## 5779 (02) Very Good (02) Very Good
    ## 5780      (03) Good      (03) Good
    ## 5781 (02) Very Good      (03) Good
    ## 5782      (03) Good      (03) Good
    ## 5783 (01) Excellent (01) Excellent
    ## 5784 (02) Very Good (01) Excellent
    ## 5785      (04) Fair      (03) Good
    ## 5786 (02) Very Good (02) Very Good
    ## 5787 (01) Excellent (01) Excellent
    ## 5788      (04) Fair      (03) Good
    ## 5789 (02) Very Good      (03) Good
    ## 5790 (02) Very Good      (04) Fair
    ## 5791      (05) Poor      (03) Good
    ## 5792      (03) Good      (03) Good
    ## 5793      (04) Fair      (04) Fair
    ## 5794 (01) Excellent (02) Very Good
    ## 5795      (04) Fair      (03) Good
    ## 5796      (04) Fair (01) Excellent
    ## 5797 (02) Very Good (02) Very Good
    ## 5798 (02) Very Good      (03) Good
    ## 5799      (03) Good (02) Very Good
    ## 5800 (02) Very Good (02) Very Good
    ## 5801      (04) Fair      (03) Good
    ## 5802      (03) Good      (03) Good
    ## 5803 (01) Excellent (01) Excellent
    ## 5804      (04) Fair      (04) Fair
    ## 5805 (02) Very Good (02) Very Good
    ## 5806 (01) Excellent (01) Excellent
    ## 5807 (02) Very Good (02) Very Good
    ## 5808      (03) Good (02) Very Good
    ## 5809      (03) Good (01) Excellent
    ## 5810      (03) Good (02) Very Good
    ## 5811      (04) Fair (02) Very Good
    ## 5812 (02) Very Good (02) Very Good
    ## 5813 (02) Very Good      (03) Good
    ## 5814      (04) Fair      (04) Fair
    ## 5815 (02) Very Good      (03) Good
    ## 5816 (02) Very Good (02) Very Good
    ## 5817      (04) Fair (01) Excellent
    ## 5818      (03) Good      (03) Good
    ## 5819      (03) Good (02) Very Good
    ## 5820      (03) Good      (03) Good
    ## 5821 (01) Excellent (02) Very Good
    ## 5822      (03) Good      (04) Fair
    ## 5823 (02) Very Good (02) Very Good
    ## 5824 (02) Very Good (02) Very Good
    ## 5825 (01) Excellent (02) Very Good
    ## 5826      (03) Good (01) Excellent
    ## 5827 (02) Very Good (02) Very Good
    ## 5828 (02) Very Good (02) Very Good
    ## 5829 (02) Very Good (02) Very Good
    ## 5830      (04) Fair (01) Excellent
    ## 5831 (02) Very Good (02) Very Good
    ## 5832      (05) Poor      (03) Good
    ## 5833      (03) Good (02) Very Good
    ## 5834      (03) Good      (03) Good
    ## 5835      (03) Good      (03) Good
    ## 5836      (03) Good (02) Very Good
    ## 5837      (03) Good (02) Very Good
    ## 5838      (03) Good      (03) Good
    ## 5839      (04) Fair      (04) Fair
    ## 5840      (03) Good (02) Very Good
    ## 5841 (01) Excellent (02) Very Good
    ## 5842      (03) Good (01) Excellent
    ## 5843      (03) Good (02) Very Good
    ## 5844      (04) Fair      (04) Fair
    ## 5845      (03) Good (01) Excellent
    ## 5846      (03) Good (02) Very Good
    ## 5847 (02) Very Good (01) Excellent
    ## 5848      (03) Good      (03) Good
    ## 5849      (03) Good      (03) Good
    ## 5850      (03) Good (02) Very Good
    ## 5851 (02) Very Good      (03) Good
    ## 5852 (01) Excellent (01) Excellent
    ## 5853      (03) Good (01) Excellent
    ## 5854 (02) Very Good (02) Very Good
    ## 5855 (02) Very Good (02) Very Good
    ## 5856      (03) Good (02) Very Good
    ## 5857      (04) Fair      (03) Good
    ## 5858      (03) Good      (03) Good
    ## 5859      (04) Fair (01) Excellent
    ## 5860 (02) Very Good (02) Very Good
    ## 5861 (02) Very Good      (03) Good
    ## 5862 (01) Excellent (02) Very Good
    ## 5863      (05) Poor      (03) Good
    ## 5864      (05) Poor      (05) Poor
    ## 5865      (03) Good      (03) Good
    ## 5866 (02) Very Good (02) Very Good
    ## 5867 (02) Very Good      (03) Good
    ## 5868      (03) Good (01) Excellent
    ## 5869      (03) Good      (03) Good
    ## 5870      (04) Fair (02) Very Good
    ## 5871 (01) Excellent (01) Excellent
    ## 5872 (02) Very Good (02) Very Good
    ## 5873 (02) Very Good (02) Very Good
    ## 5874 (02) Very Good (02) Very Good
    ## 5875      (03) Good      (03) Good
    ## 5876 (02) Very Good (02) Very Good
    ## 5877      (03) Good (01) Excellent
    ## 5878      (03) Good (02) Very Good
    ## 5879      (03) Good (01) Excellent
    ## 5880      (03) Good      (03) Good
    ## 5881      (04) Fair      (03) Good
    ## 5882 (02) Very Good (02) Very Good
    ## 5883      (03) Good      (03) Good
    ## 5884      (04) Fair (01) Excellent
    ## 5885      (03) Good      (04) Fair
    ## 5886      (04) Fair (01) Excellent
    ## 5887 (01) Excellent      (05) Poor
    ## 5888 (02) Very Good (02) Very Good
    ## 5889 (02) Very Good (01) Excellent
    ## 5890      (03) Good      (03) Good
    ## 5891 (02) Very Good      (03) Good
    ## 5892      (03) Good (01) Excellent
    ## 5893      (04) Fair      (03) Good
    ## 5894      (03) Good      (03) Good
    ## 5895 (01) Excellent (01) Excellent
    ## 5896 (02) Very Good (02) Very Good
    ## 5897 (02) Very Good (02) Very Good
    ## 5898 (02) Very Good (02) Very Good
    ## 5899      (04) Fair      (04) Fair
    ## 5900      (03) Good      (03) Good
    ## 5901      (04) Fair      (03) Good
    ## 5902      (03) Good      (03) Good
    ## 5903 (02) Very Good      (04) Fair
    ## 5904      (05) Poor      (04) Fair
    ## 5905 (02) Very Good (02) Very Good
    ## 5906 (02) Very Good (02) Very Good
    ## 5907 (02) Very Good      (03) Good
    ## 5908      (03) Good      (03) Good
    ## 5909      (04) Fair (01) Excellent
    ## 5910      (04) Fair      (03) Good
    ## 5911      (03) Good      (03) Good
    ## 5912 (02) Very Good (02) Very Good
    ## 5913      (05) Poor (01) Excellent
    ## 5914 (01) Excellent (01) Excellent
    ## 5915      (05) Poor      (05) Poor
    ## 5916      (04) Fair      (03) Good
    ## 5917 (02) Very Good (02) Very Good
    ## 5918      (04) Fair      (04) Fair
    ## 5919 (02) Very Good (02) Very Good
    ## 5920      (04) Fair      (03) Good
    ## 5921      (03) Good      (03) Good
    ## 5922      (04) Fair      (03) Good
    ## 5923      (04) Fair (02) Very Good
    ## 5924      (03) Good      (03) Good
    ## 5925 (01) Excellent (01) Excellent
    ## 5926 (02) Very Good (02) Very Good
    ## 5927      (03) Good      (03) Good
    ## 5928 (01) Excellent (02) Very Good
    ## 5929      (03) Good      (04) Fair
    ## 5930      (05) Poor (02) Very Good
    ## 5931      (05) Poor (02) Very Good
    ## 5932      (04) Fair      (04) Fair
    ## 5933 (02) Very Good (02) Very Good
    ## 5934      (04) Fair      (04) Fair
    ## 5935 (02) Very Good      (03) Good
    ## 5936      (03) Good (02) Very Good
    ## 5937      (03) Good      (03) Good
    ## 5938      (03) Good      (03) Good
    ## 5939 (02) Very Good      (03) Good
    ## 5940 (02) Very Good (01) Excellent
    ## 5941 (01) Excellent (01) Excellent
    ## 5942      (03) Good      (03) Good
    ## 5943      (03) Good      (03) Good
    ## 5944      (03) Good (02) Very Good
    ## 5945 (02) Very Good (02) Very Good
    ## 5946 (01) Excellent (02) Very Good
    ## 5947 (02) Very Good      (04) Fair
    ## 5948      (04) Fair      (03) Good
    ## 5949 (02) Very Good      (03) Good
    ## 5950      (03) Good      (03) Good
    ## 5951 (01) Excellent (02) Very Good
    ## 5952 (02) Very Good (02) Very Good
    ## 5953      (05) Poor (02) Very Good
    ## 5954      (03) Good      (03) Good
    ## 5955      (03) Good (02) Very Good
    ## 5956 (02) Very Good (02) Very Good
    ## 5957      (03) Good (01) Excellent
    ## 5958      (03) Good      (03) Good
    ## 5959      (03) Good (02) Very Good
    ## 5960      (03) Good (02) Very Good
    ## 5961 (01) Excellent (01) Excellent
    ## 5962 (02) Very Good (02) Very Good
    ## 5963      (03) Good      (03) Good
    ## 5964 (02) Very Good (02) Very Good
    ## 5965      (03) Good      (03) Good
    ## 5966 (02) Very Good (02) Very Good
    ## 5967      (03) Good (01) Excellent
    ## 5968      (03) Good      (03) Good
    ## 5969      (03) Good (02) Very Good
    ## 5970      (04) Fair      (03) Good
    ## 5971 (02) Very Good (02) Very Good
    ## 5972 (02) Very Good (02) Very Good
    ## 5973 (01) Excellent (01) Excellent
    ## 5974      (03) Good      (03) Good
    ## 5975      (03) Good      (03) Good
    ## 5976      (04) Fair      (03) Good
    ## 5977      (04) Fair      (03) Good
    ## 5978      (03) Good (01) Excellent
    ## 5979 (02) Very Good      (03) Good
    ## 5980      (03) Good      (03) Good
    ## 5981 (02) Very Good (02) Very Good
    ## 5982      (03) Good      (03) Good
    ## 5983      (04) Fair      (03) Good
    ## 5984 (01) Excellent (02) Very Good
    ## 5985      (03) Good (02) Very Good
    ## 5986 (02) Very Good (02) Very Good
    ## 5987      (03) Good      (03) Good
    ## 5988      (03) Good (02) Very Good
    ## 5989 (02) Very Good (02) Very Good
    ## 5990      (03) Good      (03) Good
    ## 5991      (03) Good      (03) Good
    ## 5992 (01) Excellent (01) Excellent
    ## 5993 (01) Excellent (01) Excellent
    ## 5994 (01) Excellent (01) Excellent
    ## 5995      (05) Poor      (05) Poor
    ## 5996 (02) Very Good (02) Very Good
    ## 5997      (03) Good      (03) Good
    ## 5998 (02) Very Good      (03) Good
    ## 5999      (04) Fair      (04) Fair
    ## 6000      (03) Good      (03) Good
    ## 6001      (03) Good (02) Very Good
    ## 6002 (02) Very Good (02) Very Good
    ## 6003      (03) Good      (03) Good
    ## 6004      (04) Fair      (03) Good
    ## 6005      (04) Fair (02) Very Good
    ## 6006 (02) Very Good (02) Very Good
    ## 6007 (02) Very Good (02) Very Good
    ## 6008 (01) Excellent      (03) Good
    ## 6009      (04) Fair (02) Very Good
    ## 6010 (01) Excellent (01) Excellent
    ## 6011 (02) Very Good (02) Very Good
    ## 6012      (03) Good      (03) Good
    ## 6013 (02) Very Good      (03) Good
    ## 6014 (02) Very Good (02) Very Good
    ## 6015 (02) Very Good (01) Excellent
    ## 6016 (02) Very Good      (03) Good
    ## 6017 (02) Very Good      (03) Good
    ## 6018 (02) Very Good (02) Very Good
    ## 6019 (02) Very Good      (03) Good
    ## 6020      (05) Poor      (04) Fair
    ## 6021 (02) Very Good      (03) Good
    ## 6022      (03) Good (01) Excellent
    ## 6023      (03) Good      (03) Good
    ## 6024      (03) Good      (03) Good
    ## 6025      (03) Good (02) Very Good
    ## 6026 (02) Very Good (02) Very Good
    ## 6027 (01) Excellent (01) Excellent
    ## 6028      (03) Good (02) Very Good
    ## 6029      (04) Fair      (04) Fair
    ## 6030 (01) Excellent      (03) Good
    ## 6031      (03) Good      (03) Good
    ## 6032 (02) Very Good (01) Excellent
    ## 6033 (02) Very Good (01) Excellent
    ## 6034      (03) Good      (03) Good
    ## 6035 (02) Very Good (02) Very Good
    ## 6036 (02) Very Good (02) Very Good
    ## 6037      (03) Good (02) Very Good
    ## 6038      (04) Fair      (03) Good
    ## 6039      (03) Good      (03) Good
    ## 6040 (02) Very Good (01) Excellent
    ## 6041 (02) Very Good (01) Excellent
    ## 6042      (03) Good      (03) Good
    ## 6043 (01) Excellent (01) Excellent
    ## 6044      (03) Good      (04) Fair
    ## 6045 (02) Very Good (02) Very Good
    ## 6046      (03) Good      (03) Good
    ## 6047 (01) Excellent      (03) Good
    ## 6048      (03) Good      (03) Good
    ## 6049      (03) Good (02) Very Good
    ## 6050      (03) Good (02) Very Good
    ## 6051 (01) Excellent (01) Excellent
    ## 6052 (02) Very Good (02) Very Good
    ## 6053      (04) Fair      (04) Fair
    ## 6054      (04) Fair      (03) Good
    ## 6055      (04) Fair      (04) Fair
    ## 6056      (04) Fair (02) Very Good
    ## 6057 (01) Excellent (02) Very Good
    ## 6058      (03) Good (02) Very Good
    ## 6059      (03) Good (01) Excellent
    ## 6060      (03) Good      (03) Good
    ## 6061 (02) Very Good (02) Very Good
    ## 6062 (02) Very Good (02) Very Good
    ## 6063      (04) Fair (02) Very Good
    ## 6064 (01) Excellent (01) Excellent
    ## 6065      (03) Good (02) Very Good
    ## 6066      (05) Poor      (03) Good
    ## 6067      (03) Good      (05) Poor
    ## 6068 (01) Excellent (01) Excellent
    ## 6069      (04) Fair      (04) Fair
    ## 6070 (02) Very Good (02) Very Good
    ## 6071      (04) Fair      (04) Fair
    ## 6072      (04) Fair (02) Very Good
    ## 6073      (05) Poor      (05) Poor
    ## 6074 (01) Excellent (02) Very Good
    ## 6075      (03) Good      (03) Good
    ## 6076      (03) Good      (03) Good
    ## 6077      (05) Poor      (05) Poor
    ## 6078      (03) Good      (03) Good
    ## 6079      (04) Fair      (03) Good
    ## 6080 (01) Excellent (01) Excellent
    ## 6081      (04) Fair (02) Very Good
    ## 6082 (02) Very Good (01) Excellent
    ## 6083      (03) Good      (05) Poor
    ## 6084      (04) Fair      (03) Good
    ## 6085      (05) Poor      (04) Fair
    ## 6086      (03) Good      (04) Fair
    ## 6087      (03) Good (01) Excellent
    ## 6088      (03) Good      (03) Good
    ## 6089      (04) Fair      (03) Good
    ## 6090 (02) Very Good (02) Very Good
    ## 6091 (01) Excellent (01) Excellent
    ## 6092 (01) Excellent (01) Excellent
    ## 6093 (01) Excellent (01) Excellent
    ## 6094 (01) Excellent (02) Very Good
    ## 6095      (03) Good      (03) Good
    ## 6096      (03) Good (02) Very Good
    ## 6097      (04) Fair      (03) Good
    ## 6098      (03) Good      (03) Good
    ## 6099      (05) Poor      (04) Fair
    ## 6100      (04) Fair      (03) Good
    ## 6101 (02) Very Good (02) Very Good
    ## 6102 (01) Excellent (01) Excellent
    ## 6103      (04) Fair      (03) Good
    ## 6104      (04) Fair      (03) Good
    ## 6105      (03) Good      (03) Good
    ## 6106      (05) Poor      (03) Good
    ## 6107      (04) Fair      (03) Good
    ## 6108      (03) Good      (03) Good
    ## 6109      (03) Good      (03) Good
    ## 6110      (03) Good      (03) Good
    ## 6111      (03) Good (02) Very Good
    ## 6112      (03) Good      (03) Good
    ## 6113      (05) Poor      (03) Good
    ## 6114      (05) Poor      (03) Good
    ## 6115      (03) Good      (03) Good
    ## 6116 (01) Excellent (01) Excellent
    ## 6117 (02) Very Good (02) Very Good
    ## 6118      (03) Good (02) Very Good
    ## 6119      (03) Good      (03) Good
    ## 6120      (03) Good      (03) Good
    ## 6121 (02) Very Good (02) Very Good
    ## 6122 (02) Very Good      (03) Good
    ## 6123      (03) Good (02) Very Good
    ## 6124 (02) Very Good      (04) Fair
    ## 6125      (03) Good      (03) Good
    ## 6126 (02) Very Good (02) Very Good
    ## 6127 (02) Very Good (02) Very Good
    ## 6128 (02) Very Good (02) Very Good
    ## 6129 (02) Very Good (02) Very Good
    ## 6130      (03) Good      (03) Good
    ## 6131 (02) Very Good (02) Very Good
    ## 6132      (03) Good      (03) Good
    ## 6133 (02) Very Good (02) Very Good
    ## 6134      (04) Fair      (03) Good
    ## 6135 (01) Excellent (02) Very Good
    ## 6136      (03) Good (02) Very Good
    ## 6137      (03) Good      (03) Good
    ## 6138 (01) Excellent (01) Excellent
    ## 6139 (01) Excellent (01) Excellent
    ## 6140      (03) Good (02) Very Good
    ## 6141      (03) Good      (04) Fair
    ## 6142      (04) Fair      (04) Fair
    ## 6143 (02) Very Good (02) Very Good
    ## 6144 (02) Very Good (02) Very Good
    ## 6145 (02) Very Good      (03) Good
    ## 6146      (03) Good      (03) Good
    ## 6147 (02) Very Good (02) Very Good
    ## 6148 (02) Very Good      (03) Good
    ## 6149      (03) Good      (03) Good
    ## 6150 (02) Very Good (02) Very Good
    ## 6151      (05) Poor (02) Very Good
    ## 6152 (02) Very Good      (03) Good
    ## 6153 (02) Very Good (02) Very Good
    ## 6154 (01) Excellent (01) Excellent
    ## 6155      (03) Good      (03) Good
    ## 6156      (04) Fair      (05) Poor
    ## 6157 (02) Very Good (01) Excellent
    ## 6158      (03) Good      (03) Good
    ## 6159      (03) Good      (04) Fair
    ## 6160      (04) Fair (02) Very Good
    ## 6161 (02) Very Good (02) Very Good
    ## 6162 (02) Very Good (02) Very Good
    ## 6163 (02) Very Good (02) Very Good
    ## 6164      (03) Good      (03) Good
    ## 6165      (03) Good (02) Very Good
    ## 6166 (02) Very Good (02) Very Good
    ## 6167      (04) Fair      (03) Good
    ## 6168      (04) Fair      (03) Good
    ## 6169      (03) Good      (03) Good
    ## 6170      (05) Poor (01) Excellent
    ## 6171 (02) Very Good (02) Very Good
    ## 6172 (02) Very Good (02) Very Good
    ## 6173      (04) Fair      (03) Good
    ## 6174 (01) Excellent (01) Excellent
    ## 6175 (02) Very Good (02) Very Good
    ## 6176      (03) Good      (03) Good
    ## 6177      (03) Good      (03) Good
    ## 6178      (03) Good      (03) Good
    ## 6179 (02) Very Good (02) Very Good
    ## 6180      (04) Fair (02) Very Good
    ## 6181      (03) Good      (03) Good
    ## 6182      (04) Fair (02) Very Good
    ## 6183      (03) Good (02) Very Good
    ## 6184      (03) Good (02) Very Good
    ## 6185 (01) Excellent (02) Very Good
    ## 6186 (02) Very Good (02) Very Good
    ## 6187 (01) Excellent (01) Excellent
    ## 6188 (02) Very Good (02) Very Good
    ## 6189      (05) Poor      (04) Fair
    ## 6190      (04) Fair (02) Very Good
    ## 6191      (03) Good      (03) Good
    ## 6192      (04) Fair (02) Very Good
    ## 6193      (03) Good      (03) Good
    ## 6194      (03) Good (02) Very Good
    ## 6195      (03) Good      (03) Good
    ## 6196      (03) Good (02) Very Good
    ## 6197      (04) Fair (02) Very Good
    ## 6198      (03) Good (01) Excellent
    ## 6199      (04) Fair      (04) Fair
    ## 6200      (04) Fair (02) Very Good
    ## 6201      (03) Good      (03) Good
    ## 6202      (03) Good      (04) Fair
    ## 6203 (02) Very Good (02) Very Good
    ## 6204      (04) Fair (02) Very Good
    ## 6205      (03) Good      (03) Good
    ## 6206      (04) Fair      (04) Fair
    ## 6207      (04) Fair (02) Very Good
    ## 6208      (04) Fair      (03) Good
    ## 6209      (03) Good (02) Very Good
    ## 6210      (04) Fair      (04) Fair
    ## 6211      (03) Good (02) Very Good
    ## 6212      (03) Good (02) Very Good
    ## 6213 (02) Very Good (02) Very Good
    ## 6214      (05) Poor (02) Very Good
    ## 6215      (04) Fair      (04) Fair
    ## 6216      (03) Good      (03) Good
    ## 6217      (05) Poor      (03) Good
    ## 6218 (02) Very Good (02) Very Good
    ## 6219 (02) Very Good (02) Very Good
    ## 6220 (01) Excellent (01) Excellent
    ## 6221      (04) Fair      (03) Good
    ## 6222      (03) Good (02) Very Good
    ## 6223      (03) Good      (03) Good
    ## 6224 (01) Excellent (02) Very Good
    ## 6225      (04) Fair      (04) Fair
    ## 6226      (03) Good      (03) Good
    ## 6227 (02) Very Good (01) Excellent
    ## 6228 (02) Very Good (02) Very Good
    ## 6229      (03) Good      (03) Good
    ## 6230      (03) Good      (03) Good
    ## 6231      (04) Fair      (03) Good
    ## 6232 (02) Very Good (02) Very Good
    ## 6233 (01) Excellent (01) Excellent
    ## 6234 (02) Very Good (02) Very Good
    ## 6235      (04) Fair      (03) Good
    ## 6236      (03) Good      (03) Good
    ## 6237      (03) Good      (03) Good
    ## 6238      (04) Fair      (04) Fair
    ## 6239      (03) Good (02) Very Good
    ## 6240 (02) Very Good (02) Very Good
    ## 6241      (04) Fair      (04) Fair
    ## 6242      (03) Good      (03) Good
    ## 6243 (02) Very Good      (03) Good
    ## 6244 (02) Very Good      (03) Good
    ## 6245      (03) Good      (03) Good
    ## 6246      (03) Good      (03) Good
    ## 6247      (05) Poor      (04) Fair
    ## 6248 (02) Very Good (02) Very Good
    ## 6249      (04) Fair      (03) Good
    ## 6250 (01) Excellent (02) Very Good
    ## 6251      (05) Poor (02) Very Good
    ## 6252      (04) Fair (02) Very Good
    ## 6253 (01) Excellent      (03) Good
    ## 6254      (04) Fair      (03) Good
    ## 6255 (01) Excellent (01) Excellent
    ## 6256      (03) Good      (03) Good
    ## 6257      (04) Fair      (03) Good
    ## 6258 (02) Very Good (02) Very Good
    ## 6259      (03) Good      (03) Good
    ## 6260 (02) Very Good (02) Very Good
    ## 6261      (03) Good      (03) Good
    ## 6262      (04) Fair      (03) Good
    ## 6263      (03) Good      (03) Good
    ## 6264 (02) Very Good      (03) Good
    ## 6265      (04) Fair      (03) Good
    ## 6266 (01) Excellent (01) Excellent
    ## 6267      (03) Good (02) Very Good
    ## 6268 (02) Very Good (02) Very Good
    ## 6269 (02) Very Good (02) Very Good
    ## 6270      (03) Good      (03) Good
    ## 6271      (03) Good      (03) Good
    ## 6272 (01) Excellent (01) Excellent
    ## 6273      (03) Good (01) Excellent
    ## 6274 (01) Excellent      (03) Good
    ## 6275      (03) Good (02) Very Good
    ## 6276 (02) Very Good (01) Excellent
    ## 6277 (01) Excellent (01) Excellent
    ## 6278      (04) Fair      (05) Poor
    ## 6279      (03) Good      (03) Good
    ## 6280 (01) Excellent (01) Excellent
    ## 6281      (03) Good      (03) Good
    ## 6282      (03) Good (02) Very Good
    ## 6283 (02) Very Good (01) Excellent
    ## 6284 (02) Very Good (02) Very Good
    ## 6285      (03) Good (02) Very Good
    ## 6286 (02) Very Good (02) Very Good
    ## 6287 (02) Very Good (01) Excellent
    ## 6288      (04) Fair      (03) Good
    ## 6289      (03) Good (01) Excellent
    ## 6290 (02) Very Good      (03) Good
    ## 6291 (02) Very Good (02) Very Good
    ## 6292      (04) Fair      (04) Fair
    ## 6293      (04) Fair (02) Very Good
    ## 6294      (04) Fair      (03) Good
    ## 6295 (02) Very Good (02) Very Good
    ## 6296      (04) Fair      (03) Good
    ## 6297      (03) Good      (03) Good
    ## 6298      (03) Good (02) Very Good
    ## 6299 (01) Excellent (01) Excellent
    ## 6300      (03) Good      (03) Good
    ## 6301 (01) Excellent (02) Very Good
    ## 6302      (04) Fair      (04) Fair
    ## 6303 (01) Excellent (02) Very Good
    ## 6304      (03) Good      (03) Good
    ## 6305 (02) Very Good (02) Very Good
    ## 6306      (05) Poor      (04) Fair
    ## 6307      (04) Fair      (03) Good
    ## 6308      (04) Fair (02) Very Good
    ## 6309      (04) Fair (01) Excellent
    ## 6310      (03) Good (02) Very Good
    ## 6311 (02) Very Good (01) Excellent
    ## 6312 (01) Excellent (01) Excellent
    ## 6313      (04) Fair (01) Excellent
    ## 6314      (04) Fair      (03) Good
    ## 6315      (03) Good (02) Very Good
    ## 6316      (03) Good      (03) Good
    ## 6317      (04) Fair      (03) Good
    ## 6318      (04) Fair      (03) Good
    ## 6319      (03) Good (02) Very Good
    ## 6320      (03) Good (02) Very Good
    ## 6321      (04) Fair      (04) Fair
    ## 6322      (03) Good      (03) Good
    ## 6323      (03) Good      (04) Fair
    ## 6324 (02) Very Good (02) Very Good
    ## 6325 (01) Excellent (02) Very Good
    ## 6326 (01) Excellent (01) Excellent
    ## 6327 (01) Excellent (01) Excellent
    ## 6328      (04) Fair      (03) Good
    ## 6329 (02) Very Good (02) Very Good
    ## 6330      (03) Good      (03) Good
    ## 6331 (02) Very Good (02) Very Good
    ## 6332      (03) Good (02) Very Good
    ## 6333      (03) Good      (03) Good
    ## 6334      (03) Good      (04) Fair
    ## 6335      (03) Good (02) Very Good
    ## 6336      (03) Good      (03) Good
    ## 6337 (02) Very Good (02) Very Good
    ## 6338 (02) Very Good (02) Very Good
    ## 6339 (02) Very Good (02) Very Good
    ## 6340      (03) Good (02) Very Good
    ## 6341 (01) Excellent (02) Very Good
    ## 6342 (01) Excellent (01) Excellent
    ## 6343 (02) Very Good      (04) Fair
    ## 6344      (03) Good      (03) Good
    ## 6345      (04) Fair      (04) Fair
    ## 6346      (03) Good (01) Excellent
    ## 6347      (03) Good      (03) Good
    ## 6348      (03) Good      (03) Good
    ## 6349 (01) Excellent (01) Excellent
    ## 6350      (04) Fair      (05) Poor
    ## 6351      (04) Fair      (03) Good
    ## 6352      (05) Poor      (03) Good
    ## 6353 (01) Excellent      (03) Good
    ## 6354      (03) Good      (03) Good
    ## 6355      (04) Fair      (03) Good
    ## 6356      (03) Good      (03) Good
    ## 6357      (03) Good      (03) Good
    ## 6358      (04) Fair      (04) Fair
    ## 6359      (03) Good (02) Very Good
    ## 6360 (02) Very Good      (03) Good
    ## 6361      (04) Fair      (04) Fair
    ## 6362      (03) Good (02) Very Good
    ## 6363      (03) Good      (04) Fair
    ## 6364      (04) Fair      (03) Good
    ## 6365      (04) Fair      (03) Good
    ## 6366      (04) Fair      (03) Good
    ## 6367      (03) Good (02) Very Good
    ## 6368      (03) Good      (03) Good
    ## 6369      (03) Good      (03) Good
    ## 6370      (03) Good (02) Very Good
    ## 6371 (01) Excellent (01) Excellent
    ## 6372 (02) Very Good (02) Very Good
    ## 6373 (02) Very Good (02) Very Good
    ## 6374      (04) Fair      (04) Fair
    ## 6375      (04) Fair      (03) Good
    ## 6376      (05) Poor      (03) Good
    ## 6377      (03) Good      (03) Good
    ## 6378      (03) Good (01) Excellent
    ## 6379      (03) Good      (03) Good
    ## 6380      (04) Fair (02) Very Good
    ## 6381      (03) Good      (04) Fair
    ## 6382 (01) Excellent      (03) Good
    ## 6383      (03) Good (02) Very Good
    ## 6384      (04) Fair      (03) Good
    ## 6385      (03) Good      (05) Poor
    ## 6386 (02) Very Good (02) Very Good
    ## 6387      (03) Good (02) Very Good
    ## 6388      (03) Good      (03) Good
    ## 6389      (03) Good (02) Very Good
    ## 6390      (03) Good      (03) Good
    ## 6391      (03) Good      (03) Good
    ## 6392 (02) Very Good (02) Very Good
    ## 6393      (03) Good (02) Very Good
    ## 6394      (04) Fair      (04) Fair
    ## 6395      (03) Good (02) Very Good
    ## 6396      (04) Fair      (04) Fair
    ## 6397      (03) Good      (03) Good
    ## 6398 (01) Excellent      (03) Good
    ## 6399      (03) Good      (03) Good
    ## 6400      (04) Fair      (04) Fair
