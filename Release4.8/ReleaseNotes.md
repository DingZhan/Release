# LS-PrePost 4.8

**Release Data**:

**Major new features of the 4.8 series, compared to 4.7:**

[toc]




## New keywords and improvement

### New keywords

* CONTROL_EXPLICIT_THERMAL_OUTPUT
* CONTROL_EXPLICIT_THERMAL_SOLVER
* CONTROL_ACOUSTIC
* CONTROL_FORMING_TRIMMING_SOLID_REFINEMENT
* CONTROL_MPP_PFILE
* CONTACT_AUTOMATIC_SINGLE_SURFACE_TIEBREAK
* CONTACT_AUTOMATIC_GENERAL_TIEBREAK
* CONTACT_AUTOMATIC_SINGLE_SURFACE_TIEBREAK_BEAM_OFFSET
* CONTACT_AUTOMATIC_GENERAL_TIEBREAK_BEAM_OFFSET
* CONSTRAINED_SOLID_IN_SOLID_{OPTION1}_{OPTION2}
* CONSTRAINED_IMMERSED_IN_SPG
* DATABASE_PBLAST_SENSOR
* ICFD_BOUNDARY_PERIODIC
* IGA_options
* INITIAL_STRAIN_SHELL_NURBS_PATCH
* INITIAL_STRESS_SHELL_NURBS_PATCH
* MAT_296
* MAT_291
* MAT_187_LIGHT
* PART_COMPOSITE_LONG_CONTACT
* SECTION_IGA_SHELL
* SECTION_IGA_SOLID
* SET_IGA_EDGE_{OPTION1}_{OPTION2}_{OPTION3}_
* SET_IGA_FACE_{OPTION1}_{OPTION2}_{OPTION3}
* SET_IGA_POINT_UVW_{OPTION1}_{OPTION2}



### Feature improve

1. speed up of reading keyword file by improve the process of remove space characters of each line;
2. speed up of reading keyword file by improve the process of remove space characters of each line;
3. speed up of reading keyword file by improve the process of remove space characters of each line;



### New features

1. support multiply ids in "Keyin" of entity selection panel

   <img src="pictures/keyword_feature01.png" alt="Alt text" style="zoom:60%;" />

2. support popup keyword form when right click on the cell of SortBy dialog

   <img src="pictures/keyword_feature02.png" alt="Alt text" style="zoom:60%;" />

3. support popup keyword form when right click on the cell of SortBy dialog

4. support create *INITIAL_VELOCITY in EntCreation dialog

   <img src="pictures/keyword_feature03.png" alt="Alt text" style="zoom:60%;" />

5. Identify dialog: support pop-up keyword form of selected Entity(node/element/part)

   <img src="pictures/keyword_feature04.png" alt="Alt text" style="zoom:60%;" />

6. Identify dialog: support pop-up keyword form of selected Entity(node/element/part)

   <img src="pictures/keyword_feature05.png" alt="Alt text" style="zoom:60%;" />

7. right menu of *DEFINE_CURVE to load curve from xydata file, “Load Curve” will load curve data from file and create *DEFINE_CURVE, “Load curve to table” will also use these curve ids to create *DEFINE_TABLE.

   <img src="pictures/keyword_feature06.png" alt="Alt text" style="zoom:60%;" />

8. support "Diff Parts" on model compare dialog, compare the selected two models and find out parts that are different or only exist in one model, then highlight these parts and set others as transparent.

   <img src="pictures/keyword_feature07.png" alt="Alt text" style="zoom:33%;" />

---









## NewXYPlot and OldXYplot

### NewXYPlot

1. support for the splitwindow state about "Plot" and "New" of history dialog.

2. support for draw the annotation in split window and main window by changing the annotation functions based on port area.

   <img src="pictures/newxyplot_01.png" alt="Alt text" style="zoom:75%;" />

3. support for the rubber band for annotation link line.

4. improve the annotation text boundary.

   <img src="pictures/newxyplot_02.png" alt="Alt text" style="zoom:75%;" />

5. support for the splitwindow state to fix "Comment by Shi. split window, draw histroy plot, then close lspp, crash".

6. support for the splitwindow state about "Plot" of history dialog. 

7. improve enter and exit annotation state both of them will refresh the xyplotting zone. 

8. support for showing the XYPlot on the split window state.

9. fix print bug when annotation notes on the screen.

10. Add the enter label callback function to improve the UE.

11. change default font size to smaller.

12. Add without arrow on annotation for like label to curve.

13. Add the boundary of label on annotation.

14. improve the move port on main when out of the main window boundary, Shift+ctrl+mouse left button to drag the port on main window.

15. improve the move port on main to add return default position function.

    <img src="pictures/newxyplot_03.png" alt="Alt text" style="zoom:60%;" />

16. support for the cross2d for all curves in different ports.

    <img src="pictures/newxyplot_04.png" alt="Alt text" style="zoom:60%;" />

17. Add the "X" button to exit window when crossing results. 

18. support for drawing the port with model when getting curves from external file.

19. [Bug 16213] New: Problem with x-axis label when saving FLD curve.



### OldXYPLOT

1. support for the crossing curves with different x range when interpolation.

2. support for the saej211.

   <img src="pictures/oldxyplot_01.png" alt="Alt text" style="zoom:60%;" />

3. support for interface of prepare for define curve.

4. support for the legend on XYPlot dialog and fix plotting csv file bug.

5. [Bug 16213] New: Problem with x-axis label when saving FLD curve.

6. fix bug of loading the empty csv file.

7. Fix the filter problem when GUI operated and send command results are different.

8. improve the efficient problem of drawing all of curves in file.

---











##  Multiphysics Solution

### Open

1. Open the “Multiphysics Solution” interface by checking on the “Solution Explorer” item under the “View” menu.

   <img src="pictures/ms_open01.png" alt="Alt text" style="zoom:33%;" />

2. Pop up the solution explorer file operation menus by right clicking on the top tree item in the solution explorer.

   <img src="pictures/ms_open02.png" alt="Alt text" style="zoom:33%;" />

   * *“New Solution” can create a new solution file.*

   * *“Save Solution” can save the current solution data to the already named solution file.*

   * *“Save Solution As...” can save the current solution data to a new solution file with a new name.*

   * *“Load Solution...” can load a saved solution file to the solution explorer.*

   * *“Recent” can list the latest 5 opened solution files.*

   * *“Run” can open the “LS-Run” and call the “LS-DYNA” solver to solve the defined solution file.And this item can also save the solution data to a “.solution” file and a corresponding keyword file.*

   * *“Export Keyword File...” can save the solution data to corresponding keyword file.*



### Create New Solution

1. Select the “New Solution” menu item and pop up the “New Solution” interface.

   <img src="pictures/ms_create01.png" alt="Alt text" style="zoom:60%;" />

   * *This interface can name the new solution file and set the working directory.*

   * *When the current model data is not the correct one for the new solution file, user can use the “Keyword Data” option to load a keyword file.*

   * *The unit system is based on the loaded keyword file or the current opened model data in LS-Prepost.*

   * *Solution Explorer can support “Mechanical”, “ICFD”, “Thermal(structure)” and “Structured ALE” four case types. User can choose the right one to define the whole solution tree structure.*

     

### Solution Tree Structure

1. The tree structure contains three layers:

   * *The top layer is called “Multiphysics Solution”, in this layer user can set the unit system and keyword data version for the whole analysis.*

   * *The second layer is called “Case”.*

     <img src="pictures/ms_solution01.png" alt="Alt text" style="zoom:60%;" />

   * *Different cases have the same model data(the materials of parts in different case can have different properties.), connectors data and contact data if these tree items exist in one case. So the case operations in right-clicked menu of the case item can copy the case data to other cases which can be added before or after the current case. User can choose to call the “LS-DYNA” solver from any case by clicking on the “Run...” menu item. If user choose to run from a selected case, a “.lsda” file which is got from the previous case is necessary.*

   * *The third layer is different case types. Different case types may have different tree structures. User select correct case type when create a new solution file from the “New Solution” interface, LS-Prepost will build whole tree structure automatically.*

2. The solution data contains two parts, one is the tree node in the tree structure and the other one is called property gird which is attached to the corresponding tree node. User can select different tree nodes and set their related property data in the property gird.

   <img src="pictures/ms_solution02.png" alt="Alt text" style="zoom:60%;" />



### Mechanical and Thermal Case

1. For “Mechanical” and “Thermal” case types, the whole tree structure both contains three parts:Analysis, Model,Output. It can be built like the following picture.

   <img src="pictures/ms_mechanical01.png" alt="Alt text" style="zoom:60%;" />

2. In the “Analysis” item user can set the solver data, time step data, and integration data. For “Mechanical”, the solution only support the “Nonlinear Implicit” solver for now. If user select the “Mechanical” and “Thermal” case type, the tree data under the “Analysis” item is like what the picture shows.

3. The “Model” item contains fem model data, initial conditions data, boundary conditions data, prestress data, contact data, connector data.

   * *Different analysis type mean different boundary conditions data. The “Node Constraints”, “Force/Moments”,”Pressures” and ”Prescribed Motions” belong to “Mechanical” analysis. And “Convection”, “Temperature”, “Flux” and “Radiation” are related to “Thermal” analysis.*

   * *The material property in part item is defined by a new material library. In LS-Prepost executable folder, LS-Prepost add a sample material database file called “material.xml”. It is in XML and keyword format. Users can add their own material databases as the LS-Prepost “built-in” database format. The thermal material data will be shown when the thermal analysis exists in the solution tree structure.*

     <img src="pictures/ms_mechanical02.png" alt="Alt text" style="zoom:60%;" />

   * *Contact item only support “Sliding Contact”, “Tied Contact” and “Transducer” three types for now. The data for thermal analysis is in every contact item property gird.*

4. The “Output” item can output the defined “Node Data” and “Element Data” and some default result files like “glstat”, “rcforc”, “bndout”, ”spcforc”, “matsum”, “secforc” , “sleout” and so on.

5. For now, the post analysis is added into the property grid for part items and contact items. And user can switch the item property between “pre” and “post” button. If users change any “pre” data, they need to rerun the current case to update the post data. When users choose to rerun the case, the case data after the selected one will be updated too.

   <img src="pictures/ms_mechanical03.png" alt="Alt text" style="zoom:60%;" />

   <img src="pictures/ms_mechanical04.png" alt="Alt text" style="zoom:33%;" />

   

### ICFD

The ICFD type may build a tree structure as the following picture shown. It uses the same solution data format(tree nodes and related property grid). ICFD has its special items which are related to the ICFD analysis.

1. Now solution explorer supports these six analysis types, and they are “Turbulent”, “Thermal”, “FSI”, “DEM Coupling”, “Free Surface” and “RTM”. Different analysis types have different properties.

2. Users need to define their own materials under “Material” item and mesh data under the “Mesh” item.

3. The model data is came from the loaded keyword file in “New Solution” interface or the current opened model data in LS-Prepost.

4. In “Output” item, users can set the output result data for ICFD analysis.

   

### Structured-ALE

The Structured-ALE type may build a tree structure using the same solution data format(tree nodes and their related property grid) as the following picture shown.

<img src="pictures/ms_structuredALE01.png" alt="Alt text" style="zoom:60%;" />

1. If users want to do a “FSI” analysis, they need to load the fem keyword data when create the new solution file or use the already opened model data in LS-Prepost. The “FSI” analysis data can be set under the “FSI” items.

2. The “Trim”, “Volume-Filling”, “Initial Conditions” ,“Boundary Conditions” are all based on the defined “Mesh”. And the properties about the mesh is like below picture.

   <img src="pictures/ms_structuredALE02.png" alt="Alt text" style="zoom:33%;" />

3. The “Boundary Conditions” can support six different types: “Pressure”, “Node Constraint”, “Prescribed Motion”, “Ambient Element”, “Hydro static” and “Non Reflecting”.

   

### Solution Property

Solution explorer defines some properties which will call the LS-Prepost other powerful functions.

1. Define Set Data: clicking the first button will list all defined set data in current model and clicking the second button will confirm what data users have selected on the model.

   * *Node Set:* 

     <img src="pictures/ms_property01.png" alt="Alt text" style="zoom:60%;" />

   * *Part Set:* 

     <img src="pictures/ms_property02.png" alt="Alt text" style="zoom:60%;" />

   * *Shell Element Set:* 

     <img src="pictures/ms_property03.png" alt="Alt text" style="zoom:60%;" />

   * *Segment Set:* 

     <img src="pictures/ms_property04.png" alt="Alt text" style="zoom:60%;" />

2. Define Local Coordinate System: clicking the first button will list all the defined local coordinate system in current model and clicking the second button will pop up the “Define Local Coordinate System” interface. 

   <img src="pictures/ms_property13.png" alt="Alt text" style="zoom:60%;" />

   <img src="pictures/ms_property05.png" alt="Alt text" style="zoom:60%;" />

3. Define Material: clicking the button will pop up the “Material Library” interface and list all the material databases in LS-Prepost.

   <img src="pictures/ms_property14.png" alt="Alt text" style="zoom:60%;" />

   <img src="pictures/ms_property06.png" alt="Alt text" style="zoom:60%;" />

4. Define Curve: clicking the first button will switch current property among constant, curve, curve function, function four types, and clicking the second button will list all the defined curve data, clicking the third button will pop up a interface to input all the curve data.

   <img src="pictures/ms_property07.png" alt="Alt text" style="zoom:60%;" />

   <img src="pictures/ms_property08.png" alt="Alt text" style="zoom:60%;" />

   <img src="pictures/ms_property09.png" alt="Alt text" style="zoom:60%;" />

   <img src="pictures/ms_property10.png" alt="Alt text" style="zoom:60%;" />

   <img src="pictures/ms_property11.png" alt="Alt text" style="zoom:60%;" />

   <img src="pictures/ms_property12.png" alt="Alt text" style="zoom:60%;" />

---













## Femzip

1.  improve the efficient problem of loading the first state to draw model.

2. fix problem of loading model and fringe.

3. fix crash of setting the SPH surface.

---







## 3DGraphics

1. support for visualizing DEFIND_TABLE_2D.

2. support for visualizing DEFIND_TABLE_3D.

   <img src="pictures/3dgraphics_01.png" alt="Alt text" style="zoom:60%;" />

3. fix DefTable crashing bug when no data is loaded.

4. improve the GUI.
---







## Ascii and Binout

### Ascii

1. support for the new component in the sbtout branch.

   <img src="pictures/ascii_01.png" alt="Alt text" style="zoom:60%;" />

2. support for PBLAST_SENSOR branch.

3. support for swfore about OPT=9 of *MAT_100.

4. fix crashing bug when elout including Elastic materials have no history variables.

5. fix boundary array problem.

6. fix problem of FreeNSetAsciiMemory.



### Binout

1. support for the new component in the sbtout branch. 

   <img src="pictures/binout_01.png" alt="Alt text" style="zoom:60%;" />

2. support for the sphflow branch.

3. support for pblast_sensor branch.

4. support for the hex assembly with binout of area selection.

5. Model selection the spotweld to highlight binout dialog's id list related and highlight on model when selected on binout dialog id list.

   <img src="pictures/binout_02.png" alt="Alt text" style="zoom:75%;" />

6. support for highlight the define coordinate entity when clicking the swforc solid assembly.

7. support for picking define coordinate and update the binout swforc id list.

8. support for outputting curvout to ascii file.

9. fix the rwforc bug when multiple selecting ids and components.

10. fix the bug of showing curve after the element is deleted.

11. update l2a for sphflow and pblast_sensor branches.

12. [Bug 16272] New: lspp fails to read a large binout file Ticket#2019120410000167

13. fix bug of selected multiple components to plot set id data.

---







## Scripting Command Language and Python Language

### Scripting Command Language

1. support for the "scalar" component name to get the node scalar and element scalar results.

2. support for element deletion.

3. update scl samples of control macro with file.

4. fix int array bugs to deep copy the int array results.

5. Save result node id of the command "ident xyzpt" to get ready for SCLCmdResultGetValue in SCL.

6. fix bug of xyplot related functions when no model loaded.

More examples see [SCLExamples](https://ftp.lstc.com/anonymous/outgoing/lsprepost/SCLexamples/SCL_Examples.zip)



### Python Language

At the moment, the Python language is also used as the scripting language of LS-PrePost. The user can use Python scripting in LS-PrePost. The Python modules that LS-PrePost provides include "DataCenter" and "LsPrePost", more details see [lsppscripting.pdf](https://ftp.lstc.com/anonymous/outgoing/lsprepost/SCLexamples/lsppscripting.pdf)

**How to use Python Scripting in LS-PrePost**

Firstly the user should set own Python home path(LS-PrePost4.8 only supports Python36) by using LS-PrePost command:

`setpythonhome "python/home/path"(like D:\Python36)`

<img src="pictures/python_01.png" alt="Alt text" style="zoom:75%;" />

The Python home path will be automatically saved to the config file.

And then run Python scripting with the regular LS-PrePost command, or within the command file, use the runpython command to execute the Python scripting, parameters can also be passed to the script.

The syntax:

`runpython "pythonscriptingname" optional parameters`

<img src="pictures/python_02.png" alt="Alt text" style="zoom:75%;" />

Example: the following command file will execute the script that creates a X-Y curve with the parameters defined in the command file.

```
parameter  pa 9.0E+07
parameter  pb 7000.0
parameter  pc  4.0E+07
parameter  npt  300
parameter  xmin  0.0
parameter  xmax  0.00126
runpython "customcurve.py"  &npt &pa &pb &pc &xmin &xmax
```
More examples see [PythonExamples]()

