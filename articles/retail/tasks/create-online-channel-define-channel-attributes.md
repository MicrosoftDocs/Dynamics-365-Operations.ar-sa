---
title: إنشاء قناة على الإنترنت وتحديد سمات القناة
description: يتناول هذا الإجراء إنشاء قناة جديدة عبر الإنترنت وإضافتها إلى التدرج الهرمي للمؤسسات.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e066e9901a97bd5b72815a7af472247ef519ecb9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569511"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="a30cc-103">إنشاء قناة على الإنترنت وتحديد سمات القناة</span><span class="sxs-lookup"><span data-stu-id="a30cc-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="a30cc-104">يتناول هذا الإجراء إنشاء قناة جديدة عبر الإنترنت وإضافتها إلى التدرج الهرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="a30cc-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="a30cc-105">يجب إنشاء التدرج الهرمي للمؤسسات قبل أن تتمكن من إنشاء قناة جديدة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="a30cc-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="a30cc-106">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="a30cc-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="a30cc-107">إنشاء قناة جديدة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="a30cc-107">Create a new online channel</span></span>
1. <span data-ttu-id="a30cc-108">انتقل إلى البيع بالتجزئة والتجارة > القنوات > المتاجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="a30cc-108">Go to Retail and commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="a30cc-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="a30cc-109">Click New.</span></span>
3. <span data-ttu-id="a30cc-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a30cc-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a30cc-111">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a30cc-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="a30cc-112">في حقل "‏‫المنطقة الزمنية للمتجر‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="a30cc-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="a30cc-113">في حقل "العميل الافتراضي"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a30cc-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="a30cc-114">في حقل "‏‫دفتر عناوين العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a30cc-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="a30cc-115">في حقل "‏‫شروط الدفع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a30cc-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="a30cc-116">في الحقل "أسلوب الدفع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a30cc-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="a30cc-117">في حقل "‏‫ملف تعريف الإخطار بالبريد الإلكتروني"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a30cc-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="a30cc-118">قم بتوسيع قسم الأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="a30cc-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="a30cc-119">في حقل "BusinessUnit"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a30cc-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="a30cc-120">تعيين القيمة لكافة الأبعاد الافتراضية الأخرى بالمثل.</span><span class="sxs-lookup"><span data-stu-id="a30cc-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="a30cc-121">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="a30cc-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="a30cc-122">إضافة القناة عبر الإنترنت إلى التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="a30cc-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="a30cc-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a30cc-123">Close the page.</span></span>
2. <span data-ttu-id="a30cc-124">انتقل إلى إدارة المؤسسة > المؤسسات > التدرجات الهرمية للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="a30cc-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="a30cc-125">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="a30cc-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="a30cc-126">انقر فوق "عرض".</span><span class="sxs-lookup"><span data-stu-id="a30cc-126">Click View.</span></span>
5. <span data-ttu-id="a30cc-127">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="a30cc-127">Click Edit.</span></span>
    * <span data-ttu-id="a30cc-128">يمكنك تحديد أي عقدة تدرج هرمي تقوم من خلالها بإدراج القناة الجديدة التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="a30cc-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="a30cc-129">انقر فوق إدراج.</span><span class="sxs-lookup"><span data-stu-id="a30cc-129">Click Insert.</span></span>
7. <span data-ttu-id="a30cc-130">انقر فوق "قناة البيع بالتجزئة‬".</span><span class="sxs-lookup"><span data-stu-id="a30cc-130">Click Retail channel.</span></span>
8. <span data-ttu-id="a30cc-131">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a30cc-131">Click OK.</span></span>
9. <span data-ttu-id="a30cc-132">انقر فوق "نشر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="a30cc-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="a30cc-133">في الحقل "تاريخ السريان"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="a30cc-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="a30cc-134">انقر فوق "نشر".</span><span class="sxs-lookup"><span data-stu-id="a30cc-134">Click Publish.</span></span>

