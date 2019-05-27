---
title: تعقب العمولات في نقطة البيع (POS) باستخدام مجموعات المبيعات
description: وتعد ممارسة شائعة في البيع بالتجزئة لتعقب المبيعات بواسطة الموظفين الذين قاموا بأداء العمل من العميل- تقديم المساعدة، والبيع الإضافي والبيع التكميلي ومعالجة الحركة.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ed4f9b3055e164600827b62d57b7a5068edb3b1a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559291"
---
# <a name="track-commissions-in-the-point-of-sale-pos-by-using-sales-groups"></a><span data-ttu-id="049f3-103">تعقب العمولات في نقطة البيع (POS) باستخدام مجموعات المبيعات</span><span class="sxs-lookup"><span data-stu-id="049f3-103">Track commissions in the point of sale (POS) by using sales groups</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="049f3-104">وتعد ممارسة شائعة في البيع بالتجزئة لتعقب المبيعات بواسطة الموظفين الذين قاموا بأداء العمل من العميل- تقديم المساعدة، والبيع الإضافي والبيع التكميلي ومعالجة الحركة.</span><span class="sxs-lookup"><span data-stu-id="049f3-104">It's a common retail practice to track sales by the associate who worked with the customer—providing assistance, up-selling, cross-selling, and processing the transaction.</span></span>

<span data-ttu-id="049f3-105">يُعد تعقب المبيعات من قبل ممثل المبيعات هو إجراء لقياس قدرات موظفي المبيعات، في حين يتم قياس المبيعات من قبل الكاشير بالسرعة والكفاءة.</span><span class="sxs-lookup"><span data-stu-id="049f3-105">Tracking sales by sales representative is a measure of the associates selling abilities, while sales by cashier is a measure of speed and efficiency.</span></span> <span data-ttu-id="049f3-106">في حين يتم عادةً تعقب المبيعات التي تتم من خلال ممثل المبيعات عادةُ باستخدام حساب العمولات أو غير ذلك من المكافآت التشجيعية.</span><span class="sxs-lookup"><span data-stu-id="049f3-106">Sales tracked by sales representative are also often used to calculate commissions or other incentives.</span></span>

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a><span data-ttu-id="049f3-107">تكوين عامل ليكون مندوب مبيعات في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="049f3-107">Configuring a worker to be a sales representative in POS</span></span>

<span data-ttu-id="049f3-108">عندما تتم إضافة عامل إلى مجموعة مبيعات، يصبح مؤهلًا للحصول على اعلمولة، ويمكن تعريفه كمندوب مبيعات في النظام.</span><span class="sxs-lookup"><span data-stu-id="049f3-108">When a worker is added to a sales group, they become eligible for commission and can be identified as a sales representative in the system.</span></span> <span data-ttu-id="049f3-109">ولا يؤهل العامل غير موجود في مجموعة المبيعات للحصول على العمولة، ولن يتم إدراجه كمندوب مبيعات في تطبيق نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="049f3-109">A worker who isn't in a sales group isn't eligible for commission and won't be listed as a sales representative in the point of sale (POS) application.</span></span> <span data-ttu-id="049f3-110">في نقطة البيع، يتم اشتقاق قائمة مندوبي المبيعات من كافة مجموعات المبيعات التي تحتوي على عامل واحد على الأقل يتم تعيينه للمتجر.</span><span class="sxs-lookup"><span data-stu-id="049f3-110">In POS, the list of sales representatives is derived from all sales groups that contain at least one worker assigned to the store.</span></span> <span data-ttu-id="049f3-111">يتم عرض القائمة في نقطة البيع كمجموعة من مُعرفات مجموعة المبيعات والاسم (المُعرف: الاسم).</span><span class="sxs-lookup"><span data-stu-id="049f3-111">The list is shown in POS as a combination of Sales group ID and Name (ID : Name).</span></span> <span data-ttu-id="049f3-112">يمكن تعيين مجموعة مبيعات افتراضية للعاملين لدعم سيناريوهات يختار فيها بائع التجزئة تعيين مندوب مبيعات على خطوط نقطة البيع تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="049f3-112">A default sales group can be assigned to workers to support scenarios where the retailer chooses to set the sales representative on POS lines automatically.</span></span> <span data-ttu-id="049f3-113">يمكن للمستخدمين الاختيار من أي مجموعة مبيعات يكون العامل عضوًا فيها.</span><span class="sxs-lookup"><span data-stu-id="049f3-113">Users can select from any sales group that the worker is a member of.</span></span>

## <a name="functionality-profile-settings"></a><span data-ttu-id="049f3-114">إعدادات ملف تعريف الوظيفة</span><span class="sxs-lookup"><span data-stu-id="049f3-114">Functionality profile settings</span></span>

<span data-ttu-id="049f3-115">يوجد عدد من إعداد ملف تعريف الوظيفة لمتجر، والتي ستحدد التدفق والمعالجة في نقطة البيع التي تتضمن مندوبي المبيعات.</span><span class="sxs-lookup"><span data-stu-id="049f3-115">There are a number of functionality profile settings for a store that will determine the flow and process in POS that involve sales representatives.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="049f3-116">ملف التعريف</span><span class="sxs-lookup"><span data-stu-id="049f3-116">Profile</span></span></th>
<th><span data-ttu-id="049f3-117">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="049f3-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="049f3-118">افتراضي للصراف عند التوافر</span><span class="sxs-lookup"><span data-stu-id="049f3-118">Default to cashier when available</span></span></td>
<td><span data-ttu-id="049f3-119">إذا تم تمكين هذا الخيار، سوف تقوم نقطة البيع بملء بنود الحركة تلقائيًا باستخدام مجموعة المبيعات الافتراضية للكاشير الحالي.</span><span class="sxs-lookup"><span data-stu-id="049f3-119">If this option is enabled, POS will automatically populate transaction lines with the current cashier's default sales group.</span></span> <span data-ttu-id="049f3-120">إذا لم يكن للكاشير مجموعة مبيعات افتراضية محددة، فلن يتم تعيين القيمة.</span><span class="sxs-lookup"><span data-stu-id="049f3-120">If a cashier doesn't have a default sales group specified, the value won't be set.</span></span> <span data-ttu-id="049f3-121">لا يزال بإمكان المستخدم تعيين مجموعة المبيعات باستخدام آزرار شريط أوامر نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="049f3-121">A user could still manually set the sales group by using a POS button grid button.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="049f3-122">المطالبة بمندوب المبيعات</span><span class="sxs-lookup"><span data-stu-id="049f3-122">Prompt for sales representative</span></span></td>
<td><span data-ttu-id="049f3-123">تتوفر لدى هذا الخيار ثلاث قيم ممكنة:</span><span class="sxs-lookup"><span data-stu-id="049f3-123">This option has three possible values:</span></span>
<ul>
<li><span data-ttu-id="049f3-124"><strong>لا</strong> – إذا تم تحديد هذا الخيار، فلن تتم مطالبة المستخدم بتحديد مجموعة مبيعات.</span><span class="sxs-lookup"><span data-stu-id="049f3-124"><strong>No</strong> – If this option is selected, the user won't be prompted to select a sales group.</span></span> <span data-ttu-id="049f3-125">ومن الممكن تعيين القيمة باستخدام مجموعات المبيعات الافتراضية للكاشير أو يدويًا باستخدام زر في شبكة أزرار نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="049f3-125">The value could still be set by using a cashier's default Sales group or manually by using a POS button grid button.</span></span></li>
<li><span data-ttu-id="049f3-126"><strong>بداية الحركة</strong> - إذا تم تحديد هذا الخيار، ولم يتم تمكين <strong>افتراضي للكاشير</strong>، أو لم يكن للكاشير الحالي مجموعة مبيعات افتراضية، فسوف تتم مطالبة المستخدم بتحديد مجموعة مبيعات في بداية كل حركة.</span><span class="sxs-lookup"><span data-stu-id="049f3-126"><strong>Start of transaction</strong> – If this option is selected, and either the <strong>Default to cashier</strong> option isn't enabled or the current cashier doesn't have a default sales group, the user will be prompted to select a sales group at the beginning of each transaction.</span></span> <span data-ttu-id="049f3-127">وبتحديد مجموعة مبيعات من هذه المطالبة من شأنه أن يُعيّن جميع الأسطر التالية لمجموعات المبيعات المحددة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="049f3-127">Selecting a sales group from this prompt will default all subsequent lines to the selected sales group.</span></span> <span data-ttu-id="049f3-128">لا يزال بإمكان المستخدم تعيين مجموعة المبيعات باستخدام آزرار شريط أوامر نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="049f3-128">A user could still manually set the sales group by using a POS button grid button.</span></span></li>
<li><span data-ttu-id="049f3-129"><strong>لكل بند</strong> - إذا تم تحديد هذا الخيار، ولم يتم تمكين <strong>افتراضي للكاشير</strong>، أو لم يكن للكاشير الحالي مجموعة مبيعات افتراضية، فسوف تتم مطالبة المستخدم بتحديد مجموعة مبيعات بعد إضافة كل سطر.</span><span class="sxs-lookup"><span data-stu-id="049f3-129"><strong>For each line</strong> – If this option is selected, and either the <strong>Default to cashier</strong> option isn't enabled or the current cashier doesn't have a default sales group, the user will be prompted to select a sales group after adding each line.</span></span> <span data-ttu-id="049f3-130">لا يزال بإمكان المستخدم تعيين مجموعة المبيعات باستخدام آزرار شريط أوامر نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="049f3-130">A user could still manually set the Sales group by using a POS button grid button.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="049f3-131">مطلوب</span><span class="sxs-lookup"><span data-stu-id="049f3-131">Require</span></span></td>
<td><span data-ttu-id="049f3-132">ينطبق هذا الخيار فقط عندما يتم تكوين نقاط البيع للمطالبة بمندوب مبيعات.</span><span class="sxs-lookup"><span data-stu-id="049f3-132">This option is only applicable when POS is configured to prompt for a sales representative.</span></span> <span data-ttu-id="049f3-133">في حالة التمكين، فسوف يكون المستخدم مطالبًا باختيار مجموعة مبيعات قبل المتابعة والاستمرار.</span><span class="sxs-lookup"><span data-stu-id="049f3-133">If enabled, the user will be required to choose a sales group before continuing.</span></span> <span data-ttu-id="049f3-134">وبخلاف ذلك، سوف يكون المستخدم مطالبًا، ولكنه يمكنه الإلغاء والاستمرار دون إجراء تحديد.</span><span class="sxs-lookup"><span data-stu-id="049f3-134">Otherwise, the user will be prompted, but can cancel and continue without making a selection.</span></span> <span data-ttu-id="049f3-135">بعد إضافة السطر، لا يزال بإمكان المستخدم الذي لدية الأذونات الكافية إزالة مجموعة المبيعات من السطر.</span><span class="sxs-lookup"><span data-stu-id="049f3-135">After the line is added, a user with sufficient permissions could still remove the sales group from the line.</span></span> <span data-ttu-id="049f3-136">لا يتم فرض "طلب مندوب مبيعات" في هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="049f3-136">"Require sales representative" is not enforced in this situation.</span></span></td>
</tr>
</tbody>
</table>

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a><span data-ttu-id="049f3-137">عرض معلومات مندوب المبيعات على شاشة حركات نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="049f3-137">Displaying the Sales representative information on the POS transactions screen</span></span>

<span data-ttu-id="049f3-138">يمكن تكون تخطيط شاشة حركة نقطع البيع والمحتويات باستخدام مصمم تخطيط الشاشة، وتعيين تخطيطات الشاشة إلى المخازن أو السجلات أو العمال.</span><span class="sxs-lookup"><span data-stu-id="049f3-138">The POS transaction screen layout and contents are configurable using the screen layout designer and assigned screen layouts to stores, registers, or workers.</span></span><span data-ttu-id="049f3-139"> يمكن إضافة حقل *\*مندوب المبيعات** في علامة تبويب "البنود" في جزء الإيصال.</span><span class="sxs-lookup"><span data-stu-id="049f3-139"> The *\*Sales representative** field can be added to the Lines tab of the Receipt pane.</span></span><span data-ttu-id="049f3-140">  سيؤدي ذلك إلى عرض مُعرف مجموعة المبيعات المحددة لكل بند على شاشة الحركة.</span><span class="sxs-lookup"><span data-stu-id="049f3-140">  This will display the ID of the specified Sales group for each line on the transaction screen.</span></span>

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a><span data-ttu-id="049f3-141">إضافة عمليات مندوب المبيعات إلى شبكة أزرار نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="049f3-141">Adding Sales representative operations to POS button grids</span></span>

<span data-ttu-id="049f3-142">تسمح نقطة البيع للمستخدمين بتكوين شبكات آزرار، والتي يتم تضمينها في تخطيطات الشاشة لتوفير الوصول إلى عمليات نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="049f3-142">POS allows users to configure button grids, which are included in screen layouts to provide access to POS operations.</span></span> <span data-ttu-id="049f3-143">يمكن تعيين نقاط البيع التالية لأزرار شبكة الأزرار المتعلقة بمندوبي المبيعات.</span><span class="sxs-lookup"><span data-stu-id="049f3-143">The following POS operations can be assigned to button grid buttons that pertain to Sales representatives.</span></span>

| <span data-ttu-id="049f3-144">العملية</span><span class="sxs-lookup"><span data-stu-id="049f3-144">Operation</span></span>                                 | <span data-ttu-id="049f3-145">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="049f3-145">Description</span></span> |
|-------------------------------------------|-------------|
| <span data-ttu-id="049f3-146">تعيين مندوب مبيعات في بند</span><span class="sxs-lookup"><span data-stu-id="049f3-146">Set sales representative on line</span></span>          | <span data-ttu-id="049f3-147">تعرض عملية نقطة البيع قائمة بمجموعات المبيعات المؤهلة (المُعرف: الاسم) للمتجر.</span><span class="sxs-lookup"><span data-stu-id="049f3-147">This POS operation displays a list of eligible Sales groups (ID : Name) for the store.</span></span><span data-ttu-id="049f3-148"> سيؤدي تحديد مجموعة مبيعات من هذه القائمة إلى تعيين القيمة على بند الحركة الحالية.</span><span class="sxs-lookup"><span data-stu-id="049f3-148"> Selecting a Sales group from this list will set the value on the current transaction line.</span></span> |
| <span data-ttu-id="049f3-149">مسح مندوب مبيعات في بند</span><span class="sxs-lookup"><span data-stu-id="049f3-149">Clear sales representative on line</span></span>        | <span data-ttu-id="049f3-150">تزيل عملية نقطة البيع هذه قيمة مجموعة المبيعات الحالية من سطر الحركة الحالي.</span><span class="sxs-lookup"><span data-stu-id="049f3-150">This POS operation removes the current Sales group value from the current transaction line.</span></span> |
| <span data-ttu-id="049f3-151">تعيين مندوب مبيعات في الحركة</span><span class="sxs-lookup"><span data-stu-id="049f3-151">Set sales representative on transaction</span></span>   | <span data-ttu-id="049f3-152">تعرض عملية نقطة البيع قائمة بمجموعات المبيعات المؤهلة (المُعرف: الاسم) للمتجر.</span><span class="sxs-lookup"><span data-stu-id="049f3-152">This POS operation displays a list of eligible Sales groups (ID : Name) for the store.</span></span><span data-ttu-id="049f3-153"> سيؤدي تحديد مجموعة مبيعات من هذه القائمة إلى تعيين القيمة الافتراضية في الحركة الحالية.</span><span class="sxs-lookup"><span data-stu-id="049f3-153"> Selecting a Sales group from this list will set the default value on the current transaction.</span></span> <span data-ttu-id="049f3-154">سوف يتم تعيين أي سطور موجودة بدون مجموعة مبيعات فضلًا عن أي سطور مضافة فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="049f3-154">Any existing lines without a sales group assigned will be set, as well as any subsequently added lines.</span></span> |
| <span data-ttu-id="049f3-155">مسح مندوب مبيعات في الحركة</span><span class="sxs-lookup"><span data-stu-id="049f3-155">Clear sales representative on transaction</span></span> | <span data-ttu-id="049f3-156">تزيل عملية نقطة البيع هذه قيمة مجموعة المبيعات الحالية الافتراضية من الحركة الحالية.</span><span class="sxs-lookup"><span data-stu-id="049f3-156">This POS operation removes the current default Sales group value from the current transaction.</span></span> <span data-ttu-id="049f3-157">ولا يؤثر هذا على أي سطور موجودة بالفعل في الحركة.</span><span class="sxs-lookup"><span data-stu-id="049f3-157">It does not impact any lines already existing in the transaction.</span></span> |

## <a name="calculating-commissions"></a><span data-ttu-id="049f3-158">حساب العمولات</span><span class="sxs-lookup"><span data-stu-id="049f3-158">Calculating commissions</span></span>

<span data-ttu-id="049f3-159">يتم حساب العمولة للعمال في مجموعات مبيعات محددة في وقت ترحيل كشف الحساب أو ترحيل أمر التوريد.</span><span class="sxs-lookup"><span data-stu-id="049f3-159">Commission is calculated for the workers in the specified sales groups at the time of statement posting or sales order posting.</span></span><span data-ttu-id="049f3-160"> يُحدد مبلغ العمولة استنادًا إلى حصة عمولة العامل، على النحو المحدد في مجموعة المبيعات وإعدادات حساب العمولة المقترنة للعميل و/أو المنتجات على الحركة.</span><span class="sxs-lookup"><span data-stu-id="049f3-160"> The commission amount is determined based on the worker's commission share, as defined in the sales group and the associated commission calculation settings for the customer and/or products on the transaction.</span></span>
