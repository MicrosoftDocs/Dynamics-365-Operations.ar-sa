---
title: تكوين خدمة الموظف الذاتية
description: في Microsoft Dynamics 365 Human Resources، يمكنك تكوين الإطارات المتجانبة للتنقل في المستوى الأعلى في الخدمة الذاتية للموظف.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17918fc7b894929c92c54b59b7440ab8aef980bd
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092650"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="9406b-103">تكوين خدمة الموظف الذاتية</span><span class="sxs-lookup"><span data-stu-id="9406b-103">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="9406b-104">في Microsoft Dynamics 365 Human Resources، يمكنك تكوين الإطارات المتجانبة للتنقل في المستوى الأعلى في الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="9406b-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="9406b-105">تعمل الإطارات المتجانبة لخطط الميزات على توجيه المستخدمين إلى خطط الميزات المؤهلين للتسجيل بها.</span><span class="sxs-lookup"><span data-stu-id="9406b-105">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="9406b-106">إعداد إطار متجانب لمركز الأدوار</span><span class="sxs-lookup"><span data-stu-id="9406b-106">Set up a role center tile</span></span>

1. <span data-ttu-id="9406b-107">في مساحة عمل **إدارة الميزات**، ضمن **إعداد**، حدد **محددات الخدمة الذاتية للموظف**.</span><span class="sxs-lookup"><span data-stu-id="9406b-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="9406b-108">حدد علامة التبويب **إعداد إطار متجانب لمركز الأدوار**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9406b-108">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="9406b-109">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="9406b-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="9406b-110">الحقل</span><span class="sxs-lookup"><span data-stu-id="9406b-110">Field</span></span> | <span data-ttu-id="9406b-111">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="9406b-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9406b-112">معرف التجانب</span><span class="sxs-lookup"><span data-stu-id="9406b-112">Tile ID</span></span> | <span data-ttu-id="9406b-113">المعرف الفريد للإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="9406b-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="9406b-114">نص تسمية التجانب</span><span class="sxs-lookup"><span data-stu-id="9406b-114">Tile label text</span></span> | <span data-ttu-id="9406b-115">النص الذي سيظهر للإطار المتجانب على الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="9406b-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="9406b-116">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="9406b-116">Description</span></span> | <span data-ttu-id="9406b-117">وصف الإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="9406b-117">A description of the tile.</span></span> |
   | <span data-ttu-id="9406b-118">عنوان الإنترنت</span><span class="sxs-lookup"><span data-stu-id="9406b-118">Internet address</span></span> | <span data-ttu-id="9406b-119">أدخل عنوان URL لصفحة الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="9406b-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="9406b-120">حجم التجانب</span><span class="sxs-lookup"><span data-stu-id="9406b-120">Tile size</span></span> | <span data-ttu-id="9406b-121">حجم الإطار المتجانب: صغير أو متوسط أو كبير.</span><span class="sxs-lookup"><span data-stu-id="9406b-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="9406b-122">الهدف</span><span class="sxs-lookup"><span data-stu-id="9406b-122">Target</span></span> | <span data-ttu-id="9406b-123">تحديد ما إذا كان يجب أن تفتح الصفحة في نافذة جديدة أم في النافذة الحالية.</span><span class="sxs-lookup"><span data-stu-id="9406b-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="9406b-124">صورة خلفية التجانب</span><span class="sxs-lookup"><span data-stu-id="9406b-124">Tile background image</span></span> | <span data-ttu-id="9406b-125">عنوان URL الخاص بالصورة المطلوب استخدامها للإطار المتجانب (اختياري).</span><span class="sxs-lookup"><span data-stu-id="9406b-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="9406b-126">البدء</span><span class="sxs-lookup"><span data-stu-id="9406b-126">Start</span></span> | <span data-ttu-id="9406b-127">تاريخ ووقت البداية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="9406b-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="9406b-128">الانتهاء</span><span class="sxs-lookup"><span data-stu-id="9406b-128">End</span></span> | <span data-ttu-id="9406b-129">تاريخ ووقت النهاية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="9406b-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="9406b-130">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9406b-130">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="9406b-131">إعداد إطار متجانب لخطط الميزات</span><span class="sxs-lookup"><span data-stu-id="9406b-131">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="9406b-132">في مساحة عمل **إدارة الميزات**، ضمن **إعداد**، حدد **محددات الخدمة الذاتية للموظف**.</span><span class="sxs-lookup"><span data-stu-id="9406b-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="9406b-133">حدد علامة التبويب **إعداد إطار متجانب لخطط الميزات**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9406b-133">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="9406b-134">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="9406b-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="9406b-135">الحقل</span><span class="sxs-lookup"><span data-stu-id="9406b-135">Field</span></span> | <span data-ttu-id="9406b-136">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="9406b-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9406b-137">معرف التجانب</span><span class="sxs-lookup"><span data-stu-id="9406b-137">Tile ID</span></span> | <span data-ttu-id="9406b-138">المعرف الفريد للإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="9406b-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="9406b-139">نص تسمية التجانب</span><span class="sxs-lookup"><span data-stu-id="9406b-139">Tile label text</span></span> | <span data-ttu-id="9406b-140">النص الذي سيظهر للإطار المتجانب على الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="9406b-140">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="9406b-141">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="9406b-141">Description</span></span> | <span data-ttu-id="9406b-142">وصف الإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="9406b-142">A description of the tile.</span></span> |
   | <span data-ttu-id="9406b-143">عنوان الإنترنت</span><span class="sxs-lookup"><span data-stu-id="9406b-143">Internet address</span></span> | <span data-ttu-id="9406b-144">أدخل عنوان URL لصفحة الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="9406b-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="9406b-145">حجم التجانب</span><span class="sxs-lookup"><span data-stu-id="9406b-145">Tile size</span></span> | <span data-ttu-id="9406b-146">حجم الإطار المتجانب: صغير أو متوسط أو كبير.</span><span class="sxs-lookup"><span data-stu-id="9406b-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="9406b-147">الهدف</span><span class="sxs-lookup"><span data-stu-id="9406b-147">Target</span></span> | <span data-ttu-id="9406b-148">تحديد ما إذا كان يجب أن تفتح الصفحة في نافذة جديدة أم في النافذة الحالية.</span><span class="sxs-lookup"><span data-stu-id="9406b-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="9406b-149">صورة خلفية التجانب</span><span class="sxs-lookup"><span data-stu-id="9406b-149">Tile background image</span></span> | <span data-ttu-id="9406b-150">عنوان URL الخاص بالصورة المطلوب استخدامها للإطار المتجانب (اختياري).</span><span class="sxs-lookup"><span data-stu-id="9406b-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="9406b-151">البدء</span><span class="sxs-lookup"><span data-stu-id="9406b-151">Start</span></span> | <span data-ttu-id="9406b-152">تاريخ ووقت البداية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="9406b-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="9406b-153">الانتهاء</span><span class="sxs-lookup"><span data-stu-id="9406b-153">End</span></span> | <span data-ttu-id="9406b-154">تاريخ ووقت النهاية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="9406b-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="9406b-155">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9406b-155">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="9406b-156">إعداد إطار متجانب لخطة الائتمان المرن</span><span class="sxs-lookup"><span data-stu-id="9406b-156">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="9406b-157">في مساحة عمل **إدارة الميزات**، ضمن **إعداد**، حدد **محددات الخدمة الذاتية للموظف**.</span><span class="sxs-lookup"><span data-stu-id="9406b-157">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="9406b-158">حدد علامة التبويب **إعداد إطار متجانب لخطة الائتمان المرن**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9406b-158">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="9406b-159">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="9406b-159">Specify values for the following fields:</span></span>

   | <span data-ttu-id="9406b-160">الحقل</span><span class="sxs-lookup"><span data-stu-id="9406b-160">Field</span></span> | <span data-ttu-id="9406b-161">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="9406b-161">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9406b-162">معرف التجانب</span><span class="sxs-lookup"><span data-stu-id="9406b-162">Tile ID</span></span> | <span data-ttu-id="9406b-163">المعرف الفريد للإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="9406b-163">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="9406b-164">نص تسمية التجانب</span><span class="sxs-lookup"><span data-stu-id="9406b-164">Tile label text</span></span> | <span data-ttu-id="9406b-165">النص الذي سيظهر للإطار المتجانب على الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="9406b-165">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="9406b-166">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="9406b-166">Description</span></span> | <span data-ttu-id="9406b-167">وصف الإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="9406b-167">A description of the tile.</span></span> |
   | <span data-ttu-id="9406b-168">عنوان الإنترنت</span><span class="sxs-lookup"><span data-stu-id="9406b-168">Internet address</span></span> | <span data-ttu-id="9406b-169">أدخل عنوان URL لصفحة الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="9406b-169">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="9406b-170">حجم التجانب</span><span class="sxs-lookup"><span data-stu-id="9406b-170">Tile size</span></span> | <span data-ttu-id="9406b-171">حجم الإطار المتجانب: صغير أو متوسط أو كبير.</span><span class="sxs-lookup"><span data-stu-id="9406b-171">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="9406b-172">الهدف</span><span class="sxs-lookup"><span data-stu-id="9406b-172">Target</span></span> | <span data-ttu-id="9406b-173">تحديد ما إذا كان يجب أن تفتح الصفحة في نافذة جديدة أم في النافذة الحالية.</span><span class="sxs-lookup"><span data-stu-id="9406b-173">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="9406b-174">صورة خلفية التجانب</span><span class="sxs-lookup"><span data-stu-id="9406b-174">Tile background image</span></span> | <span data-ttu-id="9406b-175">عنوان URL الخاص بالصورة المطلوب استخدامها للإطار المتجانب (اختياري).</span><span class="sxs-lookup"><span data-stu-id="9406b-175">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="9406b-176">البدء</span><span class="sxs-lookup"><span data-stu-id="9406b-176">Start</span></span> | <span data-ttu-id="9406b-177">تاريخ ووقت البداية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="9406b-177">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="9406b-178">الانتهاء</span><span class="sxs-lookup"><span data-stu-id="9406b-178">End</span></span> | <span data-ttu-id="9406b-179">تاريخ ووقت النهاية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="9406b-179">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="9406b-180">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9406b-180">Select **Save**.</span></span>
