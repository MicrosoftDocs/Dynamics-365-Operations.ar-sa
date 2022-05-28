---
title: الأسئلة المتداولة حول التدبير
description: يوفر هذا الموضوع إجابات على الأسئلة المطروحة بشكل متكرر (FAQ) حول وظيفة التدبير في Supply Chain Management
author: GalynaFedorova
ms.date: 05/31/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 718108447dcb5cec488b7fa626feb551808e8dd8
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669337"
---
# <a name="procurement-faq"></a>الأسئلة المتداولة حول التدبير

[!include [banner](../includes/banner.md)]

يوفر هذا الموضوع إجابات على الأسئلة المطروحة بشكل متكرر (FAQ) حول وظيفة التدبير في Supply Chain Management.

## <a name="can-i-show-only-purchase-orders-that-i-created"></a>هل يمكنني إظهار فقط أوامر الشراء التي قمت بإنشائها؟

هذه الوظيفة غير متوفرة حاليًا.

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a>هل يمكنني حجز المخزون وإنشاء حركات مقابل مخزون مسجل في أمر شراء؟

### <a name="issue-description"></a>وصف المشكلة

حتى عندما تكون حالة الأصناف *مسجلة* على أمر شراء، لا يزال بإمكانك حجز المخزون. بمعنىً آخر، يمكنك إنشاء حركات في مقابل المخزون المسجل.

### <a name="reproduce-the-issue"></a>إعادة إنتاج المشكلة

يعرض الإجراء التالي إحدى الطرق لإعادة إنتاج المشكلة.

1. إنشاء أمر شراء.
2. تسجيل بند أمر الشراء.
3. لاحظ أنه يمكنك إنشاء حجوزات أو حركات في مقابل المخزون المسجل.

### <a name="issue-resolution"></a>حل المشكلة

يتم هذا السلوك بسبب التصميم. الأمر المتوقع هو ان الأصناف المسجلة قد وصلت فعليًا إلى المستودع أو المخزون، وأنها بالتالي متاحة للحجز.

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a>هل يمكنني العثور على المستخدم الذي قام بإلغاء أمر الشراء؟

يتم تعقب هذه المعلومات فقط إذا كان أمر الشراء يخضع لإدارة التغيير. إذا كنت تستخدم إدارة التغيير، فيمكنك معرفة من هي الجهة التي أرسلت التغيير (الإلغاء) ووافقت عليه.

## <a name="why-cant-i-link-a-purchase-agreement-to-an-existing-purchase-order"></a>لماذا لا يمكنني ربط اتفاقية شراء بأمر شراء موجود؟

يجب ربط اتفاقية شراء ببند أمر شراء عند إنشاء أمر الشراء. بخلاف ذلك، لا يمكن ربط بنود أوامر الشراء ببنود اتفاقية الشراء.

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a>ما عمليات التحقق التي تقوم بتشغيل الرسالة "تحديث الأسعار والخصومات التي تم إدخالها يدويًا أو المستند الخارجي"؟

عند تغيير تاريخ الشحن، قد تتلقي رسالة تشير إلى "تحديث الأسعار والخصومات التي تم إدخالها يدويًا أو المستند الخارجي". سبب تلقيك هذه الرسالة هو تشغيل اتفاقية تجارية  أو اتفاقية مبيعات مختلفة وقد تتسبب في تغيير في السعر، إذا تغيّر تاريخ الشحن. من شأن تغيير تاريخ الشحن أن يؤثر أيضًا على جداول المستودع ومعلومات أخرى ذات صلة.

يتم تشغيل الرسالة عند تغيير أي من التواريخ أو بعض المعلمات الأخرى. والغرض من الرسالة هو التأكد من انك على علم بتغييرات الأسعار التي يمكنها أن تحدث بسبب هذه التغييرات.

الرسالة هي المطالبة بتقييم اتفاقية التجارة (TAE). للحصول على وصف كامل، راجع [سياسات تقييم الاتفاقية التجارية](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).

## <a name="why-cant-i-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>لماذا لا يمكنني ترحيل أكثر من فاتورة واحدة لبند أمر شراء يتضمن أصناف تستند إلى فئة؟

تكون الكمية إلزامية إذا كنت ترغب في ترحيل الفواتير. وبالتالي، إذا تمت فوترة  الكمية الكامل لأحد البنود لمبلغ جزئي فقط، فلن تتمكن من فوترة المبلغ المتبقي على فاتورة أخرى.
