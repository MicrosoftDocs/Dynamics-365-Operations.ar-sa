---
title: حدث خطأ عندما تم ترحيل دفتر يومية التقرير كمنتهٍ
description: عند ترحيل دفتر يومية الإبلاغ كمنته، تظهر رسالة خطأ توضح أنه لا يمكن تخفيض الكمية المطلوبة.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 50a11aba46519a3a81c313aa1f685d45dcf35f64b50bc921d93968efab13b7b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750920"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a>حدث خطأ عندما تم ترحيل دفتر يومية التقرير كمنتهٍ

رقم KB: 4612891

## <a name="symptoms"></a>العلامات

عند ترحيل دفتر اليومية **‏‫الإبلاغ كمنته**، يحدث خطأ، وتظهر رسالة الخطأ التالية:

> لا يمكن تقليل الكمية المطلوبة لأنه لا توجد حركات مخزون مفتوحة كافية مع الحالة "مطلوب". يتم شراء الأصناف أو استلامها أو تسجيلها.

يحدث هذا الخطأ فقط عند **كمية الخطأ** إلى السطر الأول من دفتر يومية **الإبلاغ كمنته** ويتم تعيين الحقل  **كمية البضائع** على السطر الأخير. إذا تم تعيين الحقل **كمية الخطأ** في البند الأخير، لن يحدث أي خطأ.

## <a name="resolution"></a>الدقة

لمنع حدوث هذا الخطأ، قم بفتح الصفحة **معلمات التحكم في الإنتاج**، ثم من علامة التبويب **عام**، قم بتعيين الخيار **الكمية المتبقية بخيار كمية الخطأ** إلى *نعم*.
