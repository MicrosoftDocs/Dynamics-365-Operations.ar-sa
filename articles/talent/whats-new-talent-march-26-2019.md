---
title: ما الجديد أو المتغير في Dynamics 365 Talent (26 مارس 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-26
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 17eae6c2aa2a1305b1d6f403c595c022f71da48f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529080"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-26-2019"></a>ما الجديد أو المتغير في Dynamics 365 Talent (26 مارس 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في Dynamics 365 Talent.

## <a name="changes-in-attract"></a>التغييرات في Attract

### <a name="enhancements-to-interview-scheduling"></a>تحسينات في جدولة المقابلات
تتوفر التحسينات التالية في جدولة المقابلات.

- بإمكان مدير التوظيف أو مسؤول التعيين الآن تشغيل تذكير المحاور يدويًا لمطالبته بإرسال الملاحظات. ويعتبر البريد الإلكتروني المقترن بالتذكير قابلاً للتكوين أيضًا.
- أثناء مشاركة ملخص المقابلة مع المرشح، بإمكان مجدول المقابلة اختيار إخفاء أسماء المحاورين وأيضًا اختيار إخفاء الصفوف من طريقة عرض ملخص المقابلة.

## <a name="changes-in-onboard"></a>التغييرات في Onboard

### <a name="embedded-images-in-activities"></a>الصور المضمنة في الأنشطة
يمكنك الآن تضمين الصور مباشرة في الأنشطة. بالإضافة إلى القدرة على نسخ ولصق الرسومات من الويب، يمكنك تحميل الصور من نظام ملفاتك المحلي. يتحدد حجم النشاط بميغابايت واحد. وإذا كانت الصورة كبيرة جدًا، فيمكنك تغيير حجمها ومحاولة تحميلها مرة أخرى.

[![التعيين](./media/embedimages.png)](./media/embedimages.png)

يتضمن هذا الإصدار إصلاحات أخطاء ثانوية في Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>التغييرات في Core HR
**الإصدار 8.1.2210**

### <a name="custom-field-support-available-for-select-entities-in-common-data-service"></a>يتوفر دعم الحقول المخصصة لكيانات محددة في Common Data Service 

تدعم الآن كيانات Common Data Service التالية الحقوق المخصصة المنشأة في Talent:

- العامل
- الأصل العرقي
- حالة الخبرة
- كود اللغة
- وظيفة
- نوع الوظيفة
- مهمة الوظيفة
- المهنة
- نوع المنصب
 
### <a name="employment-history-not-displayed-chronologically"></a>لا يظهر سجل التوظيف‬ حسب الترتيب الزمني
مع هذا التغيير، تعرض الآن صفحة سجل التوظيف سجلات التوظيف حسب الترتيب الزمني، بطريقة مستقلة عن الشركة. يمكنك أيضًا استخدام خيارات الفرز للفرز حسب الشركة.

### <a name="fixed-compensation-plans-dont-appear-when-restricting-user-by-company-in-security"></a>لا تظهر خطط التعويض الثابتة عند تقييد المستخدم حسب الشركة في الأمان.
في هذا الإصدار، تظهر خطط التعويض الثابتة عند تقييد المستخدمين حسب الشركة في الأمان. ستتم مراعاة جميع إعدادات الأمان، وستظهر الخطط الثابتة لتلك لشركات التي يملك المستخدم أذونات الوصول إليها. 

### <a name="cant-delete-job-records-using-open-in-excel-option-in-talent"></a>لا يمكن حذف سجلات الوظيفة باستخدام الخيار "فتح في Excel" في Talent
مع هذا الإصدار، يمكنك الآن إزالة سجلات الوظيفة باستخدام الخيار **فتح في Excel** في Talent.

### <a name="upgrade-to-common-data-service"></a>الترقية إلى Common Data Service
تقترب المواعيد النهائية للترقية إلى Common Data Service بسرعة. سجّل دخولك إلى مركز إدارة Power Apps لتحديد ما إذا كانت قاعدة بياناتك تحتاج إلى ترقية. للحصول على مزيد من المعلومات حول المواعيد النهائية والخطوات الضرورية للترقية، راجع [الترقية إلى Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).

## <a name="in-preview"></a>قيد المعاينة

للحصول على معلومات حول ميزات المعاينة، راجع [الوصول إلى ميزات المعاينة في Microsoft Dynamics 365 Talent](./access-preview-feature.md).

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>السماح بتعيين أكواد الأسباب على أنواع الإجازات
قد تحتاج الشركات إلى معلومات إضافية تتعلق بطلبات الإجازات. للحصول على هذه المعلومات، يحتاج الموظفون إلى تضمين كود سبب على طلبات الإجازات. مع هذا الإصدار، يمكنك الآن تحديد أكواد الأسباب المرتبطة بنوع إجازة محدد وتمكين الموظفين من تحديد كود سبب في طلبات الإجازات.

### <a name="configure-reason-codes-to-be-required-when-submitting-time-off-for-certain-leave-types"></a>تكوين أكواد الأسباب بحيث تكون مطلوبة عند إرسال طلبات الإجازات لبعض أنواع الإجازات
قد تطالب المؤسسات بتعيين أكواد الأسباب على أنواع إجازات معينة عند قيام الموظفين بتقديم طلب إجازة. قد يكون هذا مطلوبًا استنادًا إلى المتطلبات التنظيمية في البلد/المنطقة أو سياسة شركة. يوفر هذا الإصدار لمسؤولي الموارد البشرية القدرة على تحديد أنواع الإجازات التي تحتاج إلى كود سبب. سيتم تنفيذ ذلك عند قيام الموظفين بإرسال طلبات الإجازات حيث تحتاج الإجازة إلى كود سبب.

## <a name="coming-soon"></a>قريبًا

###  <a name="advanced-compensation-security-fixed-and-variable"></a>أمان التعويض المتقدم (التعويض الثابت والمتغير)
في الكثير من المؤسسات، قد يتوفر لدى مدراء التعويضات والمزايا حق الوصول إلى سجلات تعويض معينة فقط. وقد تكون هذه السجلات مخصصة للمدراء التنفيذيين أو الموظفين الإقليميين. مع هذا التغيير، سيتمكن قسم الموارد البشرية من إدارة خطط التعويض لمجموعات مختلفة من الموظفين في المؤسسة والمحافظة عليها. يمكن تعيين أدوار أمان إلى خطط التعويض الثابت والمتغير التي تحدد حق الوصول إلى الخطط وبيانات الموظفين ذات الصلة بها، على سبيل المثال، معلومات حول الرواتب أو سجلات المكافآت. وحدها الأدوار التي تم منح حق الوصول لها يمكنها معالجة التعويض لهؤلاء الموظفون.

###  <a name="email-support-for-alerts"></a>دعم البريد الإلكتروني للتنبيهات
مع إصدار Platform update 25 لـ Finance and Operations، بإمكان المستخدمين إنشاء قواعد تنبيه ترسل بشكل تلقائي إعلامات بالبريد الإلكتروني إلى جهات الاتصال عند تشغيلها بواسطة حدث. 

### <a name="duplicate-employee-checks-user-interface-changes"></a>عمليات التحقق من الموظفين المكررين: تغييرات واجهة المستخدم‬
مع هذا التغيير، يتم الكشف عن التكرارات عند إدخال حقول الأسماء، وتعرض الحالة عدد التكرارات التي تم العثور عليها. يمكنك تحديد الارتباط المتوفر لفتح صفحة جديدة لتقييم ما إذا كان يجب استخدام المطابقة التي تم الكشف عنها. لتجنب مقاطعة إدخال البيانات، لا يفتح نموذج التكرارات بشكل تلقائي.


[!INCLUDE[footer-include](../includes/footer-banner.md)]