---
title: تعيين المتاجر والفرق عند وجود فرق موجودة مسبقًا في Microsoft Teams
description: يغطي هذا الموضوع كيفيه تعيين المتاجر والفرق المقابلة في مقارات Dynamics 365 Commerce إذا كانت مؤسستك قد إنشات بالفعل فرقا في العمل Microsoft Teams قبل تكامل Commerce.
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
ms.openlocfilehash: c75525749d9015387cc112beda104238a93698e9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346682"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a>تعيين المتاجر والفرق عند وجود فرق موجودة مسبقًا في Microsoft Teams

[!include [banner](includes/banner.md)]

يغطي هذا الموضوع كيفيه تعيين المتاجر والفرق المقابلة في مقارات Dynamics 365 Commerce إذا كانت مؤسستك قد إنشات بالفعل فرقا في العمل Microsoft Teams قبل تكامل Commerce.

قد يكون لدي مؤسستك فرق تم إنشاؤها لبعض أو كل المتاجر قبل تكامل Dynamics 365 Commerce وMicrosoft Teams. إذا كانت هذه هي الحالة، لإنشاء مزامنة المهام بين نقطة بيع Commerce وMicrosoft Teams يجب عليك تقديم تعيين المتاجر والفريق المقابل في مقر Commerce.

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a>تعيين المتاجر والفرق المقابلة في مقرات Commerce 

لتعيين المتاجر والفرق المقابلة في مقرات Commerce، اتبع هذه الخطوات.

1. انتقل إلى **إدارة النظام \> مساحة العمل \> إدارة البيانات**.
1. حدد **تصدير**. 
1. في جزء الإجراء، حدد **جديد**.
1. ضمن **اسم المجموعة**، أدخل "تصدير تعيين Teams".
1. في علامة التبويب السريع **الكيانات المحددة**، حدد **إضافة كيان**. يظهر مربع الحوار **إضافة وحدة**.  
1. في القائمة المنسدلة **اسم الكيان**، حدد **تعيين Teams بين المصدر والفريق**.
1. في القائمة المنسدلة **تنسيق البيانات الهدف**، حدد **CSV**.
1. حدد **إضافة**، ثم حدد **إغلاق**.
1. في أعلي الجانب الأيسر ضمن جزء الاجراء، حدد **تصدير الآن**.
1. ضمن **حالة معالجة الكيان**، حدد **تنزيل الملف**.
1. في ملف CSV الذي تم تصديره، ادخل قيم **SOURCETYPE**، و **SOURCEID**، و **TEAMID** على النحو التالي:
    - بالنسبة إلى **SOURCETYPE**، أدخل "RetailStore". 
    - بالنسبة إلى **SOURCEID**، أدخل رقم المتجر (على سبيل المثال، "000135" لمتجر سان فرانسيسكو). يمكنك العثور على أرقام المتجر في **Retail وCommerce \> القنوات \> المتاجر**.
    - بالنسبة إلى **TEAMID**، أدخل معرف الفريق المقابل من Microsoft Teams (على سبيل المثال، "5f8bc92b-6aa8-451e-85d1-3949c01ddc6c"). يمكنك العثور على معلومات معرف الفريق في [admin.teams.microsoft.com](https://admin.teams.microsoft.com).
1. احفظ ملف CSV في جهازك المحلي.
1. انتقل إلى **إدارة النظام \> مساحة العمل \> إدارة البيانات**، ثم حدد **استيراد**.
1. في علامة التبويب السريع **الكيانات المحددة**، حدد **إضافة ملف**. يظهر مربع الحوار **إضافة ملف**.
1. في القائمة المنسدلة **اسم الكيان**، حدد **تعيين Teams بين المصدر والفريق**.
1. في القائمة المنسدلة **تنسيق البيانات المصدر**، حدد **CSV**.
1. حدد **تحميل وإضافة**، وحدد ملف CSV الذي قمت بحفظه مسبقًا، ثم حدد **فتح**.
1. في مربع الحوار **إضافة ملف**، حدد **إغلاق**.
1. في جزء الاجراء، حدد **حفظ**، ثم حدد **استيراد**.

توضح صورة المثال التالي مجموعة **تصدير تعيين Teams** في Commerce مع عناصر **إضافة الكيان** وتمييز رؤوس ملف CSV المُصدَّر.

![تصدير مجموعة تعيين الفرق في Commerce مع إضافة عناصر الكيان وتمييز رؤوس ملف CSV المُصدَرة.](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> بعد إكمال الخطوات السابقة، اتبع الخطوات الواردة في [مزامنة إدارة المهام بين Microsoft Teams ونقطة البيع](synchronize-tasks-teams-pos.md) لمزامنة إدارة المهام. 

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على تكامل Dynamics 365 Commerce وMicrosoft Teams](commerce-teams-integration.md)

[تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams](enable-teams-integration.md)

[توفير Microsoft Teams من Dynamics 365 Commerce](provision-teams-from-commerce.md)

[مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce](synchronize-tasks-teams-pos.md)

[إدارة أدوار المستخدمين في Microsoft Teams](manage-user-roles-teams.md)

[الأسئلة الشائعة حول تكامل Dynamics 365 Commerce وMicrosoft Teams](teams-integration-faq.md)
