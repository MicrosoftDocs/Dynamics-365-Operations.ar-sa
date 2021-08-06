---
title: الضريبة المتكاملة
description: يوضح هذا الموضوع تكامل بيانات الضريبة بين Finance and Operations وDataverse.
author: robinarh
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: rhaertle
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: e1b5d62e56dd1f87dbfedc6a8ca7379587481ff4
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542309"
---
# <a name="integrated-tax"></a>الضريبة المتكاملة

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

تحدد بيانات إعداد الضريبة الاعداد لكل من الضرائب غير المباشرة (ضريبة القيمة المضافة وGST وضريبة المبيعات) وضريبة الخصم. وهو يصف القاعدة الخاصة بحساب الضريبة ومعدل الضريبة والمحاسبة الضريبية والتسوية والمفاهيم الأخرى.

## <a name="templates"></a>القوالب

تشمل بيانات الضريبة مجموعة من مخططات الجداول تعمل معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.

| تطبيقات Finance and Operations | تطبيقات Customer Engagement | الوصف |
|-----------------------------|-----------------------------------|-------------|
[مجموعة ضريبة المبيعات للأصناف](mapping-reference.md#196) | msdyn_taxitemgroups | |
[هيئات ضريبة المبيعات](mapping-reference.md#193) | msdyn_taxauthorities | |
[كيان أكواد الإعفاء من ضريبة المبيعات CDS](mapping-reference.md#194) | msdyn_taxexemptcodes | |
[مجموعات ضريبة المبيعات](mapping-reference.md#195) | msdyn_taxgroups | |
[مجموعات ترحيل دفتر أستاذ ضريبة المبيعات V2](mapping-reference.md#197) | msdyn_taxpostinggroups | |
[أكواد ضريبة الخصم](mapping-reference.md#210) | msdyn_withholdingtaxcodes | |
[مجموعات ضرائب الخصم](mapping-reference.md#211) | msdyn_withholdingtaxgroups | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
