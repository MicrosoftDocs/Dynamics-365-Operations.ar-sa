---
title: الحد الأقصى لاتفاقيه الشراء غير فعال في طلب شراء
description: الحد الأقصى لاتفاقيه الشراء غير فعال في طلب شراء
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
ms.openlocfilehash: c19d40dce65acbe80d4572bfc4e925aa87ea4f02
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475450"
---
# <a name="the-purchase-agreement-maximum-limit-isnt-effective-on-a-purchase-requisition"></a>الحد الأقصى لاتفاقيه الشراء غير فعال في طلب شراء

## <a name="symptoms"></a>العلامات

عند ربط طلب شراء باتفاقية شراء، لا يسري الحد الأقصى من اتفاقية الشراء على طلب الشراء. يتم إدخال معلومات الأسعار الافتراضية بشكل صحيح، ولكن يمكن طلب أكثر من الحد الأقصى من اتفاقية الشراء في طلب الشراء.

## <a name="resolution"></a>الحل

هذا السلوك متوقع. نظرًا لعدم الموافقة دائمًا على الطلبات، يجب عدم حجز كمية أو مبلغ على اتفاقية الشراء. والتالي، لن تتمكن من استيفاء الحد الأقصى من اتفاقية الشراء.
