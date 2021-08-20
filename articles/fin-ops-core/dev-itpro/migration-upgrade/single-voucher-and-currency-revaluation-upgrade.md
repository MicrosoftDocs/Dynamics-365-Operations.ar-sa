---
title: ترقية دفاتر يومية الإيصالات الفردية وعمليات إعادة تقييم العملة
description: يشرح هذا الموضوع كيفية ترقية دفاتر يومية الإيصالات الفردية وعمليات إعادة تقييم العملة.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: feafcd5c309360467344618f7cec15235ddbe77df807f75873ac82c941073500
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735484"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>ترقية دفاتر يومية الإيصالات الفردية وعمليات إعادة تقييم العملة

[!include [banner](../includes/banner.md)]

تُدخل بعض المؤسسات دفاتر يومية تحتوي على إيصال واحد يشتمل على أكثر من عميل أو مورد واحد، كما تُجري عملية إعادة تقييم العملة الأجنبية للحسابات المدينة أو الحسابات الدائنة. يصف هذا الموضوع الخطوات التي يجب على هذه المؤسسات اتباعها عند الترقية إلى الإصدار 1611 من Microsoft Dynamics 365 for Operations.

اتبع هذه الخطوات عند الترقية إلى الإصدار 1611 من Microsoft Dynamics 365 for Operations.

1.  قبل الترقية إلى Finance and Operations، شغّل عمليات إعادة تقييم العملة الأجنبية للحسابات المدينة والحسابات الدائنة. عيّن الحقل **الطريقة** إلى **تاريخ الفاتورة**. يتم إنشاء حركة إعادة تقييم تعكس عملية إعادة تقييم العملة الأجنبية الأخيرة. لذلك، يتم تقييم الحركات المفتوحة بعملة المحاسبة الأصلية الخاصة بها.
2.  الترقية إلى الإصدار 1611.
3.  أجرِ عمليات إعادة تقييم العملة الأجنبية للحسابات المدينة والحسابات الدائنة مرة ثانية. في هذه المرة، عيّن **الطريقة** إلى **القياسية**. يتم إنشاء حركة إعادة تقييم جديدة استناداً إلى أسعار الصرف الحالية. تسجل هذه الحركة الأرباح/الخسائر غير المحققة وحساب دفتر الأستاذ للملخص الصحيح.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]