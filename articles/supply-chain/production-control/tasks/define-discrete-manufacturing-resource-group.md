---
title: تحديد مجموعة الموارد التصنيع المنفصلة
description: مجموعة الموارد هي مجموعة من موارد العمليات تتطابق عادة مع التنظيم المادي لخلايا العمل، المعرفة بخطوط صفراء في صالة الإنتاج.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 50733e34bbf14ae2cade6822105da4d8c2120d7d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556378"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="2ea63-103">تحديد مجموعة الموارد التصنيع المنفصلة</span><span class="sxs-lookup"><span data-stu-id="2ea63-103">Define discrete manufacturing resource group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2ea63-104">مجموعة الموارد هي مجموعة من موارد العمليات تتطابق عادة مع التنظيم المادي لخلايا العمل، المعرفة بخطوط صفراء في صالة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="2ea63-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="2ea63-105">يوضح هذا الإجراء كيفية تعريف مجموعة موارد لاستخدامها في عملية إنتاج منفصلة.</span><span class="sxs-lookup"><span data-stu-id="2ea63-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="2ea63-106">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="2ea63-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="2ea63-107">انتقل إلى مجموعات الموارد.</span><span class="sxs-lookup"><span data-stu-id="2ea63-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="2ea63-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="2ea63-108">Click New.</span></span>
3. <span data-ttu-id="2ea63-109">في حقل مجموعة "الموارد"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ea63-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="2ea63-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="2ea63-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2ea63-111">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2ea63-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="2ea63-112">في حقل وحدة "الإنتاج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2ea63-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="2ea63-113">تعريف محددات التشغيل الافتراضية</span><span class="sxs-lookup"><span data-stu-id="2ea63-113">Define default operational parameters</span></span>
1. <span data-ttu-id="2ea63-114">وسّع مقطع "العملية".</span><span class="sxs-lookup"><span data-stu-id="2ea63-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="2ea63-115">في حقل النسبة المئوية للخردة، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2ea63-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="2ea63-116">في حقل فئة "الإعداد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2ea63-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="2ea63-117">في حقل "وقت التشغيل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2ea63-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="2ea63-118">في حقل النسبة المئوية لجدولة العمليات، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="2ea63-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="2ea63-119">تحديد ساعات التشغيل</span><span class="sxs-lookup"><span data-stu-id="2ea63-119">Define operating hours</span></span>
1. <span data-ttu-id="2ea63-120">وسّع مقطع "التقويمات".</span><span class="sxs-lookup"><span data-stu-id="2ea63-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="2ea63-121">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="2ea63-121">Click Add.</span></span>
3. <span data-ttu-id="2ea63-122">في حقل "التقويم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2ea63-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="2ea63-123">إضافة موارد العمليات</span><span class="sxs-lookup"><span data-stu-id="2ea63-123">Add operations resources</span></span>
1. <span data-ttu-id="2ea63-124">وسّع مقطع "الموارد".</span><span class="sxs-lookup"><span data-stu-id="2ea63-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="2ea63-125">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="2ea63-125">Click Add.</span></span>
3. <span data-ttu-id="2ea63-126">في حقل "المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2ea63-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="2ea63-127">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="2ea63-127">Click Add.</span></span>
5. <span data-ttu-id="2ea63-128">في حقل "المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="2ea63-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="2ea63-129">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="2ea63-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="2ea63-130">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="2ea63-130">In the list, click the link in the selected row.</span></span>

