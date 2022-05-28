---
title: نظرة عامة على تكامل Dynamics 365 Commerce وMicrosoft Teams
description: يقدم هذا الموضوع نظرة عامة على تكامل Microsoft Dynamics 365 Commerce وMicrosoft Teams.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7786a527a9aca08f5d9326570e8a2dafc5059dc5
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692528"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a>نظرة عامة على تكامل Dynamics 365 Commerce وMicrosoft Teams

[!include [banner](includes/banner.md)]

يقدم هذا الموضوع نظرة عامة على تكامل Microsoft Dynamics 365 Commerce وMicrosoft Teams.

يتكامل Dynamics 365 Commerce مع Teams لمساعدة العملاء وموظفيهم على تحسين الإنتاجية من خلال مزامنة إدارة المهام بين التطبيقين. تتيح إدارة المهام السلسة التي يوفرها تكامل Commerce وTeams لمديري المتاجر والموظفين إنشاء قوائم مهام، وتعيين المهام إلى متاجر متعددة، وتتبع حالة المهام عبر المتاجر، من أي تطبيق.

يتوفر تكامل Commerce وTeams اعتبارًا من إصدار Commerce رقم 10.0.18.

## <a name="key-features"></a>الميزات الرئيسية

فيما يلي بعض الميزات الأساسية التي يوفرها تكامل Commerce وMicrosoft Teams:

- قم بتوفير Teams من خلال الاستفادة من المعلومات المحددة جيدًا من Commerce، مثل الهيكل التنظيمي والمعلومات حول المتاجر والعاملين والأذونات وسياق الأعمال.
- قم بمزامنة التغييرات الجارية بسهولة (على سبيل المثال، إضافة متاجر جديدة أو تعيين موظفين جدد) بين Commerce وTeams، ولكن حافظ على Commerce كمصدر رئيسي لبيانات الهيكل التنظيمي.
- قم بدمج إدارة المهام بين Commerce وTeams لمساعدة عمال التخزين ومديري المتاجر والمديرين الإقليميين ومديري الاتصالات على إدارة المهام من أي تطبيق.

## <a name="prerequisites-for-using-integration-features"></a>المتطلبات الأساسية لاستخدام ميزات التكامل

يجب أن تكون المتطلبات الأساسية التالية في مكانها قبل أن تتمكن من البدء في استخدام ميزات تكامل Microsoft Teams:

- ترخيص Microsoft 365 Business Standard License (يتضمن هذا الترخيص Teams.)
- حسابات Azure Active Directory (Azure AD) لجميع مديري المتاجر والعاملين
- أنظمة نقاط البيع (POS) التي تم تكوينها باستخدام مصادقة Azure AD

## <a name="conceptual-architecture"></a>بنية تصورية

يبين الرسم التوضيحي التالي البنية التصورية لتكامل Dynamics 365 Commerce وMicrosoft Teams، باستخدام متجر سان فرانسيسكو كمثال. يقوم كل من Teams وتطبيق Commerce POS باستخدام Microsoft Planner كمستودع بحيث تظهر المهام المنشورة من Teams في تطبيق نقطة البيع وتظهر المهام المخصصة التي أنشأها مديرو المتجر في تطبيق نقطة البيع في Teams، مما يؤدي إلى تجربة إدارة مهام سلسة بين التطبيقات .    

![بنية تكامل Commerce وTeams.](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a>الموارد الإضافية

[تمكين تكامل Dynamics 365 Commerce وMicrosoft Teams](enable-teams-integration.md)

[توفير Microsoft Teams من Dynamics 365 Commerce](provision-teams-from-commerce.md)

[مزامنة إدارة المهام بين Microsoft Teams ونقطة بيع Dynamics 365 Commerce](synchronize-tasks-teams-pos.md)

[إدارة أدوار المستخدمين في Microsoft Teams](manage-user-roles-teams.md)

[تعيين المتاجر والفرق عند وجود فرق موجودة مسبقًا في Microsoft Teams](map-stores-existing-teams.md)

[الأسئلة الشائعة حول تكامل Dynamics 365 Commerce وMicrosoft Teams](teams-integration-faq.md)
