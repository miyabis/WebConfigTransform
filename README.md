# WebConfigTransform


[![Build status](https://ci.appveyor.com/api/projects/status/w4061acgsjxf4p1u?svg=true)](https://ci.appveyor.com/project/miyabis/webconfigtransform)
[![NuGet](https://img.shields.io/nuget/v/MiYABiS.WebConfigTransform.svg)](https://www.nuget.org/packages/MiYABiS.WebConfigTransform/)

Web.Config and log4net.config Transform.  
In advance, Web.Debug.config, Web.Main.config, Web.Hotfix.config, Web.Release.config, 
log4net.Debug.config, log4net.Main.config, log4net.Hotfix.config, log4net.Release.config is available.  
log4net.config file will be included in the Web site publish.


How to get
==========

URL:https://www.nuget.org/packages/MiYABiS.WebConfigTransform/
```
PM> Install-Package MiYABiS.WebConfigTransform
```


log4net.config setting
==========

When you use , please install the log4net from nuget.  

C#:Properties\WebConfigTransformAssemblyInfo.cs file Please cancel comment.
```
[assembly: log4net.Config.XmlConfigurator(ConfigFile=@"log4net.config", Watch=true)]
```

VB:My Project\WebConfigTransformAssemblyInfo.vb file Please cancel comment.
```
<Assembly: log4net.Config.XmlConfigurator(ConfigFile:="log4net.config", Watch:=True)> 
```


Web.config Section Protection setting
==========

When you use , please install the Moca.NETConfiguration from nuget.  

C#:add Assembly property.
```
[assembly: Moca.Configuration.SectionProtection(Moca.Configuration.ProtectionProviderType.DPAPI, "Section Name")]
```

VB:add Assembly property.
```
<Assembly: Moca.Configuration.SectionProtection(Moca.Configuration.ProtectionProviderType.DPAPI, "Section Name")> 
```

Protection Provider Type DPAPI or RSA.

Program Startup execute method.
```
Moca.Configuration.SectionProtector.Protect()
```


License
=======

Microsoft Public License (MS-PL)

http://opensource.org/licenses/MS-PL
