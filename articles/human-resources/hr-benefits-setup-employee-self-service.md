---
title: تكوين خدمة الموظف الذاتية
description: في Microsoft Dynamics 365 Human Resources، يمكنك تكوين الإطارات المتجانبة للتنقل في المستوى الأعلى في الخدمة الذاتية للموظف.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f0d39b30b7c8d0a5729ebe3b1ed9e0d569a6660
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052975"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="b66bf-103">تكوين خدمة الموظف الذاتية</span><span class="sxs-lookup"><span data-stu-id="b66bf-103">Configure employee self service</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b66bf-104">في Microsoft Dynamics 365 Human Resources، يمكنك تكوين الإطارات المتجانبة للتنقل في المستوى الأعلى في الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="b66bf-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="b66bf-105">تعمل الإطارات المتجانبة لخطط الميزات على توجيه المستخدمين إلى خطط الميزات المؤهلين للحصول عليها.</span><span class="sxs-lookup"><span data-stu-id="b66bf-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="b66bf-106">إعداد إطار متجانب لخطط الميزات</span><span class="sxs-lookup"><span data-stu-id="b66bf-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="b66bf-107">في مساحة عمل **إدارة الميزات**، ضمن **إعداد**، حدد **محددات الخدمة الذاتية للموظف**.</span><span class="sxs-lookup"><span data-stu-id="b66bf-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="b66bf-108">حدد علامة التبويب **إعداد إطار متجانب لخطط الميزات**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b66bf-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="b66bf-109">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="b66bf-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="b66bf-110">الحقل</span><span class="sxs-lookup"><span data-stu-id="b66bf-110">Field</span></span> | <span data-ttu-id="b66bf-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="b66bf-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="b66bf-112">**معرف التجانب**</span><span class="sxs-lookup"><span data-stu-id="b66bf-112">**Tile ID**</span></span> | <span data-ttu-id="b66bf-113">المعرف الفريد للإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="b66bf-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="b66bf-114">**نص تسمية التجانب**</span><span class="sxs-lookup"><span data-stu-id="b66bf-114">**Tile label text**</span></span> | <span data-ttu-id="b66bf-115">النص الذي سيظهر للإطار المتجانب على الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="b66bf-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="b66bf-116">**‏‏الوصف**</span><span class="sxs-lookup"><span data-stu-id="b66bf-116">**Description**</span></span> | <span data-ttu-id="b66bf-117">وصف الإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="b66bf-117">A description of the tile.</span></span> |
   | <span data-ttu-id="b66bf-118">**عنوان الإنترنت**</span><span class="sxs-lookup"><span data-stu-id="b66bf-118">**Internet address**</span></span> | <span data-ttu-id="b66bf-119">أدخل عنوان URL لصفحة الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="b66bf-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="b66bf-120">**حجم التجانب**</span><span class="sxs-lookup"><span data-stu-id="b66bf-120">**Tile size**</span></span> | <span data-ttu-id="b66bf-121">حجم الإطار المتجانب: صغير أو متوسط أو كبير.</span><span class="sxs-lookup"><span data-stu-id="b66bf-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="b66bf-122">**الهدف**</span><span class="sxs-lookup"><span data-stu-id="b66bf-122">**Target**</span></span> | <span data-ttu-id="b66bf-123">تحديد ما إذا كان يجب أن تفتح الصفحة في نافذة جديدة أم في النافذة الحالية.</span><span class="sxs-lookup"><span data-stu-id="b66bf-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="b66bf-124">**صورة خلفية التجانب**</span><span class="sxs-lookup"><span data-stu-id="b66bf-124">**Tile background image**</span></span> | <span data-ttu-id="b66bf-125">عنوان URL الخاص بالصورة المطلوب استخدامها للإطار المتجانب (اختياري).</span><span class="sxs-lookup"><span data-stu-id="b66bf-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="b66bf-126">**البدء**</span><span class="sxs-lookup"><span data-stu-id="b66bf-126">**Start**</span></span> | <span data-ttu-id="b66bf-127">تاريخ ووقت البداية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="b66bf-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="b66bf-128">**الانتهاء**</span><span class="sxs-lookup"><span data-stu-id="b66bf-128">**End**</span></span> | <span data-ttu-id="b66bf-129">تاريخ ووقت النهاية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="b66bf-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="b66bf-130">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b66bf-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="b66bf-131">إعداد إطار متجانب لخطة الائتمان المرن</span><span class="sxs-lookup"><span data-stu-id="b66bf-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="b66bf-132">في مساحة عمل **إدارة الميزات**، ضمن **إعداد**، حدد **محددات الخدمة الذاتية للموظف**.</span><span class="sxs-lookup"><span data-stu-id="b66bf-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="b66bf-133">حدد علامة التبويب **إعداد إطار متجانب لخطة الائتمان المرن**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b66bf-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="b66bf-134">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="b66bf-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="b66bf-135">الحقل</span><span class="sxs-lookup"><span data-stu-id="b66bf-135">Field</span></span> | <span data-ttu-id="b66bf-136">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="b66bf-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="b66bf-137">**معرف التجانب**</span><span class="sxs-lookup"><span data-stu-id="b66bf-137">**Tile ID**</span></span> | <span data-ttu-id="b66bf-138">المعرف الفريد للإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="b66bf-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="b66bf-139">**نص تسمية التجانب**</span><span class="sxs-lookup"><span data-stu-id="b66bf-139">**Tile label text**</span></span> | <span data-ttu-id="b66bf-140">النص الذي سيظهر للإطار المتجانب على الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="b66bf-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="b66bf-141">**‏‏الوصف**</span><span class="sxs-lookup"><span data-stu-id="b66bf-141">**Description**</span></span> | <span data-ttu-id="b66bf-142">وصف الإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="b66bf-142">A description of the tile.</span></span> |
   | <span data-ttu-id="b66bf-143">**عنوان الإنترنت**</span><span class="sxs-lookup"><span data-stu-id="b66bf-143">**Internet address**</span></span> | <span data-ttu-id="b66bf-144">أدخل عنوان URL لصفحة الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="b66bf-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="b66bf-145">**حجم التجانب**</span><span class="sxs-lookup"><span data-stu-id="b66bf-145">**Tile size**</span></span> | <span data-ttu-id="b66bf-146">حجم الإطار المتجانب: صغير أو متوسط أو كبير.</span><span class="sxs-lookup"><span data-stu-id="b66bf-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="b66bf-147">**الهدف**</span><span class="sxs-lookup"><span data-stu-id="b66bf-147">**Target**</span></span> | <span data-ttu-id="b66bf-148">تحديد ما إذا كان يجب أن تفتح الصفحة في نافذة جديدة أم في النافذة الحالية.</span><span class="sxs-lookup"><span data-stu-id="b66bf-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="b66bf-149">**صورة خلفية التجانب**</span><span class="sxs-lookup"><span data-stu-id="b66bf-149">**Tile background image**</span></span> | <span data-ttu-id="b66bf-150">عنوان URL الخاص بالصورة المطلوب استخدامها للإطار المتجانب (اختياري).</span><span class="sxs-lookup"><span data-stu-id="b66bf-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="b66bf-151">**البدء**</span><span class="sxs-lookup"><span data-stu-id="b66bf-151">**Start**</span></span> | <span data-ttu-id="b66bf-152">تاريخ ووقت البداية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="b66bf-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="b66bf-153">**الانتهاء**</span><span class="sxs-lookup"><span data-stu-id="b66bf-153">**End**</span></span> | <span data-ttu-id="b66bf-154">تاريخ ووقت النهاية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="b66bf-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="b66bf-155">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b66bf-155">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]