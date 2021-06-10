---
title: ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (1‏ مايو 2020)
description: يصف هذا المقال الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 1 مايو 2020.
author: andreabichsel
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8ceea10b3157fee410e5db6e1d8c9a0366e30e2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6050959"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a>ما الجديد أو المتغير في Dynamics 365 Human Resources‏ (1‏ مايو 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

تصف هذه المقالة الميزات الجديدة أو المتغيرة في Dynamics 365 Human Resources. يتم تطبيق التغييرات على رقم الإصدار 8.1.3196. تشير الأرقام الموجودة بين أقواس في بعض العناوين إلى أرقام دعم LCS للحصول على مرجع.

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a>كيانات إدارة الأداء الجديدة متوفرة في إطار عمل إدارة البيانات (DMF)

تتوفر الآن الكيانات التالية. إذا لم تتمكن من رؤية هذه الكيانات في قائمة الكيانات، فاستخدم الخيار **تحديث الكيانات** في **معلمات إطار العمل > إعدادات الكيان > تحديث قائمة الكيانات**.

- **اختصاص المناقشة**
- **أهداف المناقشة**
- **قياس المناقشة**
- **موضع المناقشة**
- **دفتر يومية الأداء**
- **القياس**
- **قياس الهدف**

بالإضافة إلى ذلك، تمت إضافة **النتيجة الإجمالية** و **متوسط النتيجة** إلى كيان **المناقشة**.

## <a name="increase-length-of-leave-request-comments-275641"></a>زيادة طول تعليقات طلب الاجازه (275641)

تسمح الآن التعليقات على طلبات الإجازات بأكثر من 100 حرفًا.

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a>لا تظهر التعليقات النهائية على المراجعات عند تسجيل المدير أو الموظف في شركه مختلفة (431688)

ستظهر الآن كافة التعليقات عند عرض المراجعات.

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a>الارتباطات المعرفة من قبل المستخدم غير مدعومة على نموذج العامل الجديد (390374)

تم الآن تمكين الارتباطات المعرفة من قبل المستخدم في نموذج **العامل** المبسط.

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a>HcmRatingLevelEntity يسبب في حدوث عطل في OData API (439476)

يعمل هذا التغيير على تصحيح تعطل API. حدث هذا الخطأ بسبب وجود اسم مكرر.

## <a name="in-preview"></a>قيد المعاينة

## <a name="leave-suspension"></a>تعليق الإجازة

يمكنك تعليق الإجازة والغياب في Human Resources لأحد الموظفين. يؤدي تعليق الإجازة إلى إيقاف استحقاقات أنواع الإجازة المحددة. إذا حدث التعليق بعد معالجة الاستحقاق، فإن تعليق الإجازة يؤدي إلى إنشاء تسوية تناسبية لرصيد إجازات الموظف. لمزيد من المعلومات، راجع [تعليق الإجازة](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>تحديث تجربة المستخدم للاشاره إلى ان الاستحقاق معلق (429550)

وتشير تجربة المستخدم الآن إلى انه تم تعليق الاستحقاق لإحدى الخطط.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>تعليق استحقاق الإجازه لأنواع الإجازات المحددة (272447)

في هذا الإصدار، يمكن للموارد البشرية إنشاء قاعده لكي يتم تعليق استحقاق الإجازات للموظفين الذين لديهم طلبات الاجازه التي تم إدخالها لإجازه غير مدفوعة. يمكن أن تكون الإجازة غير المدفوع نوعا، ولكن ليس من الضروري أن تكون كذلك. يمكنك تعليق أي إجازة استنادا إلى نوع إجازة آخر.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>يتوفر كيان DMF لتعليقات الاستحقاق (429549)

يتوفر كيان DMF الآن لتعليقات الاستحقاق.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>إضافة كود السبب إلى تعليقات الاستحقاق (429547)

تمت إضافه أكواد السبب إلى تعليق الاستحقاق.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>بدء النقل من معلمات الموارد البشرية إلى معلمات الإجازة والغياب‬

يبدأ هذا الإصدار في دمج معلمات الموارد البشرية بمعلمات الإجازة والغياب‬.

## <a name="carry-forward-rules"></a>قواعد نقل الإجازة

يمكنك تحديد نوع الإجازة المنقولة للأرصدة المنقولة حيث يتم تحويل تسويات النقل. على سبيل المثال، إذا قام أحد الموظفين بنقل إجازة من 10 أيام، يمكنك انتقاء نوع إجازة آخر لمدة العشرة أيام هذه. لمزيد من المعلومات، راجع [تكوين أنواع الإجازة والغياب](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>مشكلات معروفة

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>معاينة SharePoint لا تعمل في بعض البيئات

إذا كانت معاينة المستندات للمستندات المخزنة في SharePoint لا تعمل، جرب الإجراء التالي:

1. تحقق من وجود بريد إلكتروني مقترن بحساب المستخدم المسؤول. يمكنك عرض هذه المعلومات في صفحة **المستخدم**. إذا لم يتم إعداد البريد الإلكتروني، فأنت بحاجة إلى إضافة البريد الإلكتروني والموفر مع وظيفة Excel في OData. افتراضيًا، لا يكون عنوان البريد الإلكتروني موجودًا في تصميم Excel. ستحتاج إلى تحرير تصميم Excel، وإضافة جميع الحقول والتطبيق والتحديث. بمجرد إكمال هذه الخطوات، يمكنك تحديث حساب المسؤول.

2. بعد أن يحتوي حساب المسؤول على حساب بريد إلكتروني مقترن، قم بتسجيل الدخول إلى Human Resources باستخدام بيانات اعتماد المسؤول.

3. يمكنك الوصول إلى مرفق في SharePoint لبدء معاينة المستند.

4. قم بتسجيل الدخول باستخدام حساب مستخدم آخر له حق الوصول إلى المرفقات وتحقق من أن المعاينة تعمل كما هو متوقع.

## <a name="see-also"></a>راجع أيضًا

[المزايا الجديدة أو المتغيرة في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 2 من إصدار Dynamics 365 Human Resources  2019](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]