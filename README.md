# DIGITAL-SOC-DESIGN-AND-PLANNING
Digital VLSI SOC Design and Planning
# DAY 1 
- Digging deeper into opensource EDA, OpenLANE and sky130 PDK
- Then jumped into LAB for day 1 and got the idea of the intial steps and more about using SKYWATER 130m PDK, Openlane EDA

## Open the working Directory


![1a](https://github.com/BhanuBangari/DIGITAL-SOC-DESIGN-AND-PLANNING/assets/166434514/e23aa061-e61a-4856-be77-2aa5cf834b61)

```bash
  cd Desktop
  cd work/tools
  cd openlane_working_dir
  cd openlane
```

## Opening the Openlane

Enter the commands
```bash
  docker
  pwd
  ls -ltr
```
Opening the openlane in interactive mode, 
```bash
 ./flow.tcl -interactive
```
Also give these commands to prepare the openlane,

```bash
  package require openlane 0.9
  prep - design picorv32a
```
## Running Synthesis

To run the Synthesis
```bash
 run_synthesis
```

After Synthesis is completed, it is shown that the "Synthesis was successful"

This contains all the details about the synthesis of the picorv32a 

![chip area](https://github.com/BhanuBangari/DIGITAL-SOC-DESIGN-AND-PLANNING/assets/166434514/d88ed806-2034-47ed-997a-6c4f6624e5d1)

Chip Area of the Module is : 147712.918400


![flop ratio 1](https://github.com/BhanuBangari/DIGITAL-SOC-DESIGN-AND-PLANNING/assets/166434514/e58559e3-00ca-4c7f-bdd1-2db86191e0d4)

- Number of cells: 14876

- Number of FF: 1613


For finding the Flop ratio.
This can be calculated by using the formula:
                 
             Flop ratio in (%) = Total No of D-FF
                               --------------------  X 100
                                Total No of Cells

                              = 1613
                              --------   X 100
                                14876 

                              = 10.8429685


## Synthesis Report

The synthesis Results are found in the directory

```bash
   /results/synthesis/picorv32a.synthesis.v
```

The Synthesis Report are found in the directory

```bash
   /reports/synthesis/1-yosys_4.stat.rpt
```

# Day 2

## Floorplanning
The Day 2 LAB gives the complete flow of the Floorplanning and the placement process

After the Synthesis process, type the command

To run floorplan
```bash
  run_floorplan
```
The configuration files are inside the location
```bash
  /Desktop/work/tools/openlane_working_dir/openlane/configurations/README.md
```
we will be getting a success message like this
![floorplan success](https://github.com/BhanuBangari/DIGITAL-SOC-DESIGN-AND-PLANNING/assets/166434514/bcbf748d-bad7-4966-8bbf-9f2ad787e43a)


In this particular location from the floorplan.def file, we can able to see the area of the chip
![Die area 2](https://github.com/BhanuBangari/DIGITAL-SOC-DESIGN-AND-PLANNING/assets/166434514/3d06628a-fcfa-40ed-96fc-3ed80a0e3a97)



             1000 unit distance = 1 Micron

             Distance in micron = value
                                ----------
                                   1000

            Die width in micron = 660685 
                                 ---------
                                   1000
                                
           Die height in micron =  671405 
                                  ---------
                                    1000

          Area of die in micron = 660.685*671.405 Square micron 

