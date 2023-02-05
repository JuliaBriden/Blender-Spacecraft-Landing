# Blender Spacecraft Landing

1. Open demo.blend

2. In Scripting, run EDL.py to set the keyframes for the powered descent animation from the .csv files in the Data folder

  a. Write new .csv files in Julia for your guidance algorithm using the following code:
  
    CSV.write("t.csv",  Tables.table(t), writeheader=false)  
    CSV.write("r.csv",  Tables.table(r), writeheader=false)
    CSV.write("γ.csv",  Tables.table(γ), writeheader=false)
    CSV.write("Thrust.csv",  Tables.table(T), writeheader=false)
    CSV.write("T_nrm.csv",  Tables.table(T_nrm), writeheader=false)
    
    Where t is your vector of time, r is your matrix of positions, γ is your matrix of pointing angles, Thrust is your matrix of thrust control inputs, and T_nrm is your vector of normalized thrust.
    
    Then copy these files to the Data/ folder.
    
 3. After running the script, bake the animation by:
 
   a. Click on the Cube object.
 
   b. Click Physics Properties tab.
   
   c. Under Fluid/Settings press the Bake button (note: you may have to click the Free Data button first).
   
 4. Now open the Timeline view and click play.
 
 To manually change the thrust vector qualities, change the Fuel in the Spacecraft/Thrust object or change the Wind objects in Spacecraft/Thrust/Wind.windnumber.
 
 
 ## Models available for from from
 
 * Spacecraft: [3D model Dummy landing moduleby Bianconi](https://www.turbosquid.com/3d-models/3d-model-dummy-landing-module-1782671)
 
 * Apollo 17 Landing Site: [Ames SpaceShop](https://nasa3d.arc.nasa.gov/detail/Apollo17-Landing)
