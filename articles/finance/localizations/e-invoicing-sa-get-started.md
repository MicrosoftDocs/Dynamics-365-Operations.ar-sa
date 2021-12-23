---
title: الشروع في العمل مع الفوترة الإلكترونية للمملكة العربية السعودية
description: يوفر هذا الموضوع معلومات ستساعدك على بدء استخدام الفوترة الإلكترونية للمملكة العربية السعودية.
author: ikondo
ms.date: 11/08/2021
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
ms.openlocfilehash: 29d78e2f26bc73d5803d0ba8ceedee40b31bfd2c
ms.sourcegitcommit: 88f8a0369ce66b82314db9639491b695e18a7e5c
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902573"
---
# <a name="get-started-with-electronic-invoicing-for-saudi-arabia"></a>الشروع في العمل مع الفوترة الإلكترونية للمملكة العربية السعودية

[!include [banner](../includes/banner.md)]

يوفر هذا الموضوع معلومات تساعدك على بدء استخدام الوظيفة الإضافية الفوترة الإلكترونية للمملكة العربية السعودية في Microsoft Dynamics 365 Finance وفي Dynamics 365 Supply Chain Management. وهو يرشدك عبر خطوات التكوين التي تعتمد على البلد/المنطقة في Regulatory Configuration Services (RCS). تقوم هذه الخطوات بتكملة الخطوات الموضحة في [بدء العمل مع الفوترة الإلكترونيه](e-invoicing-get-started.md).

### <a name="prerequisites"></a>المتطلبات الأساسية

قبل إكمال الخطوات الواردة في هذا الموضوع، يجب استيفاء المتطلبات الأساسية التالية: 

- قم باستيراد ميزة الفواتير الإلكترونية **الفاتورة الإلكترونية للمملكة العربية السعودية (SA)** إلى RCS من المستودع العالمي. لمزيد من المعلومات، راجع قسم [يمكنك استيراد ميزة الفوترة الإلكترونية من موفر تكوين Microsoft‬](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider) في موضوع "بدء استخدام الفواتير الإلكترونية".
- في Microsoft Dataverse، قم بتكوين الكيانات الافتراضية لـ Finance and Supply Chain Management. لمزيد من المعلومات، راجع [تكوين كيانات Dataverse الظاهرية](../../fin-ops-core/dev-itpro/power-platform/admin-reference.md).
- قم بتمكين الكيان الظاهري **CustomerPaymentMethodEntity**. لمزيد من المعلومات، راجع [تمكين الكيانات الظاهرية Microsoft Dataverse](../../fin-ops-core/dev-itpro/power-platform/enable-virtual-entities.md).
- أضف نقطة نهاية Dataverse كتطبيق متصل في مثيل RCS. لمزيد من المعلومات، راجع القسم [إنشاء تطبيق متصل](e-invoicing-get-started-service-administration.md#create-a-connected-application) في في موضوع "البدء في إدارة خدمة الفواتير الإلكترونية".

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
    > في العمود **الاسم**، يمكنك تحديد قيمة العنصر النائب **&#42;فارغة&#42;** أو **&#42;غير فارغة&#42;** بدلاً من طريقة معينة للدفع.

8. في علامة التبويب **عمليات الإعداد**، حدد **تحرير** للتكوين المحدد. 
9. في قسم **مسار المعالجة**، قم بتشغيل خيار **تصدير النتيجة** لخيار **تحويل المستند**.
10. إكمال ونشر ونشر ميزة **الفاتورة الإلكترونيه السعودية (SA)** إلى بيئة الخدمة. لمزيد من المعلومات، راجع القسم [نشر ميزه الفوترة الكترونيه إلى بيئة الخدمة](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) في الموضوع "الشروع في العمل بالفوترة الإلكترونيه".
11. انشر الميزة **الفاتورة الإلكترونيه السعودية (SA)** بالتطبيق المتصل. لمزيد من المعلومات، راجع القسم [نشر ميزه الفوترة الإلكترونيه إلى التطبيق المتصل](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application) في الموضوع "الشروع في العمل بالفوترة الإلكترونيه".

## <a name="additional-resources"></a>الموارد الإضافية

- [نظرة عامة على الفوترة الإلكترونية](e-invoicing-service-overview.md)
- [الشروع في العمل مع إدارة خدمة الفوترة الإلكترونية](e-invoicing-get-started-service-administration.md)
- [الشروع في العمل مع الفوترة الإلكترونية](e-invoicing-get-started.md)
- [الفواتير الإلكترونية للعملاء في المملكة العربية السعودية](emea-sau-e-invoices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
