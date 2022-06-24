---
title: إعداد بيئة تطوير التجارة الإلكترونية للتصحيح مقابل الجهاز الظاهري لملقم البيع بالتجزئة من المستوى الأول 1
description: يشرح هذا المقال كيفية إعداد بيئة تطوير التجارة الإلكترونية للتصحيح مقابل الجهاز الظاهري لملقم البيع بالتجزئة من المستوى الأول 1 (VM).
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
ms.openlocfilehash: 7cc6c936c67bc82da1a237341ac07fb69d4ac233
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855692"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a>إعداد بيئة تطوير التجارة الإلكترونية للتصحيح مقابل الجهاز الظاهري لملقم البيع بالتجزئة من المستوى الأول 1

[!include [banner](../../includes/banner.md)]

يشرح هذا المقال كيفية إعداد بيئة تطوير التجارة الإلكترونية للتصحيح مقابل الجهاز الظاهري لملقم البيع بالتجزئة من المستوى الأول 1 (VM).

## <a name="description"></a>الوصف

عادة ما يتم نشر بيئات Microsoft Dynamics 365 Commerce من المستوى 1 لتطوير ملحق Commerce runtime (CRT) ونقطة البيع (POS). وهي بيئات مستقلة. وبسبب طبيعة بنية خدمة تأجير البرامج (SaaS)، فإنها لا تتضمن مكونات التجارة الإلكترونية.

في بعض السيناريوهات، قد تحتاج إلى اختبار المكالمات إلى الملحقات في بيئة المستوى 1، بحيث يمكنك تصحيح الملحقات من مكونات التجارة الإلكترونية. للحصول على تعليمات عامة، راجع [تصحيح الأخطاء مقابل بيئة تطوير Commerce المستوى 1](../e-commerce-extensibility/debug-tier-1.md).

عندما تقوم بالتصحيح مقابل بيئة المستوى 1، لأن الموقع يقوم الآن بالاتصال بخادم بيع بالتجزئة مختلف، فقد تتسبب المكالمات عبر الخوادم المتعددة في حدوث أخطاء مختلفة متعلقة بنهج أمان المحتوى.

يبين الرسم التوضيحي التالي مثالا للخطأ الذي قد يحدث عند تحديد متغير في صفحة تفاصيل المنتج.

![حدث خطأ عند تحديد متغير في إحدى صفحات تفاصيل المنتج.](media/unhandled-rejection-error.jpg)

يبين الرسم التوضيحي التالي مثالا لخطأ مشابه في أدوات مصحح أخطاء المستعرض (أدوات المطور F12). تذكر رسالة الخطأ مخالفة توجيه نهج أمان المحتوى.

![خطأ في أدوات مصحح الأخطاء.](media/debugger-tools-error.JPG)

## <a name="resolution"></a>الحل

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a>تعطيل نهج أمان المحتوى للموقع في منشئ مواقع Commerce

1. حدد الموقع الذي تعمل عليه.
1. حدد **الإعدادات**، ثم حدد **الملحقات**.
1. في علامة التبويب **نهج أمان المحتوى**، حدد **تعطيل نهج أمان المحتوى**.
1. حدد **حفظ ونشر**.

> [!NOTE]
> تسجيل الدخول إلى الشركة-المستهلك (B2C) لا يعمل في بيئة تطوير محلية. مع ذلك، يمكنك استخدام عناصر وهمية صفحات السداد مع الخروج للضيف أو صفحات البناء لمحاكاة تسجيل دخول المستخدم كما هو مطلوب.

## <a name="additional-resources"></a>الموارد الإضافية

[‏‫بدء تطوير قابلية التوسع عبر الإنترنت للتجارة الإلكترونية](../e-commerce-extensibility/sdk-getting-started.md)

[إدارة نهج أمان المحتوى (CSP) في موقع التجارة الإلكترونية](../manage-csp.md)
