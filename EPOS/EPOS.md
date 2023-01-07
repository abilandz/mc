# Local EPOS productions

**Last update**: 20230107

### Table of Contents
* [EPOS_20221117 (pp at 13 TeV)](#EPOS_20221117)



---



### EPOS_20221117 (pp at 13 TeV) <a name="EPOS_20221117"></a>

Executive summary:


- pp at 13 TeV
- EPOS 4
- hydro (NO cascade)
- high multiplicity sample, impact parameter is set to 0: ```set bminim 0 set bmaxim 0```
- no decays 110 20 2130 -2130 2230 -2230 1130 -1130 1330 -1330 2330 -2330 3331 -3331  end
- ALICE acceptance is NOT hardwired
- total statistics: ~ 1 M events (100 x 10 per job, 100K events per ROOT file)
- the output files for this production are in: /scratch7/abilandz/sim/EPOS_20221117
- the common name of ROOT file: merged_z-EPOS_20221117.root
- the EPOS config file is here: /lustre/cbm/users/abilandz/EPOS/EPOS-01/epos4.0.0/examples/EPOS_20221117.optns



EPOS config file:

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

