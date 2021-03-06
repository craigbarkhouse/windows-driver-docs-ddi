---
UID: NC:d3dkmthk.PFND3DKMT_OPENPROTECTEDSESSIONFROMNTHANDLE
title: PFND3DKMT_OPENPROTECTEDSESSIONFROMNTHANDLE
author: windows-driver-content
description:
ms.assetid: c226000c-38a3-4956-b51d-b0ddbc6c46ca
ms.author: windowsdriverdev
ms.date:
ms.topic: callback
ms.prod: windows-hardware
ms.technology: windows-devices
req.header: d3dkmthk.h
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
-	d3dkmthk.h
apiname:
-	PFND3DKMT_OPENPROTECTEDSESSIONFROMNTHANDLE
product: 
- Windows
targetos: Windows
---

# PFND3DKMT_OPENPROTECTEDSESSIONFROMNTHANDLE callback function

## -description

Implemented by the client driver to open a protected session from the NT handle.

## -prototype

```
//Declaration

PFND3DKMT_OPENPROTECTEDSESSIONFROMNTHANDLE Pfnd3dkmtOpenprotectedsessionfromnthandle;

// Definition

NTSTATUS Pfnd3dkmtOpenprotectedsessionfromnthandle
(
	D3DKMT_OPENPROTECTEDSESSIONFROMNTHANDLE *
)
{...}

PFND3DKMT_OPENPROTECTEDSESSIONFROMNTHANDLE


```

## -parameters

### -param D3DKMT_OPENPROTECTEDSESSIONFROMNTHANDLE *

Pointer to a [D3DKMT_OPENPROTECTEDSESSIONFROMNTHANDLE](ns-d3dkmthk-_d3dkmt_openprotectedsessionfromnthandle.md) structure that contains the information needed to open the protected session.

## -returns

Return STATUS_SUCCESS if the operation succeeds. Otherwise, return an appropriate NTSTATUS Values error code.

## -remarks

Register your implementation of this callback function by setting the appropriate member of [D3DKMT_OPENPROTECTEDSESSIONFROMNTHANDLE](ns-d3dkmthk-_d3dkmt_openprotectedsessionfromnthandle.md) and then calling Pfnd3dkmtOpenProtectedSessionFromNtHandle.

