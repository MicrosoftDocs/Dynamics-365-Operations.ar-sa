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
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026227"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a>لا يمكن استيراد أحد الأصناف باستخدام الكيان المنتجات الصادرة V2

رقم KB: 4611825

## <a name="symptoms"></a>العلامات

عند محاولة استيراد أحد الأصناف باستخدام الكيان *المنتجات الصادرة V2*، تظهر رسالة خطأ مشابهة للمثال التالي:

> لا يمكن إنشاء سجل في الأصناف - مجموعات أبعاد التعقب‬ (EcoResTrackingDimensionGroupItem). رقم الصنف: 2040663، الدفعة. السجل موجود بالفعل.

## <a name="resolution"></a>الدقة

لاستيراد منتجات صادرة جديدة، فإنه يجب استخدام الكيان *إنشاء المنتج الصادر V2* بدلاً من الكيان *المنتجات الصادرة V2*.
