**How git stores data** : 
Git stores object in object database
- Stores in the form of key-values pairs 
- Object Database. values:objects
- Also git used compression library Z-lib for compressing value objects
- to generate key git uses SHA algorithm for compression

**Object Types** :
- Commits
- tree
	- represent a directory and consists a other tree or blob
- blob
	- Blob includes content of the file but not metadata sa filename

**.git** Directory : 
- this is where git stores almost everything 
- object database is stored in .git/object directory
- and contents of each object is stored in a file
- object file is named after its key 
	- c6 12f8a114d02524ea6be35477b3629304aa36f
	- Directory Name                  File Name
	- .git/objects/c6/12f8a114d02524ea6be35477b3629304aa36f this is how git calls the file
	- git cat-file blob 12f8a114d02524ea6be35477b3629304aa36f this will return the file content

**Tree** :
- blob -files 
- tree -folders
- ![[Screenshot 2023-09-22 at 12.09.27 AM.png]]

**Commits** :
- Represent single change 
- Commits are immutable
- ![[Screenshot 2023-09-22 at 12.10.42 AM.png]]

**Branches** : Its a reference to a commit ids 


**git merge** :
moves branch forward

1. Three way merge 

**Rebase** :


**Cherry Picking** :