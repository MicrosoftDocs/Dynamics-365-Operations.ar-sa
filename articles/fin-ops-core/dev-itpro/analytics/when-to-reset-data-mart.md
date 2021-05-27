---
title: متى يتم أعاده تعيين متجر البيانات
description: يسرد هذا الموضوع الحالات التي قد يتم تحسينها عن طريق أعاده تعيين متجر البيانات والظروف التي فيها أعاده تعيين متجر البيانات من المحتمل ان تساعدك.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/07/2021
ms.locfileid: "5988982"
---
# <a name="when-to-reset-a-data-mart"></a><span data-ttu-id="d2daa-103">متى يتم أعاده تعيين متجر البيانات</span><span class="sxs-lookup"><span data-stu-id="d2daa-103">When to reset a data mart</span></span>

<span data-ttu-id="d2daa-104">قد تستغرق عمليه أعاده تعيين متجر البيانات وقتا طويلا.</span><span class="sxs-lookup"><span data-stu-id="d2daa-104">Resetting a data mart can be time consuming.</span></span> <span data-ttu-id="d2daa-105">استنادا إلى الحالات، قد لا يكون هذا الاجراء هو الحل المطلوب.</span><span class="sxs-lookup"><span data-stu-id="d2daa-105">Depending on the circumstances, this action may not be the solution that's needed.</span></span> <span data-ttu-id="d2daa-106">يسرد هذا الموضوع الحالات التي قد يتم تحسينها عن طريق أعاده تعيين متجر البيانات والظروف التي فيها أعاده تعيين متجر البيانات من المحتمل ان تساعدك.</span><span class="sxs-lookup"><span data-stu-id="d2daa-106">This topic lists the circumstances that might be improved by resetting a data mart, as well as circumstances in which resetting your data mart is unlikely to help.</span></span>  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a><span data-ttu-id="d2daa-107">متى أحتاج إلى إعادة تعيين متجر بيانات؟</span><span class="sxs-lookup"><span data-stu-id="d2daa-107">When do I need to do a data mart reset?</span></span>
<span data-ttu-id="d2daa-108">اطلع علي الاسئله التالية قبل أعاده تعيين متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="d2daa-108">Consider the following questions before resetting a data mart.</span></span> <span data-ttu-id="d2daa-109">الاجابه بنعم لأحد الاسئله أو أكثر قد يشير إلى ان مؤسستك يمكن ان تستفيد من أعاده تعيين متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="d2daa-109">Answering yes to one or more questions might indicate that your organization can benefit by resetting the data mart.</span></span>

- <span data-ttu-id="d2daa-110">هل تمت استعادة قاعدة بيانات التطبيق؟</span><span class="sxs-lookup"><span data-stu-id="d2daa-110">Was the application database restored?</span></span>
- <span data-ttu-id="d2daa-111">إذا قمت بفتح حدث دعم وقام مهندس دعم بإرشادك لإعادة تعيين متجر البيانات كجزء من خطوة استكشاف الأخطاء وإصلاحها؟</span><span class="sxs-lookup"><span data-stu-id="d2daa-111">If you've opened a support incident that and a support engineer has instructed you to reset the data mart as part of a troubleshooting step?</span></span>
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a><span data-ttu-id="d2daa-112">عندما لا يكون من المناسب إعادة تعيين متجر البيانات؟</span><span class="sxs-lookup"><span data-stu-id="d2daa-112">When is it not appropriate to reset a data mart?</span></span>
<span data-ttu-id="d2daa-113">توجد بعض الحالات عندما لا نوصي باعاده تعيين متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="d2daa-113">There are some circumstances when we don't recommend resetting a data mart.</span></span> <span data-ttu-id="d2daa-114">تشمل هذه المهام ما يلي.</span><span class="sxs-lookup"><span data-stu-id="d2daa-114">These include the following.</span></span> 

- <span data-ttu-id="d2daa-115">مواجهة مشكلات في الأداء مقترنة بمزامنة البيانات.</span><span class="sxs-lookup"><span data-stu-id="d2daa-115">You're experiencing performance issues that are associated with a data sync.</span></span> 
- <span data-ttu-id="d2daa-116">إذا كان لديك نقش أعاده تعيين متكرر نتيجة لأي من الأسباب التالية:</span><span class="sxs-lookup"><span data-stu-id="d2daa-116">If you have a recurring reset pattern due to any of the following reasons:</span></span> 
  - <span data-ttu-id="d2daa-117">**بيانات مفقودة**</span><span class="sxs-lookup"><span data-stu-id="d2daa-117">**Missing data**</span></span> 
  - <span data-ttu-id="d2daa-118">**حالة التكامل العالق**</span><span class="sxs-lookup"><span data-stu-id="d2daa-118">**Stuck integration state**</span></span> 
  - <span data-ttu-id="d2daa-119">**السجلات القديمة** - السجلات التالفة بنفس الضرورة ضبط أعاده تعيين متجر البيانات بالضرورة.</span><span class="sxs-lookup"><span data-stu-id="d2daa-119">**Stale records** - Stale records by themselves don't necessarily justify resetting the data mart.</span></span> <span data-ttu-id="d2daa-120">إذا كانت لديك مجموعه كبيره من البيانات، ستتطلب عمليه أعاده التعيين بعض الوقت ليتم تشغيلها، ولكنها من المحتمل ان تؤدي إلى تحسين.</span><span class="sxs-lookup"><span data-stu-id="d2daa-120">If you have a large data set, the reset process will take some time to run, but is unlikely to result in improvement.</span></span>
 
## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="d2daa-121">ما وقت إعادة تعيين متجر البيانات؟</span><span class="sxs-lookup"><span data-stu-id="d2daa-121">What is a data mart reset?</span></span>
- <span data-ttu-id="d2daa-122">ستبدا عمليه أعاده التعيين فقط عند اكتمال المهام الموجودة.</span><span class="sxs-lookup"><span data-stu-id="d2daa-122">A reset will only start when existing tasks are complete.</span></span> <span data-ttu-id="d2daa-123">ويضمن ذلك عدم ادراج البيانات القديمة.</span><span class="sxs-lookup"><span data-stu-id="d2daa-123">This ensures that old data is not inserted.</span></span> <span data-ttu-id="d2daa-124">في هذه المرحلة، قد تظهر لك رسالة مثل، "تعذرت معالجه البيانات متجر أعاده التعيين بسبب وجود مهمة نشطه.</span><span class="sxs-lookup"><span data-stu-id="d2daa-124">At this point you may see a message such as, “The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="d2daa-125">الرجاء المحاولة مره أخرى لاحقا."</span><span class="sxs-lookup"><span data-stu-id="d2daa-125">Please try again later.”</span></span>
- <span data-ttu-id="d2daa-126">ستؤدي أعاده التعيين إلى تعطيل مهام التكامل وحذف كافة بيانات متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="d2daa-126">The reset will disable the integration tasks and delete all the data mart data.</span></span> <span data-ttu-id="d2daa-127">إعادة تمكين التكامل</span><span class="sxs-lookup"><span data-stu-id="d2daa-127">The integration is re-enabled.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="d2daa-128">إذا قمت باعادة تعيين متجر البيانات، فهل ستفقد التقارير التي قمت بتصميمها بالفعل؟</span><span class="sxs-lookup"><span data-stu-id="d2daa-128">If I reset the data mart, will I lose reports that I've already designed?</span></span> 
<span data-ttu-id="d2daa-129">لا، التقارير الخاصة بك مخزنة في جداول SQL التي لا تتأثر بإعادة تعيين متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="d2daa-129">No, your reports are stored in SQL tables that are not impacted by a reset of the data mart.</span></span> <span data-ttu-id="d2daa-130">إذا كنت مهتمًا بفقدان أية تقارير قمت بتصميمها، يمكنك إجراء النسخ الاحتياطي للتصميمات التي لا ترغب في فقدها.</span><span class="sxs-lookup"><span data-stu-id="d2daa-130">If you are concerned about losing any reports you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="d2daa-131">لنسخها احتياطيًا، افتح مصمم التقرير وانتقل إلى **الشركة > شركات > كتل الإنشاء > تصديرها**.</span><span class="sxs-lookup"><span data-stu-id="d2daa-131">To back them up, open Report Designer and go to **Company > Companies > Building Blocks > Export**.</span></span>
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a><span data-ttu-id="d2daa-132">هل من الضروري لكافة المستخدمين إنهاء النظام لإعادة تعيين متجر البيانات؟</span><span class="sxs-lookup"><span data-stu-id="d2daa-132">Is it necessary for all users to exit the system to reset the data mart?</span></span>
<span data-ttu-id="d2daa-133">لا، يمكن للمستخدمين متابعة العمل في النظام أثناء إعادة تعيين متجر البيانات.</span><span class="sxs-lookup"><span data-stu-id="d2daa-133">No, users can continue working in the system during the data mart reset.</span></span> <span data-ttu-id="d2daa-134">ومع ذلك، لن يتمكنوا من الوصول إلى أية تقارير تم إنشاؤها بواسطة التقارير المالية حتى تنتهي إعادة التعيين.</span><span class="sxs-lookup"><span data-stu-id="d2daa-134">However, they won’t be able to access any reports that were created with Financial Reporter until the reset is finished.</span></span> 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
