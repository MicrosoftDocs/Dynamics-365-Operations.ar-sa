---
title: التبديل بين تصميمات المورّدين
description: يصف هذا الموضوع كيفية تبديل تكامل بيانات البائع بين تطبيقات Finance and Operations وDataverse.
author: RamaKrishnamoorthy
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 5a18fed2eac4c120dca20a1d7797d047639275b9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750584"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="6c31e-103">التبديل بين تصميمات المورّدين</span><span class="sxs-lookup"><span data-stu-id="6c31e-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="6c31e-104">تدفق بيانات المورّد</span><span class="sxs-lookup"><span data-stu-id="6c31e-104">Vendor data flow</span></span> 

<span data-ttu-id="6c31e-105">إذا اخترت استخدام جدول **الحساب** لتخزين الموردين من نوع **المؤسسة** وجدول **جهة الاتصال** لتخزين الموردين من نوع **الشخص** ، فقم بتكوين مهام سير العمل التالية.</span><span class="sxs-lookup"><span data-stu-id="6c31e-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="6c31e-106">وإلا، فلن يكون هذا التكوين مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="6c31e-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="6c31e-107">استخدام تصميم المورد الموسع للموردين من نوع المؤسسة</span><span class="sxs-lookup"><span data-stu-id="6c31e-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="6c31e-108">تحتوي حزمة حل **Dynamics365FinanceExtended** على قوالب عملية سير العمل التالية.</span><span class="sxs-lookup"><span data-stu-id="6c31e-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="6c31e-109">ستقوم بإنشاء سير عمل لكل قالب.</span><span class="sxs-lookup"><span data-stu-id="6c31e-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="6c31e-110">إنشاء الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="6c31e-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="6c31e-111">إنشاء الموردين في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="6c31e-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="6c31e-112">تحديث الموردين في جدول الحسابات</span><span class="sxs-lookup"><span data-stu-id="6c31e-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="6c31e-113">تحديث الموردين في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="6c31e-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="6c31e-114">لإنشاء عمليات سير عمل جديدة باستخدام قوالب عملية سير العمل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="6c31e-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="6c31e-115">أنشئ عملية سير عمل لجدول **المورد**، ثم حدد قالب عمل سير العمل **إنشاء الموردين في جدول الحسابات**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="6c31e-116">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-116">Then select **OK**.</span></span> <span data-ttu-id="6c31e-117">يعالج سير العمل هذا سيناريو إنشاء المورد لجدول **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![إنشاء الموردين في عملية سير عمل جدول الحسابات](media/create_process.png)

2. <span data-ttu-id="6c31e-119">أنشئ عملية سير عمل لجدول **المورد**، ثم حدد قالب عمل سير العمل **تحديث الموردين في جدول الحسابات**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="6c31e-120">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-120">Then select **OK**.</span></span> <span data-ttu-id="6c31e-121">يعالج سير العمل هذا سيناريو تحديث المورد لجدول **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="6c31e-122">أنشئ عملية سير عمل لجدول **الحساب**، ثم حدد قالب عمل سير العمل **إنشاء الموردين في جدول الموردين**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="6c31e-123">أنشئ عملية سير عمل لجدول **الحساب**، ثم حدد قالب عمل سير العمل **تحديث الموردين في جدول الموردين**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="6c31e-124">يمكنك تكوين مهام سير العمل بمثابه عمليات سير عمل في الوقت الحقيقي أو مهام سير العمل الخلفية وفقًا لمتطلباتك.</span><span class="sxs-lookup"><span data-stu-id="6c31e-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="6c31e-125">لتكوين سير عمل كسير عمل خلفية، حدد **التحويل إلى سير عمل خلفية**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![التحويل إلى زر سير عمل في الخلفية](media/background_workflow.png)

6. <span data-ttu-id="6c31e-127">قم بتنشيط مهام سير العمل التي قمت بإنشائها في جدولي **الحساب** و **المورد** لبدء استخدام الجدول **الحساب** لتخزين المعلومات للموردين من نوع **المؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="6c31e-128">استخدام تصميم المورد الموسع للموردين من نوع الشخص</span><span class="sxs-lookup"><span data-stu-id="6c31e-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="6c31e-129">تحتوي حزمة حل **Dynamics365FinanceExtended** على قوالب عملية سير العمل التالية.</span><span class="sxs-lookup"><span data-stu-id="6c31e-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="6c31e-130">ستقوم بإنشاء سير عمل لكل قالب.</span><span class="sxs-lookup"><span data-stu-id="6c31e-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="6c31e-131">إنشاء الموردين من نوع الشخص في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="6c31e-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="6c31e-132">إنشاء الموردين من نوع الشخص في جدول جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="6c31e-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="6c31e-133">تحديث الموردين من نوع الشخص في جدول جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="6c31e-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="6c31e-134">تحديث الموردين من نوع الشخص في جدول الموردين</span><span class="sxs-lookup"><span data-stu-id="6c31e-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="6c31e-135">لإنشاء عمليات سير عمل جديدة باستخدام قوالب عملية سير العمل، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="6c31e-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="6c31e-136">أنشئ عملية سير عمل لجدول **المورد**، ثم حدد قالب عمل سير العمل **إنشاء الموردين من نوع الشخص في جدول جهات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="6c31e-137">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-137">Then select **OK**.</span></span> <span data-ttu-id="6c31e-138">يعالج سير العمل هذا سيناريو إنشاء المورد لجدول **جهة الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="6c31e-139">أنشئ عملية سير عمل لجدول **المورد**، ثم حدد قالب عمل سير العمل **تحديث الموردين من نوع الشخص في جدول جهات الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="6c31e-140">ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-140">Then select **OK**.</span></span> <span data-ttu-id="6c31e-141">يعالج سير العمل هذا سيناريو تحديث المورد لجدول **جهة الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="6c31e-142">أنشئ عملية سير عمل لجدول **جهة الاتصال**، ثم حدد قالب **إنشاء الموردين من نوع الشخص في جدول الموردين**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="6c31e-143">أنشئ عملية سير عمل لجدول **جهة الاتصال**، ثم حدد قالب **تحديث الموردين من نوع الشخص في جدول الموردين**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="6c31e-144">يمكنك تكوين مهام سير العمل بمثابه عمليات سير عمل في الوقت الحقيقي أو مهام سير العمل الخلفية وفقًا لمتطلباتك.</span><span class="sxs-lookup"><span data-stu-id="6c31e-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="6c31e-145">لتكوين سير عمل كسير عمل خلفية، حدد **التحويل إلى سير عمل خلفية**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="6c31e-146">قم بتنشيط مهام سير العمل التي قمت بإنشائها في جدولي **جهة الاتصال** و **المورد** لبدء استخدام جدول **جهة الاتصال** لتخزين المعلومات للموردين من نوع **الشخص**.</span><span class="sxs-lookup"><span data-stu-id="6c31e-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]