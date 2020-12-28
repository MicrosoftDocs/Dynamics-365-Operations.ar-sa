---
title: سياسات استحقاق الميزات
description: توفر هذه المقالة معلومات حول سياسات استحقاق الميزات، التي تساعدك على تحديد المؤهلين لميزات معينة.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: fd4def17bf60ae2812927221c45547c5ac379f2b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417030"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="b8d3d-103">سياسات استحقاق الميزات</span><span class="sxs-lookup"><span data-stu-id="b8d3d-103">Benefit eligibility policies</span></span>

<span data-ttu-id="b8d3d-104">توفر هذه المقالة معلومات حول سياسات استحقاق الميزات، التي تساعدك على تحديد المؤهلين لميزات معينة.</span><span class="sxs-lookup"><span data-stu-id="b8d3d-104">This article provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="b8d3d-105">عند إنشاء الميزات، تقرر ما الميزات التي ستكون متاحة للموظفين.</span><span class="sxs-lookup"><span data-stu-id="b8d3d-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="b8d3d-106">يعرض الجدول التالي أمثلة للفوائد التي قد توفرها لموظفين محددين.</span><span class="sxs-lookup"><span data-stu-id="b8d3d-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="b8d3d-107">الميزة</span><span class="sxs-lookup"><span data-stu-id="b8d3d-107">Benefit</span></span>          | <span data-ttu-id="b8d3d-108">الشخص الذي تتوفر له الميزة</span><span class="sxs-lookup"><span data-stu-id="b8d3d-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="b8d3d-109">التأمين الصحي</span><span class="sxs-lookup"><span data-stu-id="b8d3d-109">Health insurance</span></span> | <span data-ttu-id="b8d3d-110">كل الموظفين</span><span class="sxs-lookup"><span data-stu-id="b8d3d-110">All employees</span></span>                   |
| <span data-ttu-id="b8d3d-111">الهاتف الجوال</span><span class="sxs-lookup"><span data-stu-id="b8d3d-111">Mobile phone</span></span>     | <span data-ttu-id="b8d3d-112">فريق المبيعات، الموظفون التنفيذيون</span><span class="sxs-lookup"><span data-stu-id="b8d3d-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="b8d3d-113">مسارات وقوف السيارات</span><span class="sxs-lookup"><span data-stu-id="b8d3d-113">Parking passes</span></span>   | <span data-ttu-id="b8d3d-114">مديرون تنفيذيون</span><span class="sxs-lookup"><span data-stu-id="b8d3d-114">Executives</span></span>                      |

<span data-ttu-id="b8d3d-115">يتم استخدام المكونات التالية لإنشاء سياسات الاستحقاق:</span><span class="sxs-lookup"><span data-stu-id="b8d3d-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="b8d3d-116">أنواع قاعدة السياسة</span><span class="sxs-lookup"><span data-stu-id="b8d3d-116">Policy rule types</span></span>
-   <span data-ttu-id="b8d3d-117">سياسات استحقاق الميزات</span><span class="sxs-lookup"><span data-stu-id="b8d3d-117">Benefit eligibility policies</span></span>

<span data-ttu-id="b8d3d-118">تحدد أنواع قاعدة السياسة معلمات الاستعلام التي تستخدم عندما تقوم بتطوير قواعد نهُج معينة.</span><span class="sxs-lookup"><span data-stu-id="b8d3d-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="b8d3d-119">وبعد إنشاء أنواع قواعد السياسة، يمكنك إنشاء سياسات استحقاق الميزات.</span><span class="sxs-lookup"><span data-stu-id="b8d3d-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="b8d3d-120">وتتيح لك السياسات إنشاء مجموعة من القواعد التي تنطبق على واحد أو أكثر من الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="b8d3d-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="b8d3d-121">وضمن كل سياسة، يمكنك عرض أنواع قاعدة سياسة استحقاق الميزات التي قمت بإنشائها سابقًا.</span><span class="sxs-lookup"><span data-stu-id="b8d3d-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="b8d3d-122">وتحدد نطاق القاعدة ضمن السياسة.</span><span class="sxs-lookup"><span data-stu-id="b8d3d-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="b8d3d-123">على سبيل المثال، إذا قمت بإنشاء نوع قاعدة سياسة استحقاق ميزة باسم **المدير التنفيذي**، يمكنك تحديد القاعدة الموجودة في تلك السياسة.</span><span class="sxs-lookup"><span data-stu-id="b8d3d-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="b8d3d-124">في هذا المثال، قد تنص القاعدة على أن أي مسمى وظيفي يحتوي على كلمة "المدير التنفيذي" يجب تضمينه في القاعدة.</span><span class="sxs-lookup"><span data-stu-id="b8d3d-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="b8d3d-125">وبعد أن قمت بتحديد المعلمات الخاصة بالقاعدة أو القواعد المضنة في السياسة، يمكنك تعيين قاعدة محددة للميزة.</span><span class="sxs-lookup"><span data-stu-id="b8d3d-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>




