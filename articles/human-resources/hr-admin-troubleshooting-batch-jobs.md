---
title: تحسين الأداء من خلال جدولة وظائف دفعية بعد ساعات العمل
description: يوضح هذا الموضوع كيفية حل بعض مشكلات الأداء باستخدام Microsoft Dynamics 365 Human Resources عن طريق جدولة الوظائف الدفعية التي يستغرق تشغيلها فترة طويلة بعد ساعات العمل.
author: andreabichsel
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: f67b4b4c20345297f186c792fe2766c686e2ddbf
ms.sourcegitcommit: bdfc84aa7f607511981c0b2f20f03fabcb773510
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500495"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="ce51e-103">تحسين الأداء من خلال جدولة وظائف دفعية بعد ساعات العمل</span><span class="sxs-lookup"><span data-stu-id="ce51e-103">Optimize performance by scheduling batch jobs after hours</span></span>

## <a name="issue"></a><span data-ttu-id="ce51e-104">المشكلة</span><span class="sxs-lookup"><span data-stu-id="ce51e-104">Issue</span></span>

<span data-ttu-id="ce51e-105">يمكن أن يواجه Microsoft Dynamics 365 Human Resources مشكلات في الأداء إذا كانت الوظائف الدفعية التي يستغرق تشغيلها فترة طويلة تعمل أثناء ساعات العمل العادية.</span><span class="sxs-lookup"><span data-stu-id="ce51e-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="ce51e-106">الحل‬</span><span class="sxs-lookup"><span data-stu-id="ce51e-106">Resolution</span></span>

<span data-ttu-id="ce51e-107">قم بجدولة الوظائف الدفعية التالية أثناء الساعات توقف العمل.</span><span class="sxs-lookup"><span data-stu-id="ce51e-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="ce51e-108">نوصي أيضًا بمراجعة تكرار الوظائف الدفعية التي تعمل بشكل متكرر.</span><span class="sxs-lookup"><span data-stu-id="ce51e-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="ce51e-109">قم بتخفيض تكرار الوظيفة الدفعية إذا كان ذلك ممكنا.</span><span class="sxs-lookup"><span data-stu-id="ce51e-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="ce51e-110">في العديد من الحالات، يكون التكرار الافتراضي كافيًا.</span><span class="sxs-lookup"><span data-stu-id="ce51e-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="ce51e-111">يجب تشغيل الوظائف الدفعية التالية ليلا أو بعد ساعات العمل.</span><span class="sxs-lookup"><span data-stu-id="ce51e-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="ce51e-112">تأكد من التحقق من المنطقة الزمنية لهذه الوظائف الدفعية المتكررة.</span><span class="sxs-lookup"><span data-stu-id="ce51e-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="ce51e-113">قد تستخدم بعض الوظائف الدفعية التوقيت الرسمي الباسيفيكي (PST).</span><span class="sxs-lookup"><span data-stu-id="ce51e-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="ce51e-114">وظيفة دفعية</span><span class="sxs-lookup"><span data-stu-id="ce51e-114">Batch job</span></span> | <span data-ttu-id="ce51e-115">التكرار الافتراضي</span><span class="sxs-lookup"><span data-stu-id="ce51e-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="ce51e-116">تنظيف محفوظات الوظائف الدفعية</span><span class="sxs-lookup"><span data-stu-id="ce51e-116">Batch job history cleanup</span></span> | <span data-ttu-id="ce51e-117">مرة واحدة كل شهر</span><span class="sxs-lookup"><span data-stu-id="ce51e-117">1 time per month</span></span> |
| <span data-ttu-id="ce51e-118">تصدير تنظيف التشغيل المرحلي</span><span class="sxs-lookup"><span data-stu-id="ce51e-118">Export staging cleanup</span></span> | <span data-ttu-id="ce51e-119">مرة واحدة كل يوم</span><span class="sxs-lookup"><span data-stu-id="ce51e-119">1 time per day</span></span> |
| <span data-ttu-id="ce51e-120">مزامنة الطلب المفقود لتكامل Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ce51e-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="ce51e-121">مرة واحدة كل يوم</span><span class="sxs-lookup"><span data-stu-id="ce51e-121">1 time per day</span></span> |
| <span data-ttu-id="ce51e-122">وظيفة نظام ضغط قاعدة البيانات التي يلزم تشغيلها بشكل منتظم خلال ساعات توقف العمل</span><span class="sxs-lookup"><span data-stu-id="ce51e-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="ce51e-123">مرة واحدة كل يوم</span><span class="sxs-lookup"><span data-stu-id="ce51e-123">1 time per day</span></span> |
| <span data-ttu-id="ce51e-124">وظيفة نظام إعادة بناء فهرس قاعدة البيانات التي يلزم تشغيلها بشكل منتظم خلال ساعات توقف العمل</span><span class="sxs-lookup"><span data-stu-id="ce51e-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="ce51e-125">مرة واحدة كل يوم</span><span class="sxs-lookup"><span data-stu-id="ce51e-125">1 time per day</span></span> |

1. <span data-ttu-id="ce51e-126">في Human Resources، حدد **إدارة النظام**.</span><span class="sxs-lookup"><span data-stu-id="ce51e-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="ce51e-127">في شريط **البحث**، ابحث عن إحدى الوظائف الدفعية المذكورة أعلاه.</span><span class="sxs-lookup"><span data-stu-id="ce51e-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="ce51e-128">حدد **تشغيل في الخلفية**، ثم حدد **التكرار**.</span><span class="sxs-lookup"><span data-stu-id="ce51e-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![تعيين التكرار](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="ce51e-130">تحت **تعريف التكرار**، قم بتعيين **تاريخ البدء** و**وقت البدء** بحيث يقعان خلال ساعات التوقف عن العمل أو عطلة نهاية الأسبوع.</span><span class="sxs-lookup"><span data-stu-id="ce51e-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="ce51e-131">حدد **بلا تاريخ انتهاء**.</span><span class="sxs-lookup"><span data-stu-id="ce51e-131">Select **No end date**.</span></span> 

   ![تعيين تاريخ بدء التكرار ووقته](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="ce51e-133">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ce51e-133">Select **OK**.</span></span>

6. <span data-ttu-id="ce51e-134">إذا لزم الأمر، قم بتغيير أي معلمات أخرى تحت **تشغيل في الخلفية**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="ce51e-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce51e-135">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ce51e-135">Additional resources</span></span>

[<span data-ttu-id="ce51e-136">تحسين الأداء باستخدام مهام التنظيف التلقائية</span><span class="sxs-lookup"><span data-stu-id="ce51e-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)
