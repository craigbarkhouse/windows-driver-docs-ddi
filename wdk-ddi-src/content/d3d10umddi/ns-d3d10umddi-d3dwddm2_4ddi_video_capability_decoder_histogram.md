---
UID: NS:d3d10umddi.D3DWDDM2_4DDI_VIDEO_CAPABILITY_DECODER_HISTOGRAM
title: D3DWDDM2_4DDI_VIDEO_CAPABILITY_DECODER_HISTOGRAM
author: windows-driver-content
description:
ms.assetid: 612d483a-fc73-4781-a84c-dd9bbb8b0dd6
ms.author: windowsdriverdev
ms.date:
ms.topic: struct
ms.prod: windows-hardware
ms.technology: windows-devices
ms.keywords: D3DWDDM2_4DDI_VIDEO_CAPABILITY_DECODER_HISTOGRAM, D3DWDDM2_4DDI_VIDEO_CAPABILITY_DECODER_HISTOGRAM,
req.header: d3d10umddi.h
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
req.typenames: D3DWDDM2_4DDI_VIDEO_CAPABILITY_DECODER_HISTOGRAM
topictype:
-	apiref
apitype:
-	HeaderDef
apilocation:
-	d3d10umddi.h
apiname:
-	D3DWDDM2_4DDI_VIDEO_CAPABILITY_DECODER_HISTOGRAM
product: 
- Windows
targetos: Windows
---

# D3DWDDM2_4DDI_VIDEO_CAPABILITY_DECODER_HISTOGRAM structure

## -description

Data structure for the associated D3DWDDM2_4DDI_VIDEO_CAPABILITY_QUERY_DECODER_HISTOGRAM value in the video capability query [D3DWDDM2_0DDI_VIDEO_CAPABILITY_QUERY enumeration](ne-d3d10umddi-d3dwddm2_0ddi_video_capability_query.md).

## -struct-fields

### -field DecoderDesc

The decoder description for the decoder to be used with decode histogram.

### -field Components

The components (or channels) of a DXGI_FORMAT that the hardware supports.

### -field BinCount

The number of per component bins supported. BinCount must be >= 64 and must be a power of 2 (64, 128, 256, 512, etc.).

### -field CounterBitDepth

The bit depth of the bin counter. The counter is always stored in a 32-bit value and is therefore 32 bits or less. The counter is stored in the lower bits of the 32 bit storage. The upper bits are set to zero. If the in count exceeds this bit depth, the value is set to the maximum counter value. Valid values for CounterBitDepth are 16, 24, and 32.

## -remarks

## -see-also