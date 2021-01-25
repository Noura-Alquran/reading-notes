# Reading 02b summary
## Git Tutorial
 In order to explain Git, we have to first explain various aspects of ***Version Control***.
 ### Version Control
Version Control is a system that allows you to revisit various versions of a file or set of files by recording changes.
Through version control, one can
+ revert a file or project to a previous version
+ track modifications and modifying individuals 
+ compare changes. 
> By utilizing a Version Control System (VCS), mistakes with files can easily be rectified.

#### 1. Local Version Control
#### 2. Centralized Version Control
  ![Centralized Version Control](https://i0.wp.com/homes.cs.washington.edu/~mernst/advice/version-control-fig2.png?zoom=2)
#### 3. Distributed Version Control
![Distributed Version Control](https://i1.wp.com/homes.cs.washington.edu/~mernst/advice/version-control-fig3.png?zoom=2)
### Git
**is a DVCS that stores data in a file system made up of snapshots. Each time you save a changed version of your project — called commit — Git creates a snapshot of the file and stores a reference to it. If the file has not changed, Git only stores a reference to the already-stored identical version of it**.
  1. Relies on local operations because most necessary information can be found in local resources. 

  2. Detect file corruption or loss of information in transit.

  3. Minimize the possibility of irreversible damage to files.

 ##### States
  ![states](https://1.bp.blogspot.com/-CtkCo1YBqXw/XS34ZPnXLfI/AAAAAAAANXI/3B6VsP-YlbQdYJrulJAZWvHVhQOMIkNAQCLcBGAs/s400/git%2Bstates.png)
