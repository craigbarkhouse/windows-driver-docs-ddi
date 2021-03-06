---
UID: NS:d3dkmthk._D3DKMT_CREATESWAPCHAIN
title: _D3DKMT_CREATESWAPCHAIN
author: windows-driver-content
description:
ms.assetid: 998e0e16-2680-4073-88a0-81d326d482a8
ms.author: windowsdriverdev
ms.date:
ms.topic: struct
ms.prod: windows-hardware
ms.technology: windows-devices
ms.keywords: _D3DKMT_CREATESWAPCHAIN, D3DKMT_CREATESWAPCHAIN,
req.header: d3dkmthk.h
req.include-header:
req.target-type:
req.target-min-winverclnt:
req.target-min-winversvr:
req.kmdf-ver:
req.umdf-ver:
req.lib:
req.dll:
req.ddi-compliance:
req.unicode-ansi:
req.max-support:
req.typenames: D3DKMT_CREATESWAPCHAIN
topictype:
-	apiref
apitype:
-	HeaderDef
apilocation:
-	d3dkmthk.h
apiname:
-	_D3DKMT_CREATESWAPCHAIN
product: 
- Windows
targetos: Windows
---

# _D3DKMT_CREATESWAPCHAIN structure

## -description

Used to create a swap chain.

## -struct-fields

### -field bProducer

[in] Indicates if producer or consumer.

### -field hDevice

[in] Handle to the device.

### -field pObjectAttributes

[in] Security attribute of swap chain.

### -field DesiredAccess

[in] Desired access for swap chain.

### -field SurfaceCount

[in] Number of buffers.

### -field pNtSurfaceHandles

[in] Array of NT handles.

### -field Flags

[in] Flags.

### -field BufferAvailableEvent

[in_opt] Option handle to event.

### -field hNtSwapChain

[out] NT handle for swap chain in this process.
