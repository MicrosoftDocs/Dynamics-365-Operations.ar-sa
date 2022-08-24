---
title: دفتر الأستاذ المتكامل
description: توضح هذه المقالة تكامل بيانات دفتر الأستاذ بين تطبيقات التمويل والعمليات وتطبيقات Dynamics 365 الأخرى باستخدام Dataverse.
author: RamaKrishnamoorthy
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 728c131c260586e7f1f787f22ccf02ed81c94c01
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289137"
---
# <a name="integrated-ledger"></a>دفتر الأستاذ المتكامل

[!include [banner](../../includes/banner.md)]



في تطبيق العمل، تقوم بيانات دفتر الأستاذ بتعريف الأساس الذي تم إعداده لكيفيه عمل أحدي الشركات. علي سبيل المثال، تصف بيانات دفتر الأستاذ السنه المالية التي تتبعها الشركة، والعملات التي تتعامل فيها، والحسابات التي تستخدمها. توضح هذه المقالة تكامل البيانات المالية الرئيسية هذه.

## <a name="templates"></a>القوالب

تشمل بيانات دفتر الأستاذ مجموعة من مخططات الجداول المالية الرئيسية تعمل معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.

تطبيقات Finance and Operations | تطبيقات Customer Engagement     | الوصف
---------------------------------|----------------------------------|------------
[أسعار الصرف في CDS](mapping-reference.md#123) | msdyn_currencyexchangerates |
[دليل الحسابات](mapping-reference.md#121) | msdyn_chartofaccountses |
[العملات](mapping-reference.md#218) | transactioncurrencies |
[سعر صرف زوج العملات](mapping-reference.md#122) | msdyn_currencyexchangeratepairs |
[نوع سعر الصرف](mapping-reference.md#129) | msdyn_exchangeratetypes |
[تنسيق البعد المالي](mapping-reference.md#130) | msdyn_financialdimensionformats |
[الأبعاد المالية](mapping-reference.md#128) | msdyn_dimensionattributes |
[كيان تكامل التقويم المالي](mapping-reference.md#132) | msdyn_fiscalcalendars |
[فترة التقويم المالي](mapping-reference.md#131) | msdyn_fiscalcalendarperiods |
[كيان تكامل سنة التقويم المالي](mapping-reference.md#133) | msdyn_fiscalcalendaryears |
[دفتر الأستاذ](mapping-reference.md#148) | msdyn_ledgers |
[الحساب الرئيسي](mapping-reference.md#152) | msdyn_mainaccounts |
[فئات الحساب الرئيسية](mapping-reference.md#151) | msdyn_mainaccountcategories |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

