---
title: لا يمكن أن يحتوي الصنف على قائمة مكونات الصنف (BOM)‬ أو معادلة
description: عند محاولة التأكيد على أمر، فإنك تتلقى رسالة خطأ أثناء التحقق من صحة الصنف. يوضح أن الصنف لا يمكن ان قائمة مكونات الصنف (BOM) أو المعادلة.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1e946adc3a04db60bf15ac7bb44163085e1c19802872964877d3929b1f79bf7d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730096"
---
# <a name="item-cant-have-a-bom-or-formula"></a>لا يمكن أن يحتوي الصنف على قائمة مكونات الصنف (BOM)‬ أو معادلة

رمز الخطأ: PRO2614

## <a name="symptoms"></a>العلامات

عند محاولة التأكيد على أمر، فإنك تتلقى رسالة الخطأ التالية أثناء التحقق من صحة الصنف:

> لا يمكن أن يحتوي الصنف على قائمة مكونات صنف أو معادلة

## <a name="resolution"></a>الحل

يجب أن تكون الأصناف التي تحتوي على قائمة مكونات الصنف (BOM) أو المعادلة من النوع *صنف التخطيط* أو *قائمة مكونات الصنف* أو *المعادلة*. لتغيير نوع صنف، اتبع هذه الخطوات.

1. انتقل إلى **إدارة معلومات المنتج‬ \> المنتجات \> المنتجات الصادرة**.
1. افتح المنتج ذا الصلة.
1. في علامة التبويب السريعة **المهندس**، قم بتعيين الحقل **نوع الإنتاج** إلى *صنف التخطيط* أو *قائمة مكونات الصنف* أو *المعادلة*.
