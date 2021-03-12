---
title: تحديد مجموعة الموارد التصنيع المنفصلة
description: مجموعة الموارد هي مجموعة من موارد العمليات تتطابق عادة مع التنظيم المادي لخلايا العمل، المعرفة بخطوط صفراء في صالة الإنتاج.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1930999604fb2605a88bad9a5972afd3579976a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975100"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="0856d-103">تحديد مجموعة الموارد التصنيع المنفصلة</span><span class="sxs-lookup"><span data-stu-id="0856d-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0856d-104">مجموعة الموارد هي مجموعة من موارد العمليات تتطابق عادة مع التنظيم المادي لخلايا العمل، المعرفة بخطوط صفراء في صالة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="0856d-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="0856d-105">يوضح هذا الإجراء كيفية تعريف مجموعة موارد لاستخدامها في عملية إنتاج منفصلة.</span><span class="sxs-lookup"><span data-stu-id="0856d-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="0856d-106">يمكنك استعراض هذا الإجراء في شركة بيانات العرض التوضيحي USMF، أو باستخدام البيانات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="0856d-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="0856d-107">انتقل إلى مجموعات الموارد.</span><span class="sxs-lookup"><span data-stu-id="0856d-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="0856d-108">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="0856d-108">Click New.</span></span>
3. <span data-ttu-id="0856d-109">في حقل مجموعة "الموارد"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0856d-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="0856d-110">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="0856d-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0856d-111">في حقل "الموقع"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0856d-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="0856d-112">في حقل وحدة "الإنتاج"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0856d-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="0856d-113">تعريف محددات التشغيل الافتراضية</span><span class="sxs-lookup"><span data-stu-id="0856d-113">Define default operational parameters</span></span>
1. <span data-ttu-id="0856d-114">وسّع مقطع "العملية".</span><span class="sxs-lookup"><span data-stu-id="0856d-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="0856d-115">في حقل النسبة المئوية للخردة، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="0856d-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="0856d-116">في حقل فئة "الإعداد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0856d-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="0856d-117">في حقل "وقت التشغيل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0856d-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="0856d-118">في حقل النسبة المئوية لجدولة العمليات، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="0856d-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="0856d-119">تحديد ساعات التشغيل</span><span class="sxs-lookup"><span data-stu-id="0856d-119">Define operating hours</span></span>
1. <span data-ttu-id="0856d-120">وسّع مقطع "التقويمات".</span><span class="sxs-lookup"><span data-stu-id="0856d-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="0856d-121">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0856d-121">Click Add.</span></span>
3. <span data-ttu-id="0856d-122">في حقل "التقويم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0856d-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="0856d-123">إضافة موارد العمليات</span><span class="sxs-lookup"><span data-stu-id="0856d-123">Add operations resources</span></span>
1. <span data-ttu-id="0856d-124">وسّع مقطع "الموارد".</span><span class="sxs-lookup"><span data-stu-id="0856d-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="0856d-125">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0856d-125">Click Add.</span></span>
3. <span data-ttu-id="0856d-126">في حقل "المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0856d-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="0856d-127">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="0856d-127">Click Add.</span></span>
5. <span data-ttu-id="0856d-128">في حقل "المورد"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="0856d-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="0856d-129">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="0856d-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="0856d-130">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="0856d-130">In the list, click the link in the selected row.</span></span>

