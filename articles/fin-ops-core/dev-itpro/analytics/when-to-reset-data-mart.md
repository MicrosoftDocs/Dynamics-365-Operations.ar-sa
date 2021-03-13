---
title: متى يتم أعاده تعيين متجر البيانات
description: يسرد هذا الموضوع الحالات التي قد يتم تحسينها عن طريق أعاده تعيين متجر البيانات والظروف التي فيها أعاده تعيين متجر البيانات من المحتمل ان تساعدك.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c1524c7a1a3fbe71c51b23571996d87641cdf7e
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093202"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="67dee-103">متى يتم أعاده تعيين متجر البيانات</span><span class="sxs-lookup"><span data-stu-id="67dee-103">When to reset a data mart</span></span>

<span data-ttu-id="67dee-104">قد تستغرق عمليه أعاده تعيين متجر البيانات وقتا طويلا.</span><span class="sxs-lookup"><span data-stu-id="67dee-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="67dee-105">استنادا إلى الحالات، قد لا يكون هذا الاجراء هو الحل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="67dee-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="67dee-106">يسرد هذا الموضوع الحالات التي قد يتم تحسينها عن طريق أعاده تعيين متجر البيانات والظروف التي فيها أعاده تعيين متجر البيانات من المحتمل ان تساعدك.</span><span class="sxs-lookup"><span data-stu-id="67dee-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a><span data-ttu-id="67dee-107">متى تحتاج متجر أعاده تعيين البيانات؟</span><span class="sxs-lookup"><span data-stu-id="67dee-107">When do you need to do a data mart reset?</span></span>
<span data-ttu-id="67dee-108">اطلع علي الاسئله التالية قبل أعاده تعيين متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="67dee-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="67dee-109">الاجابه بنعم لأحد الاسئله أو أكثر قد يشير إلى ان مؤسستك يمكن ان تستفيد من أعاده تعيين متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="67dee-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="67dee-110">تمت استعادة قاعدة بيانات التطبيق، ولكن لم تتم استعادة قاعدة بيانات متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="67dee-110">The application database was restored, but the data mart database was not restored.</span></span>
- <span data-ttu-id="67dee-111">تظهر بيانات غير صحيحه لفتره محاسبيه، وليست نتيجة لمشكله في تصميم التقرير.</span><span class="sxs-lookup"><span data-stu-id="67dee-111">You see incorrect data for an accounting period, which isn't the result of an issue with the report design.</span></span>
- <span data-ttu-id="67dee-112">تظهر بيانات غير صحيحه لفتره محاسبيه ، ويتم سرد السجلات ضمن محاولات التكامل في صفحه **حاله التكامل** في مصمم التقرير (بدء تشغيل مصمم التقارير وتحديد **الادخالات > حاله التكامل**).</span><span class="sxs-lookup"><span data-stu-id="67dee-112">You see incorrect data for an accounting period, and records are listed under Integration attempts on the **Integration status** page in Report Designer (start the Report Designer and select **Tools > Integration status**).</span></span>
- <span data-ttu-id="67dee-113">لقد قمت بفتح حدث دعم وقام مهندس دعم بإرشادك لأعاده تعيين متجر البيانات كجزء من خطوه استكشاف الأخطاء وإصلاحها.</span><span class="sxs-lookup"><span data-stu-id="67dee-113">You've opened a support incident and a support engineer has instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="67dee-114">عندما لا يكون من المناسب أعاده تعيين متجر البيانات؟</span><span class="sxs-lookup"><span data-stu-id="67dee-114">When it's not appropriate to reset a data mart?</span></span>
<span data-ttu-id="67dee-115">توجد بعض الحالات عندما لا نوصي باعاده تعيين متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="67dee-115">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="67dee-116">تشمل هذه المهام ما يلي.</span><span class="sxs-lookup"><span data-stu-id="67dee-116">These include the following.</span></span> 

- <span data-ttu-id="67dee-117">في اي وقت لا يتم سرد السبب في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="67dee-117">Anytime the reason isn’t listed in this topic.</span></span>
- <span data-ttu-id="67dee-118">مواجهه مشكلات في الأداء مقترنة بمزامنة البيانات. في هذه الحالة، قد لا تساعد أعاده تعيين متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="67dee-118">You're experiencing performance issues that are associated with a data sync. In this circumstance, resetting the data mart probably won't help.</span></span>
- <span data-ttu-id="67dee-119">إذا كان لديك نقش أعاده تعيين متكرر نتيجة لأي من الأسباب التالية:</span><span class="sxs-lookup"><span data-stu-id="67dee-119">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="67dee-120">**البيانات المفقودة** - أولا، استبعاد مشاكل تصميم التقرير وإصدارات مزامنة البيانات، علي سبيل المثال، لاحظ انه لم يتم تشغيل خريطة الحقيقة نظرا لأنه قد تم نشر البيانات المفقودة.</span><span class="sxs-lookup"><span data-stu-id="67dee-120">**Missing data** - First, eliminate report design issues and data sync timing issues, for example, you observe that the fact map hasn’t run since missing data was posted.</span></span>
  - <span data-ttu-id="67dee-121">**حاله التكامل العالق** - إذا كان التكامل بطيئا أو إذا كان عالقا، فان أعاده تعيين البيانات متجر هو أمر لا يمكن حل المشكلة.</span><span class="sxs-lookup"><span data-stu-id="67dee-121">**Stuck integration state** - If the integration is slow or seems stuck, resetting the data mart is unlikely to resolve the issue.</span></span>
  - <span data-ttu-id="67dee-122">**فشلت محاولات أعاده التعيين** - إذا تم اجراء عدد من المحاولات لإكمال عمليه أعاده تعيين، وكانت غير ناجحه بسبب البيانات المفقودة، فاننا نوصي بفتح حدث الدعم والعمل مع مهندس دعم لتحليل الموقف قبل محاولة أعاده تعيين متجر البيانات مره أخرى.</span><span class="sxs-lookup"><span data-stu-id="67dee-122">**Attempts to reset have been unsuccessful** - If a number of attempts to complete a reset have been made, and have been unsuccessful because of missing data, we recommend opening a support incident and working with a support engineer to analyze your situation before attempting to reset the data mart again.</span></span>
  - <span data-ttu-id="67dee-123">**السجلات القديمة** - السجلات التالفة بنفس الضرورة ضبط أعاده تعيين متجر البيانات بالضرورة.</span><span class="sxs-lookup"><span data-stu-id="67dee-123">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="67dee-124">إذا كانت لديك مجموعه كبيره من البيانات، ستتطلب عمليه أعاده التعيين بعض الوقت ليتم تشغيلها، ولكنها من المحتمل ان تؤدي إلى تحسين.</span><span class="sxs-lookup"><span data-stu-id="67dee-124">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-a-data-mart-reset-does-not-do"></a><span data-ttu-id="67dee-125">ما لا يقوم به متجر أعاده تعيين البيانات.</span><span class="sxs-lookup"><span data-stu-id="67dee-125">What a data mart reset does not do</span></span>  
- <span data-ttu-id="67dee-126">ستبدا عمليه أعاده التعيين فقط عند اكتمال المهام الموجودة.</span><span class="sxs-lookup"><span data-stu-id="67dee-126">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="67dee-127">ويضمن ذلك عدم ادراج البيانات القديمة.</span><span class="sxs-lookup"><span data-stu-id="67dee-127">This ensures that old data is not inserted.</span></span> <span data-ttu-id="67dee-128">في هذه المرحلة، قد تظهر لك رسالة مثل، "تعذرت معالجه البيانات متجر أعاده التعيين بسبب وجود مهمة نشطه.</span><span class="sxs-lookup"><span data-stu-id="67dee-128">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="67dee-129">الرجاء المحاولة مره أخرى لاحقا."</span><span class="sxs-lookup"><span data-stu-id="67dee-129">Please try again later.”</span></span>
- <span data-ttu-id="67dee-130">ستؤدي أعاده التعيين إلى تعطيل مهام التكامل وحذف كافة بيانات متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="67dee-130">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="67dee-131">إعادة تمكين التكامل</span><span class="sxs-lookup"><span data-stu-id="67dee-131">The integration is re-enabled.</span></span>

> [!NOTE]
> <span data-ttu-id="67dee-132">تحدد النقاط التالية شيئين لأعاده تعيين متجر البيانات *لن* يفعلون.</span><span class="sxs-lookup"><span data-stu-id="67dee-132">The following points specify two things that resetting a data mart will *not* do.</span></span> <br>
> - <span data-ttu-id="67dee-133">أعاده تعيين عدم مسح تصميمات التقرير.</span><span class="sxs-lookup"><span data-stu-id="67dee-133">Resets do not clear report designs.</span></span> <br>
> - <span data-ttu-id="67dee-134">ولا يتم أعاده تعيين بيانات الشركة أو بيانات المستخدم الا إذا تم تحديدها.</span><span class="sxs-lookup"><span data-stu-id="67dee-134">Resets do not clear company data or user data unless selected.</span></span>
