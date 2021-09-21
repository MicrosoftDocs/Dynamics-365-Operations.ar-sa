---
title: لا يمكن معالجة تصحيح مذكرة التسليم
description: إذا حاولت تصحيح إحدى ملاحظات التسليم بعد نشرها، ستتلقى خطأ. توضح هذه الصفحة كيفية تصحيح أيصالات التعبئة المنشورة للأصناف التي تم تمكينها لـ WMS.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bb0d827adff8abd8762bf2de844cad5574628e4b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475498"
---
# <a name="delivery-note-correction-cant-be-processed"></a>لا يمكن معالجة تصحيح مذكرة التسليم

## <a name="symptoms"></a>العلامات

بعد نشر مذكرة تسليم، لا يمكنك إلغاؤها لأنه لم يتم توفير الزر **إلغاء**. لا يمكنك أيضا تصحيح مذكرة التسليم. وإذا حاولت، فقد تتلقى رسالة الخطأ التالية:

> لا يمكن معالجة تصحيح مذكرة التسليم. لا يحتوي إشعار التسليم إلا على الأصناف التي تخضع لعمليات إدارة المستودع، لأن هذه الأصناف غير معتمدة من قبل تصحيح مذكرة التسليم.

## <a name="resolution"></a>الحل

لتصحيح إيصالات التعبئة التي تم ترحيلها للأصناف التي تم تمكينها لأداره المستودعات المتقدمة (WMS) ، يجب القيام بالترحيل من التحميل ، وليس من الأمر مباشره.
