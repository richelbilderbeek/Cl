[Go back to Richel Bilderbeek's homepage](index.htm).

[Go back to Richel Bilderbeek's command line page](Cl.htm).

 

 

 

 

 

([Command line](Cl.htm)) [pack2port script](ClPack2port.htm)
============================================================

 

I used this script to zip multiple folder and files ito a single
archive, with maintaining/copying the same folder structure.

 

The [tool](Tools.htm)
[CreateQtProjectZipFile](ToolCreateQtProjectZipFile.htm) automates this
task.

 

  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  ` #!/bin/sh #pack2port packs all the files to port into a single .zip file, #minicking the same folder structure #Folder structure # Projects #  ProjectRampal #    143                    <-- pack *.* # Tools #   ToolTestBinaryNewickVector    <-- pack *.* #   ToolTestTwoDigitNewick  <-- pack *.* echo "Removing old zip archive" rm 143.zip echo "Mimicking file structure" mkdir temp_zip mkdir temp_zip/Projects mkdir temp_zip/Projects/ProjectRampal mkdir temp_zip/Projects/ProjectRampal/143 mkdir temp_zip/Tools mkdir temp_zip/Tools/ToolTestBinaryNewickVector mkdir temp_zip/Tools/ToolTestTwoDigitNewick echo "Copying files" cp *.* temp_zip/Projects/ProjectRampal/143 cp ../../../Tools/ToolTestBinaryNewickVector/*.* temp_zip/Tools/ToolTestBinaryNewickVector cp ../../../Tools/ToolTestTwoDigitNewick/*.* temp_zip/Tools/ToolTestTwoDigitNewick echo "Compressing files" cd temp_zip #Zip the folder Projects recursively in 143.zip zip -r 143 Projects #Zip the folder Tools recursively in 143.zip zip -r 143 Tools cd .. cp temp_zip/143.zip 143.zip echo "Cleaning up" rm temp_zip/Projects/ProjectRampal/143/*.* rmdir temp_zip/Projects/ProjectRampal/143 rmdir temp_zip/Projects/ProjectRampal rmdir temp_zip/Projects rm temp_zip/Tools/ToolTestBinaryNewickVector/*.* rm temp_zip/Tools/ToolTestTwoDigitNewick/*.* rmdir temp_zip/Tools/ToolTestTwoDigitNewick rmdir temp_zip/Tools/ToolTestBinaryNewickVector rmdir temp_zip/Tools rm temp_zip/*.* rmdir temp_zip echo "Done"`
  --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

 

 

 

 

 

[Go back to Richel Bilderbeek's command line page](Cl.htm).

[Go back to Richel Bilderbeek's homepage](index.htm).

 

[![Valid XHTML 1.0 Strict](valid-xhtml10.png){width="88"
height="31"}](http://validator.w3.org/check?uri=referer)
