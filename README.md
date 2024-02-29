# NiCrCoFe_HEA
# Quantitative analysis of multiple deformation mechanisms in NiCrCoFe high-entropy alloy 
In this repositiory, we demonstrate the LAMMPS code by taking the equimolar NiCrCoFe high entropy alloy system with seven different grain sizes as an example.

# Establish the initial model, Calculate stacking fault energy and Tensile simulation
If you wish to run our code, we use the Atomsk (beta-0.11 released) and the LAMMPS (lammps-3Mar2020) under the Linux system.


# 1.Construction of initial models with different grain sizes
  (1) The **`Ni_cell.xsf`** file is a single crystal cell used to construct polycrystalline structures.  
         The lattice parameter is 3.54 Angstroms.
  (2) The **`polycrystal-xxx.txt`** seed file is a single crystal cell used to construct polycrystalline structures. 
         The positions and crystallographic orientations of the grains can be given explicitely, Please note that the orientations of the grains should be identical.
  (3)  Run the atomsk code to generate polycrystalline models with different grain sizes.The code is as follows :
         atomsk --polycrystal  Ni_cell.xsf  polycrystal-xxx.txt Ni-xxxnm.lmp -wrap
  (4) Use Ni-xxxnm.lmp to generate initial sample of NiCrCoFe HEAs .

# 2.Calculate stacking fault energy
   The calculation program of stacking fault energy  refers K-T Chen 's calculation program.

# 3.Tensile simulation
The **`in.tensile`** is our input file. The simulation process is as follows:
(1)  Energy minimization
(2)  Lattice relaxation
(3)  Monte Carlo simulation
(4)  Boundary condition readjustment
(5)  Tensile simulation


If you have any question about our project, please contact our email address: houzy@chd.edu.cn


## References
<a id="1">[1]</a> 
Jun Chen, Zhaoyang Houa, Zhen Wanga, Kefan Li, Pengfei Zou, Kejun Dong, Gang Shi, Quantitative analysis of multiple deformation mechanisms in NiCrCoFe high-entropy alloy(2024).

<a id="1">[2]</a> 
K-T Chen, T-J Wei, G-C Li, M-Y Chen, Y-S Chen, S-W Chang, H-W Yen, C-S Chen, Mechanical properties and deformation mechanisms in CoCrFeMnNi high entropy alloys: a molecular dynamics study, Materials Chemistry and Physics, 271, 124912, (2021).

<a id="2">[3]</a> 
W.-M. Choi, Y.H. Jo, S.S. Sohn, S. Lee, B.-J. Lee, Understanding the physical metallurgy of the CoCrFeMnNi high-entropy alloy: an atomistic simulation study, npj Computational Materials 4(1) (2018).

