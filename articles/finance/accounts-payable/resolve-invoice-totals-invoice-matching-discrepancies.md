---
title: نظرة عامة حول حل الاختلافات أثناء مطابقة إجماليات الفواتير
description: يمكنك استخدام مطابقة إجماليات الفواتير للمساعدة على التأكد من أن مبالغ الفواتير الإجمالية لا تحيد عن المبالغ المتوقعة بما يزيد على فرق مقبول.
author: abruer
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 63413,  ""intro-internal
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.form: VendTotalPriceTolerance
ms.openlocfilehash: fa248622a21b0571b08c97eff507ee1035daa7f9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268576"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching-overview"></a>نظرة عامة حول حل الاختلافات أثناء مطابقة إجماليات الفواتير

[!include [banner](../includes/banner.md)]

يتمثل نوع واحد من التحقق من صحة مطابقة الفواتير في مطابقة إجماليات الفواتير. ولتحديد أن النظام يجب عليه تنفيذ مطابقة إجماليات الفواتير، في صفحة **معلمات الحسابات الدائنة**، في علامة التبويب **التحقق من صحة الفواتير**، قم بتعيين خيار **مطابقة إجماليات الفواتير** إلى **نعم**. 

يمكنك استخدام مطابقة إجماليات الفواتير للمساعدة على التأكد من أن مبالغ الفواتير الإجمالية لا تحيد عن المبالغ المتوقعة بما يزيد على فرق مقبول. وتتم مقارنة ستة إجماليات في صفحة **تفاصيل مطابقة إجماليات الفواتير**. وإذا انحرف أي إجمالي من الإجماليات عن إجمالي أمر الشراء المقابل المتوقع، فإنه يتم وضع علامة لاختلاف المطابقة. 

ولمراجعة الفاتورة المشتملة على اختلاف مطابقة الإجماليات، في مساحة عمل **إدخال فاتورة مورد**، انقر فوق تجانب **الفواتير المعلقة**. وبعد ذلك، في جزء الإجراءات، في علامة التبويب **مراجعة**، انقر فوق **تفاصيل المطابقة**. وإذا تم الكشف عن اختلافات في المطابقة، تظهر رموز تحذير بجوار مبلغ الفاتورة. ويمكنك عرض المزيد من التفاصيل حول الإجماليات بعرض تفاصيل مطابقة إجماليات الفواتير. 

وبعد تحديد اختلاف، قد تحتاج إلى الاتصال بالمورّد إذا كنت تعتقد أن المعلومات الموجودة في الفاتورة غير صحيحة. ووفقًا لما ستتفق عليه مع المورّد، يمكنك القيام بأيٍ من الإجراءات التالية:

-   قبول الاختلاف في السعر وترحيل الفاتورة التي تشتمل على اختلافات المطابقة. ويمكن إعداد النظام لتتطلب الموافقة قبل أن يمكنه الترحيل إذا كانت هناك اختلافات في المطابقة. وفي هذه الحالة، يجب عليك الموافقة على اختلاف المطابقة ويمكنك إدخال تعليق موافقة بشكل اختياري. وبعد ذلك، يمكنك اختيار ترحيل الفاتورة.
-   قم بتعديل مبلغ الفاتورة إلى المبلغ المتوقع وترحيل الفاتورة.
-   اطلب ائتمانًا كاملاً، فاتورة مصححة جديدة من المورد.

للحصول على مزيد من المعلومات، راجع [البحث عن/حل الاستثناءات](tasks/research-resolve-exceptions.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
