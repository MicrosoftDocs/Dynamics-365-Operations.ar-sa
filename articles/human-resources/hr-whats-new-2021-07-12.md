---
title: ما الجديد والمتغير في Dynamics 365 Human Resources  12 يوليو 2021
description: توضح هذه المقالة الميزات الجديدة أو المتغيرة في Microsoft Dynamics 365 Human Resources لإصدار 12 يوليو 2021.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-12
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 259004773c4e5a7d8865d563da9bcfea3a116632
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870947"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-12-2021"></a>ما الجديد والمتغير في Dynamics 365 Human Resources  12 يوليو 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

توضح هذه المقالة الميزات الجديدة أو المتغيرة أو التي ستصدر قريبًا في Dynamics 365 Human Resources.

لمزيد من المعلومات حول عملية التحديث الخاصة بنا والجدول، راجع [عملية التحديث](hr-admin-setup-update-process.md).

لمزيد من المعلومات حول الميزات الجديدة وتواريخ التوفر العام المتوقعة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>في هذا الإصدار

يتضمن هذا الإصدار الميزات الجديدة التالية وإصلاحات الأخطاء. يتم تطبيق التغييرات على رقم الإصدار 8.1.4353.

### <a name="new-features"></a>الميزات الجديدة

تتوفر الميزات التالية بشكل عام مع هذا الإصدار.

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
|  تبديل عرض سنوات الخدمة | |توفر هذه الميزة الخيار لاستخدام تواريخ مختلفة لحساب سنوات الخدمة المعروضة في الصفحة **إدخال الموظف المبسط** وفي النموذج **أشخاص**.  سيتوفر ذلك في [معلمات الموارد البشرية](/dynamics365/human-resources/hr-setup-parameters). |


### <a name="bug-fixes"></a>إصلاح الأخطاء

يتضمن هذا الإصدار إصلاحات الأخطاء التالية.

> [!NOTE]
> هدفنا هو الحصول على هذه المعلومات لك في أسرع وقت ممكن. يمكن أن نقوم بتحديث هذه المقالة لتضمين إصلاحات الأخطاء التي أجريتها في البناء بعد أن يتم نشر هذه المقالة مبدئيًا.

| رقم الإصدار | المشكلة |  ‏‏الوصف‬ |
| --- | --- | --- |
| 595871 | حول جزء في الموارد البشرية له مصطلحات Dataverse غير صحيحة | مع تغيير العلامة التجارية Common Data Service إلى Dataverse، تم تحديث المصطلحات في جزء معلومات Microsoft Dynamics 365 Human Resources (**تعليمات ودعم > حول**). |
| 598676 | نموذج إدخال الموظف المبسط يتجاوز المهمة يمكن أن يخلق خطأ عند استخدامه مع طريقة العرض المحفوظة| في صفحة **العامل**، إذا تم تشغيل ميزة "إدخال الموظف المبسط"، فقد يفشل التطبيق إذا تم تعيين **فتح التحرير دوما على طريقة العرض المحفوظة**. |
| 592344 |يجب قراءة قسم شركات العمال على الموقف فقط عندما يتم تمكين إدارة المزايا | يتم إنشاء معلومات شركات العمال باستخدام وظائف الفوائد القديمة.  عند تمكين إدارة الفوائد، سيتم قراءة الحقول فقط. عند تشغيل إدارة المزايا وتعيين **نماذج المزايا القديمة** إلى **نعم** في المعلمات المشتركة للموارد البشرية، سيتم إخفاء علامة التبويب **تعويض العمال**. |
| 598617 | **HcmDiscussion** نموذج تنشيط علامة التبويب يسبب حلقة لانهائية عند تطبيق التخصيصات | عندما يكون كل من الشبكة وعرض التفاصيل **مفتوحة دائما للتحرير** قيد التشغيل، رمز تنشيط علامة التبويب في أسلوب المهمة تجاوز يتعارض مع التخصيص حول ما ينبغي أن يكون عنصر التحكم التركيز ويخلق حلقة لانهائية. |
| 593553 | يظهر حقل تاريخ دفتر اليومية في دفتر يومية الأداء بالتوقيت العالمي المنسق | يعرض الحقل **تاريخ دفتر اليومية** لدفاتر يومية الأداء في المنطقة الزمنية UTC بدلا من المنطقة الزمنية المعرفة في إعداد تاريخ النظام، مما يؤدي إلى أن يكون التاريخ غير صحيح لبعض المناطق الزمنية. |
| 586930 | فتح الأنشطة لأهداف الأداء يفتح سجلا مختلفا تماما | عند تمكين ميزة "عروض التقارير الموسعة لدفاتر يومية الأداء" في إدارة الميزات، يؤدي تحديد أهداف الأداء للتقارير الموسعة في علامة التبويب **فريقي** في **الخدمة الذاتية للموظف** إلى فتح أهداف الموظف بدلا من الموظف المحدد. |
| 569959 |  لا يقوم كيان HcmPositionWorkerAssignmentV2 بتعيين عامل إلى منصب | تلقى المستخدمون خطأ عند إضافة سجل تعيين موضع عبر الكيان وفشل النشر. |
| 582259 | يستخدم تقرير VETS 4212 نموذج 2017 بدلا من نموذج 2020 | تم التحديث إلى تنسيق 2020.  لتحميل التنسيق الجديد، انتقل إلى **تكوينات التقرير** واحذف تقرير VETS-4212 في العمود الأيمن. انتقل إلى **التقارير الإلكترونية - المستودعات - موارد الموارد البشرية** وحدد **فتح**.  حدد **VETS-4212 PDF المطبوع** ثم حدد **استيراد**.|


## <a name="in-preview"></a>قيد المعاينة

الميزات الجديدة التالية موجودة في المعاينة. للحصول على مزيد من المعلومات حول تشغيل الميزات أو إيقاف تشغيلها، راجع [إدارة الميزات](hr-admin-manage-features.md).

| الميزة | خطة الإصدار | الوثائق |
| --- | --- | --- |
| مساحة عمل إدارة المزايا | [مساحة عمل إدارة المزايا (معاينة)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [مساحة عمل إدارة المزايا](hr-benefits-management-workspace.md) |
| تمكين تكامل كشوف المرتبات المبسط (واجهات برمجة تطبيقات تكامل الرواتب) | [تمكين التكامل المبسط مع موفري كشوف المرتبات](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [‏‫واجهة برمجة التطبيقات لتكامل كشف الرواتب](hr-admin-integration-payroll-api-introduction.md)|
|  تمكين مدير الغياب لإدارة الإجازة | [تمكين مدير الغياب لإدارة الإجازة](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | [تكوين دور مدير الغياب](https://go.microsoft.com/fwlink/?linkid=2168107)|
|  تكوين متطلبات المرفق لكل نوع إجازة | [تكوين متطلبات المرفق لكل نوع إجازة](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[تكوين أنواع الإجازة والغياب](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  تكوين وحدات الإجازات لكل نوع إجازة | [تكوين وحدات الإجازات لكل نوع إجازة](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[تكوين أنواع الإجازة والغياب](https://go.microsoft.com/fwlink/?linkid=2168215)|
| تمكين وضع علامة جاهز للدفع للموظفين | [تمكين وضع علامة جاهز للدفع للموظفين](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [جاهز للدفع](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>قريبًا

| الميزة | تفاصيل |
| --- | --- |
| Platform update 10.0.20 (44) | تمت جدولة تحديث النظام الأساسي 10.0.20 بحيث يبدأ نشره مع إصدار الخدمة في 26 يوليو 2021. لمعرفة المزيد، راجع [تحديثات النظام الأساسي للإصدار 10.0.20 من تطبيقات التمويل والعمليات (أغسطس 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20). |

للحصول على قائمة كاملة بالميزات المخططة والإصدارات المجدولة الخاصة بها، راجع [نظرة عامة حول Dynamics 365 Human Resources الإصدار 2021، الموجة 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>راجع أيضًا

[ما الجديد أو المتغير في Human Resources](hr-admin-whats-new.md)</br>
[نظره عامة حول الموجة 1 من إصدار Dynamics 365 Human Resources  2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[تحديث العملية](hr-admin-setup-update-process.md)</br>
[إدارة الميزات](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
