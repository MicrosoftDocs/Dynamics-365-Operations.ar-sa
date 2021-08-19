---
title: تحرير الأبعاد المالية لحركات البيع بالتجزئة
description: يوضح هذا الموضوع كيفية تحرير الأبعاد المالية لحركات البيع بالتجزئة في Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
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
ms.openlocfilehash: d5fee5f5dfee73ddb9fbcf8a33df66c29f9438b49136181633b989d1a02ef4f5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765304"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>تحرير الأبعاد المالية لحركات البيع بالتجزئة

[!include [banner](../includes/banner.md)]

يوضح هذا الموضوع كيفية تحرير الأبعاد المالية لحركات البيع بالتجزئة في Microsoft Dynamics 365 Commerce.

## <a name="edit-financial-dimensions"></a>تحرير الأبعاد المالية

لتحرير الأبعاد المالية لحركات البيع بالتجزئة في المركز الرئيسي لـ Commerce، اتبع هذه الخطوات.

1. فتح صفحة **تكوين الأبعاد المالية لتكامل التطبيقات**.
1. حدد **سجل تكامل الأبعاد الافتراضية** النشطة.
1. في علامة التبويب السريعة **الأبعاد المالية**، تأكد من أن جميع الأبعاد التي تريد تحريرها في ورقة عمل Excel موجودة في القائمة **المحددة**. لمزيد من المعلومات، راجع [كيانات البيانات](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).
1. قم بتنزيل ملف Excel وافتحه من صفحة **كشوف الحسابات**، أو صفحة **معاملات البيع بالتجزئة**، أو مربع الإطار المتجانب **إخفاقات التحقق من صحة المعاملات** في مساحة العمل **ماليات المتجر**.
1. لتغيير البعد المالي للمعاملة، حدد **تصميم**، ثم حدد رمز القلم المجاور لصف **معاملة (قابلة للمراجعة)**.
1. ابحث عن الحقل **FinancialDimensionDisplayValue** وحدده، وحدد خلية في جزء الرأس بورقة عمل Excel، ثم حدد **إضافة تسمية**.
1. حدد خلية أسفل الخلية التي حددتها في الخطوة السابقة، وحدد **إضافة قيمة**، ثم حدد **تحديث**. تُضاف الأبعاد المالية إلى ورقة عمل Excel، ويمكن بعد ذلك تحريرها ونشرها.
1. لتغيير الأبعاد في بنود المعاملة، حدد صف **معاملات المبيعات (قابل للمراجعة)**، وحدد رمز القلم، ثم كرر الخطوتين 6 و7.
1. لتغيير الأبعاد في بنود الدفع، حدد صف **معاملات الدفع (قابل للمراجعة)**، وحدد رمز القلم، ثم كرر الخطوتين 6 و7.

## <a name="additional-resources"></a>الموارد الإضافية

[تحرير ومراجعة معاملات الدفع نقدًا والاستلام فورًا وإدارة النقد](edit-cash-trans.md)

[تحرير ومراجعة الأوامر عبر الإنترنت وحركات أوامر العميل غير المتزامنة](edit-order-trans.md)

[إنشاء دفتر عمل Excel لتحرير معاملات البيع بالتجزئة](create-excel-edit.md)

[إضافة الحقول إلى دفتر عمل Excel لتحرير معاملات البيع بالتجزئة](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]