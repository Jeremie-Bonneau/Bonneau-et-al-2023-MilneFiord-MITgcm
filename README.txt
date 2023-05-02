These are the necessary files to rerun the numerical experiment by Bonneau et al. (2023)
Steps:
1. Download MITgcm code, I used checkpoint 67z.
2. Download the Iceplume package by Tom Cowton (https://github.com/tcowton/iceplume)
3. Replace the pkg folder of the Iceplume package by the files provided in the iceplume_angle folder here
4. Unzip the code subdirectory provided here
5. In build subdir, Generate a make file using the genmake tool that comes with the MITgcm file (see MITgcm manual)
6. In build subdir, Manually delete the two -implicit-none flags for the compilers in Makefile (necessary because of the ODPAK routine that IcePlume uses)
7. In build subdir, Compile the model by executing Makefile (make depend command then make command, see MITgcm manual), now you have the compiled model
8. Unzip the input subdir
9. In run subdir, Add symbolic link to the files from the input subdir
10. In run subdir, Run MITgcm

Contact jbonneau@mail.ubc.ca for any inquiries.
