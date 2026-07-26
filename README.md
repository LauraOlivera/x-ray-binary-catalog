# x-ray-binary-catalog
This repository contains a machine-readable version of the table described in [https://arxiv.org/abs/2607.06360](https://arxiv.org/abs/2607.06360).

It consists of black-hole candidate X-ray binary catalog constructed by combining and expanding existing catalogues.

In particular, it merges information from the WATCHDOG catalogue (Tetarenko et al 2016), the BlackCat catalogue (Corral-Santana et al 2016) and the XRBCat catalogues (Neumann et al 2023, Avakyan et al 2023).

## How to use
The easiest way to read the file while conveniently retaining all the metadata is as an `astropy.table.Table` as

```python
from astropy.table import table
table = Table.read("BHXRB_candidate_table_OliveraNieto2026.ecsv")
```

 The definition of each column is in the metadata of the file and also shown in the file `table_info.md` for convenience

 ## How to reference
 If you use this table, please reference the paper (currently under review in A&A)
 ```
@ARTICLE{2026arXiv260706360O,
       author = {{Olivera-Nieto}, Laura and {Cowie}, Fraser J. and {Markoff}, Sera and {Fender}, Rob and {Crook-Mansour}, Justine},
        title = "{Extreme particle acceleration in X-ray binaries is linked to their jets}",
      journal = {arXiv e-prints},
     keywords = {High Energy Astrophysical Phenomena},
         year = 2026,
        month = jul,
          eid = {arXiv:2607.06360},
        pages = {arXiv:2607.06360},
          doi = {10.48550/arXiv.2607.06360},
archivePrefix = {arXiv},
       eprint = {2607.06360},
 primaryClass = {astro-ph.HE},
       adsurl = {https://ui.adsabs.harvard.edu/abs/2026arXiv260706360O},
      adsnote = {Provided by the SAO/NASA Astrophysics Data System}
}


 ```

 but also the original catalogues,

 WATCHDOG

 ```
@ARTICLE{2016ApJS..222...15T,
       author = {{Tetarenko}, B.~E. and {Sivakoff}, G.~R. and {Heinke}, C.~O. and {Gladstone}, J.~C.},
        title = "{WATCHDOG: A Comprehensive All-sky Database of Galactic Black Hole X-ray Binaries}",
      journal = {\apjs},
     keywords = {accretion, accretion disks, black hole physics, catalogs, stars: black holes, X-rays: binaries, Astrophysics - High Energy Astrophysical Phenomena},
         year = 2016,
        month = feb,
       volume = {222},
       number = {2},
          eid = {15},
        pages = {15},
          doi = {10.3847/0067-0049/222/2/15},
archivePrefix = {arXiv},
       eprint = {1512.00778},
 primaryClass = {astro-ph.HE},
       adsurl = {https://ui.adsabs.harvard.edu/abs/2016ApJS..222...15T},
      adsnote = {Provided by the SAO/NASA Astrophysics Data System}
}
```

BlackCAT ([website](https://www.astro.puc.cl/BlackCAT/citation.php))
```
@ARTICLE{2016A&A...587A..61C,
       author = {{Corral-Santana}, J.~M. and {Casares}, J. and {Mu{\~n}oz-Darias}, T. and {Bauer}, F.~E. and {Mart{\'\i}nez-Pais}, I.~G. and {Russell}, D.~M.},
        title = "{BlackCAT: A catalogue of stellar-mass black holes in X-ray transients}",
      journal = {\aap},
     keywords = {X-rays: binaries, stars: black holes, catalogs, Astrophysics - High Energy Astrophysical Phenomena, Astrophysics - Solar and Stellar Astrophysics},
         year = 2016,
        month = mar,
       volume = {587},
          eid = {A61},
        pages = {A61},
          doi = {10.1051/0004-6361/201527130},
archivePrefix = {arXiv},
       eprint = {1510.08869},
 primaryClass = {astro-ph.HE},
       adsurl = {https://ui.adsabs.harvard.edu/abs/2016A&A...587A..61C},
      adsnote = {Provided by the SAO/NASA Astrophysics Data System}
}
 ```

 and XRBCat ([website](http://astro.uni-tuebingen.de/~xrbcat/index.html))
 ```
@ARTICLE{2023A&A...675A.199A,
       author = {{Avakyan}, A. and {Neumann}, M. and {Zainab}, A. and {Doroshenko}, V. and {Wilms}, J. and {Santangelo}, A.},
        title = "{XRBcats: Galactic low-mass X-ray binary catalogue}",
      journal = {\aap},
     keywords = {catalogs, binaries: close, stars: late-type, X-rays: binaries, Astrophysics - High Energy Astrophysical Phenomena},
         year = 2023,
        month = jul,
       volume = {675},
          eid = {A199},
        pages = {A199},
          doi = {10.1051/0004-6361/202346522},
archivePrefix = {arXiv},
       eprint = {2303.16168},
 primaryClass = {astro-ph.HE},
       adsurl = {https://ui.adsabs.harvard.edu/abs/2023A&A...675A.199A},
      adsnote = {Provided by the SAO/NASA Astrophysics Data System}
}
```
```
@ARTICLE{2023A&A...677A.134N,
       author = {{Neumann}, M. and {Avakyan}, A. and {Doroshenko}, V. and {Santangelo}, A.},
        title = "{XRBcats: Galactic High Mass X-ray Binary Catalogue★}",
      journal = {\aap},
     keywords = {catalogs, binaries: close, stars: early-type, X-rays: binaries, Astrophysics - High Energy Astrophysical Phenomena},
         year = 2023,
        month = sep,
       volume = {677},
          eid = {A134},
        pages = {A134},
          doi = {10.1051/0004-6361/202245728},
archivePrefix = {arXiv},
       eprint = {2303.16137},
 primaryClass = {astro-ph.HE},
       adsurl = {https://ui.adsabs.harvard.edu/abs/2023A&A...677A.134N},
      adsnote = {Provided by the SAO/NASA Astrophysics Data System}
}
 ```

The table has columns (`WD`, `BK`, `XR`) which indicate which catalogues each source was included in - so you can cite what is most appropiate for your case.