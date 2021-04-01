---
title: اتفاقيات الضمان
description: يشرح هذا الموضوع اتفاقيات الضمان في إدارة الأصول.
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 35b5c89751d17687bd7e306094a1e4e5e144a8dc
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245337"
---
# <a name="warranty-agreements"></a><span data-ttu-id="63c46-103">اتفاقيات الضمان</span><span class="sxs-lookup"><span data-stu-id="63c46-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="63c46-104">في إدارة الأصول، يمكنك إعداد شروط الضمان التي يمكن ربطها بأصل أو نوع أصل.</span><span class="sxs-lookup"><span data-stu-id="63c46-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="63c46-105">يتم إنشاء شروط الضمان لفترة محددة.</span><span class="sxs-lookup"><span data-stu-id="63c46-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="63c46-106">يمكن إعداد الضمان بحيث يوفر تغطية كاملة أو تغطية جزئية، ويمكنك إعداد الشروط المرتبطة بالساعات والمصروفات والأصناف.</span><span class="sxs-lookup"><span data-stu-id="63c46-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="63c46-107">الخطوة الاولي هي إنشاء اتفاقيات ضمان المورّد موجودة لديك لمعداتك.</span><span class="sxs-lookup"><span data-stu-id="63c46-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="63c46-108">يمكنك بعد ذلك إرفاق اتفاقيات الضمان بالأصول أو بأنواع الأصول.</span><span class="sxs-lookup"><span data-stu-id="63c46-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="63c46-109">يتم استخدام اتفاقيات ضمان المورّد لأغراض إعلاميه فقط.</span><span class="sxs-lookup"><span data-stu-id="63c46-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="63c46-110">إذا تم إعداد ضمان المورّد على أحد الأصول، يمكنك رؤية فترة تغطية الضمان على الأصل.</span><span class="sxs-lookup"><span data-stu-id="63c46-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="63c46-111">إنشاء اتفاقية ضمان</span><span class="sxs-lookup"><span data-stu-id="63c46-111">Create a warranty agreement</span></span>

<span data-ttu-id="63c46-112">بإمكان اتفاقية الضمان أن تشتمل على عدد كثير من بنود الاتفاقية لتغطية الضمان لساعات العمل والمصروفات والأصناف.</span><span class="sxs-lookup"><span data-stu-id="63c46-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="63c46-113">حدد **إدارة الأصول** \> **الإعداد‏‎** \> **الأصول‏‎** \> **الضمان**.</span><span class="sxs-lookup"><span data-stu-id="63c46-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="63c46-114">حدد **جديد** لإنشاء منتج.</span><span class="sxs-lookup"><span data-stu-id="63c46-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="63c46-115">في حقل **الضمان**، أدخل معرف الضمان‏‎.</span><span class="sxs-lookup"><span data-stu-id="63c46-115">In the **Warranty** field, enter a warranty ID.</span></span> 
4. <span data-ttu-id="63c46-116">في حقل **الاسم**، أدخل وصفًا.</span><span class="sxs-lookup"><span data-stu-id="63c46-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="63c46-117">على علامة التبويب السريعة **التفاصيل**، يعرض حقل **الأصول** عدد الأصول النشطة التي تستخدم اتفاقية الضمان.</span><span class="sxs-lookup"><span data-stu-id="63c46-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="63c46-118">في علامة التبويب السريعة **بنود الضمان** ، اتبع الخطوات التالية لإضافة البنود التي يجب تضمينها في اتفاقيه الضمان:</span><span class="sxs-lookup"><span data-stu-id="63c46-118">On the **Warranty lines** FastTab, follow these steps to add lines that should be included in a warranty agreement:</span></span>

    1. <span data-ttu-id="63c46-119">حدد **إضافة بند‬** لإضافة شرط جديد إلى الضمان.</span><span class="sxs-lookup"><span data-stu-id="63c46-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="63c46-120">يتم إدخال رقم بند تسلسلي بشكل تلقائي في حقل **البند**.</span><span class="sxs-lookup"><span data-stu-id="63c46-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="63c46-121">في حقل **الفترة**، حدد نوع فترة الضمان.</span><span class="sxs-lookup"><span data-stu-id="63c46-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="63c46-122">في الحقل **الفاصل الزمني**، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="63c46-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="63c46-123">يحدد هذا الحقل عدد الفترات التي يجب أن يكون خلالها الضمان صالحًا.</span><span class="sxs-lookup"><span data-stu-id="63c46-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="63c46-124">في حقل **النسبة المئوية**، أدخل النسبة المئوية للتغطية الخاصة ببند الضمان.</span><span class="sxs-lookup"><span data-stu-id="63c46-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="63c46-125">تشير النسبة المئوية إلى المقدار الذي تغطيه شركتك.</span><span class="sxs-lookup"><span data-stu-id="63c46-125">The percentage indicates how much is covered by your company.</span></span>

![صفحة الضمان](media/01-warranty.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]