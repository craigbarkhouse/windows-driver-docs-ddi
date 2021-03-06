---
UID: NS:d3dkmdt._DXGK_ADAPTER_PERFDATACAPS
title: _DXGK_ADAPTER_PERFDATACAPS
author: windows-driver-content
description:
ms.assetid: 4193f977-8617-4c1a-965b-040633d29eb3
ms.author: windowsdriverdev
ms.date:
ms.topic: struct
ms.prod: windows-hardware
ms.technology: windows-devices
ms.keywords: _DXGK_ADAPTER_PERFDATACAPS, DXGK_ADAPTER_PERFDATACAPS,
req.header: d3dkmdt.h
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
req.typenames: DXGK_ADAPTER_PERFDATACAPS
topictype:
-	apiref
apitype:
-	HeaderDef
apilocation:
-	d3dkmdt.h
apiname:
-	_DXGK_ADAPTER_PERFDATACAPS
product: 
- Windows
targetos: Windows
---

# _DXGK_ADAPTER_PERFDATACAPS structure

## -description

The physical adapter index in a LDA chain.

## -struct-fields

### -field MaxMemoryBandwidth

Max memory bandwidth in bytes for 1 second.

### -field MaxPCIEBandwidth

Max PCIE bandwidth in bytes for 1 second.

### -field MaxFanRPM

The max fan rpm of the main fan.

### -field TemperatureMax

The max temperature before damage levels occur in deci Celsius. 1 = 0.1C.

### -field TemperatureWarning

The temperature level where temperature based throttling begins in deci Celsius. 1 = 0.1C.

