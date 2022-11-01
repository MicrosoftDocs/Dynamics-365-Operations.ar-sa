---
title: معاينة Dynamics 365 Commerce 10.0.31 (فبراير 2023)
description: تصف هذه المقالة الميزات الجديدة أو المتغيرة في 10.0.31. Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 10/18/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-10-01
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 05ccd9794ffeba6a09d6fec0a57ffad2b59707ad
ms.sourcegitcommit: 87e75aa6af2c3280316d7d73eafa14a52353a5e4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/21/2022
ms.locfileid: "9709850"
---
# <a name="preview-of-dynamics-365-commerce-10031-february-2023"></a>معاينة Dynamics 365 Commerce 10.0.31 (فبراير 2023)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

يصف هذا المقالا الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Commerce إصدار 10.0.31. رقم بنية هذا الإصدار هي 10.0.1406، وهو يتوفر وفق الجدول التالي:

- **معاينه الإصدار:** أكتوبر 2022
- **التوفر العام للإصدار (تحديث ذاتي):** يناير 2023
- **التوفر العام للإصدار (تحديث تلقائي):** فبراير 2023

## <a name="features-included-in-this-release"></a>الميزات المضمنة في هذا الإصدار

يسرد الجدول التالي الميزات المضمنة في هذا الإصدار. قد نقوم بتحديث هذا الموضوع ليشمل الميزات التي تمت إضافتها إلى البنية بعد نشر هذا الموضوع.

| منطقة الميزة | الميزة | معلومات إضافية | تم التمكين بواسطة |
|---|---|---|---|
| رموز الخطأ | قدمت التجارة مراجع خطأ موحدة ليتم تضمينها في أخطاء السداد عبر قناة الإنترنت المقدمة إلى المتسوقين عبر الإنترنت.| [أكواد الخطأ للوحدة النمطية للسداد](../checkout-module-error-codes.md)  | قيد التشغيل بشكل افتراضي |
| المدفوعات | [تمكين Apple Pay مع Dynamics 365 Payment Connector لـ Adyen](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-apple-pay-dynamics-365-payment-connector-adyen)  | يمكن لعملاء التجارة الإلكترونية استخدام Apple Pay في صفحات سلة التسوق والدفع عند استخدام الأجهزة أو المتصفحات المدعومة. | اشتراك المطور |
| المدفوعات  |  أضافت التجارة القدرة على الحد من كيفية تفاعل المستخدمين مع رموز الدفع المميزة المتكررة عبر واجهة مستخدم Commerce headquarters‬. لم تعد نماذج الدفع، مثل صفحة **‏‫أوامر مبيعات مركز الاتصال‬**، تعرض رمز الدفع المميز المتكرر المستخدم مسبقًا للعميل لاستخدامه في معاملة جديدة. سيتم تقديم إدخال "بطاقة في الملف" محدد فقط في شاشة التجارة **مدفوعات العميل**، أو بالاتفاق مع العميل أثناء الدفع من خلال أمر مبيعات ، إلى مركز الاتصال أو مستخدمي Commerce headquarters عند المعالجة دفعة لمعاملة جديدة. | [تقييد استخدام رمز الدفع](../dev-itpro/limit-token-usage.md)  |  إدارة الميزات<p>*تقييد استخدام الرمز المميز للدفع بسياق الأمر*  |
| نقطة البيع | [إنشاء أوامر شراء من نقاط البيع](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/create-purchase-orders-pos)  |  تم تحسين عملية المخزون الوارد في تطبيق نقاط البيع (POS) للسماح للمستخدمين بإنشاء طلبات أوامر الشراء وتعديلها وتأكيدها. |  إدارة الميزات<p>*القدرة على إنشاء طلب أمر شراء في نقطة البيع (POS)*   |



## <a name="additional-resources"></a>الموارد الإضافية

### <a name="platform-updates-for-finance-and-operations-apps"></a>تحديثات النظام الأساسي لتطبيقات التمويل والعمليات

يتضمن الإصدار 10.0.31 من Microsoft Dynamics 365 Commerce تحديثات النظام الأساسي. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.31 من تطبيقات التمويل والعمليات (فبراير 2023)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-31.md). 
  

### <a name="bug-fixes"></a>إصلاح الأخطاء

للحصول على معلومات حول إصلاحات الأخطاء المضمنة في كل تحديث من التحديثات التي تعد جزءًا من الإصدار 10.0.31، قم بتسجيل الدخول إلى Microsoft Dynamics Lifecycle Services واعرض [مقالة قاعدة المعارف](https://fix.lcs.dynamics.com/Issue/Details?bugId=758525).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 وسحابات الصناعة: خطة إصدار 2 لعام 2022

هل تتساءل عن الإمكانات القادمة والتي تم إصدارها حديثًا في أيٍّ من تطبيقات العمل أو النظام الأساسي الخاص بنا؟

راجع [Dynamics 365 وسحابات الصناعة: خطة إصدار 2 لعام 2022](/dynamics365-release-plan/2022wave2/). لقد التقطنا جميع التفاصيل بشكل شامل، ومن الأعلى إلى الأسفل، في مستند واحد يمكنك استخدامه للتخطيط.

### <a name="removed-and-deprecated-commerce-features"></a>ميزات التجارة التي تمت إزالتها وإهمالها

توضح الميزات التي [تمت ازالتها أو إهمالها في Dynamics 365 Commerce](removed-deprecated-features-commerce.md) المقالة الميزات التي تمت ازالتها أو إهمالها للتجارة.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

قبل إزالة أي ميزة من المنتج، سيتم إعلان إشعار إهمال في المقال [الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Commerce](removed-deprecated-features-commerce.md) 12 شهرًا قبل الإزالة.


بالنسبة للتغييرات الفاصلة التي تؤثر فقط على وقت التحويل البرمجي، ولكنها متوافقة ثنائيًا مع بيئة الاختبار المعزولة وبيئات الإنتاج، فسيكون وقت الإهلاك أقل من 12 شهرًا. بشكل عام، هذه هي التحديثات الوظيفية التي يجب إجراؤها للمحول البرمجي.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
