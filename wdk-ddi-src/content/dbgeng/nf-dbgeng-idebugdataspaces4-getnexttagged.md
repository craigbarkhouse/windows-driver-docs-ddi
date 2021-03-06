---
UID: NF:dbgeng.IDebugDataSpaces4.GetNextTagged
title: IDebugDataSpaces4::GetNextTagged
author: windows-driver-content
description: The GetNextTagged method returns the GUID for the next block of tagged data in the enumeration.
old-location: debugger\getnexttagged.htm
tech.root: debugger
ms.assetid: 529ef33a-adad-4242-96a8-01cdd273cc35
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetNextTagged, GetNextTagged method [Windows Debugging], GetNextTagged method [Windows Debugging],IDebugDataSpaces3 interface, GetNextTagged method [Windows Debugging],IDebugDataSpaces4 interface, IDebugDataSpaces3 interface [Windows Debugging],GetNextTagged method, IDebugDataSpaces3::GetNextTagged, IDebugDataSpaces4 interface [Windows Debugging],GetNextTagged method, IDebugDataSpaces4.GetNextTagged, IDebugDataSpaces4::GetNextTagged, IDebugDataSpaces_24254a63-1fcd-4ad9-a370-6b0760ed37cd.xml, dbgeng/IDebugDataSpaces3::GetNextTagged, dbgeng/IDebugDataSpaces4::GetNextTagged, debugger.getnexttagged
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
-	COM
api_location:
-	dbgeng.h
api_name:
-	IDebugDataSpaces3.GetNextTagged
-	IDebugDataSpaces4.GetNextTagged
product:
- Windows
targetos: Windows
req.typenames: 
---

# IDebugDataSpaces4::GetNextTagged


## -description


The <b>GetNextTagged</b> method returns the GUID for the next block of tagged data in the enumeration.


## -parameters




### -param Handle [in]

Specifies the handle identifying the enumeration.  This is the handle returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff558801">StartEnumTagged</a>.


### -param Tag [out]

Receives the GUID identifying the tagged data.  The data may be retrieved by passing this GUID to <a href="https://msdn.microsoft.com/library/windows/hardware/ff554336">ReadTagged</a>.


### -param Size [out]

Receives the size of the data identified by the GUID <i>Tag</i>.


## -returns



This method can also return error values.  See <a href="https://msdn.microsoft.com/713f3ee2-2f5b-415e-9908-90f5ae428b43">Return Values</a> for more details.

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
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There are no more blocks of tagged data available in this enumeration.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550537">IDebugDataSpaces3</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff550546">IDebugDataSpaces4</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff554336">ReadTagged</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff558801">StartEnumTagged</a>
 

 

