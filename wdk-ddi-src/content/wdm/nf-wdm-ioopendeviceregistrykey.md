---
UID: NF:wdm.IoOpenDeviceRegistryKey
title: IoOpenDeviceRegistryKey function
author: windows-driver-content
description: The IoOpenDeviceRegistryKey routine returns a handle to a device-specific or a driver-specific registry key for a particular device instance.
old-location: kernel\ioopendeviceregistrykey.htm
tech.root: kernel
ms.assetid: c3b67c73-446b-42a8-bc41-2ca42fde3513
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IoOpenDeviceRegistryKey, IoOpenDeviceRegistryKey routine [Kernel-Mode Driver Architecture], k104_7b6ab819-56e3-4d4a-956a-51e4a83300f0.xml, kernel.ioopendeviceregistrykey, wdm/IoOpenDeviceRegistryKey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdm.h
req.include-header: Wdm.h, Ntddk.h, Ntifs.h
req.target-type: Universal
req.target-min-winverclnt: Available starting with Windows 2000.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: PowerIrpDDis, HwStorPortProhibitedDDIs
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NtosKrnl.lib
req.dll: NtosKrnl.exe
req.irql: PASSIVE_LEVEL (see Remarks section)
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	NtosKrnl.exe
api_name:
-	IoOpenDeviceRegistryKey
product:
- Windows
targetos: Windows
req.typenames: 
---

# IoOpenDeviceRegistryKey function


## -description


The <b>IoOpenDeviceRegistryKey</b> routine returns a handle to a device-specific or a driver-specific registry key for a particular device instance. 


## -parameters




### -param DeviceObject [in]

Pointer to the PDO of the device instance for which the registry key is to be opened.


### -param DevInstKeyType [in]

Specifies flags indicating whether to open a device-specific hardware key or a driver-specific software key. The flags also indicate whether the key is relative to the current hardware profile. For more information about hardware and software keys, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/overview-of-registry-trees-and-keys">Registry Keys for Drivers</a>.

The flags are defined as follows:





#### PLUGPLAY_REGKEY_DEVICE

Open the <b>Device Parameters</b> subkey under the device's <a href="https://msdn.microsoft.com/3be5c842-d1b6-4c34-8990-e23e2d08dd23">hardware key</a>. The key is located under the key for the device instance specified by <i>DeviceObject</i>. This flag cannot be specified with PLUGPLAY_REGKEY_DRIVER.



#### PLUGPLAY_REGKEY_DRIVER

Open a <a href="https://msdn.microsoft.com/5f6fec1a-1134-4765-81be-9b50939e5e66">software key</a> for storing driver-specific information. This flag cannot be specified with PLUGPLAY_REGKEY_DEVICE.



#### PLUGPLAY_REGKEY_CURRENT_HWPROFILE

Open a key relative to the current hardware profile for device or driver information. This allows the driver to access configuration information that is hardware-profile-specific. The caller must specify either PLUGPLAY_REGKEY_DEVICE or PLUGPLAY_REGKEY_DRIVER with this flag. 


### -param DesiredAccess [in]

Specifies the <a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a> value that represents the access the caller needs to the key. See the <a href="https://msdn.microsoft.com/library/windows/hardware/ff566425">ZwCreateKey</a> routine for a description of each KEY_<i>XXX</i> access right.


### -param DeviceRegKey [out]

Pointer to a caller-allocated buffer that, on successful return, contains a handle to the requested registry key. 


## -returns



<b>IoOpenDeviceRegistryKey</b> returns STATUS_SUCCESS if the call was successful. Possible error return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Possibly indicates that the caller specified an illegal set of <i>DevInstKeyType</i> flags.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_DEVICE_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
Possibly indicates that the <i>DeviceObject</i> is not a valid PDO.

</td>
</tr>
</table>
 




## -remarks



The driver must call <a href="https://msdn.microsoft.com/library/windows/hardware/ff566417">ZwClose</a> to close the handle returned from this routine when access is no longer required.

The registry keys opened by this routine are nonvolatile.

User-mode setup applications, such as <a href="https://msdn.microsoft.com/ac439eb8-b491-4215-877d-5ee177fbdb39">class installers</a>, can access these registry keys using <a href="https://msdn.microsoft.com/library/windows/hardware/ff541299">device installation functions</a> such as <a href="https://msdn.microsoft.com/library/windows/hardware/ff552079">SetupDiOpenDevRegKey</a>.

To create registry keys, use <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/install/inf-addreg-directive">INF AddReg directives</a> in an INF file or use <a href="https://msdn.microsoft.com/library/windows/hardware/ff550973">SetupDiCreateDevRegKey</a> in a setup application.

Callers of <b>IoOpenDeviceRegistryKey</b> must be running at IRQL = PASSIVE_LEVEL in the context of a system thread. 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff540466">ACCESS_MASK</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff566417">ZwClose</a>
 

 

