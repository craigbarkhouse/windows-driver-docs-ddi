---
UID: NC:d3d12umddi.PFND3D12DDI_DESTROY_COMMAND_RECORDER_0040
title: PFND3D12DDI_DESTROY_COMMAND_RECORDER_0040
author: windows-driver-content
description:
ms.assetid: 361f2b22-ea1e-4535-a0e7-302dab683485
ms.author: windowsdriverdev
ms.date:
ms.topic: callback
ms.prod: windows-hardware
ms.technology: windows-devices
req.header: d3d12umddi.h
req.include-header:
req.target-type:
req.target-min-winverclnt:
req.target-min-winversvr:
req.kmdf-ver:
req.umdf-ver:
req.lib:
req.dll:
req.irql:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
topictype:
-	apiref
apitype:
-	UserDefined
apilocation:
-	d3d12umddi.h
apiname:
-	PFND3D12DDI_DESTROY_COMMAND_RECORDER_0040
product: 
- Windows
targetos: Windows
---

# PFND3D12DDI_DESTROY_COMMAND_RECORDER_0040 callback function

## -description

Implemented by the client driver to clean up command recorder resources.

## -prototype

```
//Declaration

PFND3D12DDI_DESTROY_COMMAND_RECORDER_0040 Pfnd3d12ddiDestroyCommandRecorder0040;

// Definition

VOID Pfnd3d12ddiDestroyCommandRecorder0040
(
	 D3D12DDI_HDEVICE
	 D3D12DDI_HCOMMANDRECORDER_0040
)
{...}

PFND3D12DDI_DESTROY_COMMAND_RECORDER_0040


```

## -parameters

### -param D3D12DDI_HDEVICE

A handle to the display device (graphics context).

### -param D3D12DDI_HCOMMANDRECORDER_0040:

A handle to the command recorder.

## -returns

This callback function does not return a value.



## -see-also