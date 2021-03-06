---
UID: NF:dbgeng.DebugCreate
title: DebugCreate function
author: windows-driver-content
description: The DebugCreate function creates a new client object and returns an interface pointer to it.
old-location: debugger\debugcreate.htm
tech.root: debugger
ms.assetid: 9dd3632c-4c88-470d-8419-10959eda0454
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: ClientFns_4a96fd16-32b9-40f5-bc7f-60ae6ecadb32.xml, DebugCreate, DebugCreate function [Windows Debugging], dbgeng/DebugCreate, debugger.debugcreate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dbgeng.h
req.include-header: Dbgeng.h
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	dbgeng.dll
api_name:
-	DebugCreate
product:
- Windows
targetos: Windows
req.typenames: 
---

# DebugCreate function


## -description


The <b>DebugCreate</b> function creates a new client object and returns an interface pointer to it.


## -parameters




### -param InterfaceId [in]

Specifies the interface identifier (IID) of the desired debugger engine client interface.  This is the type of the interface that will be returned in <i>Interface</i>. For information about the interface identifier, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff560088">Using Client Objects</a>.


### -param Interface [out]

Receives an interface pointer for the new client.  The type of this interface is specified by <i>InterfaceId</i>.


## -returns



This method may also return other error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE </b></dt>
</dl>
</td>
<td width="60%">
The client object doesn't implement the specified interface.

</td>
</tr>
</table>
 




## -remarks



The parameters passed to <b>DebugCreate</b> are the same as those passed to <b>IUnknown::QueryInterface</b>, and they are treated the same way.

As with <b>IUnknown::QueryInterface</b>, when the returned interface is no longer needed, its <b>IUnknown::Release</b> method should be called.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539140">Client Objects</a>
 

 

