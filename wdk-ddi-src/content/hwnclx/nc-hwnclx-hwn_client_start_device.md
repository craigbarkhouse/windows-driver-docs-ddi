---
UID: NC:hwnclx.HWN_CLIENT_START_DEVICE
title: HWN_CLIENT_START_DEVICE
author: windows-driver-content
description: Implemented by the client driver to start the hardware notification component. It is invoked as a result of a call to EVT_WDF_DEVICE_D0_ENTRY.
old-location: gpiobtn\hwn_client_start_device.htm
tech.root: gpiobtn
ms.assetid: 79ad880a-74a2-48e8-b16b-0d488003889f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PHWN_CLIENT_START_DEVICE, *PHWN_CLIENT_START_DEVICE callback function pointer, HWN_CLIENT_START_DEVICE, HwnClientStartDevice, HwnClientStartDevice callback function, gpiobtn.hwn_client_start_device, hwnclx/HwnClientStartDevice"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: hwnclx.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709
req.target-min-winversvr: Windows Server 2016
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
req.irql: PASSIVE_LEVEL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Hwnclx.h
api_name:
-	*PHWN_CLIENT_START_DEVICE
product:
- Windows
targetos: Windows
req.typenames: HPMI_QUERY_CAPABILITIES_RESPONSE, *PHPMI_QUERY_CAPABILITIES_RESPONSE
---

# HWN_CLIENT_START_DEVICE callback


## -description



Implemented by the client driver to start the hardware notification component. It is invoked as a result of a call to <a href="..\wdfdevice\nc-wdfdevice-evt_wdf_device_d0_entry.md">EVT_WDF_DEVICE_D0_ENTRY</a>.


## -prototype


````
HWN_CLIENT_START_DEVICE HwnClientStartDevice;

NTSTATUS HwnClientStartDevice(
  _In_ PVOID Context
)
{ ... }

typedef HWN_CLIENT_START_DEVICE *PHWN_CLIENT_START_DEVICE;
````


## -parameters




### -param Context [in]

Pointer to the client driver's context information. This memory space is available for use by the client driver. It is allocated as part of the framework object context space by <a href="..\wdfdevice\nf-wdfdevice-wdfdevicecreate.md">WdfDeviceCreate</a>. For more information, see <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/gpiobtn/create-a-hardware-notification-client-driver">HWN_CLIENT_REGISTRATION_PACKET</a> and <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/wdf/framework-object-context-space">Framework Object Context Space</a>.


## -returns




Return STATUS_SUCCESS if the operation succeeds. Otherwise, return an appropriate <a href="https://msdn.microsoft.com/7792201b-63bb-4db5-803d-2af02893d505">NTSTATUS</a> error code.




## -remarks



Register your implementation of this callback function by setting the appropriate member of <a href="https://docs.microsoft.com/en-us/windows-hardware/drivers/gpiobtn/create-a-hardware-notification-client-driver">HWN_CLIENT_REGISTRATION_PACKET</a> and then calling <a href="..\hwnclx\nf-hwnclx-hwnregisterclient.md">HwNRegisterClient</a>.




## -see-also

<a href="https://msdn.microsoft.com/en-us/library/windows/hardware/dn789335">Hardware notifications support</a>



<a href="https://msdn.microsoft.com/405ff6db-9bc0-42f3-a740-49dd3967a8b3">Hardware notifications reference</a>



 

 


