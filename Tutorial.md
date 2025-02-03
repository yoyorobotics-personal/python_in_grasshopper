# How to use python in grasshopper (rhino version 7 and 8 in windows)  
There are generally 3 ways of using full python tools in grasshopper (rhino)  
## 1. gh_cpython (open sourced, no longer maintained, ok for starters)
Food4rhino: https://www.food4rhino.com/en/app/ghcpython  
Github: https://github.com/MahmoudAbdelRahman/GH_CPython  
Advantages: use any version of python existing on your computer, working exactly the same as coding in any other IDE  
Caution: **OPEN RHINO AS ADMINISTRATOR!!!**  
Tutorial:
1. download python from `https://www.python.org/downloads/`
2. find the path where python locates by:
   1. type `cmd` in your research bar, the one at the bottom of your entire screen, next to your windows icon  
   2. at the newly opened black window, type `where python`, the path of python will show as:  
      `C:\Users\<Username>\AppData\Local\Programs\Python\<PythonVersion>\python.exe`  
      TERMS IN <> ARE TO REPLACED ACCORDING TO YOUR WINDOW
   3. copy this path to a notepad or somewhere you like
3. set rhino and grasshopper:
   1. open rhino as ADMINISTRATOR by right clicking and choosing `Run as an administrator`
   2. open grasshopper by typing grasshopper in the command bar in rhino
   3. on grasshopper canvas, double click with a search bar poping up, type "cpython", and click on the cpython bar
   4. the cpython component should be there on your grasshopper canvas
   5. left click on the blue bar at the bottom of cpython component
   6. the locatePython window pops up and left click `Browse`
   7. paste the path you copied at step 2:
       `C:\Users\<Username>\AppData\Local\Programs\Python\<PythonVersion>\python.exe`
       or paste the parents excluding `python.exe`:  
       `C:\Users\<Username>\AppData\Local\Programs\Python\<PythonVersion>`and choose `python.exe` in the folder
   8. click `Apply`
4. now that the GH_CPython component should work. lets do some tests:  
   1. run some simple python script (You can do it by yourself)
   2. show input and output in grasshopper and link this component to others (You can do it by yourself)
   3. install a external library and run it in grasshopper:
      1. 
