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
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294002"
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
