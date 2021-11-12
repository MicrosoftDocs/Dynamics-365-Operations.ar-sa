---
title: الشروع في العمل مع الفوترة الإلكترونية للمملكة العربية السعودية
description: يوفر هذا الموضوع معلومات ستساعدك على بدء استخدام الفوترة الإلكترونية للمملكة العربية السعودية.
author: ikondo
ms.date: 10/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 574540
ms.assetid: ''
ms.search.region: Saudi Arabia
ms.author: ilyako
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: AX 10.0.21
ms.openlocfilehash: cb8ec0d489bcb22d9c5272a095e8f8819831b90e
ms.sourcegitcommit: 2113678369f47944f8725ca656f461fa159f87f6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/27/2021
ms.locfileid: "7700449"
---
# <a name="get-started-with-electronic-invoicing-for-saudi-arabia"></a>الشروع في العمل مع الفوترة الإلكترونية للمملكة العربية السعودية

[!include [banner](../includes/banner.md)]

يوفر هذا الموضوع معلومات تساعدك على بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية للمملكة العربية السعودية في Microsoft Dynamics 365 Finance وفي Dynamics 365 Supply Chain Management. وهو يرشدك عبر خطوات التكوين التي تعتمد على البلد/المنطقة في Regulatory Configuration Services (RCS). تقوم هذه الخطوات بتكملة الخطوات الموضحة في [بدء العمل مع الفوترة الإلكترونيه](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-the-saudi-arabian-electronic-invoice-sa-electronic-invoicing-feature"></a>التكوين الخاص بالدولة لميزة الفوترة الإلكترونية (SA) في المملكة العربية السعودية

اتبع هذه الخطوات قبل نشر إعداد التطبيق في التطبيق المتصل بـ Finance أو Supply Chain Management.

يكمل هذا القسم [قسم التكوين الخاص بالبلد لإعداد التطبيق](e-invoicing-get-started.md#country-specific-configuration-of-application-setup) في الموضوع "الشروع في العمل" باستخدام الفوترة الإلكترونية الذي تم ذكره من قبل.

1. في RCS، في مساحة العمل **ميزة العولمة**، في قسم **الميزات**، حدد الإطار المتجانب **الفوترة الإلكترونية**.
2. في صفحة **ميزات الفوترة الإلكترونية**، تحقق من تحديد ميزة الفوترة الإلكترونية لـ **الفاتورة الإلكترونية السعودية (SA)**.
3. في علامة تبويب **الإصدارات**، تحقق من تحديد إصدار **المسودة**.
4. في علامة التبويب **تكوينات** ، انتقل إلى **المعلمات** الخاصة بالتطبيق الخاصة بالتكوين المحدد. في المقطع **عمليات البحث** ، تاكد من تحديد بحث **PaymentMethodSubstitutionLookup**.
5. في المقطع **الشروط** ، حدد **أضافه** لأضافه شرط.
6. في العمود **الاسم** للشرط الجديد ، حدد طريقه الدفع التي يتم تحديدها في التطبيق. وبعد ذلك ، في العمود **نتيجة البحث** ، حدد طريقه قياسيه لكود الدفع وفقا [لقائمه الأكواد UN/EDIFACT 4461](https://unece.org/fileadmin/DAM/trade/untdid/d16b/tred/tred4461.htm).
7. قم باضافه شروط معينه لكل طريقه دفع محدده في النظام ، وقم بحفظ التغييرات التي أجريتها.

    > [!NOTE]
    > في العمود **الاسم** ، يمكنك تحديد قيمه العنصر النائب **فارغة** أو **غير فارغة** بدلا من طريقه معينه للدفع.

8. إكمال ونشر ونشر ميزة **الفاتورة الإلكترونيه السعودية (SA)** إلى بيئة الخدمة. لمزيد من المعلومات، راجع القسم [نشر ميزه الفوترة الكترونيه إلى بيئة الخدمة](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) في الموضوع "الشروع في العمل بالفوترة الإلكترونيه".
9. انشر الميزة **الفاتورة الإلكترونيه السعودية (SA)** بالتطبيق المتصل. لمزيد من المعلومات، راجع القسم [نشر ميزه الفوترة الإلكترونيه إلى التطبيق المتصل](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application) في الموضوع "الشروع في العمل بالفوترة الإلكترونيه".

## <a name="additional-resources"></a>الموارد الإضافية

- [نظرة عامة على الفوترة الإلكترونية](e-invoicing-service-overview.md)
- [الشروع في العمل مع إدارة خدمة الفوترة الإلكترونية](e-invoicing-get-started-service-administration.md)
- [الشروع في العمل مع الفوترة الإلكترونية](e-invoicing-get-started.md)
- [الفواتير الإلكترونية للعملاء في المملكة العربية السعودية](emea-sau-e-invoices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
