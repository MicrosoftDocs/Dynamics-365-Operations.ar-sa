---
title: تكوين خدمة الموظف الذاتية
description: ''
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
ms.openlocfilehash: e44a35071b8d0987e6c949fb11312204317b44a1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3007969"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="5e352-102">تكوين خدمة الموظف الذاتية</span><span class="sxs-lookup"><span data-stu-id="5e352-102">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="5e352-103">في Microsoft Dynamics 365 Human Resources، يمكنك تكوين الإطارات المتجانبة للتنقل في المستوى الأعلى في الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="5e352-103">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="5e352-104">تعمل الإطارات المتجانبة لخطط الميزات على توجيه المستخدمين إلى خطط الميزات المؤهلين للتسجيل بها.</span><span class="sxs-lookup"><span data-stu-id="5e352-104">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="5e352-105">إعداد إطار متجانب لمركز الأدوار</span><span class="sxs-lookup"><span data-stu-id="5e352-105">Set up a role center tile</span></span>

1. <span data-ttu-id="5e352-106">في مساحة عمل **إدارة الميزات**، ضمن **إعداد**، حدد **محددات الخدمة الذاتية للموظف**.</span><span class="sxs-lookup"><span data-stu-id="5e352-106">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="5e352-107">حدد علامة التبويب **إعداد إطار متجانب لمركز الأدوار**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="5e352-107">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="5e352-108">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="5e352-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="5e352-109">الحقل</span><span class="sxs-lookup"><span data-stu-id="5e352-109">Field</span></span> | <span data-ttu-id="5e352-110">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="5e352-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5e352-111">معرف التجانب</span><span class="sxs-lookup"><span data-stu-id="5e352-111">Tile ID</span></span> | <span data-ttu-id="5e352-112">المعرف الفريد للإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="5e352-112">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="5e352-113">نص تسمية التجانب</span><span class="sxs-lookup"><span data-stu-id="5e352-113">Tile label text</span></span> | <span data-ttu-id="5e352-114">النص الذي سيظهر للإطار المتجانب على الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="5e352-114">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="5e352-115">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="5e352-115">Description</span></span> | <span data-ttu-id="5e352-116">وصف الإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="5e352-116">A description of the tile.</span></span> |
   | <span data-ttu-id="5e352-117">عنوان الإنترنت</span><span class="sxs-lookup"><span data-stu-id="5e352-117">Internet address</span></span> | <span data-ttu-id="5e352-118">أدخل عنوان URL لصفحة الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="5e352-118">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="5e352-119">حجم التجانب</span><span class="sxs-lookup"><span data-stu-id="5e352-119">Tile size</span></span> | <span data-ttu-id="5e352-120">حجم الإطار المتجانب: صغير أو متوسط أو كبير.</span><span class="sxs-lookup"><span data-stu-id="5e352-120">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="5e352-121">الهدف</span><span class="sxs-lookup"><span data-stu-id="5e352-121">Target</span></span> | <span data-ttu-id="5e352-122">تحديد ما إذا كان يجب أن تفتح الصفحة في نافذة جديدة أم في النافذة الحالية.</span><span class="sxs-lookup"><span data-stu-id="5e352-122">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="5e352-123">صورة خلفية التجانب</span><span class="sxs-lookup"><span data-stu-id="5e352-123">Tile background image</span></span> | <span data-ttu-id="5e352-124">عنوان URL الخاص بالصورة المطلوب استخدامها للإطار المتجانب (اختياري).</span><span class="sxs-lookup"><span data-stu-id="5e352-124">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="5e352-125">البدء</span><span class="sxs-lookup"><span data-stu-id="5e352-125">Start</span></span> | <span data-ttu-id="5e352-126">تاريخ ووقت البداية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="5e352-126">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="5e352-127">الانتهاء</span><span class="sxs-lookup"><span data-stu-id="5e352-127">End</span></span> | <span data-ttu-id="5e352-128">تاريخ ووقت النهاية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="5e352-128">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="5e352-129">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5e352-129">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="5e352-130">إعداد إطار متجانب لخطط الميزات</span><span class="sxs-lookup"><span data-stu-id="5e352-130">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="5e352-131">في مساحة عمل **إدارة الميزات**، ضمن **إعداد**، حدد **محددات الخدمة الذاتية للموظف**.</span><span class="sxs-lookup"><span data-stu-id="5e352-131">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="5e352-132">حدد علامة التبويب **إعداد إطار متجانب لخطط الميزات**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="5e352-132">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="5e352-133">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="5e352-133">Specify values for the following fields:</span></span>

   | <span data-ttu-id="5e352-134">الحقل</span><span class="sxs-lookup"><span data-stu-id="5e352-134">Field</span></span> | <span data-ttu-id="5e352-135">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="5e352-135">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5e352-136">معرف التجانب</span><span class="sxs-lookup"><span data-stu-id="5e352-136">Tile ID</span></span> | <span data-ttu-id="5e352-137">المعرف الفريد للإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="5e352-137">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="5e352-138">نص تسمية التجانب</span><span class="sxs-lookup"><span data-stu-id="5e352-138">Tile label text</span></span> | <span data-ttu-id="5e352-139">النص الذي سيظهر للإطار المتجانب على الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="5e352-139">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="5e352-140">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="5e352-140">Description</span></span> | <span data-ttu-id="5e352-141">وصف الإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="5e352-141">A description of the tile.</span></span> |
   | <span data-ttu-id="5e352-142">عنوان الإنترنت</span><span class="sxs-lookup"><span data-stu-id="5e352-142">Internet address</span></span> | <span data-ttu-id="5e352-143">أدخل عنوان URL لصفحة الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="5e352-143">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="5e352-144">حجم التجانب</span><span class="sxs-lookup"><span data-stu-id="5e352-144">Tile size</span></span> | <span data-ttu-id="5e352-145">حجم الإطار المتجانب: صغير أو متوسط أو كبير.</span><span class="sxs-lookup"><span data-stu-id="5e352-145">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="5e352-146">الهدف</span><span class="sxs-lookup"><span data-stu-id="5e352-146">Target</span></span> | <span data-ttu-id="5e352-147">تحديد ما إذا كان يجب أن تفتح الصفحة في نافذة جديدة أم في النافذة الحالية.</span><span class="sxs-lookup"><span data-stu-id="5e352-147">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="5e352-148">صورة خلفية التجانب</span><span class="sxs-lookup"><span data-stu-id="5e352-148">Tile background image</span></span> | <span data-ttu-id="5e352-149">عنوان URL الخاص بالصورة المطلوب استخدامها للإطار المتجانب (اختياري).</span><span class="sxs-lookup"><span data-stu-id="5e352-149">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="5e352-150">البدء</span><span class="sxs-lookup"><span data-stu-id="5e352-150">Start</span></span> | <span data-ttu-id="5e352-151">تاريخ ووقت البداية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="5e352-151">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="5e352-152">الانتهاء</span><span class="sxs-lookup"><span data-stu-id="5e352-152">End</span></span> | <span data-ttu-id="5e352-153">تاريخ ووقت النهاية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="5e352-153">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="5e352-154">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5e352-154">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="5e352-155">إعداد إطار متجانب لخطة الائتمان المرن</span><span class="sxs-lookup"><span data-stu-id="5e352-155">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="5e352-156">في مساحة عمل **إدارة الميزات**، ضمن **إعداد**، حدد **محددات الخدمة الذاتية للموظف**.</span><span class="sxs-lookup"><span data-stu-id="5e352-156">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="5e352-157">حدد علامة التبويب **إعداد إطار متجانب لخطة الائتمان المرن**، ثم حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="5e352-157">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="5e352-158">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="5e352-158">Specify values for the following fields:</span></span>

   | <span data-ttu-id="5e352-159">الحقل</span><span class="sxs-lookup"><span data-stu-id="5e352-159">Field</span></span> | <span data-ttu-id="5e352-160">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="5e352-160">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5e352-161">معرف التجانب</span><span class="sxs-lookup"><span data-stu-id="5e352-161">Tile ID</span></span> | <span data-ttu-id="5e352-162">المعرف الفريد للإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="5e352-162">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="5e352-163">نص تسمية التجانب</span><span class="sxs-lookup"><span data-stu-id="5e352-163">Tile label text</span></span> | <span data-ttu-id="5e352-164">النص الذي سيظهر للإطار المتجانب على الخدمة الذاتية.</span><span class="sxs-lookup"><span data-stu-id="5e352-164">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="5e352-165">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="5e352-165">Description</span></span> | <span data-ttu-id="5e352-166">وصف الإطار المتجانب.</span><span class="sxs-lookup"><span data-stu-id="5e352-166">A description of the tile.</span></span> |
   | <span data-ttu-id="5e352-167">عنوان الإنترنت</span><span class="sxs-lookup"><span data-stu-id="5e352-167">Internet address</span></span> | <span data-ttu-id="5e352-168">أدخل عنوان URL لصفحة الخدمة الذاتية للموظف.</span><span class="sxs-lookup"><span data-stu-id="5e352-168">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="5e352-169">حجم التجانب</span><span class="sxs-lookup"><span data-stu-id="5e352-169">Tile size</span></span> | <span data-ttu-id="5e352-170">حجم الإطار المتجانب: صغير أو متوسط أو كبير.</span><span class="sxs-lookup"><span data-stu-id="5e352-170">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="5e352-171">الهدف</span><span class="sxs-lookup"><span data-stu-id="5e352-171">Target</span></span> | <span data-ttu-id="5e352-172">تحديد ما إذا كان يجب أن تفتح الصفحة في نافذة جديدة أم في النافذة الحالية.</span><span class="sxs-lookup"><span data-stu-id="5e352-172">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="5e352-173">صورة خلفية التجانب</span><span class="sxs-lookup"><span data-stu-id="5e352-173">Tile background image</span></span> | <span data-ttu-id="5e352-174">عنوان URL الخاص بالصورة المطلوب استخدامها للإطار المتجانب (اختياري).</span><span class="sxs-lookup"><span data-stu-id="5e352-174">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="5e352-175">البدء</span><span class="sxs-lookup"><span data-stu-id="5e352-175">Start</span></span> | <span data-ttu-id="5e352-176">تاريخ ووقت البداية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="5e352-176">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="5e352-177">الانتهاء</span><span class="sxs-lookup"><span data-stu-id="5e352-177">End</span></span> | <span data-ttu-id="5e352-178">تاريخ ووقت النهاية الذي يجب أن يكون الإطار المتجانب متاحًا به.</span><span class="sxs-lookup"><span data-stu-id="5e352-178">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="5e352-179">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="5e352-179">Select **Save**.</span></span>
