---
title: تحرير الابعاد المالية لحركات البيع بالتجزئة
description: يوضح هذا الموضوع كيفية تحرير الأبعاد المالية لحركات البيع بالتجزئة في Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: e26bd4eb53fa44330f15c7cda004cb3d19dfec6d
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/04/2020
ms.locfileid: "4458408"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>تحرير الابعاد المالية لحركات البيع بالتجزئة

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية تحرير الأبعاد المالية لحركات البيع بالتجزئة في Microsoft Dynamics 365 Commerce.

## <a name="edit-financial-dimensions"></a>تحرير الأبعاد المالية

لتحرير الأبعاد المالية لمعاملات البيع بالتجزئة في المركز الرئيسي لـ Commerce، اتبع هذه الخطوات.

1. فتح صفحة **تكوين الأبعاد المالية لتكامل التطبيقات**.
1. حدد **سجل تكامل الابعاد الافتراضية** النشطة.
1. في علامة التبويب السريعة **الأبعاد المالية** ، تأكد من أن جميع الأبعاد التي تريد تحريرها في ورقة عمل Excel موجودة في القائمة **المحددة**. لمزيد من المعلومات، راجع [كيانات البيانات](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).
1. قم بتنزيل ملف Excel وافتحه من صفحة **كشوف الحسابات** ، أو صفحة **حركات البيع بالتجزئة** ، أو مربع الإطار المتجانب **إخفاقات التحقق من صحة الحركات** في مساحة العمل **ماليات المتجر**.
1. لتغيير البعد المالي للحركة، حدد **تصميم**، ثم حدد رمز القلم المجاور لصف **حركة (قابلة للتدقيق)**.
1. ابحث عن الحقل **FinancialDimensionDisplayValue** وحدده، وحدد خلية في جزء الرأس بورقة عمل Excel، ثم حدد **إضافة تسمية**.
1. حدد خلية أسفل الخلية التي حددتها في الخطوة السابقة ، وحدد **إضافة قيمة**، ثم حدد **تحديث**. تُضاف الأبعاد المالية إلى ورقة عمل Excel، ويمكن بعد ذلك تحريرها ونشرها.
1. لتغيير الابعاد في بنود الحركة، حدد صف **حركات المبيعات (قابل للتدقيق)** ، وحدد رمز القلم، ثم كرر الخطوتين 6 و7.
1. لتغيير الابعاد في بنود الدفع، حدد صف **حركات الدفع (قابل للتدقيق)** ، وحدد رمز القلم، ثم كرر الخطوتين 6 و7.

## <a name="additional-resources"></a>الموارد الإضافية

[تحرير وتدقيق حركات الدفع نقدًا والاستلام فورًا وإدارة النقد](edit-cash-trans.md)

[تحرير وتدقيق الأوامر عبر الإنترنت وحركات أمر العميل غير المتزامنة](edit-order-trans.md)

[إنشاء مصنف Excel لتحرير حركات البيع بالتجزئة](create-excel-edit.md)

[إضافة الحقول إلى مصنف Excel لتحرير حركات البيع بالتجزئة](add-fields-excel.md)
