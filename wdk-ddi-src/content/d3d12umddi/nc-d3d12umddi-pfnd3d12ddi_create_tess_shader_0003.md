---
UID: NC:d3d12umddi.PFND3D12DDI_CREATE_TESS_SHADER_0003
title: PFND3D12DDI_CREATE_TESS_SHADER_0003
author: windows-driver-content
description: 
ms.assetid: 9a80bdac-138c-4025-99d9-7afaee97b6da
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
-	PFND3D12DDI_CREATE_TESS_SHADER_0003
product: 
- Windows
targetos: Windows
---

# PFND3D12DDI_CREATE_TESS_SHADER_0003 callback function

## -description

Implemented by the client driver to ... 

## -prototype

```
//Declaration

PFND3D12DDI_CREATE_TESS_SHADER_0003 Pfnd3d12ddiCreateTessShader0003; 

// Definition

VOID Pfnd3d12ddiCreateTessShader0003 
(
	 D3D12DDI_HDEVICE
	CONST UINT *pShaderCode
	 D3D12DDI_HROOTSIGNATURE
	 D3D12DDI_HSHADER
	CONST D3D12DDIARG_TESSELLATION_IO_SIGNATURES *
	 D3D12DDI_CREATE_SHADER_FLAGS
)
{...}

PFND3D12DDI_CREATE_TESS_SHADER_0003 


```

## -parameters

### -param D3D12DDI_HDEVICE: 
### -param *pShaderCode: 
### -param D3D12DDI_HROOTSIGNATURE: 
### -param D3D12DDI_HSHADER: 
### -param *: 
### -param D3D12DDI_CREATE_SHADER_FLAGS: 



## -returns

Returns VOID that ...

## -remarks

Register your implementation of this callback function by setting the appropriate member of <!-- REPLACE ME --> and then calling <!-- REPLACE ME -->.


## -see-also