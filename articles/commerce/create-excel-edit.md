---
title: إنشاء مصنف Excel لتحرير حركات البيع بالتجزئة
description: يوضح هذا الموضوع كيفية إنشاء دفتر عمل Excel بحيث يمكنك تحرير حركات البيع بالتجزئة في Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3a4bc0a91ee2215dcde2f18575d58ab1ef2f5581
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207933"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="6a2e4-103">إنشاء مصنف Excel لتحرير حركات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="6a2e4-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a2e4-104">يوضح هذا الموضوع كيفية إنشاء دفتر عمل Excel بحيث يمكنك تحرير حركات البيع بالتجزئة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6a2e4-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="6a2e4-105">Overview</span></span>

<span data-ttu-id="6a2e4-106">يوجد نموذج Excel محدد مسبقًا يمكن للعملاء الوصول إليه من أجزاء مختلفة من النظام واستخدامه لتحرير وتدقيق حركات البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="6a2e4-107">ولكن، يمكن للعملاء أيضًا إنشاء دفتر عمل Excel مخصص لهذا الغرض.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="6a2e4-108">إنشاء دفتر عمل Excel وتكوينه</span><span class="sxs-lookup"><span data-stu-id="6a2e4-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="6a2e4-109">لإنشاء وتكوين دفتر عمل Excel بحيث يمكنك تحرير حركات البيع بالتجزئة، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="6a2e4-110">افتح برنامج Excel، وقم بإنشاء دفتر عمل فارغ.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="6a2e4-111">في علامة التبويب **إدراج** ، حدد **وظائفي الإضافية**.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="6a2e4-112">في الجزء الأيمن، حدد الارتباط **إضافة معلومات الخادم**.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="6a2e4-113">ادخل عنوان URL الخاص بالخادم، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="6a2e4-114">في حاله ظهور رسالة الخطأ "لم يتم العثور علي تسجيلات في البرنامج"، اتبع الخطوات التالية لحل المشكلة:</span><span class="sxs-lookup"><span data-stu-id="6a2e4-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="6a2e4-115">في Commerce، انتقل إلى **‏‫إدارة النظام‬ \> إعداد \> معلمات تطبيق Office**.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="6a2e4-116">علي علامة التبويب السريعة **معلمات التطبيق** ، حدد **تهيئه معلمات التطبيق**.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="6a2e4-117">في المربع رسالة التأكيد، حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="6a2e4-118">علي علامة التبويب السريعة **التطبيقات المسجلة** ، حدد **تهيئه تسجيل التطبيقات**.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="6a2e4-119">كرر الخطوات الثلاث السابقة حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="6a2e4-120">حدد **تصميم**، ثم حدد **إضافة تطبيق**.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="6a2e4-121">استنادًا إلى البيانات التي يتعين تعديلها، حدد الكيانات التي يتعين إضافتها إلى مصنف Excel للتحرير.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="6a2e4-122">استخدم الجدول التالي كمرجع.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="6a2e4-123">نوع المعاملة</span><span class="sxs-lookup"><span data-stu-id="6a2e4-123">Transaction type</span></span> | <span data-ttu-id="6a2e4-124">كيانات البيانات المراد استخدامها</span><span class="sxs-lookup"><span data-stu-id="6a2e4-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="6a2e4-125">معاملات الدفع نقدًا والاستلام فورًا‬‬‏‫، الطلبات عبر الإنترنت، أوامر عملاء غير متزامنة، عروض أسعار للعملاء غير متزامنة</span><span class="sxs-lookup"><span data-stu-id="6a2e4-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="6a2e4-126">المعاملات (القابلة للتدقيق)، ومعاملات المبيعات (القابلة للتدقيق)، وحركات الدفع (القابلة للتدقيق)، والحركات الضريبية (القابلة للتدقيق)، وحركات الخصم (القابلة للتدقيق)، وحركات المصروفات (القابلة للتدقيق)</span><span class="sxs-lookup"><span data-stu-id="6a2e4-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="6a2e4-127">إيداع بنكي</span><span class="sxs-lookup"><span data-stu-id="6a2e4-127">Bank drop</span></span> | <span data-ttu-id="6a2e4-128">معاملة (قابلة للتدقيق)، ومعاملات الدفع البنكية (قابلة للتدقيق)</span><span class="sxs-lookup"><span data-stu-id="6a2e4-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="6a2e4-129">إيداع بالخزينة</span><span class="sxs-lookup"><span data-stu-id="6a2e4-129">Safe drop</span></span> | <span data-ttu-id="6a2e4-130">معاملة (قابلة للتدقيق)، ومعاملات الإيداع بالخزينة (قابلة للتدقيق)</span><span class="sxs-lookup"><span data-stu-id="6a2e4-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="6a2e4-131">إقرار الدفع</span><span class="sxs-lookup"><span data-stu-id="6a2e4-131">Tender declaration</span></span> | <span data-ttu-id="6a2e4-132">معاملة (قابلة للتدقيق)، ومعاملات إقرار الدفع (قابلة للتدقيق)</span><span class="sxs-lookup"><span data-stu-id="6a2e4-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="6a2e4-133">الإيرادات والمصروفات</span><span class="sxs-lookup"><span data-stu-id="6a2e4-133">Income, Expense</span></span> | <span data-ttu-id="6a2e4-134">معاملة (قابلة للتدقيق)، ومعاملات الإيرادات والمصروفات (قابلة للتدقيق)، ومعاملات الدفع (قابلة للتدقيق)</span><span class="sxs-lookup"><span data-stu-id="6a2e4-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="6a2e4-135">إعلان مبلغ البدء، وإزالة الدفع، وإدخال معوم، وتغيير الدفع، ودفع الفاتورة، وإيداع العميل</span><span class="sxs-lookup"><span data-stu-id="6a2e4-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="6a2e4-136">معاملة (قابلة للتدقيق)، ومعاملات الدفع (قابلة للتدقيق)</span><span class="sxs-lookup"><span data-stu-id="6a2e4-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="6a2e4-137">من المهم أن تقوم بإضافة كيان بيانات واحد فقط لكل دفتر عمل Excel.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="6a2e4-138">بالإضافة إلى ذلك، يجب إضافة جميع الحقول التي تم تمييزها برمز مفتاح إلى المصنف ذي الصلة.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="6a2e4-139">بعد تكوين المصنف، قم بتطبيق عوامل التصفية المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="6a2e4-140">تأكد من تطبيق نفس عوامل التصفية علي كافة أوراق العمل الموجودة في الملف.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="6a2e4-141">تجنب تحميل كميات كبيرة جدًا من البيانات في ملف Excel.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="6a2e4-142">وإلا فقد يتأثر الأداء، وقد يتباطأ برنامج Excel والنظام الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="6a2e4-143">نوصيك باستخدام "الشركة" وإما "رقم كشف الحساب" أو "رقم الحركة" كعوامل تصفية للملف الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="6a2e4-144">بعد تكوين عوامل التصفية، حدد **تحديث** لتحميل البيانات.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="6a2e4-145">قم بتحرير البيانات المطلوبة، ثم قم بنشرها.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="6a2e4-146">إذا لم يكن الزر **نشر** متوفرًا، فمن المحتمل عدم إضافة بعض الحقول الأساسية إلى دفتر عمل Excel.</span><span class="sxs-lookup"><span data-stu-id="6a2e4-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6a2e4-147">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6a2e4-147">Additional resources</span></span>

[<span data-ttu-id="6a2e4-148">تحرير وتدقيق حركات الدفع نقدًا والاستلام فورًا وإدارة النقد</span><span class="sxs-lookup"><span data-stu-id="6a2e4-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="6a2e4-149">تحرير وتدقيق الأوامر عبر الإنترنت وحركات أوامر العميل غير المتزامنة</span><span class="sxs-lookup"><span data-stu-id="6a2e4-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="6a2e4-150">تحرير الأبعاد المالية لحركات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="6a2e4-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="6a2e4-151">إضافة حقول إلى مصنف Excel لتحرير حركات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="6a2e4-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]