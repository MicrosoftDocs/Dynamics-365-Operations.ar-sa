---
title: الضريبة المتكاملة
description: توضج هذه المقالة تكامل بيانات الضريبة بين Finance and Operations و Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8864a9567d57739aa72fa1859f5cfce6df33e8f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864532"
---
# <a name="integrated-tax"></a>الضريبة المتكاملة

[!include [banner](../../includes/banner.md)]



تحدد بيانات إعداد الضريبة الاعداد لكل من الضرائب غير المباشرة (ضريبة القيمة المضافة وGST وضريبة المبيعات) وضريبة الخصم. وهو يصف القاعدة الخاصة بحساب الضريبة ومعدل الضريبة والمحاسبة الضريبية والتسوية والمفاهيم الأخرى.

## <a name="templates"></a>القوالب

تشمل بيانات الضريبة مجموعة من مخططات الجداول تعمل معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.

| تطبيقات Finance and Operations | تطبيقات Customer Engagement | ‏‏الوصف‬ |
|-----------------------------|-----------------------------------|-------------|
[مجموعة ضريبة المبيعات للأصناف](mapping-reference.md#196) | msdyn_taxitemgroups | |
[هيئات ضريبة المبيعات](mapping-reference.md#193) | msdyn_taxauthorities | |
[كيان أكواد الإعفاء من ضريبة المبيعات CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[مجموعات ضريبة المبيعات](mapping-reference.md#195) | msdyn_taxgroups | |
[مجموعات ترحيل دفتر أستاذ ضريبة المبيعات V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[أكواد ضريبة الخصم](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[مجموعات ضرائب الخصم](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
