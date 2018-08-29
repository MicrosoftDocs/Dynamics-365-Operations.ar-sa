--- 
title: "إنشاء كشوف حسابات لمتجر بيع بالتجزئة وحسابه وترحيله"
description: "يتناول هذا الإجراء الخطوات اليدوية لإنشاء كشف حساب وحسابه وترحيله لمتجر."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 1c31c849c4c72762f0fdeb3f1d256cd3529394b2
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="415ad-103">إنشاء كشوف حسابات لمتجر بيع بالتجزئة وحسابه وترحيله</span><span class="sxs-lookup"><span data-stu-id="415ad-103">Create, calculate, and post statements for a retail store</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="415ad-104">يتناول هذا الإجراء الخطوات اليدوية لإنشاء كشف حساب وحسابه وترحيله لمتجر.</span><span class="sxs-lookup"><span data-stu-id="415ad-104">This procedure walks through the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="415ad-105">هناك أيضا وظائف دفعية والتي يمكن تكوينها لنفس المهام.</span><span class="sxs-lookup"><span data-stu-id="415ad-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="415ad-106">يمكن العثور على الخطوات لتكوين الوظائف الدفعية وتشغيلها في مواضيع أخرى.</span><span class="sxs-lookup"><span data-stu-id="415ad-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="415ad-107">ولإكمال هذا الإجراء، يجب أن يكون لديك حركات تم إكمالها في نقطة البيع ثم سحبها إلى Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="415ad-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics AX.</span></span> <span data-ttu-id="415ad-108">ويستخدم هذا التسجيل شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="415ad-108">This recording uses the USRT company in demo data.</span></span> <span data-ttu-id="415ad-109">قد يشير هذا الإجراء إلى Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="415ad-109">This procedure may refer to Microsoft Dynamics AX.</span></span> <span data-ttu-id="415ad-110">تجدر الإشارة إلى أن Dynamics AX يسمى الآن Microsoft Dynamics 365 for Operations.</span><span class="sxs-lookup"><span data-stu-id="415ad-110">Please note that Dynamics AX is now called Microsoft Dynamics 365 for Operations.</span></span>

1. <span data-ttu-id="415ad-111">انتقل إلى كل مساحات العمل > ..</span><span class="sxs-lookup"><span data-stu-id="415ad-111">Go to All workspaces > ..</span></span> <span data-ttu-id="415ad-112">> ماليات متجر البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="415ad-112">> Retail store financials.</span></span>
2. <span data-ttu-id="415ad-113">انقر فوق كشف حساب جديد.</span><span class="sxs-lookup"><span data-stu-id="415ad-113">Click New statement.</span></span>
3. <span data-ttu-id="415ad-114">في حقل "‏‫رقم المتجر‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="415ad-114">In the Store number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="415ad-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="415ad-115">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="415ad-116">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="415ad-116">Click OK.</span></span>
    * <span data-ttu-id="415ad-117">تتضمن مجموعة الإعداد الإعدادات التي تتحكم في الحركات التي يتم تضمينها في كشف الحساب وكيفية تجميعها في بنود كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="415ad-117">The Setup group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="415ad-118">يمكنك فتح مجموعة الإعداد وتغيير هذه الإعدادات، أو يمكنك استخدام الإعدادات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="415ad-118">You can open the Setup group and change these settings, or you can use the defaults.</span></span>  
    * <span data-ttu-id="415ad-119">يحدد حقل "‏‫طريقة كشف الحساب‬" كيف سيتم تجميع بنود كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="415ad-119">The Statement method field defines how the statement lines will be grouped.</span></span>  
    * <span data-ttu-id="415ad-120">حدد أحد الموظفين أو السجلات إذا أردت حساب كشف حساب لموظف أو سجل معين فقط.</span><span class="sxs-lookup"><span data-stu-id="415ad-120">Select a staff member or a register if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="415ad-121">في حقل "‬‏‫أسلوب الإقفال"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="415ad-121">In the Closing method field, select an option.</span></span>
7. <span data-ttu-id="415ad-122">انقر فوق حساب كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="415ad-122">Click Calculate statement.</span></span>
8. <span data-ttu-id="415ad-123">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="415ad-123">Click Yes.</span></span>
    * <span data-ttu-id="415ad-124">بعد حساب كشف الحساب، ينبغي أن تكون هناك بنودًا تم إنشاؤها باستخدام المبالغ الإجمالية لكل طريقة دفع وطريقة كشف حساب تم استخدامها.</span><span class="sxs-lookup"><span data-stu-id="415ad-124">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    * <span data-ttu-id="415ad-125">أدخل المبلغ المحسوب في كل بند إذا كان يحتاج إلى أن يتم إدخاله أو تحديثه.</span><span class="sxs-lookup"><span data-stu-id="415ad-125">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="415ad-126">يتم ملء الحقل المحسوب بمبالغ من إقرارات الدفع التي تمت في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="415ad-126">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="415ad-127">انقر فوق ترحيل كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="415ad-127">Click Post statement.</span></span>
10. <span data-ttu-id="415ad-128">انقر فوق "إغلاق".</span><span class="sxs-lookup"><span data-stu-id="415ad-128">Click Close.</span></span>
11. <span data-ttu-id="415ad-129">انتقل إلى البيع بالتجزئة والتجارة > القنوات > ‏‫ماليات متجر البيع بالتجزئة‬.</span><span class="sxs-lookup"><span data-stu-id="415ad-129">Go to Retail and commerce > Channels > Retail store financials.</span></span>
12. <span data-ttu-id="415ad-130">انقر فوق علامة التبويب ‏‫كشوف الحسابات المرحلة.</span><span class="sxs-lookup"><span data-stu-id="415ad-130">Click the Posted statements tab.</span></span>


