# Eclipse_Derby_WorkspaceDerby-IJ source code modification description:

Modified IJ source code to connect to db automatically with a hard coded connect-string using ij.bat or by running a script myscript.sql with the connect-string in it and then switch to the System.in input to interact with the db through ij cmd prompt using start_ij.bat. All files except for bin.7z and lib.7z belong to the Eclipse workspace. Mouse over bin.7z and lib.7z for more info.

Compiled Environment working out of the box: zip lib folder: Contains the compile Derby Library after the source code was modified and compiled in Eclipse and then the Jars generated through Ant. bin: Contains the modified batch files to just double click and connect to existing derby database: MyDatabase start_derby.bat // starts the Derby database Server ij.bat // connects automatically to MyDatabase using hard coded connection-string in StatementFinder.java and remains in command line to work with the database. start_ij.bat // connects automatically using the connection-string within the file myscript.sql and once connected switches to keyboard input so that you can work with the db through command line. Note 1: if you want to modify the source code then remember to compile it and to generate the Jars using Ant in Sane directory and copy them over the lib folder and then execute the batch from the bin folder and your change should effective. Note 2: Or you can compile clean, compile and generate the Jars using the Ant commands by running them once inside Derby folder in the Eclipse workspace: Note 3: You need to download and install Ant in your computer so that you can run the below command from the file system. Note 4: You need to put in the path Env. variables of your computer the java, ant and derby paths so all this will work

Ant commands to clean > compile > generate Jars in Sane Directory ant -quiet clobber

ant -quiet buildsource // this is equivalent to run the main build.xml through Eclipse/Ant Run As

ant -quiet buildjars

My Path Environment so all these project work compilation, batch running of Ant and ij.bat and start_ij.bat :

ANT_HOME C:\Ant
JAVA_HOME C:\Program Files\Java\jdk1.8.0_121 Path C:\ProgramData\Oracle\Java\javapath;C:\Program Files (x86)\Intel\iCLS Client;C:\Program Files\Intel\iCLS Client;C:\Windows\system32;C:\Windows;C:\Windows\System32\Wbem;C:\Windows\System32\WindowsPowerShell\v1.0;C:\Program Files (x86)\Intel\Intel(R) Management Engine Components\DAL;C:\Program Files\Intel\Intel(R) Management Engine Components\DAL;C:\Program Files (x86)\Intel\Intel(R) Management Engine Components\IPT;C:\Program Files\Intel\Intel(R) Management Engine Components\IPT;C:\Program Files (x86)\NVIDIA Corporation\PhysX\Common;%USERPROFILE%.dnx\bin;C:\Program Files\Microsoft DNX\Dnvm;C:\Program Files\Microsoft SQL Server\130\Tools\Binn;C:\Ant\bin;C:\Program Files\Java\jdk1.8.0_121;C:\Program Files\Git\cmd

Download and Compilation steps:

Clone this repository to your local repository in yout computer computer.
mkdir git_workspace cd git_workspace/ git init git clone https://github.com/cborrero2000/Eclipse_Derby_Workspace.git

Launch Eclipse and set workspace to the folder downloaded from GitHub:
Workspace: C:\Users\cborr\Documents\Programming\git_workspace\Eclipse_Derby_Workspace

Compile from Eclipse by R-Click on build.xml located in the root of Derby project. Select Run As > Ant Build

IDE: eclipse neon.2
