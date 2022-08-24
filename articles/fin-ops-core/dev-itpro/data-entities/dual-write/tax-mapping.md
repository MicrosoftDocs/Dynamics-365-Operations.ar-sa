---
title: الضريبة المتكاملة
description: توضح هذه المقالة تكامل بيانات الضريبة بين Finance and Operations و Dataverse.
author: josaw
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8f148b710e2294edf1e402b9b8b22cb24e60a1f2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288783"
---
# <a name="integrated-tax"></a>الضريبة المتكاملة

[!include [banner](../../includes/banner.md)]



تحدد بيانات إعداد الضريبة الاعداد لكل من الضرائب غير المباشرة (ضريبة القيمة المضافة وGST وضريبة المبيعات) وضريبة الخصم. وهو يصف القاعدة الخاصة بحساب الضريبة ومعدل الضريبة والمحاسبة الضريبية والتسوية والمفاهيم الأخرى.

## <a name="templates"></a>القوالب

تشمل بيانات الضريبة مجموعة من مخططات الجداول تعمل معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.

| تطبيقات التمويل والعمليات | تطبيقات Customer Engagement | ‏‏الوصف‬ |
|-----------------------------|-----------------------------------|-------------|
[مجموعة ضريبة المبيعات للأصناف](mapping-reference.md#196) | msdyn_taxitemgroups | |
[هيئات ضريبة المبيعات](mapping-reference.md#193) | msdyn_taxauthorities | |
[كيان أكواد الإعفاء من ضريبة المبيعات CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[مجموعات ضريبة المبيعات](mapping-reference.md#195) | msdyn_taxgroups | |
[مجموعات ترحيل دفتر أستاذ ضريبة المبيعات V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[أكواد ضريبة الخصم](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[مجموعات ضرائب الخصم](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

