---
title: "سياسات استحقاق الميزات"
description: "توفر هذه المقالة معلومات حول سياسات استحقاق الميزات، التي تساعدك على تحديد المؤهلين لميزات معينة."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 5c0af3d9446b4f8ae80eeb44494f1ef1e6667e55
ms.contentlocale: ar-sa
ms.lasthandoff: 01/19/2018

---

# <a name="benefit-eligibility-policies"></a><span data-ttu-id="db05b-103">سياسات استحقاق الميزات</span><span class="sxs-lookup"><span data-stu-id="db05b-103">Benefit eligibility policies</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="db05b-104">يوفر هذا الموضوع معلومات حول سياسات استحقاق الميزات، التي تساعدك على تحديد المؤهلين لميزات معينة.</span><span class="sxs-lookup"><span data-stu-id="db05b-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="db05b-105">عند إنشاء الميزات، تقرر ما الميزات التي ستكون متاحة للموظفين.</span><span class="sxs-lookup"><span data-stu-id="db05b-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="db05b-106">يعرض الجدول التالي أمثلة للفوائد التي قد توفرها لموظفين محددين.</span><span class="sxs-lookup"><span data-stu-id="db05b-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="db05b-107">الميزة</span><span class="sxs-lookup"><span data-stu-id="db05b-107">Benefit</span></span>          | <span data-ttu-id="db05b-108">الشخص الذي تتوفر له الميزة</span><span class="sxs-lookup"><span data-stu-id="db05b-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="db05b-109">التأمين الصحي</span><span class="sxs-lookup"><span data-stu-id="db05b-109">Health insurance</span></span> | <span data-ttu-id="db05b-110">كل الموظفين</span><span class="sxs-lookup"><span data-stu-id="db05b-110">All employees</span></span>                   |
| <span data-ttu-id="db05b-111">الهاتف الجوال</span><span class="sxs-lookup"><span data-stu-id="db05b-111">Mobile phone</span></span>     | <span data-ttu-id="db05b-112">فريق المبيعات، الموظفون التنفيذيون</span><span class="sxs-lookup"><span data-stu-id="db05b-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="db05b-113">مسارات وقوف السيارات</span><span class="sxs-lookup"><span data-stu-id="db05b-113">Parking passes</span></span>   | <span data-ttu-id="db05b-114">مديرون تنفيذيون</span><span class="sxs-lookup"><span data-stu-id="db05b-114">Executives</span></span>                      |

<span data-ttu-id="db05b-115">يتم استخدام المكونات التالية لإنشاء سياسات الاستحقاق:</span><span class="sxs-lookup"><span data-stu-id="db05b-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="db05b-116">أنواع قاعدة السياسة</span><span class="sxs-lookup"><span data-stu-id="db05b-116">Policy rule types</span></span>
-   <span data-ttu-id="db05b-117">سياسات استحقاق الميزات</span><span class="sxs-lookup"><span data-stu-id="db05b-117">Benefit eligibility policies</span></span>

<span data-ttu-id="db05b-118">تحدد أنواع قاعدة السياسة معلمات الاستعلام التي تستخدم عندما تقوم بتطوير قواعد نهُج معينة.</span><span class="sxs-lookup"><span data-stu-id="db05b-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="db05b-119">وبعد إنشاء أنواع قواعد السياسة، يمكنك إنشاء سياسات استحقاق الميزات.</span><span class="sxs-lookup"><span data-stu-id="db05b-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="db05b-120">وتتيح لك السياسات إنشاء مجموعة من القواعد التي تنطبق على واحد أو أكثر من الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="db05b-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="db05b-121">وضمن كل سياسة، يمكنك عرض أنواع قاعدة سياسة استحقاق الميزات التي قمت بإنشائها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="db05b-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="db05b-122">وتحدد نطاق القاعدة ضمن السياسة.</span><span class="sxs-lookup"><span data-stu-id="db05b-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="db05b-123">على سبيل المثال، إذا قمت بإنشاء نوع قاعدة سياسة استحقاق ميزة باسم **المدير التنفيذي**، يمكنك تحديد القاعدة الموجودة في تلك السياسة.</span><span class="sxs-lookup"><span data-stu-id="db05b-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="db05b-124">في هذا المثال، قد تنص القاعدة على أن أي مسمى وظيفي يحتوي على كلمة "المدير التنفيذي" يجب تضمينه في القاعدة.</span><span class="sxs-lookup"><span data-stu-id="db05b-124">In this example, the rule might state that any job title that contains the word “executive” should be included in the rule.</span></span> <span data-ttu-id="db05b-125">وبعد أن قمت بتحديد المعلمات الخاصة بالقاعدة أو القواعد المضنة في السياسة، يمكنك تعيين قاعدة محددة للميزة.</span><span class="sxs-lookup"><span data-stu-id="db05b-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="see-also"></a><span data-ttu-id="db05b-126">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="db05b-126">See also</span></span>
--------

[<span data-ttu-id="db05b-127">تحديد برنامج ميزات وإدارته</span><span class="sxs-lookup"><span data-stu-id="db05b-127">Defining and managing a benefit program</span></span>](manage-benefit-program.md)




