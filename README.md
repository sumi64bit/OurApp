cpp-template-layout
===

`cpp-template-layout` is a template for a simple Visual Studio based C++ solution: it can be used as a base for new projects.

It is designed for Visual Studio Community 2019 for single or multiple projects inside one solution.

Project structure
-------------

This project has been set up with a specific file/folder structure in mind. The following describes some important features of this setup:

  - `bin` : Contains the final executabiles (generated)
  - `build`: Contains intermediate files generated during build time (generated)
  - `include`: Public projects header files that need to be exposed (generated)
  - `lib`: External libraries used in the projects
  - `src`: Solution source files (*.cpp), organised in separate folders for multiple .vxcproj projects or only a `main.cpp` for single projects


How to set up the project
-------------

0. This github project is just an example. I am going to show you how I made the solution as it is.
1. Create an empty solution.
2. Switch to Folder view by clicking Toggle between Solution and Folder views.
3. Add the folders bin, build, docs, lib, src
4. Switch to Solution view by clicking Toggle between Solution and Folder views.
5. Right click the solution and add the first project in the src folder! You can add multiple projects in this step.
6. Right click the first project and  enter `$(SolutionDir)bin\$(Configuration)\` in Properties/General/OutputDirectory.
7. Right click the first project and  enter `$(SolutionDir)build\$(ProjectName)\$(Configuration)\` in Properties/General/IntermediateDirectory.


Options
-------------

You can generate the `.gitignore` file using [gitignore.io](https://www.gitignore.io/)

