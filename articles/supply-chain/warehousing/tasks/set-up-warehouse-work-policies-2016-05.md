---
title: إعداد سياسات عمل المستودع (استمارة تقديم، أيار/مايو 2016)
description: لا تشمل عمليات المستودع دائمًا عمل المستودع.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34b4255c85bb53f7e238b60559890571070953a6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569069"
---
# <a name="set-up-warehouse-work-policies-application-may-2016"></a><span data-ttu-id="e945d-103">إعداد سياسات عمل المستودع (استمارة تقديم، أيار/مايو 2016)</span><span class="sxs-lookup"><span data-stu-id="e945d-103">Set up warehouse work policies (Application, May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e945d-104">لا تشمل عمليات المستودع دائمًا عمل المستودع.</span><span class="sxs-lookup"><span data-stu-id="e945d-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="e945d-105">بتحديد سياسة العمل، يمكنك منع إنشاء عمل لانتقاء المواد الخام ووضع البضائع المنتهية بعيدًا لمجموعة من المنتجات في مواقع محددة.</span><span class="sxs-lookup"><span data-stu-id="e945d-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="e945d-106">تم استخدام شركة بيانات العرض التوضيحي USMF لإنشاء هذا التسجيل.</span><span class="sxs-lookup"><span data-stu-id="e945d-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="e945d-107">يتطلب دليل المهام هذا الإصدار 7.0.1 أو أحدث من تطبيق Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="e945d-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="e945d-108">انتقل إلى إدارة المستودعات > الإعداد > العمل > سياسات العمل.</span><span class="sxs-lookup"><span data-stu-id="e945d-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="e945d-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e945d-109">Click New.</span></span>
3. <span data-ttu-id="e945d-110">في الحقل "اسم سياسة العمل"، اكتب "لا عمل تخزين".</span><span class="sxs-lookup"><span data-stu-id="e945d-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="e945d-111">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e945d-111">Click Save.</span></span>
5. <span data-ttu-id="e945d-112">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="e945d-112">Click Add.</span></span>
6. <span data-ttu-id="e945d-113">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e945d-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="e945d-114">في الحقل "نوع طلب العمل"، حدد "تخزين البضائع المنتهية".</span><span class="sxs-lookup"><span data-stu-id="e945d-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="e945d-115">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="e945d-115">Click Add.</span></span>
9. <span data-ttu-id="e945d-116">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e945d-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="e945d-117">في الحقل "نوع طلب العمل"، حدد "مخزون المنتج المساعد والمنتج الثانوي".</span><span class="sxs-lookup"><span data-stu-id="e945d-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="e945d-118">قم بتوسيع مقطع "مواقع المخزون".</span><span class="sxs-lookup"><span data-stu-id="e945d-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="e945d-119">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="e945d-119">Click Add.</span></span>
13. <span data-ttu-id="e945d-120">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e945d-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="e945d-121">في قائمة المستودع، أدخل "51".</span><span class="sxs-lookup"><span data-stu-id="e945d-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="e945d-122">في الحقل "الموقع"، أدخل قيمة "001" أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e945d-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="e945d-123">قم بتوسيع قسم "المنتجات".</span><span class="sxs-lookup"><span data-stu-id="e945d-123">Expand the Products section.</span></span>
17. <span data-ttu-id="e945d-124">في الحقل "‏‫قسم المنتج‬"، حدد "محدد".</span><span class="sxs-lookup"><span data-stu-id="e945d-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="e945d-125">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="e945d-125">Click Add.</span></span>
19. <span data-ttu-id="e945d-126">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e945d-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="e945d-127">في الحقل "رقم الصنف"، أدخل "L0101" أو حددها.</span><span class="sxs-lookup"><span data-stu-id="e945d-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="e945d-128">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e945d-128">Click Save.</span></span>

