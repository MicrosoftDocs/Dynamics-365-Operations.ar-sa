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
# <a name="integrated-tax"></a><span data-ttu-id="653ac-103">الضريبة المتكاملة</span><span class="sxs-lookup"><span data-stu-id="653ac-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="653ac-104">تحدد بيانات إعداد الضريبة الاعداد لكل من الضرائب غير المباشرة (ضريبة القيمة المضافة وGST وضريبة المبيعات) وضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="653ac-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="653ac-105">وهو يصف القاعدة الخاصة بحساب الضريبة ومعدل الضريبة والمحاسبة الضريبية والتسوية والمفاهيم الأخرى.</span><span class="sxs-lookup"><span data-stu-id="653ac-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="653ac-106">القوالب</span><span class="sxs-lookup"><span data-stu-id="653ac-106">Templates</span></span>

<span data-ttu-id="653ac-107">تشمل بيانات الضريبة مجموعة من مخططات الكيانات تعمل معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="653ac-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="653ac-108">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="653ac-108">Finance and Operations</span></span>   | <span data-ttu-id="653ac-109">تطبيقات Dynamics 365 الأخرى</span><span class="sxs-lookup"><span data-stu-id="653ac-109">Other Dynamics 365 apps</span></span>
-------------------------|---------------------------------
<span data-ttu-id="653ac-110">الأكواد الضريبية</span><span class="sxs-lookup"><span data-stu-id="653ac-110">Tax codes</span></span>                  | <span data-ttu-id="653ac-111">msdyn\_taxcodes.md</span><span class="sxs-lookup"><span data-stu-id="653ac-111">msdyn\_taxcodes.md</span></span>
<span data-ttu-id="653ac-112">مجموعات الضرائب</span><span class="sxs-lookup"><span data-stu-id="653ac-112">Tax groups</span></span>               | <span data-ttu-id="653ac-113">msdyn\_taxgroups.md</span><span class="sxs-lookup"><span data-stu-id="653ac-113">msdyn\_taxgroups.md</span></span>
<span data-ttu-id="653ac-114">مجموعات أصناف الضرائب</span><span class="sxs-lookup"><span data-stu-id="653ac-114">Tax item groups</span></span>          | <span data-ttu-id="653ac-115">msdyn\_taxitemgroups.md</span><span class="sxs-lookup"><span data-stu-id="653ac-115">msdyn\_taxitemgroups.md</span></span>
<span data-ttu-id="653ac-116">الإعفاءات الضريبية</span><span class="sxs-lookup"><span data-stu-id="653ac-116">Tax Exemptions</span></span>           | <span data-ttu-id="653ac-117">msdyn\_taxexemptcodes.md</span><span class="sxs-lookup"><span data-stu-id="653ac-117">msdyn\_taxexemptcodes.md</span></span>
<span data-ttu-id="653ac-118">هيئات الضرائب</span><span class="sxs-lookup"><span data-stu-id="653ac-118">Tax Authorities</span></span>          | <span data-ttu-id="653ac-119">msdyn\_taxauthorities.md</span><span class="sxs-lookup"><span data-stu-id="653ac-119">msdyn\_taxauthorities.md</span></span>
<span data-ttu-id="653ac-120">أكواد ضريبة الخصم</span><span class="sxs-lookup"><span data-stu-id="653ac-120">Withholding tax codes</span></span>      | <span data-ttu-id="653ac-121">msdyn\_withholdingtaxcodes.md</span><span class="sxs-lookup"><span data-stu-id="653ac-121">msdyn\_withholdingtaxcodes.md</span></span>
<span data-ttu-id="653ac-122">مجموعات ضرائب الخصم</span><span class="sxs-lookup"><span data-stu-id="653ac-122">Withholding tax groups</span></span>   | <span data-ttu-id="653ac-123">msdyn\_withholdingtaxgroups.md</span><span class="sxs-lookup"><span data-stu-id="653ac-123">msdyn\_withholdingtaxgroups.md</span></span>
<span data-ttu-id="653ac-124">مجموعات حسابات دفتر أستاذ الضريبة</span><span class="sxs-lookup"><span data-stu-id="653ac-124">Tax Ledger Account Group</span></span> | <span data-ttu-id="653ac-125">msdyn\_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="653ac-125">msdyn\_taxpostinggroups</span></span>  

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

