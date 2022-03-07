---
title: الأسئلة الشائعة حول تكامل Dynamics 365 Commerce وMicrosoft Teams
description: يوفر هذا الموضوع إجابات للأسئلة الشائعة حول تكامل Microsoft Dynamics 365 Commerce وMicrosoft Teams.
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
ms.openlocfilehash: 3fc7cff0a3f8d0fbfb196ec5951b138088afece7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019460"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a>الأسئلة الشائعة حول تكامل Dynamics 365 Commerce وMicrosoft Teams

[!include [banner](includes/banner.md)]

يوفر هذا الموضوع إجابات للأسئلة الشائعة حول تكامل Microsoft Dynamics 365 Commerce وMicrosoft Teams.

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a>من في المتجر يصبح مالكًا للفريق أثناء توفير Teams من Commerce؟ 

تتم إضافة جميع مديري المتاجر تلقائيًا كمالكين إلى مجموعة الفريق المقابلة حتى يتمكنوا من إجراء عمليات مثل إضافة قناة خاصة وإضافة الأعضاء أو حذفهم. 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a>كيف يمكنني تعيين دور "مدير الاتصالات" لموظف في إدارة Commerce؟ 

يتمتع مديرو الاتصالات في Microsoft Teams بالقدرة علي إنشاء قوائم مهام ونشرها. يجب أن يكون لموظفي المؤسسة الذين يحتاجون إلى أن يصبحوا مديري اتصالات دور "مدير مهام البيع بالتجزئة" المعين لهم في إدارة Commerce.

لتعيين دور مدير مهام البيع بالتجزئة إلى موظف في إدارة Commerce، اتبع هذه الخطوات.

1. انتقل إلى **Retail and Commerce \> الموظفون \> المستخدمون**.
1. حدد موظفًا.
1. في علامة التبويب السريعة، **أدوار المستخدم** حدد **تعيين‏‎ الأدوار**.
1. في مربع الحوار **تعيين أدوار للمستخدم** حدد دور **مدير مهمة البيع بالتجزئة** ثم حدد **موافق**.

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a>كيف أجعل التسلسل الهرمي لمؤسسة معينة متاحًا للتحميل في Microsoft Teams؟

في إدارة Commerce، يرتبط التسلسل الهرمي لكل مؤسسة بهدف أو أكثر. تاكد من ان التدرج الهرمي الذي تريد توفيره في Microsoft Teams به غرض **تقارير Retail** مقترنًا به، كما هو موضح في صورة المثال التالية. 

![مثال لغرض التدرج الهرمي للمؤسسات في إدارة Commerce](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a>كيف يمكنني تمكين عمال متجر البيع بالتجزئة من تسجيل الدخول إلى نقطة بيع Commerce (POS) باستخدام Azure Active Directory (Azure AD)؟

للحصول على معلومات حول كيفية تكوين تجربة تسجيل الدخول إلى نقطة بيع Commerce لاستخدام مصادقة Azure AD، راجع [تمكين مصادقة Azure Active Directory لتسجيل الدخول إلى نقطة البيع (POS)](aad-pos-logon.md).

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a>كيف يمكنني تعيين المتاجر والفرق المقابلة في إدارة Commerce إذا كانت مؤسستي قد أنشأت بالفعل فرقًا في Microsoft Teams؟

للحصول على معلومات حول كيفية تعيين المتاجر والفرق في حالة وجود فرق موجودة مسبقًا، راجع [تعيين المتاجر والفرق المقابلة إذا كان لدى مؤسستك فرق موجودة مسبقًا في Microsoft Teams](map-stores-existing-teams.md).

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a>كيف يمكنني مسح رمز Microsoft Graph API المميز المخزن في تخزين الجلسة؟

المستخدم الذي قام بتسجيل الدخول إلى نقطة البيع (POS) باستخدام حساب Azure Active Directory (Azure AD) يجب عليه تسجيل الخروج من نقطة البيع أو إغلاق التطبيق لمسح تخزين الجلسة. 

> [!TIP]
> من أفضل الممارسات الموصى بها أن تجعل عمال المتجر يغلقون محطة نقاط البيع أو يسجلون الخروج من الجلسة عند عدم استخدام الوحدة الطرفية. 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a>ماذا يحدث إذا لم يكن لدى المتجر مديرو متجر؟

إذا لم يكن لدى المتجر مديرين، فلن يتم إنشاء مجموعة فريق للمتجر أو في Teams. 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a>ماذا يحدث إذا ترك مدير المتجر الشركة؟

يمكن لأي شخص لديه دور المالك إضافة مدير متجر جديد في إدارة Commerce وإعادة توفير Teams بحيث يتمتع المدير الجديد بالامتيازات الضرورية في Teams للمجموعة. 

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على تكامل Dynamics 365 Commerce وMicrosoft Teams](commerce-teams-integration.md)

[تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams](enable-teams-integration.md)

[توفير Microsoft Teams من Dynamics 365 Commerce](provision-teams-from-commerce.md)

[مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce](synchronize-tasks-teams-pos.md)

[إدارة أدوار المستخدمين في Microsoft Teams](manage-user-roles-teams.md)

[تعيين المتاجر والفرق عند وجود فرق موجودة مسبقًا في Microsoft Teams](map-stores-existing-teams.md)
