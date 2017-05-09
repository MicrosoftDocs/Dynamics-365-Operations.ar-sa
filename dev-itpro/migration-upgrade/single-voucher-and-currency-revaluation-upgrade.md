---
title: "ترقية إعادة تقييم العملة والإيصال الواحد لنظام Microsoft Dynamics 365 for Operations الإصدار 1611"
description: "تُدخل بعض المؤسسات دفاتر يومية تحتوي على إيصال واحد يشتمل على أكثر من عميل أو مورد واحد، كما تُجري عملية إعادة تقييم العملة الأجنبية للحسابات المدينة أو الحسابات الدائنة. يوضح هذا الموضوع الخطوات التي يجب على هذه المؤسسات اتباعها عند الترقية إلى Microsoft Dynamics 365 for Operations الإصدار 1611."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-28 16 - 04 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d42c753d0dc8b8efc2a0d2a26da32a4951d85503
ms.lasthandoff: 03/31/2017


---

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>ترقية إعادة تقييم العملة والإيصال الواحد لنظام Microsoft Dynamics 365 for Operations الإصدار 1611

تُدخل بعض المؤسسات دفاتر يومية تحتوي على إيصال واحد يشتمل على أكثر من عميل أو مورد واحد، كما تُجري عملية إعادة تقييم العملة الأجنبية للحسابات المدينة أو الحسابات الدائنة. يوضح هذا الموضوع الخطوات التي يجب على هذه المؤسسات اتباعها عند الترقية إلى Microsoft Dynamics 365 for Operations الإصدار 1611.

اتبع هذه الخطوات عند الترقية إلى Microsoft Dynamics 365 for Operations الإصدار 1611.

1.  قبل الترقية إلى Dynamics 365 for Operations، أجرِ عمليات إعادة تقييم العملة الأجنبية للحسابات المدينة والحسابات الدائنة. عيّن الحقل **الطريقة** إلى **تاريخ الفاتورة**. يتم إنشاء حركة إعادة تقييم تعكس عملية إعادة تقييم العملة الأجنبية الأخيرة. لذلك، يتم تقييم الحركات المفتوحة بعملة المحاسبة الأصلية الخاصة بها.
2.  أجرِ الترقية إلى Dynamics 365 for Operations الإصدار 1611.
3.  أجرِ عمليات إعادة تقييم العملة الأجنبية للحسابات المدينة والحسابات الدائنة مرة ثانية. في هذه المرة، عيّن **الطريقة** إلى **القياسية**. يتم إنشاء حركة إعادة تقييم جديدة استناداً إلى أسعار الصرف الحالية. تسجل هذه الحركة الأرباح/الخسائر غير المحققة وحساب دفتر الأستاذ للملخص الصحيح.



