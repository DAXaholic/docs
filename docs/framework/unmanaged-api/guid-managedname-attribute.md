---
title: "GUID_ManagedName Attribute | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "reference"
api_name: 
  - "GUID_ManagedName"
api_location: 
  - "alink.dll"
api_type: 
  - "COM"
f1_keywords: 
  - "GUID_ManagedName"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "GUID_ManagedName attribute"
ms.assetid: 11e18095-e444-47bc-aff6-b887ac5dc01e
topic_type: 
  - "apiref"
caps.latest.revision: 6
author: "rpetrusha"
ms.author: "ronpet"
manager: "wpickett"
---
# GUID_ManagedName Attribute
Defines a custom interface attribute that specifies the managed namespace name for a component object model (COM) library.  
  
## Syntax  
  
```  
[  
   custom(GUID_ManagedName, value)  
]  
```  
  
#### Parameters  
 `value`  
 The managed namespace name for the library.  
  
## Definition  
 `GUID_ManagedName` is defined in Cor.h as follows:  
  
```  
// {0F21F359-AB84-41e8-9A78-36D110E6D2F9}  
EXTERN_GUID(GUID_ManagedName, 0xf21f359, 0xab84, 0x41e8, 0x9a, 0x78, 0x36, 0xd1, 0x10, 0xe6, 0xd2, 0xf9);  
```  
  
## Remarks  
 A custom interface attribute defines metadata for an object in the type library.  
  
 Use <xref:System.Runtime.InteropServices.ComTypes.ITypeInfo2.GetCustData%2A?displayProperty=fullName> or <xref:System.Runtime.InteropServices.ComTypes.ITypeLib2.GetCustData%2A?displayProperty=fullName> to retrieve the managed name from the attribute.  
  
 For more information, see [Interface Attributes](http://msdn.microsoft.com/library/27fcdfee-abce-4585-8b53-ee31635356e8) in the Visual C++ reference documentation.  
  
## Example  
 The following example shows a library definition using the `GUID_ManagedName` attribute.  
  
```  
[  
   ...  
   custom(GUID_ManagedName, Microsoft.VisualStudio.CommandBars.dll")  
]  
library Microsoft_VisualStudio_CommandBars  
{  
   ...  
}  
```  
  
## Requirements  
 **Header:** Cor.h