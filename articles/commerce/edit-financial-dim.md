---
title: تحرير الأبعاد المالية لمعاملات البيع بالتجزئة
description: يوضح هذا الموضوع كيفية تحرير الأبعاد المالية لمعاملات البيع بالتجزئة في Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5a5a82adbad16d8fea2ccf60ae0dbfbd2fd9f3c1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010166"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>تحرير الأبعاد المالية لمعاملات البيع بالتجزئة

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية تحرير الأبعاد المالية لمعاملات البيع بالتجزئة في Microsoft Dynamics 365 Commerce.

## <a name="edit-financial-dimensions"></a>تحرير الأبعاد المالية

لتحرير الأبعاد المالية لمعاملات البيع بالتجزئة في المركز الرئيسي لـ Commerce، اتبع هذه الخطوات.

1. فتح صفحة **تكوين الأبعاد المالية لتكامل التطبيقات**.
1. حدد **سجل تكامل الأبعاد الافتراضية** النشطة.
1. في علامة التبويب السريعة **الأبعاد المالية** ، تأكد من أن جميع الأبعاد التي تريد تحريرها في ورقة عمل Excel موجودة في القائمة **المحددة**. لمزيد من المعلومات، راجع [كيانات البيانات](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration#data-entities).
1. قم بتنزيل ملف Excel وافتحه من صفحة **كشوف الحسابات** ، أو صفحة **معاملات البيع بالتجزئة** ، أو مربع الإطار المتجانب **إخفاقات التحقق من صحة المعاملات** في مساحة العمل **ماليات المتجر**.
1. لتغيير البعد المالي للمعاملة، حدد **تصميم**، ثم حدد رمز القلم المجاور لصف **معاملة (قابلة للتدقيق)**.
1. ابحث عن الحقل **FinancialDimensionDisplayValue** وحدده، وحدد خلية في جزء الرأس بورقة عمل Excel، ثم حدد **إضافة تسمية**.
1. حدد خلية أسفل الخلية التي حددتها في الخطوة السابقة ، وحدد **إضافة قيمة**، ثم حدد **تحديث**. تُضاف الأبعاد المالية إلى ورقة عمل Excel، ويمكن بعد ذلك تحريرها ونشرها.
1. لتغيير الأبعاد في بنود المعاملة، حدد صف **معاملات المبيعات (قابل للتدقيق)** ، وحدد رمز القلم، ثم كرر الخطوتين 6 و7.
1. لتغيير الأبعاد في بنود الدفع، حدد صف **معاملات الدفع (قابل للتدقيق)** ، وحدد رمز القلم، ثم كرر الخطوتين 6 و7.

## <a name="additional-resources"></a>الموارد الإضافية

[تحرير وتدقيق معاملات الدفع نقدًا والاستلام فورًا وإدارة النقد](edit-cash-trans.md)

[تحرير وتدقيق الأوامر عبر الإنترنت ومعاملات أمر العميل غير المتزامنة](edit-order-trans.md)

[إنشاء دفتر عمل Excel لتحرير معاملات البيع بالتجزئة](create-excel-edit.md)

[إضافة الحقول إلى دفتر عمل Excel لتحرير معاملات البيع بالتجزئة](add-fields-excel.md)
