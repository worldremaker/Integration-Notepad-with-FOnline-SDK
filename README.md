# Integration-Notepad-with-FOnline-SDK

Preparing
1. Download and install the latest Notepad++ release from here: https://notepad-plus-plus.org/
2. Download this package: http://files.fonline-aftertimes.net/tools/integration_with_npp.zip
3. Download and unpack to C:\Program Files\Notepad++\ with all subdirectories this package: http://files.fonline-aftertimes.net/tools/PluginManager_v1.4.9_x64.zip

Code marks
1. Unpack fo.xml file to c:\Program Files\Notepad++\plugins\APIs\ directory.
2. Unpack userDefineLang.xml file to C:\Documents and Settings\<UserName>\Application Data\Notepad++ (for Windows XP) or C:\Users\<UserName>\AppData\Roaming\Notepad++ (for Windows Vista or Windows 7).

Running
1. Open any *.fos file by doubleclick.
2. In "Open with..." table select Notepad++.exe (from c:\Program Files\Notepad++\)
3. You should see similar window:


Compilator
1. Unpack ASCompiler.exe file to any place on your hard disk drive (f.ex. D:\ASCompiler\)
2. Run Notepad++, go to menu Plugins -> Plugin Manager -> Show Plugin Manager, find and install NppExec plugin.

3. After install and Notepad++'s restart press F6 button on your keyboard. You should see this small window:

4. Now write there:
Code: [Select]
npp_save
D:\ASCompiler\ASCompiler.exe "$(FULL_CURRENT_PATH)"
5. Click Save... button, name it as CompileServer and click on Save button. You should get this:

6. Do the same for client and mapper script compilations:
Code: [Select]
npp_save
D:\ASCompiler\ASCompiler.exe "$(FULL_CURRENT_PATH)" -client
and save it as CompileClient
Code: [Select]
npp_save
D:\ASCompiler\ASCompiler.exe "$(FULL_CURRENT_PATH)" -mapper
and save it as CompileMapper
7. Test it - open *.fos file, press F6, select proper compile script. In case of error you can click the error line and go to error place in the script.


Configure the compilator's results
1. Press Shift + F6 combination keys to run the NppExec Console Filters window.
2. Configure highlights for:
%FILE%(%LINE%) : INFO*
%FILE%(%LINE%) : ERROR*
%FILE%(%LINE%) : WARNING*
Success*
Unable to build*

3. And now results will be like:

or


Function List
1. Unpack functionList.xml file to C:\Users\<UserName>\AppData\Roaming\Notepad++\ and overwrite (or if you have it customized then merge with) existing one.
Note: My file is already merged with original one from Notepad++ package. If you don't have it customized for your preferences then you don't have to worry about it and just overwrite existing one.
2. Select from menu View -> Function List
3. When you'll open some *.fos file then you'll see.
