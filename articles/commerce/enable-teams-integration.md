---
title: تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams
description: يوضح هذا المقال كيفيه تمكين تكامل Microsoft Dynamics 365 Commerce وMicrosoft Teams.
author: gvrmohanreddy
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 505e3854818e4d5b73fc1a22724be16036300c3b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872818"
---
# <a name="enable-dynamics-365-commerce-and-microsoft-teams-integration"></a>تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams

[!include [banner](includes/banner.md)]

يوضح هذا المقال كيفيه تمكين تكامل Microsoft Dynamics 365 Commerce وMicrosoft Teams.

لتوفير Teams مع المعلومات من Dynamics 365 Commerce ومزامنة ميزات أداره المهام بين فرق العمل وتطبيق نقطه البيع (POS)، يجب تمكين ميزات التكامل في إدارة Commerce.

> [!NOTE]
> عند تمكين تكامل Teams، فأنت توافق علي مشاركه البيانات مع فرق العمل. وقد تتواجد البيانات المشتركة مع Teams في بلد مختلف عن بيانات Commerce الخاصة بك، وقد يكون عرضه لمعايير توافق مختلفة. لمزيد من المعلومات، راجع [Microsoft Trust Center](https://www.microsoft.com/trust-center). للحصول علي معلومات حول سياسات خصوصية Microsoft، راجع [بيان خصوصية Microsoft ](https://aka.ms/privacy).

## <a name="enable-teams-integration"></a>تمكين تكامل Teams

قبل ان تتمكن من تمكين تكامل Microsoft Teams مع Commerce، يجب تسجيل تطبيق Teams مع المستأجر الخاص بك في مدخل Azure.

لتسجيل تطبيق Teams مع المستأجر الخاص بك في مدخل Azure، اتبع الخطوات التالية.

1. اتبع الخطوات الموجودة في [بدء التشغيل السريع: تسجيل تطبيق في النظام الأساسي لهوية Microsoft](/azure/active-directory/develop/quickstart-register-app) لتسجيل تطبيق Teams مع المستأجر الخاص بك في مدخل Azure.
1. في علامة التبويب **تسجيل التطبيق**، حدد التطبيق الذي أنشأته في الخطوة السابقة. ثم على علامة التبويب **المصادقة**، حدد **إضافة نظام أساسي**.
1. في مربع الحوار، حدد **ويب**. ثم في الحقل **عناوين URL لإعادة التوجيه‬**، أدخل عنوان URL بالتنسيق **\<HQUrl\>/oauth**. استبدل **\<HQUrl\>** بعنوان URL لـ Commerce Headquarters (على سبيل المثال، `https://hxennugbjtweufmdeo385f47fadb6aa9a0aos.cloudax.int.dynamics.com/oauth`).
1. في الصفحة **نظرة عامة** للتطبيق المسجل، انسخ قيمة **معرف التطبيق (العميل)**. سيتعين عليك توفير هذه القيمة لتمكين تكامل Teams في Commerce Headquarters في القسم التالي.
1. اتبع الإرشادات الموجودة في [إضافة سر العميل](/azure/active-directory/develop/quickstart-register-app#add-a-client-secret) لإضافة سر العميل. ثم انسخ **قيمة السر** للعميل. سيتعين عليك توفير هذه القيمة لتمكين تكامل Teams في Commerce Headquarters في القسم التالي.
1. حدد **أذونات API**، ثم حدد **إضافة إذن**.
1. في مربع الحوار **طلب أذونات API**، حدد **Microsoft Graph**، وحدد **الأذونات المفوضة**، ووسّع **المجموعة**، وحدد **Group.ReadWrite.All**، ثم حدد **إضافة أذونات**.
1. في مربع الحوار **طلب أذونات API**، حدد **إضافة إذن**، وحدد **Microsoft Graph**، وحدد **أذونات التطبيق**، ووسّع **المجموعة‏‎**، وحدد **Group.ReadWrite.All**، ثم حدد **إضافة أذونات**.
1. في مربع الحوار **طلب أذونات API**، حدد **إضافة إذن**. على علامة التبويب **واجهات API التي تستخدمها مؤسستي‬‏‫**، ابحث عن **Microsoft Teams خدمة البيع بالتجزئة**، وحددها
1. حدد **الأذونات المفوضة**، ووسّع **TaskPublishing**، وحدد **TaskPublising.ReadWrite.All**، ثم حدد **إضافة أذونات**. لمزيد من المعلومات، راجع [تكوين تطبيق عميل للوصول إلى واجهة API الويب](/azure/active-directory/develop/quickstart-configure-app-access-web-apis).

لتمكين تكامل Teams في إدارة Commerce، اتبع هذه الخطوات.

1. انتقل إلى **Retail وCommerce \> إعداد القناة \> تكوين تكامل Microsoft Teams**.
1. في جزء الإجراءات، حدد **تحرير**.
1. قم بتعيين خيار **تمكين تكامل Microsoft Teams** إلى **نعم**.
1. في حقل **معرف التطبيق**، أدخل قيمة **معرف التطبيق (العميل)‬** التي حصلت عليها عندما قمت بتسجيل تطبيق Teams في مدخل Azure.
1. في حقل **مفتاح التطبيق**، أدخل **قيمة السر‬** التي حصلت عليها عندما أضفت سر العميل في مدخل Azure.
1. في جزء الإجراءات، حدد **حفظ**.

يبين الرسم التوضيحي التالي مثالا لتكوين تكامل Teams في إدارة Commerce.

![تكوين تكامل Teams في المركز الرئيسي لـ Commerce.](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)

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
