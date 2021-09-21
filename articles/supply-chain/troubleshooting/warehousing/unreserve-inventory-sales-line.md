---
title: لا يمكن إلغاء حجز المخزون في سطر أمر المبيعات
description: إذا كان هناك عمل مفتوح مقابل بند مبيعات وأنت تحاول إلغاء عكس المخزون على البند، ستتلقى خطأ. قم بإكمال العمل أو حذفه لتحرير الحجز.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1a042065dc4cd637aff58e55cf16179b7022f6ca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475481"
---
# <a name="cant-unreserve-inventory-on-a-sales-order-line"></a>لا يمكن إلغاء حجز المخزون في سطر أمر المبيعات

## <a name="symptoms"></a>العلامات

إذا كان هناك عمل مفتوح مقابل بند أمر مبيعات وأنت تحاول إلغاء عكس المخزون على هذا البند، ستتلقى رسالة الخطأ التالية.

> لا يمكن إزالة الحجوزات نظرًا لوجود عمل منشأ يعتمد على الحجوزات.

## <a name="resolution"></a>الحل

التحقق من وجود عمل مجموعه التعبئة المفتوحة لإحضار الصنف من محطه تعبئة إلى موقع آخر (مثل *باب الخليج*). قم بمراجعه السجلات الموجودة في الصفحتين **سجل محفوظات إنشاء العمل** و **وتفاصيل العمل** لتحديد ما يقوم بحجز المخزون فعليا ، ثم قم بإكمال العمل أو حذفه لتحرير الحجز.
