# 怎么在grasshopper里正常用python，题主测试了rhino7和8
见仁见智，gh_cpython已经不再维护了，但是可爱萌新拿到祖传代码之后还是希望先用cpython跑起来，所以题主写了这个教程。题主没有尝试过`GH Python Remote`，但是gh python remote与python3 不兼容，让题主感到疑惑。最新的rhino8支持python3.9，上手快,可以试试。
## gh_cpython (开源，不再维护，新手友好)
### ⚡提个醒: 虽然cpython跑起来没什么问题，但是正经编程请用正常的IDE，比如vscode，虽然也是大玩具，但是好用多了
Food4rhino: https://www.food4rhino.com/en/app/ghcpython  
Github: https://github.com/MahmoudAbdelRahman/GH_CPython  
gh_cpython的优点: 不局限于python的版本，准确说，你电脑上装的哪个就能用哪个，rhino8自带的3.9真的太落伍了 
### ⚡重要提醒: **打开rhino的时候请使用管理员模式!!!**  
逐步教程，图片分步教程在后面，题主推荐先看下字，不过如果你很急，那也可以先看图:
1. 从官网下载python `https://www.python.org/downloads/`
2. 通过以下方式找到 Python 所在的路径：
   1. 在屏幕底部的搜索栏中输入 `cmd`，该栏位于 Windows 图标旁边
   2. 在新打开的黑色窗口中输入 `where python`，Python 的路径将显示为：  
      `C:\Users\<用户名>\AppData\Local\Programs\Python\<Python版本>\python.exe`  
      <> 中的用户名和版本需要根据您的 Windows 替换
      如果你用的是anaconda，请打开anaconda prompt，然后建立一个虚拟环境，然后找python的路径（python3.9是一个例子， 你想用啥版本都行）：
      ```bash
      conda create --name myenv python=3.9 
      conda activate myenv
      where python    
   3. 将这个路径复制到记事本或其他你爱咋咋
3. 设置 Rhino 和 Grasshopper：
   1. 通过右键单击并选择“以管理员身份运行”打开 Rhino
   2. 在 Rhino 的命令栏中输入 `grasshopper` 打开 Grasshopper
   3. 在 Grasshopper 画布上，双击会弹出搜索栏，输入 "cpython"，并点击 cpython 栏
   4. cpython 组件应该会出现在 Grasshopper 画布上
   5. 左键单击 cpython 组件底部的蓝色栏
   6. 会弹出 locatePython 窗口，左键单击 `Browse`
   7. 粘贴您在步骤 2 中复制的路径：
       `C:\Users\<用户名>\AppData\Local\Programs\Python\<Python版本>\python.exe`
       或者粘贴除 `python.exe` 以外的父目录：
       `C:\Users\<用户名>\AppData\Local\Programs\Python\<Python版本>` 然后在文件夹中选择 `python.exe`
   8. 点击 `Apply`
4. 现在 GH_CPython 组件应该可以正常工作。让我们进行一些测试：
   1. 运行一个简单的 Python 脚本（你自己来）
   2. 在 Grasshopper 中显示输入和输出，并将此组件与其他组件链接（你自己来）
   3. 安装一个外部库并在 Grasshopper 中运行：
      1. 在搜索栏中输入 `cmd`，或者你也可以使用 IDE 终端，如果你喜欢的话
      2. 输入 `pip install <package_name>`，如果有互联网连接，它将为你下载该包，记得将 `<package_name>` 替换为你需要的包
      3. 如果你用的是anaconda， 其实不需要安装numpy，因为这是它自带的，不过你也有可能想安装其他的包，可以打开anaconda prompt，然后：
         ```bash
         conda activate myenv
         conda install <package_name>  
      在这里，我想提一下，如果你的电脑上有多个 Python 版本，或者你正在使用 Anaconda，请检查你是否正在用正确的 Python 版本安装包，确保路径和 cpython Python 解释器一致  
      4. 返回 Rhino、Grasshopper 和 cpython，它现在应该可以正常工作。记住**以管理员身份打开 Rhino!!!**  
      5. 这是在 Grasshopper 中使用 numpy 与 cpython 的示例：
      ![image](https://github.com/user-attachments/assets/f41026f6-d778-4f89-9e93-5267686d6612)  
      1. 找到python的下载路径  
      ![Screenshot 2025-02-03 150339](https://github.com/user-attachments/assets/d259c688-88cd-41e1-b490-139d650b2b61)  
      2. 管理员身份运行rhino
      ![Screenshot 2025-02-03 153329](https://github.com/user-attachments/assets/f62f371f-823b-4409-af91-86e3fe27d324)  
      3. 设置 cpython的python interpreter
      ![Screenshot 2025-02-03 151025](https://github.com/user-attachments/assets/6871cdf3-850f-476d-82d2-09cb27379547)
      4. 安装 numpy
      ![image](https://github.com/user-attachments/assets/135b29e2-84e2-498f-9e85-9a59a59c3dd6)
      5. 应该没问题了，如果还有问题，请给题主发邮件，或者移步其他平台
### ⚡提个醒: 虽然cpython跑起来没什么问题，但是正经编程请用正常的IDE，比如vscode，虽然也是大玩具，但是好用多了
### ⚡这个教程还有个英文版本，不明白中文的盆友可以去看英文的，毕竟grasshopper自身是英文的，可能更好理解一丢





      
