---
title: إرجاع أصناف عبر عدة فواتير وأوامر مبيعات خاصة بالعملاء
description: يصف هذا الموضوع الوظيفة التي تمكّن عمليات الإرجاع عبر عدة فواتير وأوامر مبيعات خاصة بالعملاء في Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 1/08/2019
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
ms.openlocfilehash: d2cf6f92e90ef196827abb599c65c732615ec7bb
ms.sourcegitcommit: e72eae546d48d41d4b07ff78cfc0242c32b793e7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/01/2019
ms.locfileid: "373058"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>إرجاع أصناف عبر عدة فواتير وأوامر مبيعات خاصة بالعملاء

[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

في الإصدار 10.0 من Dynamics 365 for Finance and Operations، يمكنك إجراء عمليات إرجاع عبر أوامر وفواتير متعددة، في حين أن معالجة عمليات الإرجاع في الإصدارات التي تسبق الإصدار 10.0 كانت تتم فقط بواسطة كل فاتورة على حدة. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>تكوين Retail لدعم عمليات الإرجاع عبر عدة فواتير وأوامر مبيعات خاصة بالعملاء

1. انتقل إلى **معلمات Retail \> أوامر العميل‬**.
1. قم بتشغيل المعلمة **تمكين المرتجعات لأوامر متعددة‬**. 

## <a name="process-returns"></a>معالجة المرتجعات

بعد تشغيل المعلمة ومزامنة التغييرات مع المتاجر، بإمكان أمين الصندوق في المتجر تحديد أوامر مبيعات متعددة لعميل لمعالجة المرتجعات.

عند تحديد الأوامر، تظهر قائمة بكافة المنتجات القابلة للإرجاع عبر كافة الفواتير الخاصة بالأوامر. بإمكان أمين الصندوق عندئذٍ تحديد المنتجات المطلوب إرجاعها. سيتم إنشاء أمر إرجاع واحد لكافة المنتجات المحددة.
