Command line utility for formatting the C/C++ code using Eclipse's code style.
==================================

This utility is designed to format the C/C++ source code using the formatting tool built into the Eclipse CDT (CCodeFormatter).


How to use?
-----------------------------------------------------------------------------------------------
just run command with a list of files or dir names, see examples:

    cppformat file.c
    cppformat dir_name

Where to get the config file org.eclipse.cdt.core.prefs?
-----------------------------------------------------------------------------------------------
Generating a config file for the formatter utility involves
modifying the code formatter settings for a C/C++ project and
copying org.eclipse.cdt.core.prefs out of the .settings directory for that project.

- Select a C/C++ project, open the pop-up menu and choose Properties.
- Select the "C/C++ General" > "Code Style" page and check "Enable project specific settings".
- Select or edit a profile.
- Click OK when you are done.
- Use either a file manager or the command line
to copy workspace/YourProject/.settings/org.eclipse.cdt.core.prefs to a new location.

OPTIONS:
-----------------------------------------------------------------------------------------------
- -help                Display help message.
- -quiet               Only print error messages.
- -verbose             Be verbose about the formatting job.


How to build?
-----------------------------------------------------------------------------------------------
1. Download and install "Eclipse IDE for Java Developers"
2. Download source code of Eclipse CDT 8.2.0 from [http://git.eclipse.org/c/cdt/org.eclipse.cdt.git/](http://git.eclipse.org/c/cdt/org.eclipse.cdt.git/)
3. Copy source code of EclipseCCodeFormatter to appropriate directory (or perform Import in Eclipse Project Explorer).
4. In Eclipse Project Explorer select org.eclipse.cdt.core -> utils -> org.eclipse.cdt.utils.CCodeFormatter
5. Perform Export: Java -> Runnable JAR file.
