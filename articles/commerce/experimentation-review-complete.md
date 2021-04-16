---
title: ترقية التباين وإكمال تجربة
description: يوضح هذا الموضوع كيفيه ترقيه التباين الناجح وإكمال تجربه في Dynamics 365 Commerce.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0ea0fc8d50c25312b184ec1d3bd613695870d121
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792549"
---
# <a name="promote-a-variation-and-complete-an-experiment"></a><span data-ttu-id="f3ac3-103">ترقية التباين وإكمال تجربة</span><span class="sxs-lookup"><span data-stu-id="f3ac3-103">Promote a variation and complete an experiment</span></span>

<span data-ttu-id="f3ac3-104">يوضح هذا الموضوع كيفيه ترقيه الاختلافات التي أنتجت أفضل النتائج في التجربة، وكيفيه إكمال التجربة.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-104">This topic describes how to promote the variation that produced the best results in your experiment, and how to complete the experiment.</span></span> <span data-ttu-id="f3ac3-105">يوضح الرسم التخطيطي التالي كافة الخطوات المتضمنة في اعداد وتشغيل تجربه علي أحد مواقع التجارة الالكترونيه في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="f3ac3-106">وتتم تغطيه الخطوات الاضافيه في موضوعات منفصلة.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="f3ac3-107">[![رحلة مستخدم التجربة - المراجعة والإكمال](./media/experimentation_review_complete.svg)](./media/experimentation_review_complete.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="f3ac3-107">[ ![Experimentation user journey - Review & Complete](./media/experimentation_review_complete.svg) ](./media/experimentation_review_complete.svg#lightbox)</span></span>

<span data-ttu-id="f3ac3-108">بعد [تشغيل الاختبار الخاص بك](experimentation-run-monitor.md)وتجميع البيانات الكافية لتحديد اي التغيرات التي تريد استخدامها علي موقعك المباشر، ستقوم بترقيه التباين وإنهاء التجربة.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-108">After you've [run your experiment](experimentation-run-monitor.md) and collected sufficient data to determine which variation you want to use on your live site, you'll promote the variation and end the experiment.</span></span>

## <a name="promote-a-variation"></a><span data-ttu-id="f3ac3-109">ترقيه تباين</span><span class="sxs-lookup"><span data-stu-id="f3ac3-109">Promote a variation</span></span>
<span data-ttu-id="f3ac3-110">استخدم البيانات والتحليلات المرتبطة بالتجربة في الخدمة التابعة لجهة أخرى لتحديد الاختلافات التي أنتجت أفضل النتائج.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-110">Use the data and analytics related to the experiment in the third-party service to decide which variation produced the best results.</span></span> <span data-ttu-id="f3ac3-111">ثم يمكنك ترقيتها عن طريق استبدال المحتوى الحالي على الموقع المباشر بالتباين الفائز بحيث يكون متوفرًا لكافة مستخدمي موقع الويب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-111">You can then promote it by replacing the current content on the live site with the winning variation so that it's available to all users of your website.</span></span>

<span data-ttu-id="f3ac3-112">لترقية التباين الفائز، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-112">To promote the winning variation, follow these steps.</span></span> 

1. <span data-ttu-id="f3ac3-113">في منشئ موقع Commerce، حدد **التجارب** في جزء التنقل الأيسر، ثم حدد التجربة.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-113">In Commerce site builder, select **Experiments** in the left navigation pane, and then select the experiment.</span></span>
1. <span data-ttu-id="f3ac3-114">على شريط الأدوات، حدد **التجربة الكاملة**.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-114">On the command bar, select **Complete experiment**.</span></span>
1. <span data-ttu-id="f3ac3-115">في مربع حوار **إكمال التجربة**، حدد **مراجعة بيانات التجربة**.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-115">In the **Complete the experiment** dialog box, select **Review the experiment data**.</span></span> <span data-ttu-id="f3ac3-116">ويتم فتح الخدمة الخاصة بجهات خارجية حيث يمكنك التحقق من صحة القياسات وتحديد اي تباينات قدمت أفضل أداء.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-116">The third-party service opens where you can validate the metrics and determine which variation performed the best.</span></span>
1. <span data-ttu-id="f3ac3-117">في مربع حوار **إكمال التجربة**، حدد التباين الفائز، ثم حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-117">In the **Complete the experiment** dialog box, select the winning variation, and then select **Next**.</span></span>
1. <span data-ttu-id="f3ac3-118">افتح الخدمة التابعة لجهة أخرى وأوقف التجربة.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-118">Open the third-party service and stop the experiment.</span></span>
1. <span data-ttu-id="f3ac3-119">في منشئ الموقع، حدد **إكمال** للكتابة فوق الصفحة المباشرة الاصليه ونشر التباين الفائز بحيث تكون متوفرة لكافة مستخدمي موقع الويب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-119">In site builder, select **Complete** to overwrite the original live page and publish the winning variation so that it's available to all users of your website.</span></span> 

> [!NOTE]
> <span data-ttu-id="f3ac3-120">إذا اخترت الاحتفاظ بالصفحة المباشرة الحالية وعدم نشر التباين، حدد **أعاده نشر الصفحة الاصليه**.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-120">If you choose to keep the current live page and not publish a variation, select **Republish the original page**.</span></span>

## <a name="delete-your-experiment"></a><span data-ttu-id="f3ac3-121">حذف التجربة الخاصة بك</span><span class="sxs-lookup"><span data-stu-id="f3ac3-121">Delete your experiment</span></span>
<span data-ttu-id="f3ac3-122">بينما لا يتطلب ذلك حذف تجربه مكتملة في التجارة، يمكنك اختيار حذفها لتوفير مساحة أو لتنظيف مساحة العمل الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-122">While it's not required that you delete a completed experiment in Commerce, you may choose to delete it to save space or clean up your workspace.</span></span> 

<span data-ttu-id="f3ac3-123">لحذف تجربة في منشئ مواقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-123">To delete an experiment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="f3ac3-124">حدد **تجارب** في جزء التنقل الأيسر، ثم حدد التجربة.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-124">Select **Experiments** in the left navigation pane, and then select the experiment.</span></span> 
    > [!NOTE]
    > <span data-ttu-id="f3ac3-125">في حاله استمرار نشاط التجربة، قم بإيقاف التجربة في خدمه الجهة الأخرى قبل المتابعة.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-125">If the experiment is still active, stop the experiment in the third-party service before proceeding.</span></span>
1. <span data-ttu-id="f3ac3-126">في شريط الأوامر، حدد **إلغاء النشر** لإزالة محتوى التباين من الموقع المباشر.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-126">On the command bar, select **Unpublish**  to remove the variation content from the live site.</span></span>
1. <span data-ttu-id="f3ac3-127">حدد **حذف** لحذف التجربة.</span><span class="sxs-lookup"><span data-stu-id="f3ac3-127">Select **Delete** to delete the experiment.</span></span>

## <a name="previous-step"></a><span data-ttu-id="f3ac3-128">الخطوة السابقة</span><span class="sxs-lookup"><span data-stu-id="f3ac3-128">Previous step</span></span>
[<span data-ttu-id="f3ac3-129">تشغيل تجربة ومراقبتها</span><span class="sxs-lookup"><span data-stu-id="f3ac3-129">Run and monitor an experiment</span></span>](experimentation-run-monitor.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]