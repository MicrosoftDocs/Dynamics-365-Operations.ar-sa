---
title: إرسال الفواتير إلى نظام سير العمل ومطابقة بنود إيصال استلام المنتجات (معاينة)
description: يشرح هذا الموضوع عملية إرسال فواتير المورد إلى نظام سير العمل وتلقائيًا مطابقه بنود إيصال استلام المنتجات المرحلة إلى فواتير المورد المعلقة.
author: abruer
manager: AnnBe
ms.date: 09/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cde164ee89b542d769d81d8d483049fb7ca001c4
ms.sourcegitcommit: 3387595e41fb03e98bb437588f6de78794ae383f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930909"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines-preview"></a><span data-ttu-id="df8ca-103">إرسال الفواتير إلى نظام سير العمل ومطابقة بنود إيصال استلام المنتجات (معاينة)</span><span class="sxs-lookup"><span data-stu-id="df8ca-103">Submit invoices to the workflow system and match product receipt lines (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="df8ca-104">يشرح هذا الموضوع عملية إرسال فواتير المورد إلى نظام سير العمل وتلقائيًا مطابقه بنود إيصال استلام المنتجات المرحلة إلى فواتير المورد المعلقة.</span><span class="sxs-lookup"><span data-stu-id="df8ca-104">This topic explains the process of submitting vendor invoices to the workflow system and automatically matching posted product receipt lines to vendor invoices.</span></span>

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a><span data-ttu-id="df8ca-105">إرسال فواتير المورد المستوردة إلى نظام سير العمل ومطابقه بنود إيصال استلام المنتجات المرحلة إلى بنود فاتورة المورد المعلقة.</span><span class="sxs-lookup"><span data-stu-id="df8ca-105">Submitting imported vendor invoices to the workflow system and matching posted product receipt lines to pending vendor invoice lines</span></span>

<span data-ttu-id="df8ca-106">كجزء من عمليه فوتره الحسابات الدائنة بدون لمس، يمكنك جعل النظام يقوم تلقائيا بإرسال فاتورة مستورده إلى نظام سير العمل.</span><span class="sxs-lookup"><span data-stu-id="df8ca-106">As part of a touchless Accounts payable invoicing process, you can have the system automatically submit an imported invoice to the workflow system.</span></span> <span data-ttu-id="df8ca-107">يمكنك تكوين عمليه إرسال الفواتير المستوردة إلى نظام سير العمل في علامة التبويب **التنفيذ التلقائي لفاتورة المورد** في الصفحة **معلمات الحسابات الدائنة** ( **الحسابات الدائنة \>الاعداد \>معلمات الحسابات الدائنة** .)</span><span class="sxs-lookup"><span data-stu-id="df8ca-107">You can configure the process of submitting imported invoices to the workflow system on the **Vendor invoice automation** tab of the **Accounts payable parameters** page ( **Accounts payable \> Setup \> Accounts payable parameters** ).</span></span> <span data-ttu-id="df8ca-108">سيتم تشغيل عملية الإرسال إلى دفق العمل في الخلفية، بتكرار تحدده (سواء بالساعة أو يوميا).</span><span class="sxs-lookup"><span data-stu-id="df8ca-108">The submit-to-workflow process will run in the background, at a frequency that you specify (either hourly or daily).</span></span>

<span data-ttu-id="df8ca-109">عندما تقوم بتقديم الفواتير تلقائيا إلى نظام سير العمل، يجب البدء بفاتورة تم استيرادها.</span><span class="sxs-lookup"><span data-stu-id="df8ca-109">When you automatically submit invoices to the workflow system, you must begin with an imported invoice.</span></span> <span data-ttu-id="df8ca-110">لضمان امكانيه معالجه الفاتورة من البداية إلى النهاية بدون تدخل يدوي، يجب تضمين مهمة ترحيل مؤتمتة في تكوين سير العمل.</span><span class="sxs-lookup"><span data-stu-id="df8ca-110">To ensure that the invoice can be processed from start to finish without manual intervention, you must include an automated posting task in the workflow configuration.</span></span> <span data-ttu-id="df8ca-111">يمكن إرسال الفواتير المرتبطة بأوامر الشراء (نقطه البيع) والفواتير التي تحتوي علي فئة تدبير بخلاف أمر الشراء وبنود غير مخزنه تلقائيا إلى نظام سير العمل.</span><span class="sxs-lookup"><span data-stu-id="df8ca-111">Invoices that are related to purchase orders (POs), and invoices that contain a non-PO procurement category and non-stocked lines, can automatically be submitted to the workflow system.</span></span> <span data-ttu-id="df8ca-112">ويجب ان يتم إرسال الفواتير التي يتم إدخالها يدويا إلى نظام سير العمل.</span><span class="sxs-lookup"><span data-stu-id="df8ca-112">Invoices that are manually entered must be manually submitted to the workflow system.</span></span>

<span data-ttu-id="df8ca-113">تم إدخال القيمة **الإرسال بواسطة** الموجودة في سير العمل هو معرف المستخدم الذي تم إدخاله للمهمة في الخلفية **إرسال فواتير المورد إلى سير العمل** في الصفحة **أتمتة العملية** .</span><span class="sxs-lookup"><span data-stu-id="df8ca-113">The **Submitted by** value in the workflow is the user ID that was entered for the **Submit vendor invoices to workflow** background task on the **Process automation** page.</span></span> <span data-ttu-id="df8ca-114">سيتمكن المستخدم الذي لديه معرف المستخدم هذا من استدعاء الفاتورة من نظام سير العمل كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="df8ca-114">The user who has that user ID will be able to recall the invoice from the workflow system as required.</span></span>

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a><span data-ttu-id="df8ca-115">مطابقه إيصالات استلام المنتجات ببنود الفواتير التي لها سياسة مطابقه ثلاثية الاتجاه</span><span class="sxs-lookup"><span data-stu-id="df8ca-115">Matching posted product receipts to invoice lines that have a three-way matching policy</span></span>

<span data-ttu-id="df8ca-116">كجزء من عمليه فوتره الحسابات الدائنة بدون لمس، يمكن للنظام تلقائيا مطابقه إيصالات استلام المنتجات المرحلة ببنود الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="df8ca-116">As part of a touchless Accounts payable invoicing process, the system can automatically match posted product receipts to invoice lines.</span></span> <span data-ttu-id="df8ca-117">يجب تحديد نهج التوافق ثلاثي الاتجاهات لهذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="df8ca-117">A three-way matching policy must be defined for this task.</span></span> <span data-ttu-id="df8ca-118">تتوفر هذه الميزة إذا تم تمكين ميزه **أتمتة فاتورة المورد** في الصفحة **أداره الميزات** .</span><span class="sxs-lookup"><span data-stu-id="df8ca-118">This feature is available if the **Vendor invoice automation** feature has been enabled on the **Feature management** page.</span></span>

<span data-ttu-id="df8ca-119">سيتم تشغيل العملية حتى تساوي كميه إيصالات استلام المنتجات المطابقة كميه الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="df8ca-119">The process will run until the matched product receipt quantity equals the invoice quantity.</span></span> <span data-ttu-id="df8ca-120">كجزء من هذه العملية، يمكنك تحديد الحد الأقصى لعدد المرات التي يجب ان يحاول النظام فيها مطابقه إيصالات استلام المنتجات ببند الفاتورة قبل ان يدرك فشل العملية.</span><span class="sxs-lookup"><span data-stu-id="df8ca-120">As part of this process, you can specify the maximum number of times that the system should try to match product receipts to an invoice line before it concludes that the process failed.</span></span> <span data-ttu-id="df8ca-121">سيتم تشغيل العملية في الخلفية أو يوميا.</span><span class="sxs-lookup"><span data-stu-id="df8ca-121">The process will run in the background, either hourly or daily.</span></span> <span data-ttu-id="df8ca-122">يمكنك تشغيل عمليه المطابقة التلقائية كجزء من عمليه إرسال الفواتير إلى نظام سير العمل.</span><span class="sxs-lookup"><span data-stu-id="df8ca-122">You can run the automated matching process as part of the process for submitting invoices to the workflow system.</span></span> <span data-ttu-id="df8ca-123">بدلا من ذلك، يمكنك تشغيلها كعمليه مستقله.</span><span class="sxs-lookup"><span data-stu-id="df8ca-123">Alternatively, you can run it as a standalone process.</span></span> <span data-ttu-id="df8ca-124">إعدادات عملية مطابقة إيصالات استلام المنتجات ببنود الفاتورة مكونة في علامة التبويب **التنفيذ التلقائي لفاتورة المورد** في الصفحة **معلمات الحسابات الدائنة** ( **الحسابات الدائنة \>الاعداد \>معلمات الحسابات الدائنة** .)</span><span class="sxs-lookup"><span data-stu-id="df8ca-124">The settings for the match-product-receipts-to-invoice-lines process are configured on the **Vendor invoice automation** tab of the **Accounts payable parameters** page ( **Accounts payable \> Setup \> Accounts payable parameters** ).</span></span>

<span data-ttu-id="df8ca-125">يتم تضمين بنود الفواتير التي لها سياسة مطابقه ثلاثية الاتجاه، حيث تكون كميه الإيصالات المطابقة اقل من كميه الفاتورة، في عمليه المطابقة التلقائية للمنتج.</span><span class="sxs-lookup"><span data-stu-id="df8ca-125">Invoice lines that have a three-way matching policy, where the matched receipt quantity is less than the invoice quantity, will be included in the automated match-to-product-receipt process.</span></span>

<span data-ttu-id="df8ca-126">لعرض **حاله المطابقة** الاخيره للفواتير التي لا تعد جزءا من عمليه الإرسال إلى سير العمل التلقائية، افتح الفاتورة من الصفحة **فواتير المورد** .</span><span class="sxs-lookup"><span data-stu-id="df8ca-126">To view the **Last match** status for invoices that aren't part of the automated submit-to-workflow process, open the invoice from the **Vendor invoices** page.</span></span> <span data-ttu-id="df8ca-127">عند عرض الفاتورة، يتم تحديث المعلومات المطابقة للتحقق من الصحة.</span><span class="sxs-lookup"><span data-stu-id="df8ca-127">When you view the invoice, the matching validation information is updated.</span></span>

<span data-ttu-id="df8ca-128">سيتم استبعاد بند الفاتورة من المعالجة التلقائية في حاله استيفاء اي من الشروط التالية:</span><span class="sxs-lookup"><span data-stu-id="df8ca-128">An invoice line will be excluded from the automated processing if any of the following conditions are met:</span></span>

- <span data-ttu-id="df8ca-129">قيمة **حاله مطابقه الإيصال التلقائي** لبند الفاتورة بالحالة **فاشلة** .</span><span class="sxs-lookup"><span data-stu-id="df8ca-129">The **Automated receipt match status** value of the invoice line is **Failed** .</span></span>
- <span data-ttu-id="df8ca-130">الفاتورة قيد الاستخدام.</span><span class="sxs-lookup"><span data-stu-id="df8ca-130">The invoice is being used.</span></span>
- <span data-ttu-id="df8ca-131">الفاتورة في نظام سير العمل.</span><span class="sxs-lookup"><span data-stu-id="df8ca-131">The invoice is in the workflow system.</span></span>