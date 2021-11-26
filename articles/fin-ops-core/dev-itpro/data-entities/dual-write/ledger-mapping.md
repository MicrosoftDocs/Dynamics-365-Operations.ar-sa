---
title: دفتر الأستاذ المتكامل
description: يوضح هذا الموضوع تكامل بيانات دفتر الأستاذ بين Finance and Operations وتطبيقات Dynamics 365 الأخرى باستخدام Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e41d600464d707d01a0e319dd3cd343b04aa26b7
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782370"
---
# <a name="integrated-ledger"></a>دفتر الأستاذ المتكامل

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

في تطبيق العمل، تقوم بيانات دفتر الأستاذ بتعريف الأساس الذي تم إعداده لكيفيه عمل أحدي الشركات. علي سبيل المثال، تصف بيانات دفتر الأستاذ السنه المالية التي تتبعها الشركة، والعملات التي تتعامل فيها، والحسابات التي تستخدمها. يصف هذا الموضوع تكامل البيانات المالية الرئيسية هذه.

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
