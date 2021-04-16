---
title: إنشاء كشوف حسابات لمتجر بيع بالتجزئة وحسابها وترحيلها
description: يصف هذا الموضوع الخطوات اليدوية لإنشاء كشف حساب وحسابه وترحيله لمتجر.
author: jashanno
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58900ca4d3f6893689822a8cc5657d8c91772f65
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798527"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a><span data-ttu-id="36109-103">إنشاء كشوف حسابات لمتجر بيع بالتجزئة وحسابها وترحيلها</span><span class="sxs-lookup"><span data-stu-id="36109-103">Create, calculate, and post statements for a retail store</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36109-104">يصف هذا الموضوع الخطوات اليدوية لإنشاء كشف حساب وحسابه وترحيله لمتجر.</span><span class="sxs-lookup"><span data-stu-id="36109-104">This topic describes the manual steps for creating, calculating, and posting a statement for a store.</span></span> <span data-ttu-id="36109-105">هناك أيضا وظائف دفعية والتي يمكن تكوينها لنفس المهام.</span><span class="sxs-lookup"><span data-stu-id="36109-105">There are also batch jobs that can be configured for the same tasks.</span></span> <span data-ttu-id="36109-106">يمكن العثور على الخطوات لتكوين الوظائف الدفعية وتشغيلها في مواضيع أخرى.</span><span class="sxs-lookup"><span data-stu-id="36109-106">The steps for configuring and running the batch jobs can be found in other topics.</span></span> <span data-ttu-id="36109-107">لإكمال هذا الإجراء، يجب أن يكون لديك حركات تم إكمالها في نقطة البيع ثم سحبها إلى Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="36109-107">To complete this procedure, you must have transactions that were completed in POS and then pulled into Dynamics 365 Commerce.</span></span> <span data-ttu-id="36109-108">ويستخدم هذا التسجيل شركة USRT في بيانات العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="36109-108">This recording uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="36109-109">حدد **ماليات المتجر** من الصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="36109-109">Select **Store financials** from the home page.</span></span>
2. <span data-ttu-id="36109-110">حدد **كشف حساب جديد**.</span><span class="sxs-lookup"><span data-stu-id="36109-110">Select **New statement**.</span></span>
3. <span data-ttu-id="36109-111">في الحقل **رقم المتجر**، حدد خيارًا من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="36109-111">In the **Store number** field, select a option from the drop-down.</span></span>
4. <span data-ttu-id="36109-112">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="36109-112">Select **OK**.</span></span>
5. <span data-ttu-id="36109-113">تتضمن مجموعة **الإعداد** الإعدادات التي تتحكم في الحركات التي يتم تضمينها في كشف الحساب وكيفية تجميعها في بنود كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="36109-113">The **Setup** group has the settings that control what transactions are included in the statement and how they are grouped into statement lines.</span></span> <span data-ttu-id="36109-114">يمكنك فتح مجموعة **الإعداد** وتغيير هذه الإعدادات، أو يمكنك استخدام الإعدادات الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="36109-114">You can open the **Setup** group and change these settings, or you can use the defaults.</span></span>  
    - <span data-ttu-id="36109-115">يحدد حقل **طريقة كشف الحساب**‬ كيف سيتم تجميع بنود كشف الحساب.</span><span class="sxs-lookup"><span data-stu-id="36109-115">The **Statement method** field defines how the statement lines will be grouped.</span></span>  
    - <span data-ttu-id="36109-116">حدد أحد الموظفين أو السجلات في حقل **فريق العمل/السجل‬** إذا أردت حساب كشف حساب لموظف أو سجل معين فقط.</span><span class="sxs-lookup"><span data-stu-id="36109-116">Select a staff member or a register in the **staff/register** field if you want to calculate a statement only for the specific staff member or register.</span></span>  
6. <span data-ttu-id="36109-117">في حقل **أسلوب الإقفال**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="36109-117">In the **Closing method** field, select an option.</span></span>
7. <span data-ttu-id="36109-118">حدد **حساب كشف الحساب‬** من جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="36109-118">Select **Calculate statement** from the Action Pane.</span></span>
8. <span data-ttu-id="36109-119">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="36109-119">Select **Yes**.</span></span>
    - <span data-ttu-id="36109-120">بعد حساب كشف الحساب، ينبغي أن تكون هناك بنودًا تم إنشاؤها باستخدام المبالغ الإجمالية لكل طريقة دفع وطريقة كشف حساب تم استخدامها.</span><span class="sxs-lookup"><span data-stu-id="36109-120">After calculating the statement, there should be lines created with total amounts for each payment method and statement method that was used.</span></span>  
    - <span data-ttu-id="36109-121">أدخل المبلغ المحسوب في كل بند إذا كان يحتاج إلى أن يتم إدخاله أو تحديثه.</span><span class="sxs-lookup"><span data-stu-id="36109-121">Enter a counted amount in each line if it needs to be entered or updated.</span></span> <span data-ttu-id="36109-122">يتم ملء الحقل المحسوب بمبالغ من إقرارات الدفع التي تمت في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="36109-122">The counted field is populated with amounts from tender declarations done in POS.</span></span>  
9. <span data-ttu-id="36109-123">حدد **ترحيل كشف الحساب‬** من جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="36109-123">Select **Post statement** from the Action Pane.</span></span>
10. <span data-ttu-id="36109-124">حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="36109-124">Select **Close**.</span></span>
11. <span data-ttu-id="36109-125">قم بإغلاق الجزء.</span><span class="sxs-lookup"><span data-stu-id="36109-125">Close the pane.</span></span>
12. <span data-ttu-id="36109-126">حدد **ماليات المتجر** في الصفحة الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="36109-126">At the home page, select **Store financials**.</span></span>
13. <span data-ttu-id="36109-127">حدد علامة التبويب ‏‫**كشوف الحسابات المرحلة**.</span><span class="sxs-lookup"><span data-stu-id="36109-127">Select the **Posted statements** tab.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]