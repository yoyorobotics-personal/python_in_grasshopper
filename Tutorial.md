# How to use python in grasshopper (rhino version 7 and 8 in windows)  
There are many ways of using full python tools in grasshopper (rhino). gh_cpython is no longer widely used, but I still want to introduce it first. Because I think it is more useful than the Python 3 that comes with Rhino 8. GH Python Remote is also good, but considering that people always start with legacy code, I believe quickly getting familiar with gh_cpython is the first step for beginners to smoothly progress.
## gh_cpython (open sourced, no longer maintained, ok for starters)
### ⚡Caution: You can also open python files with cpython, it works the same with vscode or other IDEs, but I recommend to code in typical IDEs than in grasshopper or cpython
Food4rhino: https://www.food4rhino.com/en/app/ghcpython  
Github: https://github.com/MahmoudAbdelRahman/GH_CPython  
Advantages: use any version of python existing on your computer, working exactly the same as coding in any other IDE  
### ⚡Caution: **OPEN RHINO AS ADMINISTRATOR!!!**  
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
   3. install an external library and run it in grasshopper:
      1. type `cmd` in your research bar or your can use IDE terminal if you like
      2. type `pip install <package_name>`, with the internet, it should download the package for you, remember to replace `<package_name>`with the package you need  
         here, i want to mention that if you have mutiple python versions on your computer or you are working with anaconda, please check whether you are installing package with the correct python version, same as the path to the cpython python interpreter.
      4. go back to rhino, grasshopper and cpython, it should work now. REMEMBER TO **OPEN RHINO AS ADMINISTRATOR!!!**
      5. here is an example of using numpy with cpython in grasshopper:
      ![image](https://github.com/user-attachments/assets/f41026f6-d778-4f89-9e93-5267686d6612)  
      1. get python path  
      ![Screenshot 2025-02-03 150339](https://github.com/user-attachments/assets/d259c688-88cd-41e1-b490-139d650b2b61)  
      2. OPEN RHINO AS ADMINISTRATOR
      ![Screenshot 2025-02-03 153329](https://github.com/user-attachments/assets/f62f371f-823b-4409-af91-86e3fe27d324)  
      3. set cpython python interpreter path
      ![Screenshot 2025-02-03 151025](https://github.com/user-attachments/assets/6871cdf3-850f-476d-82d2-09cb27379547)
      4. install numpy
      ![image](https://github.com/user-attachments/assets/135b29e2-84e2-498f-9e85-9a59a59c3dd6)
      5. it should work well
## You can also open python files with cpython, it works the same with vscode or other IDEs, but I recommend to code in typical IDEs than in grasshopper or cpython





      
