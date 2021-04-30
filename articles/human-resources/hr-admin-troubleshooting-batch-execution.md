---
title: إعادة تعيين المهام الدفعية العالقة
description: يشرح هذا الموضوع كيفية حل المشكلات المتعلقة بالوظائف الدفعية المتوقفة.
author: andreabichsel
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: 906a391b3c28d15445f6ddf0fc547ebcf842ba19
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881750"
---
# <a name="reset-stuck-batch-jobs"></a><span data-ttu-id="bfb4e-103">إعادة تعيين المهام الدفعية العالقة</span><span class="sxs-lookup"><span data-stu-id="bfb4e-103">Reset stuck batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a><span data-ttu-id="bfb4e-104">إصدار</span><span class="sxs-lookup"><span data-stu-id="bfb4e-104">Issue</span></span>

<span data-ttu-id="bfb4e-105">يمكن أن يواجه Microsoft Dynamics 365 Human Resources مشكلات في وظائف الدفعات المتوقفة إما في حالة **قيد التنفيذ** أو **قيد الإلغاء** ولم تكتمل.</span><span class="sxs-lookup"><span data-stu-id="bfb4e-105">Microsoft Dynamics 365 Human Resources can experience issues with batch jobs that are stuck in either an **Executing** or **Canceling** state and don't complete.</span></span>

## <a name="resolution"></a><span data-ttu-id="bfb4e-106">الدقة</span><span class="sxs-lookup"><span data-stu-id="bfb4e-106">Resolution</span></span>

<span data-ttu-id="bfb4e-107">عندما تكون وظيفة الدفعة متوقفة في حالة **قيد التنفيذ** أو **قيد إلغاء**، يمكنك إعادة تعيين الحالة من خلال فرض إلغاء الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="bfb4e-107">When a batch job is stuck in an **Executing** or **Canceling** state, you can reset the status by forcing the cancellation of the job.</span></span> <span data-ttu-id="bfb4e-108">وبعد إلغائها، يمكنك إعادة تعيين وظيفة الدفعة عن طريق تعيينها على حالة **قيد الانتظار**.</span><span class="sxs-lookup"><span data-stu-id="bfb4e-108">After you cancel it, you can reset the batch job by setting it to a **Waiting** status.</span></span> <span data-ttu-id="bfb4e-109">سيتم بعد ذلك انتقاؤها مرة أخرى للتنفيذ في تشغيل الدُفعة المجدولة التالي.</span><span class="sxs-lookup"><span data-stu-id="bfb4e-109">It will then be picked up again for execution in the next scheduled batch run.</span></span>

1. <span data-ttu-id="bfb4e-110">في مساحة عمل **إدارة النظام**، حدد صفحة **الارتباطات**، وحدد **وظائف الدفعات**.</span><span class="sxs-lookup"><span data-stu-id="bfb4e-110">In the **System administration** workspace, select the **Links** page, and select **Batch jobs**.</span></span>

2. <span data-ttu-id="bfb4e-111">في صفحة قائمة **وظيفة الدفعة**، حدد الوظيفة التي تحتاج إلى إعادة التعيين.</span><span class="sxs-lookup"><span data-stu-id="bfb4e-111">On the **Batch job** list page, select the job that needs to be reset.</span></span>

3. <span data-ttu-id="bfb4e-112">على شريط الاجراء، حدد **فرض الإلغاء**، وقم بتأكيد الإجراء.</span><span class="sxs-lookup"><span data-stu-id="bfb4e-112">On the action ribbon, select **Force cancel**, and confirm the action.</span></span>

   > [!NOTE]
   > <span data-ttu-id="bfb4e-113">يتوفر إجراء **فرض الإلغاء** فقط عندما تكون حالة وظيفة الدفعة المحددة هي إما **قيد التنفيذ** أو **قيد الإلغاء**، ولا يتم تشغيل عمليات تنفيذ الدفعة أو إلغائها للوظيفة.</span><span class="sxs-lookup"><span data-stu-id="bfb4e-113">The **Force cancel** action is only available when the selected batch job has a status of either **Executing** or **Canceling**, and no batch execution or cancellation processes are running for the job.</span></span>

4. <span data-ttu-id="bfb4e-114">على شريط الإجراء، حدد **تغيير الحالة**.</span><span class="sxs-lookup"><span data-stu-id="bfb4e-114">On the action ribbon, select **Change status**.</span></span>

5. <span data-ttu-id="bfb4e-115">في صفحة **تحديد الحالة الجديدة**، حدد **قيد الانتظار**، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bfb4e-115">On the **Select new status** page, select **Waiting**, and then select **OK**.</span></span>

   ![تحديد حالة وظيفة دفعة جديدة](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a><span data-ttu-id="bfb4e-117">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="bfb4e-117">See also</span></span>

[<span data-ttu-id="bfb4e-118">تحسين الأداء عن طريق جدولة الوظائف الدُفعية بعد الساعات</span><span class="sxs-lookup"><span data-stu-id="bfb4e-118">Optimize performance by scheduling batch jobs after hours</span></span>](hr-admin-troubleshooting-batch-jobs.md)<br>
[<span data-ttu-id="bfb4e-119">تحسين الأداء باستخدام مهام التنظيف التلقائية</span><span class="sxs-lookup"><span data-stu-id="bfb4e-119">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
