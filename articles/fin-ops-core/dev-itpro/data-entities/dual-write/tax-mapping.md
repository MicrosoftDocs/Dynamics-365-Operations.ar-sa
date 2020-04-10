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
ms.openlocfilehash: a4da37d45698290b40f6c72148f1500bef72127a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173074"
---
# <a name="integrated-tax"></a><span data-ttu-id="cc836-103">الضريبة المتكاملة</span><span class="sxs-lookup"><span data-stu-id="cc836-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="cc836-104">تحدد بيانات إعداد الضريبة الاعداد لكل من الضرائب غير المباشرة (ضريبة القيمة المضافة وGST وضريبة المبيعات) وضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="cc836-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="cc836-105">وهو يصف القاعدة الخاصة بحساب الضريبة ومعدل الضريبة والمحاسبة الضريبية والتسوية والمفاهيم الأخرى.</span><span class="sxs-lookup"><span data-stu-id="cc836-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="cc836-106">القوالب</span><span class="sxs-lookup"><span data-stu-id="cc836-106">Templates</span></span>

<span data-ttu-id="cc836-107">تشمل بيانات الضريبة مجموعة من مخططات الكيانات تعمل معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="cc836-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="cc836-108">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc836-108">Finance and Operations apps</span></span> | <span data-ttu-id="cc836-109">التطبيقات المستندة إلى نموذج في Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="cc836-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="cc836-110">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="cc836-110">Description</span></span> |
-------------------------|---------------------------------
<span data-ttu-id="cc836-111">الأكواد الضريبية</span><span class="sxs-lookup"><span data-stu-id="cc836-111">Tax codes</span></span>                   | <span data-ttu-id="cc836-112">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="cc836-112">msdyn\_taxcodes.md</span></span> | 
<span data-ttu-id="cc836-113">مجموعات الضرائب</span><span class="sxs-lookup"><span data-stu-id="cc836-113">Tax groups</span></span>                 | <span data-ttu-id="cc836-114">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="cc836-114">msdyn\_taxgroups.md</span></span> | 
<span data-ttu-id="cc836-115">مجموعات أصناف الضرائب</span><span class="sxs-lookup"><span data-stu-id="cc836-115">Tax item groups</span></span>             | <span data-ttu-id="cc836-116">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="cc836-116">msdyn\_taxitemgroups.md</span></span> | 
<span data-ttu-id="cc836-117">الإعفاءات الضريبية</span><span class="sxs-lookup"><span data-stu-id="cc836-117">Tax Exemptions</span></span>             | <span data-ttu-id="cc836-118">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="cc836-118">msdyn\_taxexemptcodes.md</span></span> | 
<span data-ttu-id="cc836-119">هيئات الضرائب</span><span class="sxs-lookup"><span data-stu-id="cc836-119">Tax Authorities</span></span>             | <span data-ttu-id="cc836-120">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="cc836-120">msdyn\_taxauthorities.md</span></span> | 
<span data-ttu-id="cc836-121">أكواد ضريبة الخصم</span><span class="sxs-lookup"><span data-stu-id="cc836-121">Withholding tax codes</span></span>       | <span data-ttu-id="cc836-122">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="cc836-122">msdyn\_withholdingtaxcodes.md</span></span> | 
<span data-ttu-id="cc836-123">مجموعات ضرائب الخصم</span><span class="sxs-lookup"><span data-stu-id="cc836-123">Withholding tax groups</span></span>     | <span data-ttu-id="cc836-124">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="cc836-124">msdyn\_withholdingtaxgroups.md</span></span> | 
<span data-ttu-id="cc836-125">مجموعات حسابات دفتر أستاذ الضريبة</span><span class="sxs-lookup"><span data-stu-id="cc836-125">Tax Ledger Account Group</span></span> | <span data-ttu-id="cc836-126">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="cc836-126">msdyn\_taxpostinggroups</span></span>     | 

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

