---
title: إنشاء شروط احتجاز مدفوعات المورّد وتطبيقها
description: يوفر هذا الموضوع معلومات حول كيفية إعداد شروط احتجاز مدفوعات المورّد وتطبيقها‬.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410189"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="54795-103">إنشاء شروط احتجاز مدفوعات المورّد وتطبيقها</span><span class="sxs-lookup"><span data-stu-id="54795-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="54795-104">يعتبر إعداد شروط احتجاز مدفوعات المورّد وتطبيقها‬ لمشروع ما مفيدًا عندما ترغب مؤسستك في الاحتفاظ بجزء من المدفوعات التي تم تسديدها للمورّد.</span><span class="sxs-lookup"><span data-stu-id="54795-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="54795-105">على سبيل المثال، عندما تريد تعليق الدفع للمورّد حتى تلبي المنتجات التي تم تسليمها توقعاتك.</span><span class="sxs-lookup"><span data-stu-id="54795-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="54795-106">يمكنك تحديد شروط احتجاز مدفوعات المورّد عند التفاوض بشأن عقد المورّد.</span><span class="sxs-lookup"><span data-stu-id="54795-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="54795-107">إنشاء شروط احتجاز مدفوعات المورّد</span><span class="sxs-lookup"><span data-stu-id="54795-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="54795-108">يمكنك إدخال النسبة المئوية لدفع المورّد التي تريد احتجاها والنسبة المئوية للمبالغ التي تم الاحتفاظ بها سابقًا والتي يجب إصدارها.</span><span class="sxs-lookup"><span data-stu-id="54795-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="54795-109">يتم الاحتفاظ بالمبالغ تلقائيًا في فواتير المورد حتى يصل الاتفاق إلى حالة الاكتمال المحددة .</span><span class="sxs-lookup"><span data-stu-id="54795-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="54795-110">بعد إعداد شروط الاحتجاز، يمكنك تطبيقها على أي مشروع خاص بهذا المورّد.</span><span class="sxs-lookup"><span data-stu-id="54795-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="54795-111">استخدم الخطوات التالية لإعداد شروط احتجاز مدفوعات المورّد والمحافظة عليها.</span><span class="sxs-lookup"><span data-stu-id="54795-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="54795-112">انتقل إلى **إدارة المشاريع ومحاسبتها‬** > **الاحتجاز** > **شروط احتجاز مدفوعات المورّد**.</span><span class="sxs-lookup"><span data-stu-id="54795-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="54795-113">حدد **جديد** لإضافة شرط احتجاز دفع مورّد جديد.</span><span class="sxs-lookup"><span data-stu-id="54795-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="54795-114">يتم إدخال قيمة **معرف القاعدة** للشرط الجديد تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="54795-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="54795-115">ادخل وصفًا مختصرًا في حقل **الوصف**، وعلى علامة التبويب السريعة **الشروط**، حدد **إضافة بند** لإدخال قيم الشروط لما يلي:</span><span class="sxs-lookup"><span data-stu-id="54795-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="54795-116">**النسبة المئوية للوحدات المسلمة**: أدخل النسبة المئوية لإكمال الشرط.</span><span class="sxs-lookup"><span data-stu-id="54795-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="54795-117">يتم احتجاز المبالغ تلقائيًا في فواتير المورّد حتى تساوي مرحلة استكمال المشروع النسبة المئوية المحددة.</span><span class="sxs-lookup"><span data-stu-id="54795-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="54795-118">على سبيل المثال، إذا أدخلت 50.00، فإن المبالغ يتم احتجازها حتى يصبح مكتملاً بنسبة 50 في المائة.</span><span class="sxs-lookup"><span data-stu-id="54795-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="54795-119">**نسبة الاحتجاز المئوية**: أدخل نسبة مئوية لمبلغ فاتورة المورّد يجب احتجازها.</span><span class="sxs-lookup"><span data-stu-id="54795-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="54795-120">على سبيل المثال، إذا أدخلت 10.00، سيتم عندئذٍ احتجاز 10 بالنسبة من المبلغ على فاتورة المورّد حتى يصل المشروع إلى النسبة المئوية للاكتمال كما تم تعيينها في **‎حقل النسبة المئوية للوحدات المسلمة**.</span><span class="sxs-lookup"><span data-stu-id="54795-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="54795-121">**النسبة المئوية التي سيتم إصدارها‬**: حدد **إضافة بند** لإدخال نسبة مئوية لأي مبالغ تم احتجازها سابقًا لإصدارها للمستوى المحدد من إكمال المشروع.</span><span class="sxs-lookup"><span data-stu-id="54795-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="54795-122">إذا كان لديك أكثر من مرحلة رئيسية لمستويات مختلفة من إكمال المشروع، فأدخل بند شرط منفصل لاحتجاز دفع المورّد لكل قاعدة احتجاز.</span><span class="sxs-lookup"><span data-stu-id="54795-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="54795-123">بإمكان كل بند أن يحدد نسبةً مئوية مختلفة للاحتجاز ونسبة مئوية مختلفة للإصدار لكل مستوى معين من مستويات إكمال المشروع.</span><span class="sxs-lookup"><span data-stu-id="54795-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="54795-124">بعد إنشاء شروط الاحتجاز لدفع المورّد، يمكنك تطبيقها على مشروع.</span><span class="sxs-lookup"><span data-stu-id="54795-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="54795-125">تطبيق شروط احتجاز المورّد على مشروع</span><span class="sxs-lookup"><span data-stu-id="54795-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="54795-126">انتقل إلى **إدارة المشاريع ومحاسبتها‬** > **المشاريع** > **جميع المشاريع** وافتح مشروعًا من صفحة قائمة المشاريع.</span><span class="sxs-lookup"><span data-stu-id="54795-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="54795-127">في علامة التبويب السريعة **اتفاقات المورد**، حدد **إضافة بند**.</span><span class="sxs-lookup"><span data-stu-id="54795-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="54795-128">في حقل **كود الحساب**، حدد أحد الخيارات التالية:</span><span class="sxs-lookup"><span data-stu-id="54795-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="54795-129">**جدول**: شروط احتجاز المورّد تنطبق على مورد واحد.</span><span class="sxs-lookup"><span data-stu-id="54795-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="54795-130">**مجموعة**: شروط احتجاز المورّد تنطبق على جميع المورّدين في مجموعة مورّدين.</span><span class="sxs-lookup"><span data-stu-id="54795-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="54795-131">**الكل**: شروط احتجاز المورّد تنطبق على جميع المورّدين.</span><span class="sxs-lookup"><span data-stu-id="54795-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="54795-132">في حقل **المورّد/مجموعة المورّدين**، حدد المورّد أو مجموعة المورّدين التي تنطبق عليها شروط احتجاز المورّد.</span><span class="sxs-lookup"><span data-stu-id="54795-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="54795-133">إذا قمت بتحديد **الكل** في الخطوة السابقة، فسيكون هذا الحقل غير متاح.</span><span class="sxs-lookup"><span data-stu-id="54795-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="54795-134">في حقل **شروط احتجاز المورّد**، حدد شروط الاحتجاز التي قمت بإنشائها في الإجراء السابق.</span><span class="sxs-lookup"><span data-stu-id="54795-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="54795-135">إذا كان المشروع يتضمن شروط الدفع عند الاستحقاق (PWP) للمورّد، فأدخل النسبة المئوية للحد الخاصة بالمشروع في الحقل **النسبة المئوية لحد PWP**.</span><span class="sxs-lookup"><span data-stu-id="54795-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="54795-136">يتم أيضًا عرض شروط احتجاز المورد في أوامر الشراء التي تنشؤها للمورد.</span><span class="sxs-lookup"><span data-stu-id="54795-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
