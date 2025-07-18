# Local EPOS productions

**Last update**: 20250714

### Table of Contents

* [EPOS_20250416 (PbPb at 5.36 TeV, min bias, EPOS 4.0.3)](#20250416) &mdash; **RUNNING** 
* [EPOS_20250320 (pp at 433 TeV, min bias, EPOS 3.117)](#20250320) 
* [EPOS_20230810 (pp at 13 TeV, high mult, EPOS 4.0.0)](#20230810)
* [EPOS_20230714 (pp at 53 GeV, min bias, EPOS 4.0.0)](#20230714) 
* [EPOS_20230418 (pp at 13 TeV, high mult, EPOS 3.117)](#20230418)
* [EPOS_20230330 (Au-Au at 62.4 GeV, min bias, EPOS 3.117)](#20230330)
* [EPOS_20230201 (pp at 13 TeV, min bias, large-scale, EPOS 4.0.0)](#20230201)
* [EPOS_20221228 (pp at 13 TeV, min bias, EPOS 3.117)](#20221228) 
* [EPOS_20221117 (pp at 13 TeV, high mult, EPOS 4.0.0)](#20221117)
* [EPOS_20220901 (Xe-Xe at 5.44 TeV, min bias, EPOS 3.117)](#20220901)
* [EPOS_20220510 (pp at 13 TeV, high mult, large-scale, EPOS 3.117)](#20220510)
* [EPOS_20220121-3 (pp at 62.4 GeV, min bias, EPOS 3.117)](#20220121.3)
* [EPOS_20220121-2 (pp at 6.7 GeV, min bias, EPOS 3.117)](#20220121.2)
* [EPOS_20220121-1 (pp at 6.1 GeV, min bias, EPOS 3.117)](#20220121.1)
* [EPOS_20210611-1 (pp at 13 TeV, high mult, large-scale, EPOS 3.117)](#20210611.1)
* [EPOS_20210125-2 (Au-Au at 200 GeV, min bias, EPOS 3.117)](#20210125.2)
* [EPOS_20210125-1 (O-O at 6.35 TeV, min bias, hydro+cascade, EPOS 3.117)](#20210125.1)
* [EPOS_20210118-1 (O-O at 6.35 TeV, min bias, only hydro, EPOS 3.117)](#20210118.1)
* [EPOS_20210106-1 (O-O at 7 TeV, min bias, EPOS 3.117)](#20210106.1)
* [EPOS_20201113-1 (pp at 17.3 GeV, min bias, EPOS 3.117)](#20201113.1)
* [EPOS_20201030 (Au-Au at 200 GeV, min bias, EPOS 3.117)](#20201030)
* [EPOS_20201028 (pp at 200 GeV, min bias, EPOS 3.117)](#20201028)
* [EPOS_20201027 (Au-Au at 39 GeV, min bias, EPOS 3.117)](#20201027)
* [EPOS_20201014-2 (pp at 13 TeV, min bias, EPOS 3.117)](#20201014.2) 
* [EPOS_20201014-1 (pp at 7 TeV, min bias, EPOS 3.117)](#20201014.1) 
* [EPOS_20201007 (Au-Au at 200 GeV, min bias, different nodecays, EPOS 3.117)](#20201007)
* [EPOS_20201006-2 (pp at 200 GeV, min bias, EPOS 3.117)](#20201006.2)
* [EPOS_20201006-1 (pp at 17.3 GeV, min bias, EPOS 3.117)](#20201006.1)
* [EPOS_20201001-6 (Au-Au at 200 GeV, min bias, EPOS 3.117)](#20201001.6)
* [EPOS_20201001-2 (pp at 17.3 GeV, min bias, EPOS 3.117)](#20201001.2)
* [EPOS_20201001-1 (pp at 200 GeV, min bias, EPOS 3.117)](#20201001.1)
* [EPOS_20200608 (pp at 17.3 GeV, min bias, EPOS 3.117)](#20200608)
* [EPOS_20200602 (pp at 200 GeV, min bias, EPOS 3.117)](#20200602)
* [EPOS_20200316 (p-C at 17.2 GeV, min bias, EPOS 3.117)](#20200316)
* [EPOS_20200207-3 (pp at 12.3 GeV, min bias, EPOS 3.117)](#20200207.3)
* [EPOS_20200207-2 (pp at 8.8 GeV, min bias, EPOS 3.117)](#20200207.2)
* [EPOS_20200207-1 (pp at 7.7 GeV, min bias, EPOS 3.117)](#20200207.1) 
* [EPOS_20200121 (pp at 13 TeV, min bias, EPOS 3.117)](#20200121)
* [EPOS_20190114 (pp at 13 TeV, min bias, ALICE acceptance, EPOS 3.117)](#20190114)
* [EPOS_20181220 (pp at 13 TeV, min bias, ALICE acceptance, EPOS 3.117)](#20181220)
* [EPOS_20180703 (p-Pb at 5.02 TeV, min bias, EPOS 3.117)](#20180703)
* [EPOS_20170901 (Pb-Pb at 5.02 TeV, min bias, ALICE acceptance, EPOS 3.117)](#20170901)
* [EPOS_20170210 (p-Pb at 5.02 TeV, min bias, ALICE acceptance, EPOS 3.117)](#20170210)
* [EPOS_20160901 (pp at 7 TeV, min bias, ALICE acceptance, EPOS 3.117)](#20160901)




### EPOS_20250416 <a name="20250416"></a>
Remarks: This was the first production using EPOS 4.0.3. It was obtained using 2 different batch farms. Output of each batch farm is stored in a separate output directory, and then intentionally across different 'scratch' disks. To get one common list of ROOT files for all batch farms, simply use:

```bash
find /scratch?/abilandz/sim/EPOS_20250416-? -maxdepth 2 -type f -name "*.root" | tee list.txt
```

Executive summary:

- PbPb at 5.36 TeV
- EPOS 4.0.3
- hydro + cascade (UrQMD turned on)
- min bias sample (set centrality 0)
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331 end
- ALICE acceptance is NOT hardwired
- fillTree4(C1) ('bim' variable = impact parameter)
- current statistics: 4197000 (4.20 M) events (1000 events per final merged ROOT file)
- the output files for this production are in:
	- /scratch4/abilandz/sim/EPOS_20250416-1 => 2.20 M events (local, cluster "ktacluster", partition "kta") &mdash; **RUNNING**
	- /scratch6/abilandz/sim/EPOS_20250416-2 => 2.00 M events (GSI, cluster "Virgo", partition "main") &mdash; **RUNNING** 
- common name of ROOT file: merged_z-EPOS_20250416.root 



EPOS 4.0.3 config file:

```bash
!-------------------------------------------------------------
!       PbPb collisions with hydro and hadronic cascade
!-------------------------------------------------------------
application hadron !hadron-hadron, hadron-nucleus, or nucleus-nucleus collision
set laproj 82  !projectile atomic number
set maproj 208 !projectile mass number
set latarg 82  !target atomic number
set matarg 208 !target mass number
set ecms 5360  !sqrt(s)_pp

set istmax 25
set iranphi 1
ftime on

!suppressed decays:
nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331 end

core full                !core/corona activated
hydro hlle               !hydro activated
eos x3ff                 !eos activated
hacas full               !hadronic cascade activated, set to 'off' to de-activate, or 'full' to activate

set ninicon 1            !number of initial conditions used for hydro evolution
set nfull 4              !number of events
set nfreeze 1            !number of freeze out events per hydro event
set modsho 100           !certain printout every modsho events
set centrality 0         ! 0=min bias

fillTree4(C1)            ! writes results into a ROOT file, where C1 refers to the impact parameter as centrality variable, or C2 for number of pomerons

!---put here online analysis part----
```



---




### EPOS_20250320 <a name="20250320"></a>

Executive summary:

- pp at 433 TeV
- EPOS 3.117
- hydro (NO cascade)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C1) ('bim' variable = impact parameter)
- current statistics: 100000 (100 K) events (100 K events per final merged ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20250320-1
- common name of ROOT file: merged_z-EPOS_20250320.root 



EPOS 3.117 config file:

```bash
application hadron
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 433000
set bminim 0 set bmaxim 1.4
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10  set modsho 100   set centrality 0  set ijetfluid 1  !hydro
!core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 30000 set nfreeze 1  set modsho 1000 set centrality 0                   !no hydro no casc

fillTree(C1)

echo off
```



---




### EPOS_20230810 <a name="20230810"></a>
Remarks: This was the large-scale production, obtained using 2 different batch farms. Output of each batch farm is stored in a separate output directory, and then intentionally across different 'scratch' disks. To get one common list of ROOT files for all batch farms, simply use:

```bash
find /scratch?/abilandz/sim/EPOS_20230810-? -type f -name "*.root" | tee list.txt
```

Executive summary:
- pp at 13 TeV
- EPOS 4.0.0 (+ patches from Klaus, for a very simple broadening formula)
- hydro + cascade (UrQMD turned on)
- high multiplicity sample, impact parameter is set to 0: set bminim 0 set bmaxim 0
- nodecays 110 20 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331 end
- ALICE acceptance is NOT hardwired
- fillTree(C1) ('bim' variable = impact parameter)
- set ibreit 1 !(or 2 to get printout)
- total statistics: 84.7 M events (100 K events per ROOT file after final merging) 
- the output files for this production are in:
	- /scratch4/abilandz/sim/EPOS_20230810-1 => 74.5 M (GSI, cluster "Virgo", partition "main") 
	- /scratch6/abilandz/sim/EPOS_20230810-2 => 10.2 M events (local, cluster "ktacluster", partition "kta") 
- the common name of ROOT file: merged_z-EPOS_20230810.root

EPOS 4.0.0 config file:

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
 110 20 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331
end

set ninicon 1            !number of initial conditions used for hydro evolution
core full                !core/corona activated
hydro hlle               !hydro activated (hlle)
eos x3ff                 !eos activated (standard epos eos x3ff)
hacas full               !hadronic cascade activated
set nfull 20             !number of events
set nfreeze 10           !number of freeze out events per hydro event
set modsho 1             !certain printout every modsho events
set centrality 0         ! 0=min bias
set ibreit 1             !(or 2 to get printout)

!print * 2                  !printout of event to ...check file

fillTree4(C1) !root output

!-----put here online analysis part----
```



---




### EPOS_20230714 <a name="20230714"></a>

Executive summary:
- pp at 53 GeV
- EPOS 4.0.0 (+ patches from Klaus for pp at 53 GeV)
- hydro (NO cascade)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- no decays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C1) ('bim' variable = impact parameter)
- total statistics: ~ 11.6 M events (100 K events per ROOT file after final merging) 
- the output files for this production are in: /scratch6/abilandz/sim/EPOS_20230714
- the common name of ROOT file: merged_z-EPOS_20230714.root

EPOS 4.0.0 config file:

```bash
!-------------------------------------------------------------
!      proton-proton with hydro and hadronic cascade
!-------------------------------------------------------------

application hadron !hadron-hadron, hadron-nucleus, or nucleus-nucleus 
set laproj 1       !projectile atomic number
set maproj 1       !projectile mass number
set latarg 1       !target atomic number
set matarg 1       !target mass number
set ecms 53        !sqrt(s)_pp

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
set nfull 10             !number of events
set nfreeze 10           !number of freeze out events per hydro event 
set modsho 1             !certain printout every modsho events
set centrality 0         ! 0=min bias 

!print * 2                  !printout of event to ...check file

fillTree4(C1) !root output

!-----put here online analysis part----
```

---




### EPOS_20230418 <a name="20230418"></a>
Remarks: Same as **EPOS_20201014-2**, just high multiplicity sample, and fillTree(C1) is set.

Executive summary:

- pp at 13 TeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- high multiplicity sample, impact parameter is set to 0: set bminim 0 set bmaxim 0
- nodecays 110 20 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331 end
- ALICE acceptance is NOT hardwired
- fillTree(C1) ('bim' variable = impact parameter)
- total statistics: 40.60 M events (100 K events per final ROOT file)
- output files for this production are in: /scratch7/abilandz/sim/EPOS_20230418
- common name of ROOT file: merged_z-EPOS_20230418.root



EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 13000
set bminim 0 set bmaxim 0
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays  110 20 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 20    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0                   !no hydro no casc

fillTree(C1)

echo off

```



---




### EPOS_20230330 <a name="20230330"></a>
Remarks: Same as **EPOS_20201007**, just the collision energy is 62.4 GeV, and fillTree(C1) is set.

Executive summary:

- Au-Au at 62.4 GeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 20
- nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C1) ('bim' variable = impact parameter)
- total statistics: 3.311 M events (1000 events per final ROOT file)
- output files for this production are in: /scratch5/abilandz/sim/EPOS_20230330
- common name of ROOT file: merged_z-EPOS_20230330.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 79 set maproj 197 set latarg 79 set matarg 197  set ecms 62.4
set bminim 0 set bmaxim 20
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 5    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 5    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 5    set nfreeze 10 set modsho 100   set centrality 0                   !no hydro no casc

fillTree(C1)

echo off
```

---



### EPOS_20230201 <a name="20230201"></a>
Remarks: This was the large-scale production, obtained using 7 different batch farms. Output of each batch farm is stored in a separate output directory, and then intentionally across different 'scratch' disks. To get one common list of ROOT files for all batch farms, simply use:

```bash
find /scratch?/abilandz/sim/EPOS_20230201-? -type f -name "*.root" | tee list.txt
```

Executive summary:
- pp at 13 TeV
- EPOS 4.0.0
- hydro (NO cascade)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- no decays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C1) ('bim' variable = impact parameter)
- total statistics: 304.5 M events (100 K events per ROOT file after final merging)
  the output files for this production are in: 
  - /scratch7/abilandz/sim/EPOS_20230201-1 => 246.1 M (GSI, cluster "Virgo", partition "main")
  - /scratch5/abilandz/sim/EPOS_20230201-2 => 34.6 M (local, cluster "ktacluster", partition "kta")
  -  /scratch8/abilandz/sim/EPOS_20230201-3 => 8.8 M (LRZ, cluster "serial", partition "serial_std")
  -  /scratch8/abilandz/sim/EPOS_20230201-4 => 9.3 M (LRZ, cluster "cm2_tiny", partition "cm2_tiny")
  -  /scratch8/abilandz/sim/EPOS_20230201-5 => 1.3 M (LRZ, cluster "cm2", partition "cm2_std")
  -  /scratch8/abilandz/sim/EPOS_20230201-6 => 4.1 M (LRZ, cluster "mpp3", partition "mpp3_batch")
  -  /scratch8/abilandz/sim/EPOS_20230201-7 => 0.3 M (LRZ, cluster "cm2", partition "cm2_large")
- the common name of ROOT file: merged_z-EPOS_20230201.root

EPOS 4.0.0 config file:
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

Remarks: This production was restarted on March 27th, to increase the initial statistics of ~150 M events to reach new target statistics of ~500 M. Subdirectories >= 985 contain results after major Virgo upgrade which finished on May 11th. 

Executive summary:

- pp at 13 TeV
- EPOS 3.117
- hydro (NO cascade)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C1) ('bim' variable = impact parameter)
- current statistics: 487964000 (~487.96 M) events (~1 M or ~100 K events per final merged ROOT file, see below)
- output files for this production are in: /scratch7/abilandz/sim/EPOS_20221228 
  - subdirectories 0-154 have ~1 M events per final merged ROOT file (original production)
  - subdirectories 155-3540 have ~100 K events per final merged ROOT file (additional production)
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

Remarks: This was the first EPOS 4.0.0 production, used for benchmarking of large-scale production EPOS_20220510 (obtained with EPOS 3.117).

Executive summary:
- pp at 13 TeV
- EPOS 4.0.0
- hydro (NO cascade)
- high multiplicity sample, impact parameter is set to 0: set bminim 0 set bmaxim 0
- no decays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: ~ 42 M events (100 x 10 per job, 100 K events per final merged ROOT file)
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
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
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
Remarks: This was the large-scale production, obtained using 7 different batch farms. Output of each batch farm is stored in a separate output directory, and then intentionally across different 'scratch' disks. Production EPOS_20220510-2 was done on a local batch farm before the major upgrade at the end of 2024, and EPOS_20220510-7 after the upgrade. To get one common list of ROOT files for productions from all batch farms, simply use:

```bash
find /scratch?/abilandz/sim/EPOS_20220510-? -type f -name "merged*.root" | tee list.txt
```

Executive summary:
- pp at 13 TeV
- EPOS 3.117
- hydro (NO cascade)
- high multiplicity sample, impact parameter is set via: set bminim 0 set bmaxim 0
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: ~400 M events (~1 M events per final merged ROOT file)
- output files for this production are in:
  - /scratch7/abilandz/sim/EPOS_20220510-1 => 169.0 M events
  - /scratch5/abilandz/sim/EPOS_20220510-2 => 43.4 M events 
  - /scratch8/abilandz/sim/EPOS_20220510-3 => 13.8 M events
  - /scratch8/abilandz/sim/EPOS_20220510-4 => 29.5 M events
  - /scratch8/abilandz/sim/EPOS_20220510-5 => 10.1 M events
  - /scratch8/abilandz/sim/EPOS_20220510-6 => 49.8 M events
  - /scratch3/abilandz/sim/EPOS_20220510-7 => 100.0 M events
- common name of ROOT file: merged_merged_z-EPOS_20220510-?.root, where ? stands for 1, 2, ..., 7 (to resemble the specific original batchfarm production above)

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
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 4.4 M events (10 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20220121-3
- common name of ROOT file: merged_z-EPOS_20220121-3.root

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
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 9.88 M events (10 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20220121-2  
- common name of ROOT file: merged_z-EPOS_20220121-2.root

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
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 9.1 M events (10 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20220121-1 
- common name of ROOT file: merged_z-EPOS_20220121-1.root

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
- high multiplicity sample sample, impact parameter is set via: set bminim 0 set bmaxim 0
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 97.8 M events (100 events per final ROOT file)
- output files for this production are in: /scratch5/abilandz/sim/EPOS_20210611-1
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
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 20
- nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C1) ('bim' variable = impact parameter)
- total statistics: 499 K events (1000 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20210125-2
- common name of ROOT file: merged_z-EPOS_20210125-2.root

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
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 5.2
- nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 998 K events (1000 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20210125-1
- common name of ROOT file: merged_z-EPOS_20210125-1.root

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
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 5.2
- nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 991 K events (1000 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20210118-1
- common name of ROOT file: merged_z-EPOS_20210118-1.root

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
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 5.2
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 779 K events (1000 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20210106-1
- common name of ROOT file: merged_z-EPOS_20210106-1.root

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
- nodecays  110 20 2130 -2130 2230 -2230 1130 -1130 1220 -1220 1330 -1330 2330 -2330 3331 -3331 end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 1.6 M events (100 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20201113-1
- common name of ROOT file: merged_z-EPOS_20201113-1.root

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
- min bias sample, impact parameter is not set in the config file to any specific range
- nodecays 110 20 2130 2230 -2230 1130 -1130 1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics:  ~ 0.5 M events (1000 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20201030
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



---



### EPOS_20201028 <a name="20201028.1"></a>
Executive summary:
- pp at 200 GeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, no cut on impact parameter
- nodecays  110 20 2130 2230 -2230 1130 -1130 1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 0.9 M events (100 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20201028
- common name of ROOT file: merged_z-EPOS_20201028.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 200
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays  110 20 2130 2230 -2230 1130 -1130 1230 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20201027 <a name="20201027.1"></a>
Executive summary:
- Au-Au at 39 GeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 20
- nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 482 K events (1000 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20201027
- common name of ROOT file: merged_z-EPOS_20201027.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 79 set maproj 197 set latarg 79 set matarg 197  set ecms 39
set bminim 0 set bmaxim 20
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 5    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 5    set nfreeze 5 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 5    set nfreeze 10 set modsho 100   set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20201014-2 <a name="20201014.2"></a>
Executive summary:

- pp at 13 TeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays  110 20 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 3.3 M events (100 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20201014-2 
- common name of ROOT file: merged_z-EPOS_20201014-2.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 13000
set bminim 0 set bmaxim 1.4
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays  110 20 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20201014-1 <a name="20201014.1"></a>
Executive summary:

- pp at 7 TeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays  110 20 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 3.5 M events (100 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20201014-1
- common name of ROOT file: merged_z-EPOS_20201014-1.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 7000
set bminim 0 set bmaxim 1.4
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays  110 20 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20201007 <a name="20201007"></a>
Remarks: Use this production with care, because significant fraction of jobs crashed after they hit TTL, which means that this dataset can be biased towards low-multiplicity events. It has different nodecays and impact parameter settings, when compared to similar **EPOS_20201030** production. 



Executive summary:

- Au-Au at 200 GeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 20
- nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 2.985 M events (1000 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20201007  
- common name of ROOT file: merged_z-EPOS_20201007.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 79 set maproj 197 set latarg 79 set matarg 197  set ecms 200
set bminim 0 set bmaxim 20
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 5    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 5    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 5    set nfreeze 10 set modsho 100   set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```

---



### EPOS_20201006-2 <a name="20201006.2"></a>
Executive summary:

- pp at 200 GeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays  110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 3.9 M events (100 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20201006-2
- common name of ROOT file: merged_z-EPOS_20201006-2.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 200
set bminim 0 set bmaxim 1.4
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays  110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20201006-1 <a name="20201006.1"></a>
Executive summary:

- pp at 17.3 GeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays  110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 3.9 M events (100 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20201006-1
- common name of ROOT file: merged_z-EPOS_20201006-1.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 17.3
set bminim 0 set bmaxim 1.4
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays  110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20201001-6 <a name="20201001.6"></a>

Executive summary:

- Au-Au at 200 GeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 14.2
- nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 823 K events (1000 events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20201001-6 
- common name of ROOT file: merged_z-EPOS_20201001-6.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 79 set maproj 197 set latarg 79 set matarg 197  set ecms 200
set bminim 0 set bmaxim 14.2
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 -2130 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 5    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 5    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 5    set nfreeze 10 set modsho 100   set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20201001-2 <a name="20201001.2"></a>
Remarks: This was initially **EPOS_20200608**, but rerun here with a few modifications.

Executive summary:

- pp at 17.3 GeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 3.8 M events (100 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20201001-2
- common name of ROOT file: merged_z-EPOS_20201001-2.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 17.3
set bminim 0 set bmaxim 1.4
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20201001-1 <a name="20201001.1"></a>
Remarks: This was initially **EPOS_20200602**, but rerun here with a few modifications.

Executive summary:

- pp at 200 GeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 3.8 M events (100 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20201001-1
- common name of ROOT file: merged_z-EPOS_20201001-1.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 200
set bminim 0 set bmaxim 1.4
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 2230 -2230 1130 -1130 1230 -1230 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20200608 <a name="20200608"></a>
Remarks: From the nodecays list removed Antilambdas (-2130)

Executive summary:

- pp at 17.3 GeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end 
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 3.9 M events (100 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20200608
- common name of ROOT file: merged_z-EPOS_20200608.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 17.3
set bminim 0 set bmaxim 1.4
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20200602 <a name="20200602"></a>
Remarks: From the nodecays list removed Antilambdas (-2130)

Executive summary:

- pp at 200 GeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 3.9 M events (100 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20200602
- common name of ROOT file: merged_z-EPOS_20200602.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 200
set bminim 0 set bmaxim 1.4
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 10    set nfreeze 10 set modsho 100   set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```

 

---



### EPOS_20200316 <a name="20200316"></a>
Executive summary:

- p-C at 17.2 GeV (C is target and proton is projectile)
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 2.84
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 3.9 M events (100 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20200316 
- common name of ROOT file: merged_z-EPOS_20200316.root

EPOS 3.117 config file:

```bash
pplication hadron  
set laproj 1 set maproj 1 set latarg 6 set matarg 12  set ecms 17.2
set bminim 0 set bmaxim 2.84
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



### EPOS_20200207-3 <a name="20200207.3"></a>
Executive summary:

- pp at 12.3 GeV 
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 7.8 M events (100 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20200207-3
- common name of ROOT file: merged_z-EPOS_20200207-3.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 12.3
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



### EPOS_20200207-2 <a name="20200207.2"></a>
Executive summary:

- pp at 8.8 GeV 
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 7.8 M events (100 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20200207-2
- common name of ROOT file: merged_z-EPOS_20200207-2.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 8.8
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



### EPOS_20200207-1 <a name="20200207.1"></a>
Executive summary:

- pp at 7.7 GeV 
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 7.9 M events (100 K events per final ROOT file)
- output files for this production are in: /scratch6/abilandz/sim/EPOS_20200207-1
- common name of ROOT file: merged_z-EPOS_20200207-1.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 7.7
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



### EPOS_20200121 <a name="20200121"></a>
Executive summary:

- pp at 13.0 TeV 
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 20 M events (100 K events per final ROOT file)
- output files for this production are in: /scratch5/abilandz/sim/EPOS_20200121
- common name of ROOT file: merged_z-EPOS_20200121.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 13000
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



### EPOS_20190114 <a name="20190114"></a>
Remark: This producton was originally tagged EPOS_LBF_pp91.

Executive summary:
- pp at 13 TeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is hardwired, i.e. only particles in ALICE acceptance are kept (|eta| < 1)
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 69.8 M events (100 K events per final merged ROOT file)
- output files for this production are in:  /scratch5/abilandz/sim/EPOS_20190114
- common name of ROOT file: merged_z-EPOS_20190114.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1  set ecms 13000
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



### EPOS_20181220 <a name="20181220"></a>
Remark: This producton was originally tagged EPOS_LBF_pp90.

Executive summary:
- pp at 13 TeV
- EPOS 3.117
- hydro (NO cascade)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end 
- ALICE acceptance is hardwired, i.e. only particles in ALICE acceptance are kept (|eta| < 1)
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 66.8 M events (100 K events per final merged ROOT file)
- output files for this production are in:  /scratch5/abilandz/sim/EPOS_20181220
- common name of ROOT file: merged_z-EPOS_20181220.root

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

fillTree(C2)

echo off
```



---



### EPOS_20180703 <a name="20180703"></a>
Remarks: This production was originally tagged EPOS_LBF_pA10. It's same as EPOS_20170210, except that here there was no cut on ALICE acceptance (i.e. cut |eta| < 1) was not applied.

Executive summary:
- p-Pb at 5.02 TeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 76.5 M events (100 K events per final merged ROOT file) 
- output files for this production are in: /scratch5/abilandz/sim/EPOS_20180703
- common name of ROOT file: merged_z-EPOS_20180703.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 82 set maproj 208 set latarg 1 set matarg 1  set ecms 5020
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 40    set nfreeze 50 set modsho 50   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 30000 set nfreeze 1  set modsho 1000 set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20170901 <a name="20170901"></a>
Remarks: This production was originally tagged EPOS_LBF_AA00.

Executive summary:
- Pb-Pb at 5.02 TeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is hardwired, i.e. only particles in ALICE acceptance are kept (|eta| < 1)
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 189.8 K events (100 events per final merged ROOT file) 
- output files for this production are in: /scratch8/abilandz/sim/EPOS_20170901
- common name of ROOT file: merged_z-EPOS_20170901.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 82 set maproj 208 set latarg 82 set matarg 208 set ecms 5020
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 40    set nfreeze 50 set modsho 50   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 1    set nfreeze 2 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 30000 set nfreeze 1  set modsho 1000 set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20170210 <a name="20170210"></a>
Remarks: This production was originally tagged EPOS_LBF_pA00. It's same as EPOS_20180703, except that here cut on ALICE acceptance (i.e. cut |eta| < 1) was applied.

Executive summary:
- p-Pb at 5.02 TeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample
- nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is hardwired, i.e. only particles in ALICE acceptance are kept (|eta| < 1)
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 54.5 M events (100 K events per final merged ROOT file) 
- output files for this production are in: /scratch5/abilandz/sim/EPOS_20170210
- common name of ROOT file: merged_z-EPOS_20170210.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 82 set maproj 208 set latarg 1 set matarg 1  set ecms 5020
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on
nodecays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 40    set nfreeze 50 set modsho 50   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 10    set nfreeze 10 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 30000 set nfreeze 1  set modsho 1000 set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```



---



### EPOS_20160901 <a name="20160901"></a>
Remarks: This was the large-scale production, obtained using 2 different batch farms, originally tagged EPOS_PRODUCTION_0010 and EPOS_0010, respectively. Output of each batch farm is stored in a separate output directory, and then intentionally across different 'scratch' disks (see below). To get one common list of ROOT files for productions from all batch farms, simply use:

```bash
find /scratch?/abilandz/sim/EPOS_2016090-? -type f -name "*.root" | tee list.txt
```

Executive summary:
- pp at 7 TeV
- EPOS 3.117
- hydro + cascade (UrQMD turned on)
- min bias sample, impact parameter is set via: set bminim 0 set bmaxim 1.4
- nodecays  20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is hardwired, i.e. only particles in ALICE acceptance are kept (|eta| < 1)
- fillTree(C2) ('bim' variable = number of pomerons)
- total statistics: 988 M events (100 K events per final merged ROOT file) 
- output files for this production are in:
  - /scratch6/abilandz/sim/EPOS_20160901-1 => 134.4 M events
  - /scratch7/abilandz/sim/EPOS_20160901-2 => 853.6 M events
- common name of ROOT file: merged_z-EPOS_20160901.root

EPOS 3.117 config file:

```bash
application hadron  
set laproj 1 set maproj 1 set latarg 1 set matarg 1 set ecms 7000
set bminim 0 set bmaxim 1.4
set istmax 25  set phimin 0  set phimax 0
set ninicon 1 set iranphi 0 ftime on 
nodecays  20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end

! uncomment one of the following lines

!core full hydro x3ff   hacas off  set nfull 40    set nfreeze 50 set modsho 50   set centrality 0  set ijetfluid 1  !hydro
core full hydro x3ff   hacas full set nfull 50    set nfreeze 20 set modsho 100   set centrality 0  set ijetfluid 1  !hydro+casc
!core off hydro x3ffoff hacas off  set nfull 30000 set nfreeze 1  set modsho 1000 set centrality 0                   !no hydro no casc

fillTree(C2)

echo off
```
