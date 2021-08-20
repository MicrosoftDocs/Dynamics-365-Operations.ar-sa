---
title: لا يمكن استيراد أحد الأصناف باستخدام الكيان المنتجات الصادرة V2
description: لا يمكن استيراد أحد الأصناف باستخدام الكيان المنتجات الصادرة V2.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: efd773313f89784d8fca6b37d867e204cb2d06ab29694a19cbec7eed107a8019
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764682"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>لا يمكن استيراد أحد الأصناف باستخدام الكيان المنتجات الصادرة V2

رقم KB: 4611825

## <a name="symptoms"></a>العلامات

عند محاولة استيراد أحد الأصناف باستخدام الكيان *المنتجات الصادرة V2*، تظهر رسالة خطأ مشابهة للمثال التالي:

> لا يمكن إنشاء سجل في الأصناف - مجموعات أبعاد التعقب‬ (EcoResTrackingDimensionGroupItem). رقم الصنف: 2040663، الدفعة. السجل موجود بالفعل.

## <a name="resolution"></a>الدقة

لاستيراد منتجات صادرة جديدة، فإنه يجب استخدام الكيان *إنشاء المنتج الصادر V2* بدلاً من الكيان *المنتجات الصادرة V2*.
