# File Management
The file organization and file naming convention will vary between Fusion 360 or SolidWorks files.

> **File Archive:** All archived CAD files should include exported `.iges` and `.step` files for CAD software compatibility.

> **Note:** Individual files can only be worked on one at a time as there isn't an easy way to merge changes in CAD files, as would normally happen in code. Since SolidWorks has individual files for components, the workload can be broken up so that collaborators can work on separate components. With Fusion 360, since the overall file is an assembly, there is no easy way for multiple collaborators to work simultaneously on the design.

## Fusion 360 Files
Since Fusion 360 files are assembly files themselves, the file organization will be fairly minimal. The *current* overall design file should be saved within the main mechanical subsystem directory:

> * Poseidon
>    * Mechanical Subsystem
>       * CAD Files
>          * *Current* design file: [`Poseidon_Assembly.f3d`]() // add link

### File Organization

> * Poseidon
>    * Mechanical Subsystem
>       * CAD Files
>          * *Current* design file: [`Poseidon_Assembly.f3d`]() // add link
>          * Components
>          * Archived Design Change Files
>             * Assemblies
>             * Components

### File Naming Convention
All CAD files should follow the following naming convention: `<Project>_Assembly.f3d`. Users should provide specific details in the design changes to the commit history.

> **Example:** `Poseidon_Assembly.f3d`

**Current File:** [`Poseidon_Assembly.f3d`]() //Add link

#### Archived Files Files
The general purpose of the file archives is to provide a fresh starting point for a design revision. Therefore, none of these files should contain *design in progress* files; rather, completed design changes only.

Any archived CAD files should follow the following naming convention: `<Project>_Assembly-<Updated Component Name>-(<Date>).iges`. Where, the updated or changed component design and date are notated in the file name. Users should provide specific details in the design changes to the commit history.

> **Example:** `Poseidon_Assembly-Raspberry_Pi-(04-03-18).iges`

## SolidWorks Files
Since SolidWorks assembly files are usually based off of individual component files, the file organization will be more complex. However, it allows users to work on separate files simultaneously.

### File Organization

* Poseidon
   * Mechanical Subsystem
      * *Current* design file: [`Poseidon_Assembly.f3d`]() // add link
      * Archived Design Change Files

### File Naming Convention
`<Project>_Assembly.sldasm`

`<Project>_Assembly.sldprt`

**Current Files:** N/A (Using Fusion)

#### Archived Files Files

`Poseidon_<Updated Subassembly>-(<Date>).iges`
`Poseidon_<Subassembly>-<Updated Component Name>-(<Date>).iges`


# Making Commits

# Archiving Process

1. Export the CAD file(s) as an `.iges` file for software compatibility.
   * Follow the naming convention guidelines above.
   * Add the date at the end of the file name.
2. Commit the file(s) to the [Archive folder]().
3. Publish a release.
3. Create a branch.



##### Add Bill of Materials (?)
