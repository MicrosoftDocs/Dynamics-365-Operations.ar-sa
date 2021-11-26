---
title: الضريبة المتكاملة
description: يوضح هذا الموضوع تكامل بيانات الضريبة بين Finance and Operations وDataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: d1e74bbbeba019ca48dd823b58251643e96edd0c
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782200"
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
