---
title: إعداد الأمان لمحتوى "تحليل محاسبة التكاليف" في Power BI
description: يشرح هذا الموضوع كيفية نشر مستوى الوصول الآمن في محاسبة التكاليف إلى الأمان على مستوى الصف في Microsoft Power BI. تضمن هذه الوظيفة ألا يشاهد المستخدم سوى بيانات Power BI التي مُنح إمكانية الوصول لها.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ab9b9533ae650c05f57a45be25aec6cbe2e3db76
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849857"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="a1b88-104">إعداد الأمان لمحتوى "تحليل محاسبة التكاليف" في Power BI</span><span class="sxs-lookup"><span data-stu-id="a1b88-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1b88-105">يشرح هذا الموضوع كيفية نشر مستوى الوصول الآمن في محاسبة التكاليف إلى الأمان على مستوى الصف في Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="a1b88-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="a1b88-106">تضمن هذه الوظيفة ألا يشاهد المستخدم سوى بيانات Power BI التي مُنح إمكانية الوصول لها.</span><span class="sxs-lookup"><span data-stu-id="a1b88-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

## <a name="overview"></a><span data-ttu-id="a1b88-107">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="a1b88-107">Overview</span></span>

<span data-ttu-id="a1b88-108">يستخدم محتوى **تحليل محاسبة التكاليف** في Microsoft Power BI يستخدم الأمان على مستوى الصف في Power BI لتقييد وصول المستخدم.</span><span class="sxs-lookup"><span data-stu-id="a1b88-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="a1b88-109">يستند الأمان على التدرج الهرمي المؤسسي لمستوى الوصول الذي تم إعداده في معلمات محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="a1b88-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="a1b88-110">لمزيد من المعلومات حول محتوى **تحليل محاسبة التكاليف** في Power BI، راجع [محتوى "تحليل محاسبة التكاليف" في Power BI](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="a1b88-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="a1b88-111">الإعداد</span><span class="sxs-lookup"><span data-stu-id="a1b88-111">Setup</span></span>
<span data-ttu-id="a1b88-112">لنشر مستوى الوصول الآمن إلى Power BI، يجب على مالك محتوى Power BI اتباع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a1b88-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="a1b88-113">يصبح المستخدم الذي ينشر محتوى **تحليل محاسبة التكاليف** في Power BI مالك المحتوى بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="a1b88-113">The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="a1b88-114">بإمكان المالك فقط إعداد الأمان في Power BI.</span><span class="sxs-lookup"><span data-stu-id="a1b88-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="a1b88-115">بالإضافة إلى ذلك، وحتى قيام المالك بإضافة مستخدمين على PowerBI.com، لا يمكن لأي شخص بخلاف المالك رؤية أي بيانات في محتوى **تحليل محاسبة التكاليف** في Power BI.</span><span class="sxs-lookup"><span data-stu-id="a1b88-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1. <span data-ttu-id="a1b88-116">نشر ملف التعريف إلى Power BI.</span><span class="sxs-lookup"><span data-stu-id="a1b88-116">Publish the definition file to Power BI.</span></span>
2. <span data-ttu-id="a1b88-117">تسجيل الدخول إلى PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="a1b88-117">Sign in to PowerBI.com.</span></span>
3. <span data-ttu-id="a1b88-118">العثور على قاعدة بيانات **تحليل محاسبة التكاليف** في Power BI.</span><span class="sxs-lookup"><span data-stu-id="a1b88-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4. <span data-ttu-id="a1b88-119">فتح صفحة الأمان.</span><span class="sxs-lookup"><span data-stu-id="a1b88-119">Open the security page.</span></span>

    ![فتح صفحة الأمان](./media/CA-picture-1.png)

5. <span data-ttu-id="a1b88-121">**مراقب كائن التكلفة** قد تم إنشاؤه بالفعل.</span><span class="sxs-lookup"><span data-stu-id="a1b88-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="a1b88-122">إضافة أعضاء آخرين يشكلوا جزءًا من التدرج الهرمي المؤسسي لمستوى الوصول لمحاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="a1b88-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span>

    ![إضافة الأعضاء](./media/CA-picture-2.png)

<span data-ttu-id="a1b88-124">سوف يرى المستخدمون الذين تم إضافتهم إلى دور **مراقب كائن التكلفة** البيانات المسموح لهم برؤيتها فقط، وفقًا للتعريف في التدرج الهرمي المؤسسي لمستوى الوصول لمحاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="a1b88-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="a1b88-125">ينطبق الأمان على مستوى الصف على الإطارات المتجانبة والتقارير في Microsoft Dynamics 365 for Finance and Operations المضمنة من Power BI.</span><span class="sxs-lookup"><span data-stu-id="a1b88-125">Row-level security applies to tiles and reports in Microsoft Dynamics 365 for Finance and Operations that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="a1b88-126">تحديث الأمان</span><span class="sxs-lookup"><span data-stu-id="a1b88-126">Updating security</span></span>
<span data-ttu-id="a1b88-127">إذا تم تحديث الأمان على مستوى الوصول في محاسبة التكليف، وأردت أن يعكس Power BI هذه التحديثات، فعليك تحديث مخزن الكيانات لمحتوى **تحليل محاسبة التكاليف** في Power BI.</span><span class="sxs-lookup"><span data-stu-id="a1b88-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="a1b88-128">بعد الانتهاء من تحديث متجر الكيان من Finance and Operations، يجب عليك تحديث المنتجات على PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="a1b88-128">After you complete the entity store update from Finance and Operations, you must update the artifacts on PowerBI.com.</span></span> <span data-ttu-id="a1b88-129">لمزيد من المعلومات حول كيفية تحديث متجر الكيان، راجع [تحديثمتجر كيان](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="a1b88-129">For more information about how to do an entity store update, see [Update entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="a1b88-130">يتعين أيضًا على مالك محتوى **تحليل محاسبة التكاليف** في Power BI إجراء تحديث لمخزن الكيانات إذا تم منح مستخدمين جدد إمكانية الوصول إلى التدرج الهرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="a1b88-130">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="a1b88-131">بالإضافة إلى ذلك، يجب على المالك إضافة مستخدمين جدد إلى دور **مراقب كائن التكلفة** في PowerBI.com، حيث يتم تطبيق الأمان على مستوى الصفوف لها.</span><span class="sxs-lookup"><span data-stu-id="a1b88-131">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="a1b88-132">تعطيل الأمان</span><span class="sxs-lookup"><span data-stu-id="a1b88-132">Disabling security</span></span>
<span data-ttu-id="a1b88-133">نفترض أن مؤسستك ترغب في تقييد الوصول إلى البيانات.</span><span class="sxs-lookup"><span data-stu-id="a1b88-133">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="a1b88-134">إذا تم تعطيل معلمات الأمان، لسبب ما، عند تشغيل محاسبة التكاليف، فيجب على المالك إضافة دور **محاسب التكاليف** في Power BI بدلًا من ذلك.</span><span class="sxs-lookup"><span data-stu-id="a1b88-134">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="a1b88-135">إذا قمت بتغيير الأمان من حالة التمكين إلى حالة التعطيل، فمن المستحسن إزالة مستخدمين من دور **مراقب كائن التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="a1b88-135">If you change security from an enabled state to a disabled state, it's a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="a1b88-136">والعكس بالعكس إذا كنت تقوم بإعادة تمكين الأمان.</span><span class="sxs-lookup"><span data-stu-id="a1b88-136">And vice versa if you re-enable security.</span></span> <span data-ttu-id="a1b88-137">يمكن للمستخدمين الانتماء إلى كلا الدورين.</span><span class="sxs-lookup"><span data-stu-id="a1b88-137">Users can belong to both roles.</span></span> <span data-ttu-id="a1b88-138">يمثل الوصول المشترك اتحاد كل من الدورين.</span><span class="sxs-lookup"><span data-stu-id="a1b88-138">Joint access is the union of both roles.</span></span> <span data-ttu-id="a1b88-139">وفيما يتعلق بمحتوى **تحليل محاسبة التكاليف** في Power BI، سيتمكن المستخدمون الذين لديهم حق وصول مشترك باكتساب حق وصول غير مقيد إلى البيانات.</span><span class="sxs-lookup"><span data-stu-id="a1b88-139">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="a1b88-140">إذا كان الهدف تطبيق الوصول المقيد، يجب تعيين المستخدمين فقط على دور **مراقب كائن التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="a1b88-140">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="a1b88-141">تسري تحديثات الأمان على مستوى الصف فورًا.</span><span class="sxs-lookup"><span data-stu-id="a1b88-141">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="a1b88-142">يجب على المستخدمين المتأثرين تحديث مستعرضاتهم.</span><span class="sxs-lookup"><span data-stu-id="a1b88-142">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a1b88-143">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="a1b88-143">Additional resources</span></span>
<span data-ttu-id="a1b88-144">لمزيد من المعلومات حول الأمان على مستوى الصف في Power BI، راجع [إدارة الأمان على النموذج في Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="a1b88-144">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>
