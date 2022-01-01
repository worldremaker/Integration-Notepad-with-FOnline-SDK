# Integration Notepad with FOnline: Aftertimes S3 and FOnline: Reloaded S4 SDKs

### Important!
From 3rd revision it's related to FOnline: Aftertimes S3 only! 
From 24th revision it's also related to FOnline: Reloaded S4 (WIP)! 
 
## Preparing
1. Download and install the latest Notepad++ release from here: https://notepad-plus-plus.org/ 
2. Download this package: http://files.fonline-aftertimes.net/tools/integration_with_npp.zip (or use files from this reposiory). 
3. Download and unpack to `C:\Program Files\Notepad++\` with all subdirectories this package: http://files.fonline-aftertimes.net/tools/PluginManager_v1.4.9_x64.zip 
 
## Code marks
1. Unpack `foat.xml` and `forld.xml` files to `C:\Program Files\Notepad++\autoCompletion\` directory. 
2. Unpack `userDefineLang.xml` file to `C:\Documents and Settings\<UserName>\Application Data\Notepad++` (for Windows XP) or `C:\Users\<UserName>\AppData\Roaming\Notepad++` (for Windows Vista or Windows 7). 
 
## Running
1. Open any `*.fos` or `*.fosp` file by doubleclick. 
2. In "Open with..." table select `Notepad++.exe` (from `C:\Program Files\Notepad++\`) 
3. You should see similar window: 
![Coloured lines](https://img.fonline-aftertimes.net/closedbeta/integration_with_npp/npp01.png) 
4. Choose your User Defined Language from here: 
![UDL Chosing](https://img.fonline-aftertimes.net/closedbeta/integration_with_npp/npp01a.png) 
 
## Compilator
Here you have two different compilators for two different SDKs. You can't use Reloaded's compilator as replacement for Aftertimes and vice-versa but you always can configure them both, f.ex. by placing these in two different directories. 
 
1. Unpack ASCompiler.exe file to any place on your hard disk drive (f.ex. `D:\ASCompiler\`) 
2. Run Notepad++, go to menu Plugins -> Plugin Manager -> Show Plugin Manager, find and install NppExec plugin. 
![Plugin Manager](https://img.fonline-aftertimes.net/closedbeta/integration_with_npp/npp02.png) 
3. After install and Notepad++'s restart press F6 button on your keyboard. You should see this small window: 
![Executing window](https://img.fonline-aftertimes.net/closedbeta/integration_with_npp/npp03.png) 
4. Now write there: 
```
npp_save
D:\ASCompiler\ASCompiler.exe "$(FULL_CURRENT_PATH)"
```
5. Click Save... button, name it as CompileServer and click on Save button. You should get this: 
![Executing window](https://img.fonline-aftertimes.net/closedbeta/integration_with_npp/npp04.png) 
6. Do the same for client and mapper script compilations: 
```
npp_save
D:\ASCompiler\ASCompiler.exe "$(FULL_CURRENT_PATH)" -client
```
and save it as CompileClient 
```
npp_save
D:\ASCompiler\ASCompiler.exe "$(FULL_CURRENT_PATH)" -mapper
```
and save it as CompileMapper 
7. Test it - open `*.fos` file, press F6, select proper compile script. In case of error you can click the error line and go to error place in the script. 
![Results](https://img.fonline-aftertimes.net/closedbeta/integration_with_npp/npp05.png) 
 
## Configure the compilator's results
1. Press Shift + F6 combination keys to run the NppExec Console Filters window. 
2. Configure highlights for: 
```
%FILE%(%LINE%) : INFO*
```
```
%FILE%(%LINE%) : ERROR*
```
```
%FILE%(%LINE%) : WARNING*
```
```
Success*
```
```
Unable to build*
```
![NppExec Console Filters](https://img.fonline-aftertimes.net/closedbeta/integration_with_npp/npp06.png) 

3. And now results will be like: 
![Success results](https://img.fonline-aftertimes.net/closedbeta/integration_with_npp/npp07.png) 

or 
![Failure results](https://img.fonline-aftertimes.net/closedbeta/integration_with_npp/npp08.png) 

## Function List
1. Unpack functionList.xml file to `C:\Users\<UserName>\AppData\Roaming\Notepad++\` and overwrite (or if you have it customized then merge with) existing one. 
Note: My file is already merged with original one from Notepad++ package. If you don't have it customized for your preferences then you don't have to worry about it and just overwrite existing one. 
2. Select from menu View -> Function List 
3. When you'll open some `*.fos` or `*.fosp` file then you'll see. 
![Function list](https://img.fonline-aftertimes.net/closedbeta/integration_with_npp/npp09.png) 
