---
title: إعداد المهام الإضافية
description: يوضح هذا الإجراء كيفية إعداد مهمة إضافية.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f0ea4a3914b7214dcceb22595809eaa3118a0ca
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987270"
---
# <a name="set-up-accessorial-assignments"></a><span data-ttu-id="34d6c-103">إعداد المهام الإضافية</span><span class="sxs-lookup"><span data-stu-id="34d6c-103">Set up accessorial assignments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34d6c-104">يوضح هذا الإجراء كيفية إعداد مهمة إضافية.</span><span class="sxs-lookup"><span data-stu-id="34d6c-104">This procedure shows how to set up an accessorial assignment.</span></span> <span data-ttu-id="34d6c-105">عادة ما يتم ذلك عن طريق منسق نقل.</span><span class="sxs-lookup"><span data-stu-id="34d6c-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="34d6c-106">قبل استخدام هذا الدليل تحتاج إلى تشغيل الدليل "إعداد مصاريف الموزع الإضافية والأصول الإضافية‬".</span><span class="sxs-lookup"><span data-stu-id="34d6c-106">Before you use this guide you need to run the "Set up hub accessorial charges and accessorial masters" guide.</span></span>


## <a name="set-up-accessorial-assignment"></a><span data-ttu-id="34d6c-107">إعداد المهام الإضافية</span><span class="sxs-lookup"><span data-stu-id="34d6c-107">Set up Accessorial assignment</span></span>
1. <span data-ttu-id="34d6c-108">انتقل إلى إدارة النقل > إعداد > التقييم‬ > مهام إضافية.</span><span class="sxs-lookup"><span data-stu-id="34d6c-108">Go to Transportation management > Setup > Rating > Accessorial assignments.</span></span>
2. <span data-ttu-id="34d6c-109">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="34d6c-109">Click New.</span></span>
3. <span data-ttu-id="34d6c-110">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="34d6c-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="34d6c-111">بدّل توسيع المقطع "تفاصيل".</span><span class="sxs-lookup"><span data-stu-id="34d6c-111">Toggle the expansion of the Details section.</span></span>
5. <span data-ttu-id="34d6c-112">في الحقل "الموزِّع‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="34d6c-112">In the Hub field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="34d6c-113">في القائمة، حدد الموزِّع‬ الذي أنشأت سجلاً رئيسيًا إضافيًا له عندما قمت بتشغيل الدليل "إعداد مصاريف الموزع الإضافية والأصول الإضافية‬".</span><span class="sxs-lookup"><span data-stu-id="34d6c-113">In the list, select the Hub that you created an accessorial master for when you ran the "Set up hub accessorial charges and accessorial masters" guide.</span></span> 
7. <span data-ttu-id="34d6c-114">في الحقل "معرف الموزِّع الإضافي‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="34d6c-114">In the Hub accessorial ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="34d6c-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="34d6c-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="34d6c-116">بدّل توسيع المقطع "المعايير".</span><span class="sxs-lookup"><span data-stu-id="34d6c-116">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="34d6c-117">في المقطع "مشروط‬"، يمكنك أن تختار المعايير الدقيقة للتوقيت الذي يجب فيه تطبيق التكلفة، استنادًا إلى القيم المختلفة المقدمة هنا.</span><span class="sxs-lookup"><span data-stu-id="34d6c-117">In the Criteria section you can choose the exact criteria for when the charge should apply, based on the different values offered here.</span></span>  
10. <span data-ttu-id="34d6c-118">عيّن الخيار "تطبيق دائمًا‬‬‬" إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="34d6c-118">Set the Always apply option to Yes.</span></span>
11. <span data-ttu-id="34d6c-119">في الحقل "مستوى التعيين الإضافي‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="34d6c-119">In the Accessorial assignment level field, select an option.</span></span>
12. <span data-ttu-id="34d6c-120">بدّل توسيع المقطع "الحساب".</span><span class="sxs-lookup"><span data-stu-id="34d6c-120">Toggle the expansion of the Calculation section.</span></span>
13. <span data-ttu-id="34d6c-121">في الحقل "نوع الرسوم الإضافية‬"، حدد "الأساسي".</span><span class="sxs-lookup"><span data-stu-id="34d6c-121">In the Accessorial fee type field, select 'Flat'.</span></span>
    * <span data-ttu-id="34d6c-122">يحدد نوع "الرسوم الإضافية‬" كيفية حساب التكلفة الفعلية.</span><span class="sxs-lookup"><span data-stu-id="34d6c-122">The Accessorial fee type determines how to calculate the actual charge.</span></span> <span data-ttu-id="34d6c-123">في هذا المثال، إنها تكلفة أساسية.</span><span class="sxs-lookup"><span data-stu-id="34d6c-123">In this example it's a flat charge.</span></span>  
14. <span data-ttu-id="34d6c-124">في الحقل "الرسوم الإضافية‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="34d6c-124">In the Accessorial fee field, enter a number.</span></span>
15. <span data-ttu-id="34d6c-125">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="34d6c-125">Click Save.</span></span>

