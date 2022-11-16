---
title: مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce
description: يصف هذا المقال كيفية مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce (POS).
author: gvrmohanreddy
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f339ae031f11ad850dab47f84bc9823cf6776e74
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746087"
---
# <a name="synchronize-task-management-between-microsoft-teams-and-dynamics-365-commerce-pos"></a>مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

يصف هذا المقال كيفية مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce (POS).

أحد الأغراض الرئيسية لتكامل Teams هو تمكين مزامنة إدارة المهام بين تطبيق نقطة البيع (POS) وTeams. بهذه الطريقة، يمكن لموظفي المتجر استخدام إما تطبيق نقطة البيع (POS) أو Teams لإدارة المهام، ولا يتعين عليهم تبديل التطبيقات.

نظرًا لاستخدام Planner كمستودع للمهام في Teams، يجب أن يكون هناك ارتباط بين Teams وDynamics 365 Commerce. يتم إنشاء هذا الارتباط باستخدام معرف خطة معين لفريق متجر معين.

توضح الإجراءات التالية كيفية إعداد مزامنة إدارة المهام بين تطبيقي نقطة البيع (POS) وTeams.

## <a name="link-pos-and-teams-for-task-management"></a>ربط نقطة البيع وTeams لإدارة المهام

لربط نقطة البيع وتطبيقات Microsoft Teams لإدارة المهام في إدارة Commerce، اتبع هذه الخطوات.

> [!NOTE]
> قبل محاولة دمج إدارة المهام مع Teams، تأكد من تمكين تكامل [Dynamics 365 Commerce و Microsoft Teams](enable-teams-integration.md). 

1. انتقل إلى **Retail وCommerce \> إدارة المهام \> تكامل المهام مع Microsoft Teams**.
1. في جزء الإجراءات، حدد **تحرير**.
1. قم بتعيين خيار **تمكين تكامل إدارة المهام** إلى **نعم**.
1. في جزء الإجراءات، حدد **حفظ**.
1. في جزء الإجراء، حدد **إعداد إدارة المهام**. يجب أن تتلقى إخطارًا يشير إلى أنه جاري إنشاء وظيفة دفعية تحمل الاسم **توفير Teams**.
1. انتقل إلى **إدارة النظام \> الاستعلامات \> وظائف الدفعات**، وابحث عن الوظيفة الأحدث التي تشتمل على وصف **توفير Teams**. انتظر حتى انتهاء تشغيل هذه الوظيفة.
1. قم بتشغيل **وظيفة CDX رقم 1070** لنشر معرف الخطة ومراجع المتجر إلى خادم Retail.

## <a name="publish-a-test-task-list-in-teams"></a>نشر قائمة مهام الاختبار في Teams

يفترض الإجراء التالي أن فرق متجرك تستخدم تكامل إدارة مهام Microsoft Teams مع Commerce للمرة الأولى.

لنشر قائمة مهام اختبار في Teams، اتبع الخطوات التالية.

1. قم بتسجيل الدخول إلى Teams كمدير اتصالات. عادةً ما يكون مديرو الاتصالات مستخدمين لديهم دور **المدير الإقليمي** في Commerce.
1. في جزء التنقل الأيمن، حدد **المهام حسب Planner**
1. في علامة التبويب **القوائم المنشورة**، حدد **قائمة جديدة** في أسفل اليسار، وقم بتسمية القائمة الجديدة **قائمة مهام الاختبار**.
1. حدد **إنشاء**. تظهر القائمة الجديدة ضمن **المسودات**.
1. ضمن **عنوان المهمة**، قم بإعطاء المهمة الأولى العنوان **تكامل Teams في الاختبارات**. ثم حدد **إدخال**.
1. في قائمة **المسودات**، حدد قائمة المهام. وبعد ذلك، حدد  **نشر** في الزاوية العلوية اليمنى.
1. في مربع الحوار **تحديد من تريد النشر إليه**، حدد الفرق التي يجب أن تتلقى قائمة مهام الاختبار.
1. حدد **التالي** لمراجعة خطة المنشور. إذا كان يجب عليك إجراء التغييرات، فحدد  **السابق**. 
1. حدد **تأكيد للمتابعة**، ثم حدد **نشر**.
1. بعد اكتمال النشر، تظهر رسالة أعلى علامة التبويب **القوائم المنشورة** تشير إلى ما إذا كان قد تم تسليم قائمة المهام الخاصة بك بنجاح.

لمزيد من المعلومات، راجع [نشر قوائم المهام لإنشاء وتعقب العمل في مؤسستك](https://support.microsoft.com/office/publish-task-lists-to-create-and-track-work-in-your-organization-095409b3-f5af-40aa-9f9e-339b54e705df).

> [!NOTE]
> بعد أن يتم نشر قائمة المهام بنجاح في Teams، سيتم عرض المهام في نقطة البيع. ثم يجب على مديري نقاط البيع والصرافين تشغيل تسجيل دخول Azure AD في نقطة البيع. لمزيد من المعلومات، راجع المقال [تمكين مصادقة Azure Active Directory لتسجيل دخول نقطة البيع](aad-pos-logon.md). 

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على تكامل Dynamics 365 Commerce وMicrosoft Teams](commerce-teams-integration.md)

[تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams](enable-teams-integration.md)

[توفير Microsoft Teams من Dynamics 365 Commerce](provision-teams-from-commerce.md)

[إدارة أدوار المستخدمين في Microsoft Teams](manage-user-roles-teams.md)

[تعيين المتاجر والفرق عند وجود فرق موجودة مسبقًا في Microsoft Teams](map-stores-existing-teams.md)

[الأسئلة الشائعة حول تكامل Dynamics 365 Commerce وMicrosoft Teams](teams-integration-faq.md)
