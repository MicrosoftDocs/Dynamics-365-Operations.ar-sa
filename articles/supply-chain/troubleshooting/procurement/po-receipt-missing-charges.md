---
title: لا يتضمن إيصال استلام أمر الشراء كافة المصروفات
description: لا يتضمن إيصال استلام أمر الشراء كافة المصروفات
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb567e00ef52269db0dc866148a37c73f0a9827c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475430"
---
# <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>لا يتضمن إيصال استلام أمر الشراء كافة المصروفات

## <a name="symptoms"></a>العلامات

عند استلام أمر شراء، لا يتم تضمين كافة المصاريف في الإيصال.

### <a name="reproduce-the-issue"></a>إعادة إنتاج المشكلة

يعرض الإجراء التالي إحدى الطرق لإعادة إنتاج المشكلة.

1. في الصفحة **معلمات التدبير والتوريد**‬‏‫، ضمن علامة التبويب **التسليم**، تأكد من تعيين الخيار **إنشاء مصروفات على إيصال استلام المنتجات** إلى *نعم*.
1. أنشئ أمر شراء يتضمن مصروفات.
1. أكد أمر الشراء.
1. استلم أمر الشراء.
1. قم بإلقاء نظرة على إجمالي الإيصال، وقارنه بالإجمالي المتوقع.
1. لاحظ عدم تضمين كافة المصروفات على إيصال أمر الشراء.

## <a name="resolution"></a>الحل

يتوقف الحل على الطريقة التي تم بها إعداد المصروفات المتنوعة. للحصول على معلومات حول كيفية إعداد المصروفات المتنوعة للوفاء بمتطلباتك، راجع منشور المدونة التالي: [ترحيل المصروفات المتنوعة عند استلام المنتجات](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
