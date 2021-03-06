---
UID: NF:portabledevicetypes.IPortableDeviceValues.SetErrorValue
title: IPortableDeviceValues::SetErrorValue
author: windows-driver-content
description: Adds a new HRESULT value (type VT_ERROR) or overwrites an existing one.
old-location: wpddk\iportabledevicevalues_seterrorvalue.htm
tech.root: wpd_dk
ms.assetid: 58e21e7c-bb66-4088-b011-a2e3df28944c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IPortableDeviceValues interface,SetErrorValue method, IPortableDeviceValues.SetErrorValue, IPortableDeviceValues::SetErrorValue, IPortableDeviceValuesSetErrorValue, SetErrorValue, SetErrorValue method, SetErrorValue method,IPortableDeviceValues interface, portabledevicetypes/IPortableDeviceValues::SetErrorValue, wpddk.iportabledevicevalues_seterrorvalue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portabledevicetypes.h
req.include-header: 
req.target-type: Windows
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
-	PortableDeviceTypes.h
api_name:
-	IPortableDeviceValues.SetErrorValue
product:
-	Windows
targetos: Windows
req.typenames: 
---

# IPortableDeviceValues::SetErrorValue


## -description



Adds a new <b>HRESULT</b> value (type VT_ERROR) or overwrites an existing one.




## -parameters




### -param key [in]

A <b>REFPROPERTYKEY</b> that specifies the item to create or overwrite.


### -param Value [in]

An <b>HRESULT</b> that contains the new value.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



If an existing value has the same key specified by the <i>key</i> parameter, it overwrites the existing value without any warning.




## -see-also




<a href="https://msdn.microsoft.com/4a97301a-12cc-442f-a080-446ec9e1e245">IPortableDeviceValues Interface</a>



<a href="https://msdn.microsoft.com/6e5a0d31-3a89-4188-bf5f-6c7636c7106f">IPortableDeviceValues::GetErrorValue</a>
 

 

