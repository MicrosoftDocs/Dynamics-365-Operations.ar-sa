---
title: التبديل بين تصميمات المورّدين
description: يصف هذا الموضوع كيفية تبديل تكامل بيانات البائع بين تطبيقات Finance and Operations وDataverse.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: d2c22123d5f05945b34eb107c5b912852aec387a
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744455"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="a8812-103">التبديل بين تصميمات المورّدين</span><span class="sxs-lookup"><span data-stu-id="a8812-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="a8812-104">تدفق بيانات المورّد</span><span class="sxs-lookup"><span data-stu-id="a8812-104">Vendor data flow</span></span> 

<span data-ttu-id="a8812-105">إذا اخترت استخدام جدول **الحساب** لتخزين الموردين من نوع **المؤسسة** وجدول **جهة الاتصال** لتخزين الموردين من نوع **الشخص** ، فقم بتكوين مهام سير العمل التالية.</span><span class="sxs-lookup"><span data-stu-id="a8812-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="a8812-106">وإلا، فلن يكون هذا التكوين مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="a8812-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="a8812-107">استخدام تصميم المورد الموسع للموردين من نوع المؤسسة</span><span class="sxs-lookup"><span data-stu-id="a8812-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="a8812-108">تحتوي حزمة حل **Dynamics365FinanceExtended** على قوالب عملية سير العمل التالية.</span><span class="sxs-lookup"><span data-stu-id="a8812-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="a8812-109">ستقوم بإنشاء سير عمل لكل قالب.</span><span class="sxs-lookup"><span data-stu-id="a8812-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="a8812-110">إنشاء الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="a8812-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="a8812-111">إنشاء الموردين في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="a8812-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="a8812-112">تحديث الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="a8812-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="a8812-113">تحديث الموردين في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="a8812-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="a8812-114">لإنشاء عمليات سير عمل جديدة باستخدام قوالب عملية سير العمل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a8812-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="a8812-115">أنشئ عملية سير عمل لجدول **المورد**، ثم حدد قالب عمل سير العمل **إنشاء الموردين في جدول الحسابات**.</span><span class="sxs-lookup"><span data-stu-id="a8812-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="a8812-116">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a8812-116">Then select **OK**.</span></span> <span data-ttu-id="a8812-117">يعالج سير العمل هذا سيناريو إنشاء المورد لجدول **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="a8812-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![إنشاء الموردين في عملية سير عمل جدول الحسابات](media/create_process.png)

2. <span data-ttu-id="a8812-119">أنشئ عملية سير عمل لجدول **المورد**، ثم حدد قالب عمل سير العمل **تحديث الموردين في جدول الحسابات**.</span><span class="sxs-lookup"><span data-stu-id="a8812-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="a8812-120">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a8812-120">Then select **OK**.</span></span> <span data-ttu-id="a8812-121">يعالج سير العمل هذا سيناريو تحديث المورد لجدول **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="a8812-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="a8812-122">أنشئ عملية سير عمل لجدول **الحساب**، ثم حدد قالب عمل سير العمل **إنشاء الموردين في جدول الموردين**.</span><span class="sxs-lookup"><span data-stu-id="a8812-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="a8812-123">أنشئ عملية سير عمل لجدول **الحساب**، ثم حدد قالب عمل سير العمل **تحديث الموردين في جدول الموردين**.</span><span class="sxs-lookup"><span data-stu-id="a8812-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="a8812-124">يمكنك تكوين مهام سير العمل بمثابه عمليات سير عمل في الوقت الحقيقي أو مهام سير العمل الخلفية وفقًا لمتطلباتك.</span><span class="sxs-lookup"><span data-stu-id="a8812-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="a8812-125">لتكوين سير عمل كسير عمل خلفية، حدد **التحويل إلى سير عمل خلفية**.</span><span class="sxs-lookup"><span data-stu-id="a8812-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![التحويل إلى زر سير عمل في الخلفية](media/background_workflow.png)

6. <span data-ttu-id="a8812-127">قم بتنشيط مهام سير العمل التي قمت بإنشائها في جدولي **الحساب** و **المورد** لبدء استخدام الجدول **الحساب** لتخزين المعلومات للموردين من نوع **المؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="a8812-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="a8812-128">استخدام تصميم المورد الموسع للموردين من نوع الشخص</span><span class="sxs-lookup"><span data-stu-id="a8812-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="a8812-129">تحتوي حزمة حل **Dynamics365FinanceExtended** على قوالب عملية سير العمل التالية.</span><span class="sxs-lookup"><span data-stu-id="a8812-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="a8812-130">ستقوم بإنشاء سير عمل لكل قالب.</span><span class="sxs-lookup"><span data-stu-id="a8812-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="a8812-131">إنشاء الموردين من نوع الشخص في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="a8812-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="a8812-132">إنشاء الموردين من نوع الشخص في جدول جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="a8812-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="a8812-133">تحديث الموردين من نوع الشخص في جدول جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="a8812-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="a8812-134">تحديث الموردين من نوع الشخص في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="a8812-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="a8812-135">لإنشاء عمليات سير عمل جديدة باستخدام قوالب عملية سير العمل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="a8812-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="a8812-136">أنشئ عملية سير عمل لجدول **المورد**، ثم حدد قالب عمل سير العمل **إنشاء الموردين من نوع الشخص في جدول جهات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="a8812-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="a8812-137">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a8812-137">Then select **OK**.</span></span> <span data-ttu-id="a8812-138">يعالج سير العمل هذا سيناريو إنشاء المورد لجدول **جهة الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="a8812-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="a8812-139">أنشئ عملية سير عمل لجدول **المورد**، ثم حدد قالب عمل سير العمل **تحديث الموردين من نوع الشخص في جدول جهات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="a8812-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="a8812-140">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="a8812-140">Then select **OK**.</span></span> <span data-ttu-id="a8812-141">يعالج سير العمل هذا سيناريو تحديث المورد لجدول **جهة الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="a8812-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="a8812-142">أنشئ عملية سير عمل لجدول **جهة الاتصال**، ثم حدد قالب **إنشاء الموردين من نوع الشخص في جدول الموردين**.</span><span class="sxs-lookup"><span data-stu-id="a8812-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="a8812-143">أنشئ عملية سير عمل لجدول **جهة الاتصال**، ثم حدد قالب **تحديث الموردين من نوع الشخص في جدول الموردين**.</span><span class="sxs-lookup"><span data-stu-id="a8812-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="a8812-144">يمكنك تكوين مهام سير العمل بمثابه عمليات سير عمل في الوقت الحقيقي أو مهام سير العمل الخلفية وفقًا لمتطلباتك.</span><span class="sxs-lookup"><span data-stu-id="a8812-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="a8812-145">لتكوين سير عمل كسير عمل خلفية، حدد **التحويل إلى سير عمل خلفية**.</span><span class="sxs-lookup"><span data-stu-id="a8812-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="a8812-146">قم بتنشيط مهام سير العمل التي قمت بإنشائها في جدولي **جهة الاتصال** و **المورد** لبدء استخدام جدول **جهة الاتصال** لتخزين المعلومات للموردين من نوع **الشخص**.</span><span class="sxs-lookup"><span data-stu-id="a8812-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>
