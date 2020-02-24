---
title: الضريبة المتكاملة
description: يوضح هذا الموضوع تكامل بيانات الضريبة بين Finance and Operations وCommon Data Service.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 0d32a5f7859f0200da823a73d94b9a6b2a9c8e7d
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019616"
---
# <a name="integrated-tax"></a>الضريبة المتكاملة

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

تحدد بيانات إعداد الضريبة الاعداد لكل من الضرائب غير المباشرة (ضريبة القيمة المضافة وGST وضريبة المبيعات) وضريبة الخصم. وهو يصف القاعدة الخاصة بحساب الضريبة ومعدل الضريبة والمحاسبة الضريبية والتسوية والمفاهيم الأخرى.

## <a name="templates"></a>القوالب

تشمل بيانات الضريبة مجموعة من مخططات الكيانات تعمل معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.

Finance and Operations   | تطبيقات Dynamics 365 الأخرى
-------------------------|---------------------------------
الأكواد الضريبية                  | msdyn\_taxcodes.md
مجموعات الضرائب               | msdyn\_taxgroups.md
مجموعات أصناف الضرائب          | msdyn\_taxitemgroups.md
الإعفاءات الضريبية           | msdyn\_taxexemptcodes.md
هيئات الضرائب          | msdyn\_taxauthorities.md
أكواد ضريبة الخصم      | msdyn\_withholdingtaxcodes.md
مجموعات ضرائب الخصم   | msdyn\_withholdingtaxgroups.md
مجموعات حسابات دفتر أستاذ الضريبة | msdyn\_taxpostinggroups  

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

