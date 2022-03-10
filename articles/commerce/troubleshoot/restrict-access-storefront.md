---
title: تقييد الوصول إلى واجهة المتجر أثناء الاختبار أو التطوير
description: يشرح هذا الموضوع كيفية تقييد الوصول إلى واجهة متجر Microsoft Dynamics 365 Commerce أثناء حدوث اختبار أو تطوير داخلي.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: db3317c01cab2e123f3c2927c359f9e00b98bd8a2d5e851c2c20cb4763db1c49
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716773"
---
# <a name="restrict-access-to-a-storefront-during-testing-or-development"></a>تقييد الوصول إلى واجهة المتجر أثناء الاختبار أو التطوير

[!include [banner](../../includes/banner.md)]

يشرح هذا الموضوع كيفية تقييد الوصول إلى واجهة متجر Microsoft Dynamics 365 Commerce أثناء حدوث اختبار أو تطوير داخلي.

## <a name="description"></a>الوصف

أثناء الاختبار الداخلي أو التطوير النشط، قد تحتاج إلى تقييد الوصول إلى موقعك لمنع المستخدمين الخارجيين من الوصول إلى صفحات واجهة المتجر التي تم نشرها.

## <a name="resolution"></a>الدقة

### <a name="set-up-azure-ad-b2c-by-using-standard-user-flows"></a>إعداد B2C لـ Azure AD باستخدام تدفقات المستخدم القياسية

لمزيد من المعلومات حول كيفية تكوين B2C لـ Azure Active Directory (B2Cلـ Azure AD) لموقع التجارة الإلكترونية، راجع [إعداد مستأجر B2C في Commerce](../set-up-b2c-tenant.md).

### <a name="restrict-user-access-to-storefront-pages-and-block-the-creation-of-new-users"></a>تقييد وصول المستخدمين إلى صفحات واجهة المتجر وحظر إنشاء مستخدمين جدد

لتقييد وصول المستخدم إلى صفحات واجهة المتجر في منشئ موقع Commerce، اتبع الخطوات التالية.

1. انتقل إلى موقعك.
1. حدد **صفحات** ، ثم حدد الصفحة لتقييد صلاحية وصول المستخدم إليها.
1. حدد فتحة الوحدة النمطية أو الجزء، ثم حدد **تحرير**.
1. في جزء الخصائص ، حدد **يتطلب تسجيل الدخول؟**، ثم حدد **إنهاء التحرير**.
1. حدد **نشر**.

لحظر إنشاء مستخدمين جدد في Azure AD، اتبع الخطوات التالية.

1. انتقل إلى [مدخل Azure](https://portal.azure.com/).
1. حدد تطبيق B2C لـ Azure AD الذي قمت بإنشائه للوصول إلى الموقع الخاص بك.
1. في جزء التنقل الأيسر، حدد **تدفقات المستخدم**.
1. في أعلى صفحة **تدفقات المستخدم** ، حدد **تدفق مستخدم جديد**.
1. في صفحة **تحديد نوع تدفق المستخدم**، حدد **معاينة**.
1. في منتصف الصفحة، حدد **النسخة الثانية من تسجيل الدخول**. ثم اتبع الخطوات الموجودة في [إعداد مستأجر B2C في Commerce](../set-up-b2c-tenant.md) لتكوين التدفق باعتباره تدفق المستخدم القياسي للموقع لـ B2C Azure AD أثناء الاختبار أو التطوير.

## <a name="additional-resources"></a>الموارد الإضافية

[إعداد مستأجر متاجرة عمل-مستهلك في Commerce](../set-up-b2c-tenant.md)

[إعداد صفحات مخصصة لعمليات تسجيل دخول المستخدمين](../custom-pages-user-logins.md)
