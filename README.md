# ECH_252_final

## General information
1. `chignolin.pdb`, `chignolin.prmtop` and `chignolin.rst` are the input structure files required for the AMBER simulation.  
2. `md.in` is the AMBER run file, which contains the details of the simulation. The parameters that you can vary are  
   a.  
      `ntpr = 500   ! write energy information every 500 steps to log file`  
      `ntwx = 500   ! write coordinates every 500 steps to a trajectory file`  
      `ntwr = 500   ! write restart file every 500 steps to corresponding file`  
      
   b.  
      `nstlim = 2000000 ! perform 2000000 MD steps`  (**You need to make this change according to the question**)  
      `dt = 0.002     ! use time steps of 2fs`  
      `tempi = 300    ! initial temperature T = 300 K`  (**You need to make this change according to the question**)  
      `temp0 = 300    ! reference temperature T = 300 K`  (**You need to make this change according to the question**)

   Please note that since the simulation is **Isothermal**, **tempi=temp0**

   c. `plumed_amber.dat` runs the metadynamics plugin for AMBER using the following command:  

      ```
      metad: METAD ARG=cv SIGMA=0.4 HEIGHT=1 BIASFACTOR=10 TEMP=300 PACE=100 FILE=HILLS
      ```  
      (**You need to change the temperature according to the question**)


