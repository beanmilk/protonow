protoNow
---------------------

# How to build?
* Visual Studio 2015 or newer    

* Window 7 or newer     

* Microsoft .NET Framework 4.5 & Microsoft .NET Framework 3.5 .  Library SharpVectors(for SVG) work on .NET 3.5, you can target to .NET 4.5, the solution will build successfully, but SVG will work abnormal(SVG mainly used in protoNow application -> Libraries -> Icon ).   

* Visual Studio will restore NuGet packages automatically，if it failed, please reinstall it manually from: Tools > NuGet Package Manager > Package Manager Console    

# How to make package?
There are two ways.
* 1)Run autobuild.cmd under root path , you will get a package named "ProtoNow1.9.3-Setup.exe" under "Install" folder.( No need to install Visual Studio and NSIS)

* 2)We use NSIS to make package, if you want to compile NSIS Script yourself, please following this:
1. Install latest NSIS, and build solution in release mode using Visual studio.
2. Copy these files to the same path of your NSIS install folder(eg: C:\Program Files (x86)\NSIS).  
   Tools\NSIS\Include\FileAssociation.nsh  
   Tools\NSIS\Include\nsProcess.nsh    
   Tools\NSIS\Plugins\x86-ansi\nsProcess.dll   
   Tools\NSIS\Plugins\x86-unicode\nsProcess.dll   
 3. Run Install\protoNow.nsi   
 
 # Third party libraries
 * SharpVectors : used to dispay and edit SVG.    
  https://sharpvectors.codeplex.com/   
  Dlls：   
  SharpVectors.Converters.dll       
  SharpVectors.Core.dll       
  SharpVectors.Css.dll     
  SharpVectors.Dom.dll    
  SharpVectors.Model.dll    
  SharpVectors.Rendering.Wpf.dll    
  SharpVectors.Runtime.dll       
  

 * AvalonDock : layout of UI.   
  https://avalondock.codeplex.com/    
 Dlls:    
 Xceed.Wpf.AvalonDock.dll    
 Xceed.Wpf.AvalonDock.Themes.Aero.dll       
 
  
 * RibbonControlsLibrary : part of toolbar.       
 https://msdn.microsoft.com/en-us/library/ff799534.aspx   
 Dll:   
 RibbonControlsLibrary.dll   
 
 * Nlog   
  http://nlog-project.org/    
 Dll:   
 NLog.dll    
