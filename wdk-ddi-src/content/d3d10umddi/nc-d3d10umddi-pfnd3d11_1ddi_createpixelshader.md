---
UID: NC:d3d10umddi.PFND3D11_1DDI_CREATEPIXELSHADER
title: PFND3D11_1DDI_CREATEPIXELSHADER
author: windows-driver-content
description: Converts pixel shader code into a hardware-specific format and associates this code with a shader handle.
old-location: display\createpixelshader_d3d11_1_.htm
tech.root: display
ms.assetid: 8b5d6d2e-6a08-4841-8df5-ca88368a4e26
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: CreatePixelShader(D3D11_1), CreatePixelShader(D3D11_1) callback function [Display Devices], PFND3D11_1DDI_CREATEPIXELSHADER, PFND3D11_1DDI_CREATEPIXELSHADER callback, d3d10umddi/CreatePixelShader(D3D11_1), display.createpixelshader_d3d11_1_, display.pfncreatepixelshader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
req.target-type: Desktop
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
-	UserDefined
api_location:
-	D3d10umddi.h
api_name:
-	CreatePixelShader(D3D11_1)
product:
- Windows
targetos: Windows
req.typenames: 
---

# PFND3D11_1DDI_CREATEPIXELSHADER callback function


## -description


Converts pixel shader code into a hardware-specific format and associates this code with a shader handle.


## -parameters




### -param Arg1


### -param *pShaderCode [in]

 A pointer to an array of CONST UINT tokens that make up the shader code. The first token in the shader code stream is always the version token. The next token in the stream is the length token that determines the end of the shader code stream. For more information about the format of Direct3D version 11.1 shader code, see the comments inside the D3d10tokenizedprogramformat.hpp header file that is included with the WDK.


### -param Arg2


### -param Arg3


### -param *








#### - hDevice

 A handle to the display device (graphics context).


#### - hRTShader

 A handle to the geometry shader that the driver should use when it calls back into the Direct3D runtime.


#### - hShader

 A handle to the driver's private data for the pixel shader. The driver returns the size, in bytes, of the memory region that the Microsoft Direct3D runtime must allocate for the private data from a call to the driver's <a href="https://msdn.microsoft.com/e23c267f-41df-47a6-ae43-3bbcb48fd300">CalcPrivateShaderSize(D3D11_1)</a> function. The handle is really just a pointer to a region of memory, the size of which the driver requested. The driver uses this region of memory to store internal data structures that are related to its shader object.


#### - pSignatures [in]

 A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/hh406324">D3D11_1DDIARG_STAGE_IO_SIGNATURES</a> structure that makes up the shader's signature.


## -returns



The driver can use the <a href="https://msdn.microsoft.com/968b04a7-8869-410c-a6fc-83d57726858f">pfnSetErrorCb</a> callback function to set an error code. For more information about setting error codes, see the following Remarks section.




## -remarks




    The driver can pass E_OUTOFMEMORY (if the driver runs out of memory) or D3DDDIERR_DEVICEREMOVED (if the device has been removed) in a call to the <a href="https://msdn.microsoft.com/968b04a7-8869-410c-a6fc-83d57726858f">pfnSetErrorCb</a> function. The Direct3D runtime will determine that any other errors are critical. If the driver passes any errors, including D3DDDIERR_DEVICEREMOVED, the Direct3D runtime will determine that the handle is incorrect; therefore, the runtime will not call the <a href="https://msdn.microsoft.com/51a3e5aa-0f17-49a6-824d-7cfe8e0a1ded">DestroyShader</a> function to destroy the handle that the <i>hShader</i> parameter specifies.




## -see-also




<a href="https://msdn.microsoft.com/e23c267f-41df-47a6-ae43-3bbcb48fd300">CalcPrivateShaderSize(D3D11_1)</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406324">D3D11_1DDIARG_STAGE_IO_SIGNATURES</a>



<a href="https://msdn.microsoft.com/51a3e5aa-0f17-49a6-824d-7cfe8e0a1ded">DestroyShader</a>



<a href="https://msdn.microsoft.com/968b04a7-8869-410c-a6fc-83d57726858f">pfnSetErrorCb</a>
 

 

