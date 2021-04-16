---
title: تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams
description: يوضح هذا الموضوع كيفيه تمكين تكامل Microsoft Dynamics 365 Commerce وMicrosoft Teams.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c0dbf7a3c7fa3532e35cac240c1abb8adbdbe489
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842605"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

يوضح هذا الموضوع كيفيه تمكين تكامل Microsoft Dynamics 365 Commerce وMicrosoft Teams.

لتوفير Teams مع المعلومات من Dynamics 365 Commerce ومزامنة ميزات أداره المهام بين فرق العمل وتطبيق نقطه البيع (POS)، يجب تمكين ميزات التكامل في إدارة Commerce.

> [!NOTE]
> عند تمكين تكامل Teams، فأنت توافق علي مشاركه البيانات مع فرق العمل. وقد تتواجد البيانات المشتركة مع Teams في بلد مختلف عن بيانات Commerce الخاصة بك، وقد يكون عرضه لمعايير توافق مختلفه. لمزيد من المعلومات، راجع [Microsoft Trust Center](https://www.microsoft.com/trust-center). للحصول علي معلومات حول سياسات خصوصية Microsoft، راجع [بيان خصوصية Microsoft ](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>تمكين تكامل Teams

قبل ان تتمكن من تمكين تكامل Microsoft Teams مع Commerce، يجب تسجيل تطبيق Teams مع المستاجر الخاص بك في مدخل Azure.

لتسجيل تطبيق Teams مع المستاجر الخاص بك في مدخل Azure، اتبع الخطوات التالية.

1. اتبع الخطوات الموجودة في [بدء التشغيل السريع: تسجيل تطبيق في النظام الأساسي لهوية Microsoft](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app) لتسجيل تطبيق Teams مع المستأجر الخاص بك في مدخل Azure.
1. انسخ قيمة **معرف التطبيق (العميل)** من صفحة **النظرة العامة** للتطبيق المسجل. ستستخدم هذه القيمة لتمكين تكامل Teams في إدارة Commerce.
1. انسخ قيمه الشهادة التي تم إدخالها عند [إضافة شهادة](https://docs.microsoft.com/azure/active-directory/develop/quickstart-register-app#add-a-certificate) في الخطوة 1. تُعرف الشهادة أيضا باسم المفتاح العام أو مفتاح التطبيق. ستستخدم هذه القيمة لتمكين تكامل Teams في إدارة Commerce.

لتمكين تكامل Teams في إدارة Commerce، اتبع هذه الخطوات.

1. انتقل إلى **Retail وCommerce \> إعداد القناة \> تكوين تكامل Microsoft Teams**.
1. في جزء الإجراءات، حدد **تحرير**.
1. قم بتعيين خيار **تمكين تكامل Microsoft Teams** إلى **نعم**.
1. في حقلي **معرف التطبيق** و **مفتاح التطبيق**، أدخل القيم التي حصلت عليها عندما قمت بتسجيل تطبيق Teams في مدخل Azure.
1. في جزء الإجراءات، حدد **حفظ**.

يبين الرسم التوضيحي التالي مثالا لتكوين تكامل Teams في إدارة Commerce.

![تكوين تكامل Teams في إداره Commerce](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

## <a name="disable-teams-integration"></a>تعطيل تكامل Teams

لتعطيل تكامل Microsoft Teams في إدارة Commerce، اتبع هذه الخطوات.

1. انتقل إلى **Retail وCommerce \> إعداد القناة \> Microsoft Teams تكوين التكامل**.
1. في جزء الإجراءات، حدد **تحرير**.
3. قم بتعيين خيار **تمكين تكامل Microsoft Teams** إلى **لا**.
4. امسح القيم من حقلي **معرف التطبيق** و **مفتاح التطبيق**.
1. في جزء الإجراءات، حدد **حفظ**.

> [!NOTE]
> بعد قيامك بتعطيل تكامل Teams مع Commerce، لن تعرض أجهزة نقطة البيع الطرفية المهام التي تم ترحيلها من تطبيق Teams.

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على تكامل Dynamics 365 Commerce وMicrosoft Teams](commerce-teams-integration.md)

[توفير Microsoft Teams من Dynamics 365 Commerce](provision-teams-from-commerce.md)

[مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce](synchronize-tasks-teams-pos.md)

[إدارة أدوار المستخدمين في Microsoft Teams](manage-user-roles-teams.md)

[تعيين المتاجر والفرق عند وجود فرق موجودة مسبقًا في Microsoft Teams](map-stores-existing-teams.md)

[الأسئلة الشائعة حول تكامل Dynamics 365 Commerce وMicrosoft Teams](teams-integration-faq.md)
