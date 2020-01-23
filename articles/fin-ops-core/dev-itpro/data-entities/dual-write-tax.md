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
ms.openlocfilehash: 86e74086a5a74c7af5f2572d1a653a1658d729c0
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853849"
---
# <a name="integrated-tax"></a><span data-ttu-id="f5681-103">الضريبة المتكاملة</span><span class="sxs-lookup"><span data-stu-id="f5681-103">Integrated tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5681-104">تحدد بيانات إعداد الضريبة الاعداد لكل من الضرائب غير المباشرة (ضريبة القيمة المضافة وGST وضريبة المبيعات) وضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="f5681-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="f5681-105">وهو يصف القاعدة الخاصة بحساب الضريبة ومعدل الضريبة والمحاسبة الضريبية والتسوية والمفاهيم الأخرى.</span><span class="sxs-lookup"><span data-stu-id="f5681-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="f5681-106">القوالب</span><span class="sxs-lookup"><span data-stu-id="f5681-106">Templates</span></span>

<span data-ttu-id="f5681-107">تشمل بيانات الضريبة مجموعة من مخططات الكيانات تعمل معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="f5681-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="f5681-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f5681-108">Finance and Operations</span></span>   | <span data-ttu-id="f5681-109">تطبيقات Dynamics 365 الأخرى</span><span class="sxs-lookup"><span data-stu-id="f5681-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="f5681-110">الأكواد الضريبية</span><span class="sxs-lookup"><span data-stu-id="f5681-110">Tax codes</span></span>                  | <span data-ttu-id="f5681-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="f5681-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="f5681-112">مجموعات الضرائب</span><span class="sxs-lookup"><span data-stu-id="f5681-112">Tax groups</span></span>               | <span data-ttu-id="f5681-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="f5681-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="f5681-114">مجموعات أصناف الضرائب</span><span class="sxs-lookup"><span data-stu-id="f5681-114">Tax item groups</span></span>          | <span data-ttu-id="f5681-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="f5681-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="f5681-116">الإعفاءات الضريبية</span><span class="sxs-lookup"><span data-stu-id="f5681-116">Tax Exemptions</span></span>           | <span data-ttu-id="f5681-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="f5681-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="f5681-118">هيئات الضرائب</span><span class="sxs-lookup"><span data-stu-id="f5681-118">Tax Authorities</span></span>          | <span data-ttu-id="f5681-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="f5681-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="f5681-120">أكواد ضريبة الخصم</span><span class="sxs-lookup"><span data-stu-id="f5681-120">Withholding tax codes</span></span>      | <span data-ttu-id="f5681-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="f5681-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="f5681-122">مجموعات ضرائب الخصم</span><span class="sxs-lookup"><span data-stu-id="f5681-122">Withholding tax groups</span></span>   | <span data-ttu-id="f5681-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="f5681-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="f5681-124">مجموعات حسابات دفتر أستاذ الضريبة</span><span class="sxs-lookup"><span data-stu-id="f5681-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="f5681-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="f5681-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../includes/dual-write-symbols.md)]

[!include [Tax groups](dual-write/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](dual-write/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](dual-write/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](dual-write/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](dual-write/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](dual-write/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](dual-write/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

