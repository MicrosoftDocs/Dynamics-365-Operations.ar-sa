---
title: لا يمكن إضافة حقل وحدة السعر إلى صفحة اتفاقية الشراء
description: عند فتح صفحة "اتفاقية الشراء" في وضع طريقة عرض البند، لا يمكنك تخصيص الصفحة عبر إضافة حقل "سعر الوحدة" في النظرة العامة على البند
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
ms.openlocfilehash: 56d2ce94fb4b74d982cb6a052cca71c18190cd04
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475444"
---
# <a name="you-cant-add-the-price-unit-field-to-the-purchase-agreement-page"></a>لا يمكن إضافة حقل وحدة السعر إلى صفحة اتفاقية الشراء

## <a name="symptoms"></a>العلامات

عند فتح صفحة **اتفاقية الشراء** في وضع طريقة عرض البند، لا يمكنك تخصيص الصفحة عبر إضافة حقل **سعر الوحدة** في النظرة العامة على البند.

## <a name="resolution"></a>الحل

لا يمكن تضمين بعض الحقول المشتركة في إطار عمل الاتفاقية في عمليات التخصيص. ويحدث هذا التقييد بسبب نموذج البيانات الذي يتم تنفيذه. وبالتالي، لا يمكنك تخصيص حقل **وحدة السعر**.
