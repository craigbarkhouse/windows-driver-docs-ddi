---
UID: NF:d3dkmthk.D3DKMTDestroyProtectedSession
title: D3DKMTDestroyProtectedSession function
author: windows-driver-content
description: Used to destroy a protected session.
old-location: display\d3dkmtdestroyprotectedsession.htm
tech.root: display
ms.assetid: e27ab1db-647d-447c-b79d-2553aa088398
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: D3DKMTDestroyProtectedSession, D3DKMTDestroyProtectedSession method [Display Devices], d3dkmthk/D3DKMTDestroyProtectedSession, display.d3dkmtdestroyprotectedsession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d3dkmthk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10
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
req.lib: Gdi32.lib 
req.dll: Gdi32.dll 
req.irql: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Gdi32.dll
api_name:
-	D3DKMTDestroyProtectedSession
product:
- Windows
targetos: Windows
req.typenames: 
---

# D3DKMTDestroyProtectedSession function


## -description



			
            Used to destroy a protected session.


## -parameters




### -param Arg1






#### - D3dkmt_destroyprotectedsession [in, out]

Holds information to destroy a protected session.


## -returns




Returns STATUS_SUCCESS if completed successfully.



