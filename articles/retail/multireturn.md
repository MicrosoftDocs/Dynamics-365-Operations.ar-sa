---
title: إرجاع أصناف عبر عدة فواتير وأوامر مبيعات خاصة بالعملاء
description: يصف هذا الموضوع الوظيفة التي تمكّن عمليات الإرجاع عبر عدة فواتير وأوامر مبيعات خاصة بالعملاء في Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: c201311028b11121d626e93859a2b98497c047d1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565290"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>إرجاع أصناف عبر عدة فواتير وأوامر مبيعات خاصة بالعملاء

[!include [banner](includes/banner.md)]


في الإصدار 10.0 من Dynamics 365 for Finance and Operations، يمكنك إجراء عمليات إرجاع عبر أوامر وفواتير متعددة، في حين أن معالجة عمليات الإرجاع في الإصدارات التي تسبق الإصدار 10.0 كانت تتم فقط بواسطة كل فاتورة على حدة. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>تكوين Retail لدعم عمليات الإرجاع عبر عدة فواتير وأوامر مبيعات خاصة بالعملاء

1. انتقل إلى **معلمات البيع بالتجزئة \> أوامر العميل‬**.
1. قم بتشغيل المعلمة **تمكين المرتجعات لأوامر متعددة‬**. 

## <a name="process-returns"></a>معالجة المرتجعات

بعد تشغيل المعلمة ومزامنة التغييرات مع المتاجر، بإمكان أمين الصندوق في المتجر تحديد أوامر مبيعات متعددة لعميل لمعالجة المرتجعات.

عند تحديد الأوامر، تظهر قائمة بكافة المنتجات القابلة للإرجاع عبر كافة الفواتير الخاصة بالأوامر. بإمكان أمين الصندوق عندئذٍ تحديد المنتجات المطلوب إرجاعها. سيتم إنشاء أمر إرجاع واحد لكافة المنتجات المحددة.
