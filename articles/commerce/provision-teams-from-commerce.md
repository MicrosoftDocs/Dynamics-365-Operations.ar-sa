---
title: توفير Microsoft Teams من Dynamics 365 Commerce
description: يصف هذا الموضوع كيفية توفير Microsoft Teams باستخدام بيانات تنظيمية من Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 39dabeb8bacc4ebc3376f53f15c7fb292c8d301c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352098"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a>توفير Microsoft Teams من Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

يصف هذا الموضوع كيفية توفير Microsoft Teams باستخدام بيانات تنظيمية من Dynamics 365 Commerce.

يوفر Dynamics 365 Commerce طريقه سهله لتوفير Teams إذا لم تقم بعد بإعداد فرق لمتاجر البيع بالتجزئة الخاصة بك. ومن خلال الاستفادة من المعلومات التي تم تحديدها جيدا من Commerce التي ترغب في استخدامها في Teams، يمكنك مساعده موظفي المتجر علي البدء في Teams. تتضمن هذه المعلومات التسلسل الهرمي التنظيمي وأسماء المتاجر ومعلومات الموظف وحسابات Azure Active Directory (Azure AD). 

لعمليه توفير Teams خطوتين أساسيتين:

1. في Teams، قم بإنشاء فريق لكل متجر للبيع بالتجزئة، وأضف عمال المتجر كاعضاء في الفريق المناسب. إذا كان الموظف مرتبطا بأكثر من متجر للبيع بالتجزئة، ستعكس عضويه الفريق هذه الحقيقة. سيتم إنشاء فريق الاتصالات الذي يتضمن المديرين الإقليميين كاعضاء للمساعدة في نشر المهام من Teams.
1. تحميل التدرج الهرمي التنظيمي من Commerce إلى Teams.

## <a name="provision-teams-in-commerce-headquarters"></a>توفير Teams في إدارة Commerce

قبل توفير Microsoft Teams، قم بإكمال المهام التالية:

- التاكد من جعل كافة المديرين الإقليميين مديري الاتصالات.
- تاكد من ان حساب Azure الخاص بكل مدير متجر وعامله قد تم اقرانه بسجل العامل الخاص بالمدير أو العامل في إدارة Commerce.

لتوفير Teams في إدارة Commerce، اتبع هذه الخطوات.

1. انتقل إلى **Retail وCommerce \> إعداد القناة \> Microsoft Teams تكوين التكامل**.
1. في جزء الإجراءات، حدد **توفير الفرق**. يتم إنشاء مهمة المجموعة التي تسمي **توفير Teams**.
1. انتقل إلى **إدارة النظام \> الاستعلامات \> وظائف الدفعات**، وابحث عن الوظيفة الأحدث التي تشتمل على وصف **توفير Teams**. انتظر حتى انتهاء تشغيل هذه الوظيفة.

> [!TIP]
> إذا لم يكن أي من المديرين الإقليميين ومديري المتاجر وعمال المتجر مرتبطين بترخيص Teams، فقد تتلقى رسالة الخطأ التالية: "فشل استرداد فئات Sku القابلة للتطبيق للمستخدم." لحل المشكلة، حدد **مزامنة الفرق والأعضاء** في جزء الإجراءات.

<!-- ![Dynamics 365 Commerce - Teams integration configuration.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a>تحقق من صحة توفير Teams في مركز إدارة Teams

للتحقق من صحة توفير Microsoft Teams في مركز إدارة Microsoft Teams، اتبع الخطوات التالية.
    
1. انتقل إلى [مركز إدارة Teams](https://admin.teams.microsoft.com/)، وقم بتسجيل الدخول كمسؤول عن مستأجر التجارة الإلكترونية الخاص بك.
1. في جزء التنقل الأيمن، حدد **Teams** لتوسيعه، ثم حدد **إدارة الفرق**.
1. تأكد من إنشاء فريق واحد لكل متجر تجزئة لـ Commerce.
1. حدد فريقًا وتأكد من إضافة عمال المتجر إليه كأعضاء.
1. في جزء التنقل الأيمن، حدد **المستخدمين**، وتاكد من أضافه كافة الموظفين المتجر في كافة المتاجر كمستخدمين.

يبين الرسم التوضيحي التالي مثالا على صفحة **إدارة الفرق** في مركز إدارة Teams.

![مثال على صفحة "إدارة الفرق" في مركز إدارة Teams.](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a>تحميل التدرج الهرمي التنظيمي من Commerce إلى Teams
    
يمكن استخدام التسلسل الهرمي التنظيمي لـ Commerce في Microsoft Teams لنشر المهام على جميع المتاجر أو المتاجر المحددة التي تستخدم نفس بنية التسلسل الهرمي.

لتحميل تسلسل هرمي تنظيمي لـ Commerce إلى Teams، اتبع هذه الخطوات.
    
1. في إدارة Commerce، انتقل إلى **Retail وCommerce \> إعداد القنوات \> تكوين تكامل Microsoft Teams**.
1. حدد **تحميل التدرج الهرمي المستهدف**، ثم حدد **متاجر البيع بالتجزئة حسب المنطقة** لتنزيل ملف قيم مفصوله بفواصل (CSV) في التدرج الهرمي التنظيمي.
1. قم بتثبيت وحدة Microsoft Teams PowerShell باتباع الخطوات في [تثبيت Microsoft Teams PowerShell](/microsoftteams/teams-powershell-install).
1. عند مطالبتك في نافذة Teams PowerShell، قم بتسجيل الدخول باستخدام حساب المسؤول لمشتأجر Azure AD الخاص بك.
1. اتبع الخطوات الواردة في [إعداد التدرج الهرمي لاستهداف فريقك](/microsoftteams/set-up-your-team-hierarchy) لتحميل ملف CSV لتدرج هرمي الاستهداف.

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a>التحقق من تحميل التدرج الهرمي التنظيمي إلى Teams

للتحقق من تحميل التدرج الهرمي التنظيمي إلى Microsoft Teams، اتبع هذه الخطوات.

1. قم بتسجيل الدخول إلى Teams كمدير اتصالات.
1. في جزء التنقل الأيمن، حدد **المهام حسب Planner**
1. في علامة التبويب **القوائم المنشورة**، قم بإنشاء قائمه جديده تحتوي علي مهمة وهميه.
1. حدد **نشر**. يجب ان يظهر التدرج الهرمي التنظيمي في مربع الحوار **تحديد الأشخاص الذين سيتم النشر اليهم**، كما هو موضح في المثال الموجود في التوضيح التالي.

![مثال على التسلسل الهرمي التنظيمي في مربع الحوار تحديد من تريد النشر إليه.](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على تكامل Dynamics 365 Commerce وMicrosoft Teams](commerce-teams-integration.md)

[تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams](enable-teams-integration.md)

[مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce](synchronize-tasks-teams-pos.md)

[إدارة أدوار المستخدمين في Microsoft Teams](manage-user-roles-teams.md)

[تعيين المتاجر والفرق عند وجود فرق موجودة مسبقًا في Microsoft Teams](map-stores-existing-teams.md)

[الأسئلة الشائعة حول تكامل Dynamics 365 Commerce وMicrosoft Teams](teams-integration-faq.md)