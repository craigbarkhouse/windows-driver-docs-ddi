---
UID: NC:d3d12umddi.PFND3D12DDI_CREATE_GEOMETRY_SHADER_WITH_STREAM_OUTPUT_0010
title: PFND3D12DDI_CREATE_GEOMETRY_SHADER_WITH_STREAM_OUTPUT_0010
author: windows-driver-content
description: 
ms.assetid: 2a8743e2-330a-4fcf-b924-46150bc66d4e
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
-	PFND3D12DDI_CREATE_GEOMETRY_SHADER_WITH_STREAM_OUTPUT_0010
product: 
- Windows
targetos: Windows
---

# PFND3D12DDI_CREATE_GEOMETRY_SHADER_WITH_STREAM_OUTPUT_0010 callback function

## -description

Implemented by the client driver to ... 

## -prototype

```
//Declaration

PFND3D12DDI_CREATE_GEOMETRY_SHADER_WITH_STREAM_OUTPUT_0010 Pfnd3d12ddiCreateGeometryShaderWithStreamOutput0010; 

// Definition

VOID Pfnd3d12ddiCreateGeometryShaderWithStreamOutput0010 
(
	 D3D12DDI_HDEVICE
	CONST D3D12DDIARG_CREATE_GEOMETRY_SHADER_WITH_STREAM_OUTPUT_0010 *
	 D3D12DDI_HSHADER
)
{...}

PFND3D12DDI_CREATE_GEOMETRY_SHADER_WITH_STREAM_OUTPUT_0010 


```

## -parameters

### -param D3D12DDI_HDEVICE: 
### -param *: 
### -param D3D12DDI_HSHADER: 



## -returns

Returns VOID that ...

## -remarks

Register your implementation of this callback function by setting the appropriate member of <!-- REPLACE ME --> and then calling <!-- REPLACE ME -->.


## -see-also