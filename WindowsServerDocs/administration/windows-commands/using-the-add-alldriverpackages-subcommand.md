---
title: Using the add-AllDriverPackages subcommand
description: "Windows Commands topic for **** - "
ms.custom: na
ms.prod: windows-server-threshold
ms.reviewer: na
ms.suite: na
ms.technology: manage-windows-commands
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ba6641c1-d7e9-43a9-9819-702dad5484ed
author: coreyp-at-msft
ms.author: coreyp
manager: dongill
ms.date: 10/12/2016
---

# Using the add-AllDriverPackages subcommand

> Applies To: Windows Server 2016, Windows Server 2012 R2, Windows Server 2012

Adds all driver packages that are stored in a folder to a server.

## Syntax

```
WDSUTIL /Add-AllDriverPackages /FolderPath:<Folder Path> [/Server:<Server name>] [/Architecture:{x86 | ia64 | x64}] [/DriverGroup:<Group Name>]
```

## Parameters

|Parameter|Description|
|---------|-----------|
|/FolderPath:\<Folder Path>|Specifies the full path to the folder that contains the .inf files for the driver packages.|
|[/Server:\<Server name>]|Specifies the name of the server. This can be the NetBIOS name or the FQDN. If no server name is specified, the local server is used.|
|[/Architecture:{x86 | ia64 | x64}]|Specifies the architecture of the driver packages to add. Driver packages for other architectures are ignored.|
|[/DriverGroup:\<Group Name>]|Specifies the name of the driver group to which the packages should be added.|

## <a name="BKMK_examples"></a>Examples

To add driver packages, type one of the following:
```
WDSUTIL /verbose /Add-AllDriverPackages /FolderPath:"C:\Temp\Drivers" /Architecture:x86
```
```
WDSUTIL /Add-AllDriverPackages /FolderPath:"C:\Temp\Drivers\Printers" /DriverGroup:"Printer Drivers"
```

#### Additional references

[Command-Line Syntax Key](command-line-syntax-key.md)

[Add-WdsDriverPackage](http://technet.microsoft.com/library/dn283440.aspx)