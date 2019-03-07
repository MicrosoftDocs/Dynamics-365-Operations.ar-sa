---
title: إعداد مصاريف الموزع الإضافية والأصول الإضافية
description: يوضح هذا الإجراء كيفية إنشاء سجل رئيسي إضافي‬ للموزع واستخدامه لإنشاء رسوم الموزِّع الإضافي‬.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9959c20f9a8fd07cbf0cfd76f7760b44d7b5cae1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "331887"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="e4529-103">إعداد مصاريف الموزع الإضافية والأصول الإضافية</span><span class="sxs-lookup"><span data-stu-id="e4529-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e4529-104">يوضح هذا الإجراء كيفية إنشاء سجل رئيسي إضافي‬ للموزع واستخدامه لإنشاء رسوم الموزِّع الإضافي‬.</span><span class="sxs-lookup"><span data-stu-id="e4529-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="e4529-105">يستخدم هذا الإجراء مجموعة بيانات USMF.</span><span class="sxs-lookup"><span data-stu-id="e4529-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="e4529-106">عادة ما يتم تنفيذ هذا الإعداد عن طريق منسق نقل.</span><span class="sxs-lookup"><span data-stu-id="e4529-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="e4529-107">إعداد الخطط الرئيسية</span><span class="sxs-lookup"><span data-stu-id="e4529-107">Set up a hub master</span></span>
1. <span data-ttu-id="e4529-108">انتقل إلى إدارة النقل > إعداد > التقييم‬ > الأصول الإضافية.</span><span class="sxs-lookup"><span data-stu-id="e4529-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="e4529-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e4529-109">Click New.</span></span>
3. <span data-ttu-id="e4529-110">في الحقل "الأصول الإضافية‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e4529-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="e4529-111">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e4529-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e4529-112">في الحقل "نوع الرسوم الإضافية‬"، حدد "الموزع".</span><span class="sxs-lookup"><span data-stu-id="e4529-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="e4529-113">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e4529-113">Click Save.</span></span>
7. <span data-ttu-id="e4529-114">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e4529-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="e4529-115">إعداد رسوم الموزِّع الإضافي‬</span><span class="sxs-lookup"><span data-stu-id="e4529-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="e4529-116">انتقل إلى إدارة النقل > إعداد > التقييم‬ > تكاليف الموزِّع الإضافية‬.</span><span class="sxs-lookup"><span data-stu-id="e4529-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="e4529-117">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e4529-117">Click New.</span></span>
3. <span data-ttu-id="e4529-118">في الحقل "معرف الموزِّع الإضافي‬‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e4529-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="e4529-119">في الحقل "الموزِّع‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e4529-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e4529-120">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e4529-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="e4529-121">في الحقل "موضع الموزِّع‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="e4529-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="e4529-122">يمكنك إنشاء التكلفة كانتقاء أو تسليم.</span><span class="sxs-lookup"><span data-stu-id="e4529-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="e4529-123">بحسب اختيارك، سيتم تطبيق التكلفة على جزء النقل المناظر على مسارك.</span><span class="sxs-lookup"><span data-stu-id="e4529-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="e4529-124">في الحقل "الأصل الإضافي‬‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e4529-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e4529-125">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e4529-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e4529-126">حدد السجل الرئيسي الذي أنشأته للتوّ.</span><span class="sxs-lookup"><span data-stu-id="e4529-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="e4529-127">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e4529-127">Click Save.</span></span>
10. <span data-ttu-id="e4529-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="e4529-128">Close the page.</span></span>

