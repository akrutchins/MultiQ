# Instructions for Using the MultiQ-IT Ion Trap Simulator  

This ad hoc computer program, developed in Processing and Java, simulates ion motion within a 486-quadrupole MultiQ-IT ion trap. Detailed descriptions of the computer model can be found in:  
**A.N. Krutchinsky, I.V. Chernushevich, V.L. Spicer, W. Ens, K.G. Standing. "Collisional Damping Interface for an Electrospray Ionization Time-of-Flight Mass Spectrometer,"** *Journal of the American Society for Mass Spectrometry*, Volume 9, Issue 6, June 1998, Pages 569-579.  

## Setup Instructions  
1. **Download Files**  
   - Download all `*.pde` files and place them in a folder named `Demiurge_MultiQ_486` on your computer.  

2. **Install Processing**  
   - Install Processing 4.3 (latest version as of December 2024).  
   - Other versions may work, but they haven’t been thoroughly tested.  
   - The program has been tested on both Windows 11 and Linux.  

3. **Run the Program**  
   - Open the `Demiurge_MultiQ_486.pde` file in Processing and run the program.  
   - A new window titled "Demiurge_MultiQ_486" will open.  

## Usage Instructions  
### Step 1: Create Geometry  
1. Move the mouse cursor over the program window and press **F1** (or **Alt+F1**) to open the dialog menu.  
2. Select the **"Create Geometry"** option to define the electrode geometry.  
   - Geometry is defined in the `"Geometry"` folder, starting from **line 26**.  
   - By default, it uses the `definePotential_RF(float x, float y, float z)` function.  

### Step 2: Calculate Potential  
1. Press **F1** again and choose the option to calculate the potential for the defined geometry.  
2. Once calculations are complete, save the potential file into the program folder.  
   - By default, name the file `RF` (see the `DEFAULT_RFPOT_FILE` variable in the main folder).  

### Step 3: Define and Save Another Geometry  
1. To calculate a different geometry, edit **line 26** in the `"Geometry"` folder.  
   - For example, replace `definePotential_RF(x, y, z)` with `definePotential_DC(x, y, z)` to calculate DC potentials for the MultiQ.  
2. Repeat **Steps 1 and 2** to generate and save a DC potential file.  
   - Save this file in the same folder with the name `DC`.  

### Step 4: Load Precalculated Potentials  
1. Ensure the `Demiurge_MultiQ_486` folder contains the two generated files:  
   - `RF` (~100MB)  
   - `DC` (~100MB)  
2. Run the program and press **F2** to open the options menu.  
3. Select **"Load Precalculated Potentials"** to load the `RF` and `DC` potential arrays into memory.  

### Step 5: Run Simulations  
1. Press **F2** to open the options menu again.  
2. Choose an option to:  
   - Simulate ion motion for multiple ions.  
   - Compute ion depletion effects.  

## Notes  
- Feel free to modify, improve, or adapt the program as needed.  
- If you encounter issues or have suggestions, contributions are welcome!  
