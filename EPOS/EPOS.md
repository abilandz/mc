# Local EPOS productions

**Last update**: 20230223

### Table of Contents

* [EPOS_20230201 (pp at 13 TeV, min bias, EPOS 4)](#20230201)
* [EPOS_20221228 (pp at 13 TeV, min bias, EPOS 3.117)](#20221228)
* [EPOS_20221117 (pp at 13 TeV, high mult, EPOS 4)](#20221117)
* [EPOS_20220901 (Xe-Xe at 5.44 TeV, min bias, EPOS 3.117)](#20220901)
* [EPOS_20220510 (pp at 13 TeV, high mult, EPOS 3.117)](#20220510)
* [EPOS_20220121-3 (pp at 62.4 GeV, min bias, EPOS 3.117)](#20220121.3)
* [EPOS_20220121-2 (pp at 6.7 GeV, min bias, EPOS 3.117)](#20220121.2)
* [EPOS_20220121-1 (pp at 6.1 GeV, min bias, EPOS 3.117)](#20220121.1)
* [EPOS_20210611-1 (pp at 13 TeV, high mult, EPOS 3.117)](#20210611.1)
* [EPOS_20210125-2 (Au-Au at 200 GeV, min bias, EPOS 3.117)](#20210125.2)
* [EPOS_20210125-1 (O-O at 6.35 TeV, min bias, hydro+cascade, EPOS 3.117)](#20210125.1)
* [EPOS_20210118-1 (O-O at 6.35 TeV, min bias, only hydro, EPOS 3.117)](#20210118.1)
* [EPOS_20210106-1 (O-O at 7 TeV, min bias, EPOS 3.117)](#20210106.1)
* [EPOS_20201113-1 (pp at 17.3 GeV, min bias, EPOS 3.117)](#20201113.1)
* [EPOS_20201030 (Au-Au at 200 GeV, min bias, EPOS 3.117)](#20201030)


### EPOS_20230201 <a name="20230201"></a>
Remarks: This was the large-scale production, obtained using 6 different batch farms. Output of each batch farm is stored in a separate output directory, and then intentionally across different 'scratch' disks. 

Executive summary:
- pp at 13 TeV
- EPOS 4
- hydro (NO cascade)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- no decays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C1) ('bim' variable = impact parameter)
- total statistics: 206.6 M events (100 K events per ROOT file after final merging)
the output files for this production are in: 
  - /scratch7/abilandz/sim/EPOS_20230201-1 => 167.5 M (GSI, cluster "Virgo", partition "main")
  - /scratch5/abilandz/sim/EPOS_20230201-2 => 26.7 M (local, cluster "ktacluster", partition "kta")
  -  /scratch8/abilandz/sim/EPOS_20230201-3 => 4.6 M (LRZ, cluster "serial", partition "serial_std")
  -  /scratch8/abilandz/sim/EPOS_20230201-4 => 5.1 M (LRZ, cluster "cm2_tiny", partition "cm2_tiny")
  -  /scratch8/abilandz/sim/EPOS_20230201-5 => 0.7 M (LRZ, cluster "cm2", partition "cm2_std")
  -  /scratch8/abilandz/sim/EPOS_20230201-6 => 1.9 M (LRZ, cluster "mpp3", partition "mpp3_batch")
  -  /scratch8/abilandz/sim/EPOS_20230201-7 => 0.1 M (LRZ, cluster "cm2", partition "cm2_large")
- the common name of ROOT file: merged_z-EPOS_20230201.root

EPOS 4 config file:
* GSI, cluster "Virgo", partition "main": nfull 100, nfreeze 10
* local, cluster "ktacluster", partition "kta":  nfull 10, nfreeze 10
* LRZ, cluster "serial", partition "serial_std":  nfull 100, nfreeze 10
* LRZ, cluster "cm2_tiny", partition "cm2_tiny":  nfull 100, nfreeze 10
* LRZ, cluster "cm2", partition "cm2_std":  nfull 100, nfreeze 10
* LRZ, cluster "mpp3", partition "mpp3_batch":  nfull 10, nfreeze 10
* LRZ, cluster "cm2", partition "cm2_large":  nfull 100, nfreeze 10

```bash
!-------------------------------------------------------------
!      proton-proton with hydro and hadronic cascade
!-------------------------------------------------------------

application hadron !hadron-hadron, hadron-nucleus, or nucleus-nucleus 
set laproj 1       !projectile atomic number
set maproj 1       !projectile mass number
set latarg 1       !target atomic number
set matarg 1       !target mass number
set ecms 13000     !sqrt(s)_pp

set bminim 0 set bmaxim 1.4
set istmax 25 set phimin 0 set phimax 0
set iranphi 0 
ftime on 

!suppressed decays: 
nodecays 
 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331
end

set ninicon 1            !number of initial conditions used for hydro evolution
core full                !core/corona activated
hydro hlle               !hydro activated (hlle)
eos x3ff                 !eos activated (standard epos eos x3ff)
!hacas full              !hadronic cascade activated   
set nfull 100            !number of events
set nfreeze 10           !number of freeze out events per hydro event 
set modsho 1             !certain printout every modsho events
set centrality 0         ! 0=min bias 

!print * 2                  !printout of event to ...check file

fillTree4(C1) !root output

!-----put here online analysis part----
```

---


### EPOS_20221228 <a name="20221228"></a>

Executive summary:
- pp at 13 TeV
- EPOS 3.117
- hydro (NO cascade)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C1) ('bim' variable = impact parameter)
- total statistics: ~150 M events (~1 M events per final merged ROOT file)
- output files for this production are in: /scratch7/abilandz/sim/EPOS_20221228 
- common name of ROOT file: merged_merged_z-EPOS_20221228.root



EPOS 3.117 config file:

```bash
application hadron
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 13000
set bminim 0 set bmaxim 1.4
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
!core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 30000 set nfreeze 1  set modsho 1000 set centrality 0                   !no hydro no casc

fillTree(C1)

echo off
```



---



### EPOS_20221117 <a name="20221117"></a>

Remarks: This was the first EPOS 4 production, used for benchmarking of large-scale production EPOS_20220510 (obtained with EPOS 3.117).

Executive summary:
- pp at 13 TeV
- EPOS 4
- hydro (NO cascade)
- high multiplicity sample, impact parameter is set to 0: set bminim 0 set bmaxim 0
- no decays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: ~ 11.5 M events (100 x 10 per job, 100 K events per final merged ROOT file)
- output files for this production are in: /scratch7/abilandz/sim/EPOS_20221117
- common name of ROOT file: merged_z-EPOS_20221117.root


EPOS 4 config file:

```bash
!-------------------------------------------------------------
!      proton-proton with hydro and hadronic cascade
!-------------------------------------------------------------

application hadron !hadron-hadron, hadron-nucleus, or nucleus-nucleus 
set laproj 1       !projectile atomic number
set maproj 1       !projectile mass number
set latarg 1       !target atomic number
set matarg 1       !target mass number
set ecms 13000     !sqrt(s)_pp

set bminim 0 set bmaxim 0
set istmax 25 set phimin 0 set phimax 0
set iranphi 0 
ftime on 

!suppressed decays: 
nodecays 
 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331
end

set ninicon 1            !number of initial conditions used for hydro evolution
core full                !core/corona activated
hydro hlle               !hydro activated (hlle)
eos x3ff                 !eos activated (standard epos eos x3ff)
!hacas full              !hadronic cascade activated   
set nfull 100            !number of events
set nfreeze 10           !number of freeze out events per hydro event 
set modsho 1             !certain printout every modsho events
set centrality 0         ! 0=min bias 

!print * 2                  !printout of event to ...check file

fillTree4(C2) !root output

!-----put here online analysis part----

```



---



### EPOS_20220901 <a name="20220901"></a>

Executive summary:
- XeXe at 5.44 TeV
- EPOS 3.117
- hydro + cascade
- min bias sample, no cut on impact parameter
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C1) ('bim' variable = impact parameter)
- total statistics: ~3 M events (~10 K events per final merged ROOT file)
- output files for this production are in: /scratch7/abilandz/sim/EPOS_20220901-1 
- common name of ROOT file: merged_z-EPOS_20220901-1.root



EPOS 3.117 config file:

```bash
application hadron
set laproj 54 set maproj 129 set latarg 54 set matarg 129  set ecms 5440
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 1    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 30000 set nfreeze 1  set modsho 1000 set centrality 0                   !no hydro no casc

fillTree(C1)

echo off
```



---



### EPOS_20220510 <a name="20220510"></a>
Remarks: This was the large-scale production, obtained using 6 different batch farms. Output of each batch farm is stored in a separate output directory, and then intentionally across different 'scratch' disks. 

Executive summary:
- pp at 13 TeV
- EPOS 3.117
- hydro (NO cascade)
- high multiplicity sample, impact parameter is set via: set bminim 0 set bmaxim 0
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: ~300 M events (~1 M events per final merged ROOT file)
- output files for this production are in:
  - /scratch7/abilandz/sim/EPOS_20220510-1 => 169.0 M events
  - /scratch5/abilandz/sim/EPOS_20220510-2 => 43.4 M events 
  - /scratch8/abilandz/sim/EPOS_20220510-3 => 13.8 M events
  - /scratch8/abilandz/sim/EPOS_20220510-4 => 29.5 M events
  - /scratch8/abilandz/sim/EPOS_20220510-5 => 10.1 M events
  - /scratch8/abilandz/sim/EPOS_20220510-6 => 49.8 M events
- common name of ROOT file: merged_merged_z-EPOS_20220510.root

EPOS 3.117 config file:

```bash
application hadron
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 13000
set bminim 0 set bmaxim 0
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
!core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 30000 set nfreeze 1  set modsho 1000 set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20220121-3 <a name="20220121.3"></a>
Executive summary:
- pp at 62.4 GeV
- EPOS 3.117
- hydro + cascade
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: ~4 M events (100 events per final ROOT file)
- output files for this production are in:  /scratch6/abilandz/sim/arxiv/EPOS_20220121-3
- common name of ROOT file: z-EPOS_20220121-3.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 62.4
set bminim 0 set bmaxim 1.4
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 30000 set nfreeze 1  set modsho 1000 set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20220121-2 <a name="20220121.2"></a>
Executive summary:
- pp at 6.7 GeV
- EPOS 3.117
- hydro (NO cascade)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: ~10 M events (100 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/arxiv/EPOS_20220121-2  
- common name of ROOT file: z-EPOS_20220121-2.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 6.7
set bminim 0 set bmaxim 1.4
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

 core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
!core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 30000 set nfreeze 1  set modsho 1000 set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```

---



### EPOS_20220121-1 <a name="20220121.1"></a>
Executive summary:
- pp at 6.1 GeV
- EPOS 3.117
- hydro (NO cascade)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: ~10 M events (100 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/arxiv/EPOS_20220121-1 
- common name of ROOT file: z-EPOS_20220121-1.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 6.1
set bminim 0 set bmaxim 1.4
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

 core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
!core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 30000 set nfreeze 1  set modsho 1000 set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```

---



### EPOS_20210611-1 <a name="20210611.1"></a>
Executive summary:
- pp at 13 TeV
- EPOS 3.117
- hydro (NO cascade)
- high multiplicity sample sample, impact parameter is set via: set bminim 0 set bmaxim 0
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: ~97.91 M events (100 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/arxiv/EPOS_20220121-1 
- common name of ROOT file: z-EPOS_20210611-1.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 13000
set bminim 0 set bmaxim 0
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

 core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
!core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 30000 set nfreeze 1  set modsho 1000 set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```

---



### EPOS_20210125-2 <a name="20210125.2"></a>
Executive summary:
- Au-Au at 200 GeV
- EPOS 3.117
- hydro (NO cascade)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 20
- nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C1) ('bim' variable = impact parameter)
- total statistics: ~0.5 M events (10 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/arxiv/EPOS_20210125-2
- common name of ROOT file: z-EPOS_20210125-2.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 79 set maproj 197 set latarg 79 set matarg 197  set ecms 200
set bminim 0 set bmaxim 20
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
        
! uncomment one of the following lines

core full hydro x3ff   hacas off  set nfull 1    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
!core full hydro x3ff   hacas full set nfull 1    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 30000 set nfreeze 1  set modsho 1000 set centrality 0                   !no hydro no casc

fillTree(C1)

echo off
```

---



### EPOS_20210125-1 <a name="20210125.1"></a>
Executive summary:
- O-O at 6.35 TeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 5.2
- nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: ~1 M events (10 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/arxiv/EPOS_20210125-1
- common name of ROOT file: z-EPOS_20210125-1.root

EPOS 3.117 config file:

```bash
pplication hadron  
set laproj 8 set maproj 16 set latarg 8 set matarg 16  set ecms 6350
set bminim 0 set bmaxim 5.2
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
        
! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 1    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 1    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 30000 set nfreeze 1  set modsho 1000 set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```

---



### EPOS_20210118-1 <a name="20210118.1"></a>
Executive summary:
- O-O at 6.35 TeV
- EPOS 3.117
- hydro (NO cascade)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 5.2
- nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: ~1 M events (10 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/arxiv/EPOS_20210118-1
- common name of ROOT file: z-EPOS_20210118-1.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 8 set maproj 16 set latarg 8 set matarg 16  set ecms 6350
set bminim 0 set bmaxim 5.2
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
        
! uncomment one of the following lines

core full hydro x3ff   hacas off  set nfull 1    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
!core full hydro x3ff   hacas full set nfull 1    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 30000 set nfreeze 1  set modsho 1000 set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```

---



### EPOS_20210106-1 <a name="20210106.1"></a>
Executive summary:
- O-O at 7 TeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 5.2
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: ~1 M events (10 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/arxiv/EPOS_20210106-1
- common name of ROOT file: z-EPOS_20210106-1.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 8 set maproj 16 set latarg 8 set matarg 16  set ecms 7000
set bminim 0 set bmaxim 5.2
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 1    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 30000 set nfreeze 1  set modsho 1000 set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20201113-1 <a name="20201113.1"></a>
Executive summary:
- pp at 17.3 GeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays  110 20 2130 -2130 2230 -2230 1130 -1130 1220 -1220 1330 -1330 2330 -2330 3331 -3331
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: ~2 M events (100 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/arxiv/EPOS_20201113-1
- common name of ROOT file: z-EPOS_20201113-1.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 17.3
set bminim 0 set bmaxim 1.4
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays  110 20 2130 -2130 2230 -2230 1130 -1130 1220 -1220 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20201030 <a name="20201030"></a>
Executive summary:
- Au-Au at 200 GeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is not set in the config file to any specific range
- nodecays 110 20 2130 2230 -2230 1130 -1130 1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: ~0.5 M events (1000 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/arxiv/EPOS_20201030
- common name of ROOT file: merged_z-EPOS_20201030.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 79 set maproj 197 set latarg 79 set matarg 197  set ecms 200
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 2230 -2230 1130 -1130 1230 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 5    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 5    set nfreeze 5 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 5    set nfreeze 10 set modsho 100   set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```
