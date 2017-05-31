---
title: "ترقية إعادة تقييم العملة والإيصال الواحد"
description: "تُدخل بعض المؤسسات دفاتر يومية تحتوي على إيصال واحد يشتمل على أكثر من عميل أو مورد واحد، كما تُجري عملية إعادة تقييم العملة الأجنبية للحسابات المدينة أو الحسابات الدائنة. يوضح هذا الموضوع الخطوات التي يجب على هذه المؤسسات اتباعها عند الترقية إلى Microsoft Dynamics 365 for Operations الإصدار 1611."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d3c6d817424be79b09ccdd89deb7f31599fe9bf5
ms.contentlocale: ar-sa
ms.lasthandoff: 05/25/2017


---

# <a name="single-voucher-and-currency-revaluation-upgrade"></a>ترقية إعادة تقييم العملة والإيصال الواحد

[!include[banner](../includes/banner.md)]


تُدخل بعض المؤسسات دفاتر يومية تحتوي على إيصال واحد يشتمل على أكثر من عميل أو مورد واحد، كما تُجري عملية إعادة تقييم العملة الأجنبية للحسابات المدينة أو الحسابات الدائنة. يوضح هذا الموضوع الخطوات التي يجب على هذه المؤسسات اتباعها عند الترقية إلى Microsoft Dynamics 365 for Operations الإصدار 1611.

اتبع هذه الخطوات عند الترقية إلى Microsoft Dynamics 365 for Operations الإصدار 1611.

1.  قبل الترقية إلى Dynamics 365 for Operations، أجرِ عمليات إعادة تقييم العملة الأجنبية للحسابات المدينة والحسابات الدائنة. عيّن الحقل **الطريقة** إلى **تاريخ الفاتورة**. يتم إنشاء حركة إعادة تقييم تعكس عملية إعادة تقييم العملة الأجنبية الأخيرة. لذلك، يتم تقييم الحركات المفتوحة بعملة المحاسبة الأصلية الخاصة بها.
2.  أجرِ الترقية إلى Dynamics 365 for Operations الإصدار 1611.
3.  أجرِ عمليات إعادة تقييم العملة الأجنبية للحسابات المدينة والحسابات الدائنة مرة ثانية. في هذه المرة، عيّن **الطريقة** إلى **القياسية**. يتم إنشاء حركة إعادة تقييم جديدة استناداً إلى أسعار الصرف الحالية. تسجل هذه الحركة الأرباح/الخسائر غير المحققة وحساب دفتر الأستاذ للملخص الصحيح.





