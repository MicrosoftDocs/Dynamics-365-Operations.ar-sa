---
title: إيقاف العمل بتطبيقي Dynamics 365 Talent - ‏ Attract وOnboard
description: توضح هذه المقالة إيقاف العمل بتطبيقي Dynamics 365 Talent ‎‎Attract‏و ‎Onboard‎‎.
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 3039b0a837335a777cdd6ff22b8b6e7c014ef956
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845073"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>إيقاف العمل بتطبيقي Dynamics 365 Talent: Attract وOnboard


لقد قمنا في 2019 ديسمبر بالإعلان عن إيقاف العمل بتطبيقي Dynamics 365 Talent -‏ Attract وOnboard في 1 فبراير 2022، مما يمنح العملاء مدة سنتين للتخطيط.

لمزيد من المعلومات فيما يتعلق استبعاد هذين التطبيقين، راجع:
 - [إيقاف العمل بتطبيقي Dynamics 365 Talent - Attract وDynamics 365 Talent: Onboard](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [بناء قوى عاملة أكثر نجاحًا باستخدام Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

سنستمر في دعم Dynamics 365 Human Resources، الأمر الذي يساعد عملائنا في الحصول علي رؤى القوى العاملة المطلوبة لإنشاء تجارب الموظفين المعتمدة على البيانات عبر نواحٍ متعددة، مثل:

- التعويض
- المزايا‬
- الإجازة والغياب
- توافق
- كشف الرواتب
- ملاحظات الأداء
- التدريب والترخيص
- برامج الخدمة الذاتية

## <a name="dynamics-365-talent-apps-retirement-faq"></a>الأسئلة المتداولة حول إيقاف العمل بتطبيقي Dynamics 365 Talent

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>ما هي تجربة المستخدم لتطبيقي Dynamics 365 Talent - ‏Attract وOnboard اعتبارًا من 1 فبراير 2022؟

لن يتمكن المستخدمون من استخدام التطبيقات ويُعاد توجيههم إلى صفحة إيقاف العمل بالتطبيقات.

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>هل سيتمكن العملاء من متابعة تصدير البيانات لتطبيقي Dynamics 365 Talent - ‏Attract وOnboard بعد 1 فبراير 2022؟
  
لا، تم الإعلان عن إيقاف العمل بالتطبيقين في ديسمبر 2019 وقد تم توفير قدرات التصدير المطلوبة حتى 1 فبراير 2022. 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>هل سيتم حذف بيانات العملاء ذات الصلة بتطبيقات Dynamics 365 Talent - ‏Attract وOnboard في Dataverse بعد 1 فبراير 2022؟

لا، ستبقى كيانات Dataverse في بيئة العميل في Microsoft Dataverse حتى بعد إيقاف العمل إلا إذا تم حذف حل Talent لإدارة رؤوس الأموال البشرية أو إزالة تثبيته.

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>أنا أعرف اسم بيئة Talent. كيف يمكنني رؤية بيانات Attract وOnboard في Dataverse؟

1.  سجل دخولك إلى Power Apps: https://make.powerapps.com
2.  حدد البيئة حيث ترغب في رؤية بيانات Attract وOnboard.
3.  انتقل إلى **Dataverse > الجداول**. 
4.  اكتب “msdyn_” في **البحث**. إذا رأيت قائمة الجداول التي تبدأ بـ "msdyn_" + أسماء الجداول (مثال: msdyn_candidate)، فهذا يعني أنك عثرت على البيئة مع بيانات Attract وOnboard

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>لا أعرف اسم بيئة Talent. كيف يمكنني العثور على البيئة التي تحتوي على بيانات التطبيقين Dynamics 365 Talent: Attract وDynamics 365 Talent: Onboard؟

1)  سجل دخولك إلى مركز إدارة Power Platform:https://admin.powerplatform.microsoft.com/
2)  حدد **بيئات**.
3)  حدد بيئة معينة لتقييمها.
4)  حدد **الموارد > تطبيقات Dynamics 365**.
5)  إذا رأيت الحل **HCM Talent** مثبتًا، فيجب أن تكون بيانات Attract وOnboard مخزنة في هذه البيئة. 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> يتم أيضًا استخدام حل **HCM Talent** في Dynamics 365 Human Resources.
