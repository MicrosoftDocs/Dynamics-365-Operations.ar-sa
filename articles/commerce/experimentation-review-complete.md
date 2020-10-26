---
title: ترقية التباين وإكمال تجربة
description: يوضح هذا الموضوع كيفيه ترقيه التباين الناجح وإكمال تجربه في Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2e011f10e908d6a2efe2e928fc5e0abc7659cb8b
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930128"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="21141-103">ترقية التباين وإكمال تجربة</span><span class="sxs-lookup"><span data-stu-id="21141-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="21141-104">يوضح هذا الموضوع كيفيه ترقيه الاختلافات التي أنتجت أفضل النتائج في التجربة، وكيفيه إكمال التجربة.</span><span class="sxs-lookup"><span data-stu-id="21141-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="21141-105">يوضح الرسم التخطيطي التالي كافة الخطوات المتضمنة في اعداد وتشغيل تجربه علي أحد مواقع التجارة الالكترونيه في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="21141-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="21141-106">وتتم تغطيه الخطوات الاضافيه في موضوعات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="21141-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="21141-107">[![رحلة مستخدم التجربة - المراجعة والإكمال](./media/experimentation_review_complete.svg)](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="21141-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="21141-108">بعد [تشغيل الاختبار الخاص بك](experimentation-run-monitor.md)وتجميع البيانات الكافية لتحديد اي التغيرات التي تريد استخدامها علي موقعك المباشر، ستقوم بترقيه التباين وإنهاء التجربة.</span><span class="sxs-lookup"><span data-stu-id="21141-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="21141-109">ترقيه تباين</span><span class="sxs-lookup"><span data-stu-id="21141-109">Promote a variation</span></span>
<span data-ttu-id="21141-110">استخدم البيانات والتحليلات المرتبطة بالتجربة في الخدمة التابعة لجهة أخرى لتحديد الاختلافات التي أنتجت أفضل النتائج.</span><span class="sxs-lookup"><span data-stu-id="21141-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="21141-111">لاستبدال المحتوي الحالي علي الموقع المباشر بالتباين الفائز بحيث يكون متوفرا لكافة مستخدمي موقع الويب الخاص بك، قم بما يلي.</span><span class="sxs-lookup"><span data-stu-id="21141-111">To replace the current content on the live site with the winning variation so that it's available to all users of your website, do the following.</span></span> 

1. <span data-ttu-id="21141-112">انتقل إلى علامة التبويب **التجارب** في منشئ الموقع وحدد التجربة.</span><span class="sxs-lookup"><span data-stu-id="21141-112">Go to the **Experiments** tab in site builder and select the experiment.</span></span>
1. <span data-ttu-id="21141-113">حدد **التجربة الكاملة** علي الشريط العلوي.</span><span class="sxs-lookup"><span data-stu-id="21141-113">Select **Complete experiment** on the top bar.</span></span>
1. <span data-ttu-id="21141-114">في قائمة مربع حوار **إكمال التجربه** ، حدد **مراجعه بيانات التجربة** .</span><span class="sxs-lookup"><span data-stu-id="21141-114">In the **Complete the experiment** dialog menu, select **Review the experiment data** .</span></span> <span data-ttu-id="21141-115">ويتم فتح الخدمة الخاصة بجهات خارجية حيث يمكنك التحقق من صحة القياسات وتحديد اي تباينات قدمت أفضل أداء.</span><span class="sxs-lookup"><span data-stu-id="21141-115">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="21141-116">في قائمة مربع حوار **إكمال التجربة** في منشئ الموقع، حدد التباين الفائز ثم حدد **التالي** .</span><span class="sxs-lookup"><span data-stu-id="21141-116">In the **Complete the experiment** dialog menu in site builder, select the winning variation and then select **Next** .</span></span>
1. <span data-ttu-id="21141-117">افتح الخدمة التابعة لجهة أخرى وأوقف التجربة.</span><span class="sxs-lookup"><span data-stu-id="21141-117">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="21141-118">في منشئ الموقع، حدد **إكمال** للكتابة فوق الصفحة المباشرة الاصليه ونشر التباين الفائز بحيث تكون متوفرة لكافة مستخدمي موقع الويب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="21141-118">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="21141-119">إذا اخترت الاحتفاظ بالصفحة المباشرة الحالية وعدم نشر التباين، حدد **أعاده نشر الصفحة الاصليه** .</span><span class="sxs-lookup"><span data-stu-id="21141-119">If you choose to keep the current live page and not publish a variation, select **Republish the original page** .</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="21141-120">حذف التجربة الخاصة بك</span><span class="sxs-lookup"><span data-stu-id="21141-120">Delete your experiment</span></span>
<span data-ttu-id="21141-121">بينما لا يتطلب ذلك حذف تجربه مكتملة في التجارة، يمكنك اختيار حذفها لتوفير مساحة أو لتنظيف مساحة العمل الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="21141-121">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> <span data-ttu-id="21141-122">لحذف تجربه ، قم بما يلي:</span><span class="sxs-lookup"><span data-stu-id="21141-122">To delete an experiment, do the following.</span></span>

1. <span data-ttu-id="21141-123">انتقل إلى علامة التبويب **التجارب** في منشئ الموقع وحدد التجربة.</span><span class="sxs-lookup"><span data-stu-id="21141-123">Go to the **Experiments** tab in site builder and select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="21141-124">في حاله استمرار نشاط التجربة، قم بإيقاف التجربة في خدمه الجهة الأخرى قبل المتابعة.</span><span class="sxs-lookup"><span data-stu-id="21141-124">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="21141-125">حدد **إلغاء** النشر في شريط الأوامر لأزاله محتوي التباين من الموقع المباشر.</span><span class="sxs-lookup"><span data-stu-id="21141-125">Select **Unpublish** in the command bar to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="21141-126">حدد **حذف** في شريط الأوامر لحذف التجربة.</span><span class="sxs-lookup"><span data-stu-id="21141-126">Select **Delete** in the command bar to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="21141-127">الخطوة السابقة</span><span class="sxs-lookup"><span data-stu-id="21141-127">Previous step</span></span>
[<span data-ttu-id="21141-128">تشغيل تجربة ومراقبتها</span><span class="sxs-lookup"><span data-stu-id="21141-128">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)
