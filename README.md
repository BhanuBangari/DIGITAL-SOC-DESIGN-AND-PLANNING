# DIGITAL-SOC-DESIGN-AND-PLANNING
Digital VLSI SOC Design and Planning
# DAY 1 
- Digging deeper into opensource EDA, OpenLANE and sky130 PDK
- Then jumped into LAB for day 1 and got the idea of the intial steps and more about using SKYWATER 130m PDK, Openlane EDA
# Commands given in the terminal 
  cd Desktop
  cd work/tools
  cd openlane_working_dir
  cd openlane
![1a](https://github.com/BhanuBangari/DIGITAL-SOC-DESIGN-AND-PLANNING/assets/166434514/e23aa061-e61a-4856-be77-2aa5cf834b61)
# 
After getting into the directory, enter the commands
#  
  docker
  
  pwd
  
  ls -ltr
  
To open the openlane in interactive mode,

 ./flow.tcl -interactive
To prepare the openlane,

  package require openlane 0.9
  prep - design picorv32a
