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
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 68461f375c6d5b04f224331dc192c921cf3c4d04
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979319"
---
# <a name="integrated-tax"></a><span data-ttu-id="157ed-103">الضريبة المتكاملة</span><span class="sxs-lookup"><span data-stu-id="157ed-103">Integrated tax</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="157ed-104">تحدد بيانات إعداد الضريبة الاعداد لكل من الضرائب غير المباشرة (ضريبة القيمة المضافة وGST وضريبة المبيعات) وضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="157ed-104">Tax setup data defines the setup for both indirect taxes (VAT, GST, Sales tax) and withholding tax.</span></span> <span data-ttu-id="157ed-105">وهو يصف القاعدة الخاصة بحساب الضريبة ومعدل الضريبة والمحاسبة الضريبية والتسوية والمفاهيم الأخرى.</span><span class="sxs-lookup"><span data-stu-id="157ed-105">It describes the tax calculation rule, tax rate, tax accounting, settlement, and other concepts.</span></span>

## <a name="templates"></a><span data-ttu-id="157ed-106">القوالب</span><span class="sxs-lookup"><span data-stu-id="157ed-106">Templates</span></span>

<span data-ttu-id="157ed-107">تشمل بيانات الضريبة مجموعة من مخططات الكيانات تعمل معًا أثناء تفاعل بيانات المورّد، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="157ed-107">Tax data includes a collection of entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="157ed-108">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="157ed-108">Finance and Operations apps</span></span> | <span data-ttu-id="157ed-109">التطبيقات المستندة إلى نموذج في Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="157ed-109">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="157ed-110">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="157ed-110">Description</span></span> |
-------------------------|---------------------------------|----|
<span data-ttu-id="157ed-111">مجموعة ضريبة المبيعات للأصناف</span><span class="sxs-lookup"><span data-stu-id="157ed-111">Item sales tax group</span></span> | <span data-ttu-id="157ed-112">msdyn_taxitemgroups</span><span class="sxs-lookup"><span data-stu-id="157ed-112">msdyn_taxitemgroups</span></span> |
<span data-ttu-id="157ed-113">هيئات ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="157ed-113">Sales tax authorities</span></span> | <span data-ttu-id="157ed-114">msdyn_taxauthorities</span><span class="sxs-lookup"><span data-stu-id="157ed-114">msdyn_taxauthorities</span></span> |
<span data-ttu-id="157ed-115">كيان أكواد الإعفاء من ضريبة المبيعات CDS</span><span class="sxs-lookup"><span data-stu-id="157ed-115">Sales tax exempt code entity CDS</span></span> | <span data-ttu-id="157ed-116">msdyn_taxexemptcodes</span><span class="sxs-lookup"><span data-stu-id="157ed-116">msdyn_taxexemptcodes</span></span> |
<span data-ttu-id="157ed-117">مجموعات ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="157ed-117">Sales tax groups</span></span> | <span data-ttu-id="157ed-118">msdyn_taxgroups</span><span class="sxs-lookup"><span data-stu-id="157ed-118">msdyn_taxgroups</span></span> |
<span data-ttu-id="157ed-119">مجموعات ترحيل دفتر أستاذ ضريبة المبيعات V2</span><span class="sxs-lookup"><span data-stu-id="157ed-119">Sales tax ledger posting groups V2</span></span> | <span data-ttu-id="157ed-120">msdyn_taxpostinggroups</span><span class="sxs-lookup"><span data-stu-id="157ed-120">msdyn_taxpostinggroups</span></span> |
<span data-ttu-id="157ed-121">أكواد ضريبة الخصم</span><span class="sxs-lookup"><span data-stu-id="157ed-121">Withholding tax codes</span></span> | <span data-ttu-id="157ed-122">msdyn_withholdingtaxcodes</span><span class="sxs-lookup"><span data-stu-id="157ed-122">msdyn_withholdingtaxcodes</span></span> |
<span data-ttu-id="157ed-123">مجموعات ضرائب الخصم</span><span class="sxs-lookup"><span data-stu-id="157ed-123">Withholding tax groups</span></span> | <span data-ttu-id="157ed-124">msdyn_withholdingtaxgroups</span><span class="sxs-lookup"><span data-stu-id="157ed-124">msdyn_withholdingtaxgroups</span></span> | 


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Tax item groups](includes/TaxItemGroupHeadings-msdyn-taxitemgroups.md)]

[!include [Tax Authorities](includes/SalesTaxAuthorities-msdyn-taxauthorities.md)]

[!include [Tax Exemptions](includes/CdsTaxExemptCodes-msdyn-taxexemptcodes.md)]

[!include [Tax groups](includes/TaxGroupEntity-msdyn-taxgroups.md)]

[!include [Tax Ledger Account Group](includes/TaxPostingGroupsV2--msdyn-taxpostinggroups.md)]

[!include [Withholding tax codes](includes/WithholdingCode-msdyn-withholdingtaxcodes.md)]

[!include [Withholding tax groups](includes/WithholdingGroups-msdyn-withholdingtaxgroups.md)]

