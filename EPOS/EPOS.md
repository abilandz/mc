# Local EPOS productions

**Last update**: 20230203

[GitBook](https://abilandz.gitbook.io/monte-carlo-productions/epos/epos) 

### Table of Contents

* [EPOS_20230201 (pp at 13 TeV, min bias, EPOS 4)](#EPOS-20230201)
* [EPOS_20221228 (pp at 13 TeV, min bias, EPOS 3.117)](#EPOS-20221228)
* [EPOS_20221117 (pp at 13 TeV, high mult, EPOS 4)](#EPOS-20221117)
* [EPOS_20220901 (XeXe at 5.44 TeV, min bias, EPOS 3.117)](#EPOS-20220901)
* [EPOS_20220510 (pp at 13 TeV, high mult, EPOS 3.117)](#EPOS-20220510)
* [Catching user input: **read**](#read)


### EPOS_20230201 <a name="EPOS-20230201"></a>
Remarks: This was the large-scale production, obtained using 6 different batch farms. Output of each batch farm is stored in a separate output directory, and then intentionally across different 'scratch' disks. 

Executive summary:
- pp at 13 TeV
- EPOS 4
- hydro (NO cascade)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- no decays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C1) ('bim' variable = impact parameter)
- total statistics: 6.2 M events (100K events per ROOT file after final merging)
the output files for this production are in: 
  - /scratch7/abilandz/sim/EPOS_20230201-1 => 6.2 M (GSI, cluster "Virgo", partition "main")
  - /scratch5/abilandz/sim/EPOS_20230201-2 => TBI (local batch farm, cluster "ktacluster", partition "kta")
  -  /scratch8/abilandz/sim/EPOS_20230201-3 => TBI (LRZ, cluster "serial", partition "serial_std")
  -  /scratch8/abilandz/sim/EPOS_20230201-4 => TBI (LRZ, cluster "cm2_tiny", partition "cm2_tiny")
  -  /scratch8/abilandz/sim/EPOS_20230201-5 => TBI (LRZ, cluster "cm2", partition "cm2_std")
  -  /scratch8/abilandz/sim/EPOS_20230201-6 => TBI (LRZ, cluster "mpp3", partition "mpp3_batch")
- the common name of ROOT file: merged_z-EPOS_20230201.root

EPOS 4 config file:
* Virgo: nfull 100, nfreeze 10
* local batch farm:  nfull 10, nfreeze 10

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


### test_44 <a name="read"></a>



### EPOS_20221228 <a name="EPOS-20221228"></a>

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



### EPOS_20221117 <a name="EPOS-20221117"></a>

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



### EPOS_20220901 <a name="EPOS-20220901"></a>

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



### EPOS_20220510 <a name="EPOS-20220510"></a>
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
