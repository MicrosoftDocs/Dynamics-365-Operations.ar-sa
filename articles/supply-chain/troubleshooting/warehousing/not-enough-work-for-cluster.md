---
title: لم يتم العثور على عمل كاف لنظام المجموعة بعد تكوين ملف التعريف
description: إذا قمت بتكوين ملف تعريف لنظام مجموعة، قد تظهر رسالة خطأ تفيد بأنه لا يوجد عمل كاف. قم بتحرير ملف التعريف وتعيين تنشيط المناصب إلى لا.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 139fd72e571c8ef83af2fd0e497cf334b6ef0ea4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475438"
---
# <a name="not-enough-work-found-for-cluster-when-using-system-directed-cluster-picking"></a>عدم العثور على عمل كاف لنظام المجموعة عند استخدام النظام الموجة لانتقاء المجموعة

## <a name="symptoms"></a>العلامات

عند استخدامك عملية *انتقاء نظام المجموعة الموجهة بواسطة النظام*، إذا قمت بتكوين ملف تعريف لنظام مجموعة حيث يمكن انتقاء، على سبيل المثال ، 10 مناصب، فان العملية تعمل كما هو مخطط له عند وجود عمل كاف لانتقاء 10 مناصب. ومع ذلك، في حالة وجود ثمانية مناصب لانتقاءها، تظهر رسالة الخطأ التالية:

> تعذر الحصول على عمل كاف لنظام المجموعة.

## <a name="resolution"></a>الحل

لحل هذه المشكلة، قم بتحرير ملف تعريف المجموعة وقم بتعيين خيار **تنشيط المناصب** إلى *لا*.
