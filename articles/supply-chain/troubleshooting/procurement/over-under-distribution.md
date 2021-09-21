---
title: يوجد توزيع محاسبي إما بزيادة أو بالنقصان
description: هناك زيادة أو نقص في التوزيع في توزيع محاسبي واحد أو أكثر.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 7ff0172469df50da9e4272b3fa3f75001a4eb7eb
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475470"
---
# <a name="accounting-distributions-are-either-over--or-under-distributed"></a>يوجد توزيع محاسبي إما بزيادة أو بالنقصان


## <a name="symptoms"></a>العلامات

سوف تتلقى الخطأ التالي:

> هناك زيادة أو نقص في التوزيع في توزيع محاسبي واحد أو أكثر

## <a name="cause"></a>السبب

قد تحدث هذه المشكلة بسبب عدم الاتساق في توزيعات أمر الشراء.

## <a name="resolution"></a>الحل

لحل هذه المشكلة وإعادة تعيين أمر الشراء إلى الحالة *مسودة*، انتقل إلى **التدبير والتوريد \> المهام الدورية \> تنظيف \> إعادة تعيين توزيع أمر الشراء**. لمزيد من المعلومات، راجع منشور المدونة التالي: [حل أخطاء توزيع أمر الشراء في Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
