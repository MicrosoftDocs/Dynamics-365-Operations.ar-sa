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
ms.openlocfilehash: d54985707d82df2b947a7cb615fc25f90aa31702
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026243"
---
# <a name="directly-derived-firmed-orders-are-processed-by-an-in-review-workflow"></a>تتم معالجة الأوامر المؤكدة المشتقة مباشرة بواسطة سير عمل قيد المراجعة

رقم KB: 4612450

## <a name="symptoms"></a>العلامات

تتم معالجة الأوامر المؤكدة المشتقة مباشرة بواسطة سير عمل يحتوي على حالة *قيد المراجعة*.

## <a name="resolution"></a>الدقة

عندما يتم تمكين تعقب تغيير الحالة، فإنه يتم تعيين حالة *قيد المراجعة* للأوامر المؤكدة المشتقة (أوامر الشراء الخاصة بالعقود من الباطن). وبالتالي، إذا تم اشتقاق أمر شراء (وامر الشراء الخاصة بالعقود من الباطن)، يتم تقديمه فقط إلى سير عمل. إذا كان أمر الشراء مؤكد ومخطط، فإنه يتم اعتماده تلقائيًا لضمان أن محرك التخطيط لا يقوم بإنشاء أوامر مخططة جديدة بينما لا يزال أمر الشراء في حالة *المسودة*.
