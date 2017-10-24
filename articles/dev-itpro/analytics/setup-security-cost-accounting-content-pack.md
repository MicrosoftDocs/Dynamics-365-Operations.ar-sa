---
title: "إعداد الأمان لمحتوى Power BI - تحليل محاسبة التكاليف"
description: "يشرح هذا المقال كيفية نشر مستوى الوصول الآمن في محاسبة التكاليف إلى الأمان على مستوى الصف في Microsoft Power BI. تضمن هذه الوظيفة ألا يشاهد المستخدم سوى بيانات Power BI التي مُنح إمكانية الوصول لها."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 12fd8e11211b701304f9f4a68ff31f3b42e3e8ee
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a><span data-ttu-id="b777c-104">إعداد الأمان لمحتوى Power BI - تحليل محاسبة التكاليف</span><span class="sxs-lookup"><span data-stu-id="b777c-104">Set up security for the Cost accounting analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b777c-105">يشرح هذا المقال كيفية نشر مستوى الوصول الآمن في محاسبة التكاليف إلى الأمان على مستوى الصف في Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="b777c-105">This topic explains how you can propagate the access-level security in Cost accounting to row-level security in Microsoft Power BI.</span></span> <span data-ttu-id="b777c-106">تضمن هذه الوظيفة ألا يشاهد المستخدم سوى بيانات Power BI التي مُنح إمكانية الوصول لها.</span><span class="sxs-lookup"><span data-stu-id="b777c-106">This functionality helps guarantee that users see only Power BI data that they are granted access to.</span></span>

<a name="overview"></a><span data-ttu-id="b777c-107">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="b777c-107">Overview</span></span>
--------

<span data-ttu-id="b777c-108">يستخدم **تحليل محاسبة التكاليف** لمحتوى Microsoft Power BI الوصول الآمن على مستوى الصف لتقييد وصول المستخدم.</span><span class="sxs-lookup"><span data-stu-id="b777c-108">The **Cost accounting analysis** Microsoft Power BI content uses Power BI row-level security to limit a user's access.</span></span> <span data-ttu-id="b777c-109">يستند الأمان على التدرج الهرمي المؤسسي لمستوى الوصول الذي تم إعداده في معلمات محاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="b777c-109">Security is based on the access-level organizational hierarchy that is set up in the Cost accounting parameters.</span></span> <span data-ttu-id="b777c-110">لمزيد من المعلومات حول محتوى Power BI لـ **تحليل محاسبة التكاليف** راجع [محتوى Power BI - تحليل محاسبة التكاليف](cost-accounting-analysis-content-pack.md).</span><span class="sxs-lookup"><span data-stu-id="b777c-110">For more information about the **Cost accounting analysis** Power BI content, see [Cost accounting analysis Power BI content](cost-accounting-analysis-content-pack.md).</span></span>

## <a name="setup"></a><span data-ttu-id="b777c-111">الإعداد</span><span class="sxs-lookup"><span data-stu-id="b777c-111">Setup</span></span>
<span data-ttu-id="b777c-112">لنشر مستوى الوصول الآمن لـ Power BI، يجب على مالك محتوى Power BI اتباع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="b777c-112">To propagate access-level security to Power BI, the owner of the Power BI content must follow these steps.</span></span> <span data-ttu-id="b777c-113">**ملاحظة:** يصبح المستخدم الذي ينشر محتوى Power BI لـ **تحليل محاسبة التكاليف** المالك تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="b777c-113">**Note:** The user who publishes the **Cost accounting analysis** Power BI content automatically becomes the owner.</span></span> <span data-ttu-id="b777c-114">يمكن للمالك فقط إعداد الأمان في Power BI.</span><span class="sxs-lookup"><span data-stu-id="b777c-114">Only an owner can set up security in Power BI.</span></span> <span data-ttu-id="b777c-115">بالإضافة إلى ذلك، حتى يقوم مالك بإضافة مستخدمين على PowerBI.com، لا يمكن لأي شخص بخلاف المالك رؤية أي بيانات في محتوى Power BI لـ **تحليل محاسبة التكاليف**.</span><span class="sxs-lookup"><span data-stu-id="b777c-115">Additionally, until an owner adds other users on PowerBI.com, no one except the owner can see any data in the **Cost accounting analysis** Power BI content.</span></span>

1.  <span data-ttu-id="b777c-116">نشرف ملف التعريف إلى Power BI.</span><span class="sxs-lookup"><span data-stu-id="b777c-116">Publish the definition file to Power BI.</span></span>
2.  <span data-ttu-id="b777c-117">تسجيل الدخول إلى PowerBI.com.</span><span class="sxs-lookup"><span data-stu-id="b777c-117">Sign in to PowerBI.com.</span></span>
3.  <span data-ttu-id="b777c-118">العثور على قاعدة بيانات لمحتوى Power BI لـ **تحليل محاسبة التكاليف**.</span><span class="sxs-lookup"><span data-stu-id="b777c-118">Find the dataset for the **Cost accounting analysis** Power BI content.</span></span>
4.  <span data-ttu-id="b777c-119">افتح صفحة الأمان.</span><span class="sxs-lookup"><span data-stu-id="b777c-119">Open the security page.</span></span> 

    ![فتح صفحة الأمان](./media/CA-picture-1.png)

5.  <span data-ttu-id="b777c-121">**مراقب كائن التكلفة** قد تم إنشاؤه بالفعل.</span><span class="sxs-lookup"><span data-stu-id="b777c-121">The **Cost object controller** role is already created.</span></span> <span data-ttu-id="b777c-122">إضافة أعضاء آخرين يشكلوا جزءًا من التدرج الهرمي المؤسسي لمستوى الوصول لمحاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="b777c-122">Add other members who are part of the Cost accounting access-level organizational hierarchy.</span></span> 

    ![إضافة الأعضاء](./media/CA-picture-2.png)

<span data-ttu-id="b777c-124">سوف يرى المستخدمون الذين تم إضافتهم إلى دور **مراقب كائن التكلفة** البيانات المسموح لهم برؤيتها فقط، وفقًا للتعريف في التدرج الهرمي المؤسسي لمستوى الوصول لمحاسبة التكاليف.</span><span class="sxs-lookup"><span data-stu-id="b777c-124">Users who are added to the **Cost object controller** role will see only the data that they are allowed to see, according to the definition in the Cost accounting access-level organizational hierarchy.</span></span> <span data-ttu-id="b777c-125">**ملاحظة:** ينطبق الوصول الآمن على مستوى الصف على اللوحات والتقارير في Microsoft Dynamics 365 for Finance and Operations التي تم تضمينها من Power BI.</span><span class="sxs-lookup"><span data-stu-id="b777c-125">**Note:** Row-level security applies to tiles and reports in Microsoft Dynamics 365 for Finance and Operations that are embedded from Power BI.</span></span>

## <a name="updating-security"></a><span data-ttu-id="b777c-126">تحديث الأمان</span><span class="sxs-lookup"><span data-stu-id="b777c-126">Updating security</span></span>
<span data-ttu-id="b777c-127">في حالة إجراء تحديثات لمستوى الوصول الآمن في محاسبة التكليف، وكت تريد أن يعكس Power BI هذه التحديثات، فمن ثم يجب عليك تحديث متجر الكيان لمحتوى Power BI لـ **تحليل محاسبة التكاليف**.</span><span class="sxs-lookup"><span data-stu-id="b777c-127">If updates are made to access-level security in Cost accounting, and you want Power BI to reflect those updates, you must update the entity store for the **Cost accounting analysis** Power BI content.</span></span> <span data-ttu-id="b777c-128">بعد إكمال تحديث مخزن الكيانات من Finance and Operations، يجب تحديث المنتجات على PowerBI.com. لمزيد من المعلومات حول كيفية إجراء عملية تحديث لمخزن الكيانات، راجع [تحديث مخزن الكيانات](power-bi-integration-entity-store.md#update-entity-store).</span><span class="sxs-lookup"><span data-stu-id="b777c-128">After you complete the entity store update from Finance and Operations, you must update the artifacts on PowerBI.com. For more information about how to do an entity store update, see [Update entity store](power-bi-integration-entity-store.md#update-entity-store).</span></span> <span data-ttu-id="b777c-129">يجب على مالك محتوى Power BI لـ **تحليل محاسبة التكاليف** أيضًا القيام بإجراء تحديث متجر كيان إذا تمت منح مستخدمين جدد صلاحية الوصول للتدرج الهرمي المؤسسي.</span><span class="sxs-lookup"><span data-stu-id="b777c-129">The owner of the **Cost accounting analysis** Power BI content must also do an entity store update if new users are granted access to the organizational hierarchy.</span></span> <span data-ttu-id="b777c-130">بالإضافة إلى ذلك، يجب على المالك إضافة مستخدمين جدد إلى دور **مراقب كائن التكلفة** في PowerBI.com، حيث يتم تطبيق الأمان على مستوى الصفوف لها.</span><span class="sxs-lookup"><span data-stu-id="b777c-130">Additionally, the owner must add the new users to the **Cost object controller** role on PowerBI.com, so that row-level security is applied for them.</span></span>

## <a name="disabling-security"></a><span data-ttu-id="b777c-131">تعطيل الأمان</span><span class="sxs-lookup"><span data-stu-id="b777c-131">Disabling security</span></span>
<span data-ttu-id="b777c-132">نفترض أن مؤسستك ترغب في تقييد الوصول إلى البيانات.</span><span class="sxs-lookup"><span data-stu-id="b777c-132">We assume that your organization wants to restrict data access.</span></span> <span data-ttu-id="b777c-133">إذا تم تعطيل معلمات الأمان، لسبب ما، عندما تقوم بتشغيل محاسبة التكاليف، فمن ثم يجب على المالك إضافة مستخدمين إلى دور **محاسب التكاليف** في Power BI بدلًا من ذلك.</span><span class="sxs-lookup"><span data-stu-id="b777c-133">If, for some reason, the security parameters are disabled when you run Cost accounting, the owner must add users to the **Cost accountant** role in Power BI instead.</span></span> <span data-ttu-id="b777c-134">إذا قمت بتغيير الأمان من حالة ممكنة لحالة معطلة، فمن ثم تُعد فكرة جيدة إزالة مستخدمين من دور **مراقب كائن التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="b777c-134">If you change security from an enabled state to a disabled state, it’s a good idea to remove users from the **Cost object controller** role.</span></span> <span data-ttu-id="b777c-135">والعكس بالعكس إذا كنت تقوم بإعادة تمكين الأمان.</span><span class="sxs-lookup"><span data-stu-id="b777c-135">And vice versa if you re-enable security.</span></span> <span data-ttu-id="b777c-136">يمكن للمستخدمين الانتماء إلى كلا الدورين.</span><span class="sxs-lookup"><span data-stu-id="b777c-136">Users can belong to both roles.</span></span> <span data-ttu-id="b777c-137">يمثل الوصول المشترك اتحاد كل من الدورين.</span><span class="sxs-lookup"><span data-stu-id="b777c-137">Joint access is the union of both roles.</span></span> <span data-ttu-id="b777c-138">وفيما يتعلق بمحتوى Power BI لـ **تحليل محاسبة التكاليف**، فيكون للمستخدمين الذي لديهم حق الوصول المشترك، وصول غير مقيد للبيانات.</span><span class="sxs-lookup"><span data-stu-id="b777c-138">In the case of the **Cost accounting analysis** Power BI content, users who have joint access have unrestricted data access.</span></span> <span data-ttu-id="b777c-139">إذا كان الهدف تطبيق الوصول المقيد، يجب تعيين المستخدمين فقط على دور **مراقب كائن التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="b777c-139">If your goal is to apply restricted access, users must be assigned only to the **Cost object controller** role.</span></span> <span data-ttu-id="b777c-140">تسري تحديثات الأمان على مستوى الصف فورًا.</span><span class="sxs-lookup"><span data-stu-id="b777c-140">These row-level security updates take effect immediately.</span></span> <span data-ttu-id="b777c-141">يجب على المستخدمين المتأثرين تحديث مستعرضاتهم.</span><span class="sxs-lookup"><span data-stu-id="b777c-141">Affected users should refresh their browsers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b777c-142">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="b777c-142">Additional resources</span></span>
<span data-ttu-id="b777c-143">لمزيد من المعلومات حول مستوى الوصول الآمن على مستوى الصف لـ Power BI، راجع [إدارة الأمان على النموذج الخاص بك في Power BI"](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span><span class="sxs-lookup"><span data-stu-id="b777c-143">To learn more about Power BI row-level security, see [Manage security on your model in Power BI](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).</span></span>




