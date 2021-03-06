---
title: استكشاف أخطاء إيصالات استلام المنتجات والفوترة وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع إيصالات استلام المنتجات والفوترة.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 22b1abec0c6dd5f571e604c5c07379b397b8bdaa
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999043"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a>استكشاف أخطاء إيصالات استلام المنتجات والفوترة وإصلاحها

يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع إيصالات استلام المنتجات والفوترة.

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a>لا يمكنني ترحيل أكثر من فاتورة واحدة لبند أمر شراء لديه أصناف تستند إلى فئة.

تكون الكمية إلزامية إذا كنت ترغب في ترحيل الفواتير. وبالتالي، إذا تمت فوترة  الكمية الكامل لأحد البنود لمبلغ جزئي فقط، فلن تتمكن من فوترة المبلغ المتبقي على فاتورة أخرى.

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a>أتلقى الخطأ "لم يتم تعيين مرجع الكائن" أثناء تأكيد أمر الشراء، أو حدث الاستثناء "تم طرح استثناء بواسطة هدف استدعاء أثناء ترحيل فواتير المورّد.

قد تحدث هذه المشكلة بسبب عدم الاتساق في توزيعات أمر الشراء.

لحل هذه المشكلة وإعادة تعيين أمر الشراء إلى الحالة *مسودة*، انتقل إلى **التدبير والتوريد \> المهام الدورية \> تنظيف \> إعادة تعيين توزيع أمر الشراء**. لمزيد من المعلومات، راجع منشور المدونة التالي: [حل أخطاء توزيع أمر الشراء في Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a>لا يمكن دمج إيصالات استلام منتجات متعددة في أمر شراء واحد.

لا يمكنك دمج إيصالات استلام منتجات متعددة في أمر شراء واحد إذا كانت بنود إيصال استلام المنتجات المختلفة ذات تواريخ محاسبية مختلفة.

في الإصدارات السابقة من Microsoft Dynamics 365 Supply Chain Management، كان الدمج مسموحًا به في هذه الحالة. ومع ذلك، تعتبر الممارسة عرضة للخطأ. يجب ألا يختلف التاريخ المحاسبي في بنود أمر الشراء التي تم إنشاؤها عن التاريخ المحاسبي الموجود في بنود إيصال استلام المنتجات التي تم إنشاء بنود أمر الشراء منها. (يتطابق التاريخ المحاسبي على بنود أمر الشراء مع التاريخ المحاسبي على  رأس أمر  الشراء.) وبالتالي، لم يعد يُسمح بدمج إيصالات استلام متعددة في أمر شراء واحد.

يتم استخدام التاريخ المحاسبي، على سبيل المثال، لحجوزان الموازنة والالتزام بها. وبالتالي، يجب ان يتم الاحتفاظ بها أثناء الانتقال من إيصال استلام المنتجات إلى أمر الشراء.

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a>عند إلغاء إيصالات استلام المنتجات، يمكن ترحيل الحركات إلى حساب دفتر أستاذ معلق.

### <a name="issue-description"></a>وصف المشكلة

إذا تم إلغاء إيصال استلام المنتجات، فإن النظام يسمح بترحيل الحركات إلى حسابات دفتر أستاذ معلقة، على الرغم من كون الحسابات الرئيسية معلقة.

### <a name="reproduce-the-issue"></a>إعادة إنتاج المشكلة

يعرض الإجراء التالي إحدى الطرق لإعادة إنتاج المشكلة.

1. في الصفحة **معلمات الحسابات الدائنة**‬‏‫، على علامة التبويب **عام**، تأكد من تعيين الخيار **ترحيل إيصال استلام المنتجات إلى دفتر الأستاذ** إلى *نعم*.
1. أنشئ أمر شراء، وأضف بند أمر لديه كمية من *1,000* لمنتج.
1. أكد أمر الشراء.
1. قم بترحيل إيصال استلام المنتجات وتحقق من الإيصالات.
1. قم بتعليق الحسابين الرئيسين ذي الصلة، *200140* و *140200*.
1. قم بإلغاء إيصال استلام المنتجات المرحّل.
1. لاحظ أنه يمكن ترحيل الحركات إلى حسابات دفتر الأستاذ المعلقة.

### <a name="issue-resolution"></a>حل المشكلة

يمكن ترحيل الحركات إلى حسابات دفتر الأستاذ المعلقة عند إلغاء إيصالات استلام المنتجات، لأن هذا السلوك يسمح بالترحيلات الصحيحة.

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a>يتم استهلاك رقم إيصال استلام المنتجات حتى في حالة عدم إنشاء إيصال مالي اثناء استلام المنتجات.

إذا تم تعيين الخيار **استحقاق الالتزام على إيصال استلام المنتجات‬** إلى *لا* لمجموعة نماذج الأصناف، لن تحدث أي عمليات ترحيل لدفتر الأستاذ العام. ومع ذلك، سيتم تسجيل حدث فعلي لغرض المحاسبة في دفتر الأستاذ الفرعي، ويتطلب ذلك الحدث رقم إيصال. رقم الإيصال هذا هو رقم الإيصال الذي يُشار في حركات المخزون.

ننصحك بتعيين الخيار **استحقاق الالتزام على إيصال استلام المنتجات‬** إلى *نعم*، كما تم وصفه في منشور المدونة التالي: [ترحيل المصروفات المتنوعة عند استلام المنتجات](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>الإعداد "ترحيل إلى حساب مصاريف في دفتر الأستاذ" ليس قيد التشغيل

### <a name="issue-description"></a>وصف المشكلة

تحدث هذه المشكلة عند فوترة أمر شراء، إذا تم تعيين الخيار **ترحيل إلى حساب مصاريف في دفتر الأستاذ** إلى *نعم* على علامة تبويب **الفاتورة** في صفحة **معلمات الحسابات الدائنة**.

### <a name="reproduce-the-issue"></a>إعادة إنتاج المشكلة

يعرض الإجراء التالي إحدى الطرق لإعادة إنتاج المشكلة.

1. انتقل إلى **الحسابات الدائنة \> الإعداد \> محددات الحسابات الدائنة**.
1. من علامة التبويب **الفاتورة**، قم بتعيين الخيار **ترحيل إلى حساب مصاريف في دفتر الأستاذ** إلى *نعم*.
1. انتقل إلى **إدارة المخزون \> الإعداد \> الترحيل \> الترحيل**.
1. في علامة التبويب **أمر الشراء**، تأكد من أنك حذفت جميع البنود في نفقات الشراء الخاصة بالمنتج.
1. انتقل إلى **الحسابات الدائنة \> أوامر الشراء \> جميع أوامر الشراء**.
1. إنشاء أمر شراء. في الحقل **حساب المورّد**، حدد *1001 المستلزمات المكتبية Acme*.
1. أضف بند أمر شراء يتضمن الإعدادات التالية:

    - **رقم الصنف:** *D0011 بروجيكتور ليزر*
    - **الموقع:** *1*
    - **المستودع:** *11*
    - **الكمية:** *4*

1. في جزء الإجراءات، في علامة تبويب **الشراء** في مجموعة **الإجراء**، حدد **تأكيد**.
1. في جزء الإجراءات، في علامة التبويب **استلام** في المجموعة **إنشاء‬**، حدد **إيصال استلام المنتجات**.
1. في مربع الحوار **ترحيل إيصال استلام المنتجات**، في الحقل **إيصال استلام المنتجات**، أدخل رقمًا عشوائيًا، ثم حدد **موافق**.
1. في جزء الإجراءات، في علامة التبويب **الفاتورة**، في المجموعة **إنشاء**، حدد **فاتورة**.
1. في حقل **الرقم**، أدخل رقمًا عشوائيًا كرقم الفاتورة.
1. قم بتحديث حالة المطابقة، ثم قم بالترحيل.
1. لاحظ أنك تتلقي الآن رسالة الخطأ التالية عند إنشاء فاتورة من أمر شراء: "رقم الحساب لنوع الحركة "نفقات الشراء" للمنتج غير موجود".

### <a name="issue-resolution"></a>حل المشكلة

يتوقف ذلك على إعدادات المعلمات الخاصة بالفواتير ومجموعات الفواتير. لمزيد من المعلومات، راجع منشور المدونة التالي: [محاسبة مصروفات الشراء وتغييرات المخزون](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]