---
title: إنشاء قناة على الإنترنت وتحديد سمات القناة
description: يتناول هذا الإجراء إنشاء قناة جديدة عبر الإنترنت وإضافتها إلى التدرج الهرمي للمؤسسات.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8e92e28c721692ed92fa931ed899c48678622349
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964774"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="e74ef-103">إنشاء قناة على الإنترنت وتحديد سمات القناة</span><span class="sxs-lookup"><span data-stu-id="e74ef-103">Create online channel and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e74ef-104">يتناول هذا الإجراء إنشاء قناة جديدة عبر الإنترنت وإضافتها إلى التدرج الهرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="e74ef-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="e74ef-105">يجب إنشاء التدرج الهرمي للمؤسسات قبل أن تتمكن من إنشاء قناة جديدة عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="e74ef-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="e74ef-106">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.</span><span class="sxs-lookup"><span data-stu-id="e74ef-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="e74ef-107">إنشاء قناة جديدة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="e74ef-107">Create a new online channel</span></span>
1. <span data-ttu-id="e74ef-108">انتقل إلى البيع بالتجزئة والتجارة > القنوات > المتاجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="e74ef-108">Go to Retail and Commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="e74ef-109">انقر فوق جديد.</span><span class="sxs-lookup"><span data-stu-id="e74ef-109">Click New.</span></span>
3. <span data-ttu-id="e74ef-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e74ef-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e74ef-111">في الحقل "المستودع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e74ef-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="e74ef-112">في حقل "‏‫المنطقة الزمنية للمتجر‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="e74ef-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="e74ef-113">في حقل "العميل الافتراضي"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e74ef-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="e74ef-114">في حقل "‏‫دفتر عناوين العميل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e74ef-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="e74ef-115">في حقل "‏‫شروط الدفع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e74ef-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="e74ef-116">في الحقل "أسلوب الدفع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e74ef-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="e74ef-117">في حقل "‏‫ملف تعريف الإخطار بالبريد الإلكتروني"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e74ef-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="e74ef-118">قم بتوسيع قسم الأبعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="e74ef-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="e74ef-119">في حقل "BusinessUnit"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e74ef-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="e74ef-120">تعيين القيمة لكافة الأبعاد الافتراضية الأخرى بالمثل.</span><span class="sxs-lookup"><span data-stu-id="e74ef-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="e74ef-121">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e74ef-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="e74ef-122">إضافة القناة عبر الإنترنت إلى التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="e74ef-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="e74ef-123">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e74ef-123">Close the page.</span></span>
2. <span data-ttu-id="e74ef-124">انتقل إلى إدارة المؤسسة > المؤسسات > التدرجات الهرمية للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="e74ef-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="e74ef-125">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e74ef-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="e74ef-126">انقر فوق "عرض".</span><span class="sxs-lookup"><span data-stu-id="e74ef-126">Click View.</span></span>
5. <span data-ttu-id="e74ef-127">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="e74ef-127">Click Edit.</span></span>
    * <span data-ttu-id="e74ef-128">يمكنك تحديد أي عقدة تدرج هرمي تقوم من خلالها بإدراج القناة الجديدة التي تريدها.</span><span class="sxs-lookup"><span data-stu-id="e74ef-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="e74ef-129">انقر فوق إدراج.</span><span class="sxs-lookup"><span data-stu-id="e74ef-129">Click Insert.</span></span>
7. <span data-ttu-id="e74ef-130">انقر فوق قناة التجارة.</span><span class="sxs-lookup"><span data-stu-id="e74ef-130">Click Commerce channel.</span></span>
8. <span data-ttu-id="e74ef-131">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="e74ef-131">Click OK.</span></span>
9. <span data-ttu-id="e74ef-132">انقر فوق "نشر" لفتح مربع حوار الإسقاط‬.</span><span class="sxs-lookup"><span data-stu-id="e74ef-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="e74ef-133">في الحقل "تاريخ السريان"، أدخل تاريخًا ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="e74ef-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="e74ef-134">انقر فوق "نشر".</span><span class="sxs-lookup"><span data-stu-id="e74ef-134">Click Publish.</span></span>

## <a name="configure-orders-for-near-real-time-notification"></a><span data-ttu-id="e74ef-135">تكوين الأوامر لاقرب إخطار في الوقت الحقيقي</span><span class="sxs-lookup"><span data-stu-id="e74ef-135">Configure orders for near real-time notification</span></span>
1. <span data-ttu-id="e74ef-136">انتقل إلى البيع بالتجزئة والتجارة > إعداد المراكز الرئيسية > المعلمات > معلمات التجارة.</span><span class="sxs-lookup"><span data-stu-id="e74ef-136">Go to Retail and Commerce  > Headquarters setup > Parameters > Commerce parameters.</span></span>
2. <span data-ttu-id="e74ef-137">قم بتعيين استخدام الخدمة في الوقت الحقيقي لإنشاء أمر التجارة الإلكترونية إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="e74ef-137">Set Use realtime service for eCommerce order creation to "Yes".</span></span>
3. <span data-ttu-id="e74ef-138">قم بتشغيل جدول توزيع 1070 لمزامنة التغييرات لقاعدة بيانات القناة.</span><span class="sxs-lookup"><span data-stu-id="e74ef-138">Run the 1070 distribution schedule to sync changes to the channel database.</span></span> 


