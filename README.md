Juicebox
========

Visualization and analysis software for Hi-C data

MainWindow.java is the main method class for the visualization portion of the software.  
HiCTools is the main method class for the analysis portion.


Setup Instructions
========

[Neva's Email to Ido, Muhammad  10/29/14]

Use IntelliJ IDEA (Community edition - free)

To set up in IDEA, have the Java SDK installed; then you'll point to it (IntelliJ has lots of documentation on this sort of thing).  

* Then go to VCS -> checkout from version control.

The one other thing you'll need to do is be sure *.sizes is included as a file to be copied over to the class files.

* Go to Run -> Edit Configurations.
* Add with `+` sign, Application.
* You'll create two of these, one for the GUI (call it Juicebox GUI or whatever you want, really) and one for the CLT.
* The GUI's main class is `MainWindow` - click the little `...` button next to the text box for main class, and type `MainWindow`, should find it.
* The CLT's main class is `HiCTools`.  
* For the GUI under VM Options: `-Xmx2000m -Djnlp.loadMenu="http://hicfiles.econpy.org/juicebox.properties"`
* For the CLT I use  `-Xmx2000m`

Note that that's 2GB RAM, depending on your computer you might want more or less.  Some CLT things will break if there's not enough memory and the file is too large but don't worry about that for development; I've found 2GB is fine.
