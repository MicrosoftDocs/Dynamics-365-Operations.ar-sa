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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3e763a09e0a0f13eb7222a6ffbcb31b6230b83f4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797925"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="45c74-103">تكوين خدمة الموظف الذاتية</span><span class="sxs-lookup"><span data-stu-id="45c74-103">Configure employee self service</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="45c74-104">في Microsoft Dynamics 365 Human Resources، يمكنك تكوين الإطارات المتجانبة للتنقل في المستوى الأعلى في الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="45c74-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="45c74-105">تعمل الإطارات المتجانبة لخطط الميزات على توجيه المستخدمين إلى خطط الميزات المؤهلين للحصول عليها.</span><span class="sxs-lookup"><span data-stu-id="45c74-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="45c74-106">إعداد إطار متجانب لخطط الميزات</span><span class="sxs-lookup"><span data-stu-id="45c74-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="45c74-107">في مساحة عمل **إدارة الميزات**، ضمن **إعداد**، حدد **محددات الخدمة الذاتية للموظف**.</span><span class="sxs-lookup"><span data-stu-id="45c74-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="45c74-108">حدد علامة التبويب **إعداد إطار متجانب لخطط الميزات**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="45c74-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="45c74-109">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="45c74-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="45c74-110">الحقل</span><span class="sxs-lookup"><span data-stu-id="45c74-110">Field</span></span> | <span data-ttu-id="45c74-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="45c74-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="45c74-112">**معرف التجانب**</span><span class="sxs-lookup"><span data-stu-id="45c74-112">**Tile ID**</span></span> | <span data-ttu-id="45c74-113">المعرف الفريد للإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="45c74-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="45c74-114">**نص تسمية التجانب**</span><span class="sxs-lookup"><span data-stu-id="45c74-114">**Tile label text**</span></span> | <span data-ttu-id="45c74-115">النص الذي سيظهر للإطار المتجانب على الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="45c74-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="45c74-116">**‏‏الوصف**</span><span class="sxs-lookup"><span data-stu-id="45c74-116">**Description**</span></span> | <span data-ttu-id="45c74-117">وصف الإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="45c74-117">A description of the tile.</span></span> |
   | <span data-ttu-id="45c74-118">**عنوان الإنترنت**</span><span class="sxs-lookup"><span data-stu-id="45c74-118">**Internet address**</span></span> | <span data-ttu-id="45c74-119">أدخل عنوان URL لصفحة الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="45c74-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="45c74-120">**حجم التجانب**</span><span class="sxs-lookup"><span data-stu-id="45c74-120">**Tile size**</span></span> | <span data-ttu-id="45c74-121">حجم الإطار المتجانب: صغير أو متوسط أو كبير.</span><span class="sxs-lookup"><span data-stu-id="45c74-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="45c74-122">**الهدف**</span><span class="sxs-lookup"><span data-stu-id="45c74-122">**Target**</span></span> | <span data-ttu-id="45c74-123">تحديد ما إذا كان يجب أن تفتح الصفحة في نافذة جديدة أم في النافذة الحالية.</span><span class="sxs-lookup"><span data-stu-id="45c74-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="45c74-124">**صورة خلفية التجانب**</span><span class="sxs-lookup"><span data-stu-id="45c74-124">**Tile background image**</span></span> | <span data-ttu-id="45c74-125">عنوان URL الخاص بالصورة المطلوب استخدامها للإطار المتجانب (اختياري).</span><span class="sxs-lookup"><span data-stu-id="45c74-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="45c74-126">**البدء**</span><span class="sxs-lookup"><span data-stu-id="45c74-126">**Start**</span></span> | <span data-ttu-id="45c74-127">تاريخ ووقت البداية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="45c74-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="45c74-128">**الانتهاء**</span><span class="sxs-lookup"><span data-stu-id="45c74-128">**End**</span></span> | <span data-ttu-id="45c74-129">تاريخ ووقت النهاية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="45c74-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="45c74-130">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="45c74-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="45c74-131">إعداد إطار متجانب لخطة الائتمان المرن</span><span class="sxs-lookup"><span data-stu-id="45c74-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="45c74-132">في مساحة عمل **إدارة الميزات**، ضمن **إعداد**، حدد **محددات الخدمة الذاتية للموظف**.</span><span class="sxs-lookup"><span data-stu-id="45c74-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="45c74-133">حدد علامة التبويب **إعداد إطار متجانب لخطة الائتمان المرن**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="45c74-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="45c74-134">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="45c74-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="45c74-135">الحقل</span><span class="sxs-lookup"><span data-stu-id="45c74-135">Field</span></span> | <span data-ttu-id="45c74-136">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="45c74-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="45c74-137">**معرف التجانب**</span><span class="sxs-lookup"><span data-stu-id="45c74-137">**Tile ID**</span></span> | <span data-ttu-id="45c74-138">المعرف الفريد للإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="45c74-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="45c74-139">**نص تسمية التجانب**</span><span class="sxs-lookup"><span data-stu-id="45c74-139">**Tile label text**</span></span> | <span data-ttu-id="45c74-140">النص الذي سيظهر للإطار المتجانب على الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="45c74-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="45c74-141">**‏‏الوصف**</span><span class="sxs-lookup"><span data-stu-id="45c74-141">**Description**</span></span> | <span data-ttu-id="45c74-142">وصف الإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="45c74-142">A description of the tile.</span></span> |
   | <span data-ttu-id="45c74-143">**عنوان الإنترنت**</span><span class="sxs-lookup"><span data-stu-id="45c74-143">**Internet address**</span></span> | <span data-ttu-id="45c74-144">أدخل عنوان URL لصفحة الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="45c74-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="45c74-145">**حجم التجانب**</span><span class="sxs-lookup"><span data-stu-id="45c74-145">**Tile size**</span></span> | <span data-ttu-id="45c74-146">حجم الإطار المتجانب: صغير أو متوسط أو كبير.</span><span class="sxs-lookup"><span data-stu-id="45c74-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="45c74-147">**الهدف**</span><span class="sxs-lookup"><span data-stu-id="45c74-147">**Target**</span></span> | <span data-ttu-id="45c74-148">تحديد ما إذا كان يجب أن تفتح الصفحة في نافذة جديدة أم في النافذة الحالية.</span><span class="sxs-lookup"><span data-stu-id="45c74-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="45c74-149">**صورة خلفية التجانب**</span><span class="sxs-lookup"><span data-stu-id="45c74-149">**Tile background image**</span></span> | <span data-ttu-id="45c74-150">عنوان URL الخاص بالصورة المطلوب استخدامها للإطار المتجانب (اختياري).</span><span class="sxs-lookup"><span data-stu-id="45c74-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="45c74-151">**البدء**</span><span class="sxs-lookup"><span data-stu-id="45c74-151">**Start**</span></span> | <span data-ttu-id="45c74-152">تاريخ ووقت البداية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="45c74-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="45c74-153">**الانتهاء**</span><span class="sxs-lookup"><span data-stu-id="45c74-153">**End**</span></span> | <span data-ttu-id="45c74-154">تاريخ ووقت النهاية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="45c74-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="45c74-155">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="45c74-155">Select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]