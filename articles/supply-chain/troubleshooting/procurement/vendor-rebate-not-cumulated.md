---
title: لا يتم تجميع تخفيضات المورّد استنادًا إلى الفواتير
description: لا يتم تجميع تخفيضات المورّد استنادًا إلى الفواتير
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 9d4596a7351969bf181982a24ea1dcc6f5732831
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475515"
---
# <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a>لا يتم تجميع تخفيضات المورّد استنادًا إلى الفواتير

## <a name="symptoms"></a>العلامات

إذا كانت الفواتير المرحّلة ذات تواريخ استحقاق مختلفة، فلن تظهر هذه الفواتير في تخفيضات المورّد التي يتم إنشاؤها منها.

## <a name="resolution"></a>الحل

لا تتم مراعاة تاريخ الاستحقاق عندما يتم حساب تخفيض المورّد. يمكنك تخصيص النظام بحيث يظهر تاريخ الاستحقاق والعلاقة بالفاتورة بشكل أكبر فيما يتعلق بالتخفيض الفعلي للمورّد.
