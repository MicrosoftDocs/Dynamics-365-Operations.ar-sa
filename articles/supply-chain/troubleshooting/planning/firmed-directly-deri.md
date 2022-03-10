---
title: تتم معالجة الأوامر المؤكدة المشتقة مباشرة بواسطة سير عمل قيد المراجعة
description: تتم معالجة الأوامر المؤكدة المشتقة مباشرة بواسطة سير عمل يحتوي على حالة قيد المراجعة.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: d20f1c1d6e8fc83dd996b04bf0321a41f7b39290f306d1ac9f4fcd17514832e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721165"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>تتم معالجة الأوامر المؤكدة المشتقة مباشرة بواسطة سير عمل قيد المراجعة

رقم KB: 4612450

## <a name="symptoms"></a>العلامات

تتم معالجة الأوامر المؤكدة المشتقة مباشرة بواسطة سير عمل يحتوي على حالة *قيد المراجعة*.

## <a name="resolution"></a>الدقة

عندما يتم تمكين تعقب تغيير الحالة، فإنه يتم تعيين حالة *قيد المراجعة* للأوامر المؤكدة المشتقة (أوامر الشراء الخاصة بالعقود من الباطن). وبالتالي، إذا تم اشتقاق أمر شراء (وامر الشراء الخاصة بالعقود من الباطن)، يتم تقديمه فقط إلى سير عمل. إذا كان أمر الشراء مؤكد ومخطط، فإنه يتم اعتماده تلقائيًا لضمان أن محرك التخطيط لا يقوم بإنشاء أوامر مخططة جديدة بينما لا يزال أمر الشراء في حالة *المسودة*.
