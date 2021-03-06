---
UID: NF:ntintsafe.RtlULongPtrMult
title: RtlULongPtrMult function
author: windows-driver-content
description: Multiplies one value of type ULONG_PTR by another.
old-location: kernel\rtlulongptrmult.htm
tech.root: kernel
ms.assetid: 6E66CD0B-7CAD-4BF1-A6DD-56C5029A929E
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: RtlULongPtrMult, RtlULongPtrMult function [Kernel-Mode Driver Architecture], kernel.rtlulongptrmult, ntintsafe/RtlULongPtrMult
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntintsafe.h
req.include-header: 
req.target-type: Desktop
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
-	HeaderDef
api_location:
-	Ntintsafe.h
api_name:
-	RtlULongPtrMult
product:
- Windows
targetos: Windows
req.typenames: 
---

# RtlULongPtrMult function


## -description


Multiplies one value of type <b>ULONG_PTR</b> by another.


## -parameters




### -param ulMultiplicand

TBD


### -param ulMultiplier

TBD


### -param pulResult

TBD




#### - Multiplicand [in]

The value to be multiplied by <i>Multiplier</i>.


#### - Multiplier [in]

The value by which to multiply <i>Multiplicand</i>.


#### - pResult [out]

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns STATUS_INTEGER_OVERFLOW and this parameter is not valid.


## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



