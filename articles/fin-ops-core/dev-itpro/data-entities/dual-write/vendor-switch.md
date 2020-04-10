---
title: التبديل بين تصميمات المورّدين
description: يصف هذا الموضوع كيفية تبديل تكامل بيانات البائع بين تطبيقات Finance and Operations وCommon Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: ffd7a4c01810578b4abb6942aeff76e5147fafa9
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173029"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="7f243-103">التبديل بين تصميمات المورّدين</span><span class="sxs-lookup"><span data-stu-id="7f243-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="7f243-104">تدفق بيانات المورّد</span><span class="sxs-lookup"><span data-stu-id="7f243-104">Vendor data flow</span></span> 

<span data-ttu-id="7f243-105">إذا اخترت استخدام كيان **الحساب** لتخزين الموردين من نوع **المؤسسة** وكيان **جهة الاتصال** لتخزين الموردين من نوع **الشخص** ، فقم بتكوين مهام سير العمل التالية.</span><span class="sxs-lookup"><span data-stu-id="7f243-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="7f243-106">وإلا، فلن يكون هذا التكوين مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="7f243-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="7f243-107">استخدام تصميم المورد الموسع للموردين من نوع المؤسسة</span><span class="sxs-lookup"><span data-stu-id="7f243-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="7f243-108">تحتوي حزمة حل **Dynamics365FinanceExtended** على قوالب عملية سير العمل التالية.</span><span class="sxs-lookup"><span data-stu-id="7f243-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="7f243-109">ستقوم بإنشاء سير عمل لكل قالب.</span><span class="sxs-lookup"><span data-stu-id="7f243-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="7f243-110">إنشاء الموردين في كيان الحسابات</span><span class="sxs-lookup"><span data-stu-id="7f243-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="7f243-111">إنشاء الموردين في كيان الموردين</span><span class="sxs-lookup"><span data-stu-id="7f243-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="7f243-112">تحديت الموردين في كيان الحسابات</span><span class="sxs-lookup"><span data-stu-id="7f243-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="7f243-113">تحديث الموردين في كيان الموردين</span><span class="sxs-lookup"><span data-stu-id="7f243-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="7f243-114">لإنشاء عمليات سير عمل جديدة باستخدام قوالب عملية سير العمل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="7f243-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="7f243-115">أنشئ عملية سير عمل لكيان **المورد**، ثم حدد قالب عمل سير العمل **إنشاء الموردين في كيان الحسابات**.</span><span class="sxs-lookup"><span data-stu-id="7f243-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="7f243-116">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7f243-116">Then select **OK**.</span></span> <span data-ttu-id="7f243-117">يعالج سير العمل هذا سيناريو إنشاء المورد لكيان **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="7f243-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![إنشاء الموردين في عملية سير عمل كيان الحسابات](media/create_process.png)

2. <span data-ttu-id="7f243-119">أنشئ عملية سير عمل لكيان **المورد**، ثم حدد قالب عمل سير عمل **تحديث الموردين في كيان الحسابات**.</span><span class="sxs-lookup"><span data-stu-id="7f243-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="7f243-120">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7f243-120">Then select **OK**.</span></span> <span data-ttu-id="7f243-121">يعالج سير العمل هذا سيناريو تحديث المورد لكيان **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="7f243-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="7f243-122">أنشئ عملية سير عمل لكيان **الحساب**، ثم حدد قالب عمل سير عمل **إنشاء الموردين في كيان الموردين**.</span><span class="sxs-lookup"><span data-stu-id="7f243-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="7f243-123">أنشئ عملية سير عمل لكيان **الحساب**، ثم حدد قالب عمل سير عمل **تحديث الموردين في كيان الموردين**.</span><span class="sxs-lookup"><span data-stu-id="7f243-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="7f243-124">يمكنك تكوين مهام سير العمل بمثابه عمليات سير عمل في الوقت الحقيقي أو مهام سير العمل الخلفية وفقًا لمتطلباتك.</span><span class="sxs-lookup"><span data-stu-id="7f243-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="7f243-125">لتكوين سير عمل كسير عمل خلفية، حدد **التحويل إلى سير عمل خلفية**.</span><span class="sxs-lookup"><span data-stu-id="7f243-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![التحويل إلى زر سير عمل في الخلفية](media/background_workflow.png)

6. <span data-ttu-id="7f243-127">قم بتنشيط مهام سير العمل التي قمت بإنشائها في كياني **الحساب** و**المورد** لبدء استخدام كيان **الحساب** لتخزين المعلومات للموردين من نوع **المؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="7f243-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="7f243-128">استخدام تصميم المورد الموسع للموردين من نوع الشخص</span><span class="sxs-lookup"><span data-stu-id="7f243-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="7f243-129">تحتوي حزمة حل **Dynamics365FinanceExtended** على قوالب عملية سير العمل التالية.</span><span class="sxs-lookup"><span data-stu-id="7f243-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="7f243-130">ستقوم بإنشاء سير عمل لكل قالب.</span><span class="sxs-lookup"><span data-stu-id="7f243-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="7f243-131">إنشاء الموردين من نوع الشخص في كيان الموردين</span><span class="sxs-lookup"><span data-stu-id="7f243-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="7f243-132">إنشاء الموردين من نوع الشخص في كيان جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="7f243-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="7f243-133">تحديث الموردين من نوع الشخص في كيان جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="7f243-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="7f243-134">تحديث الموردين من نوع الشخص في كيان الموردين</span><span class="sxs-lookup"><span data-stu-id="7f243-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="7f243-135">لإنشاء عمليات سير عمل جديدة باستخدام قوالب عملية سير العمل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="7f243-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="7f243-136">أنشئ عملية سير عمل لكيان **المورد**، ثم حدد قالب عمل سير العمل **إنشاء الموردين من نوع الشخص في كيان جهات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="7f243-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="7f243-137">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7f243-137">Then select **OK**.</span></span> <span data-ttu-id="7f243-138">يعالج سير العمل هذا سيناريو إنشاء المورد لكيان **جهة الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="7f243-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="7f243-139">أنشئ عملية سير عمل لكيان **المورد**، ثم حدد قالب عمل سير العمل **تحديث الموردين من نوع الشخص في كيان جهات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="7f243-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="7f243-140">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="7f243-140">Then select **OK**.</span></span> <span data-ttu-id="7f243-141">يعالج سير العمل هذا سيناريو تحديث المورد لكيان **جهة الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="7f243-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="7f243-142">أنشئ عملية سير عمل لكيان **جهة الاتصال**، ثم حدد قالب **إنشاء الموردين من نوع الشخص في كيان الموردين**.</span><span class="sxs-lookup"><span data-stu-id="7f243-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="7f243-143">أنشئ عملية سير عمل لكيان **جهة الاتصال**، ثم حدد قالب **تحديث الموردين من نوع الشخص في كيان الموردين**.</span><span class="sxs-lookup"><span data-stu-id="7f243-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="7f243-144">يمكنك تكوين مهام سير العمل بمثابه عمليات سير عمل في الوقت الحقيقي أو مهام سير العمل الخلفية وفقًا لمتطلباتك.</span><span class="sxs-lookup"><span data-stu-id="7f243-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="7f243-145">لتكوين سير عمل كسير عمل خلفية، حدد **التحويل إلى سير عمل خلفية**.</span><span class="sxs-lookup"><span data-stu-id="7f243-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="7f243-146">قم بتنشيط مهام سير العمل التي قمت بإنشائها في كياني **جهة الاتصال** و**المورد** لبدء استخدام كيان **جهة الاتصال** لتخزين المعلومات للموردين من نوع **الشخص**.</span><span class="sxs-lookup"><span data-stu-id="7f243-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
