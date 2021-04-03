---
title: استكشاف أخطاء التصنيع التحويلي‬ وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع التصنيع التحويلي.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 71ff5eeb2065a67281393777937d50237ab78d5e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5259712"
---
# <a name="troubleshoot-process-manufacturing"></a><span data-ttu-id="22c3d-103">استكشاف أخطاء التصنيع التحويلي‬ وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="22c3d-103">Troubleshoot process manufacturing</span></span>

<span data-ttu-id="22c3d-104">يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع التصنيع التحويلي.</span><span class="sxs-lookup"><span data-stu-id="22c3d-104">This topic describes how to fix issues that you might encounter while you work with process manufacturing.</span></span>

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a><span data-ttu-id="22c3d-105">عند استخدام جهاز بطاقة الوظيفة للإبلاغ عن الكمية الجزئية في الوظيفة الاخيره في أمر إنتاج ، يتم تلقائيا إنهاء كافة الوظائف السابقة في ذلك الأمر بالحالة قيد التقدم.</span><span class="sxs-lookup"><span data-stu-id="22c3d-105">When I use the job card device to report a partial quantity on the last job in a production order, all the previous jobs on that order that have a status of In progress are automatically ended.</span></span>

<span data-ttu-id="22c3d-106">يتم هذا السلوك بسبب التصميم.</span><span class="sxs-lookup"><span data-stu-id="22c3d-106">This behavior is by design.</span></span> <span data-ttu-id="22c3d-107">في الصفحة **الإعدادات الافتراضية لأوامر الإنتاج**، في علامة التبويب **الإبلاغ كمنته**، يوجد خيار يسمي **المسار بعلامة النهاية**.</span><span class="sxs-lookup"><span data-stu-id="22c3d-107">On the **Production order defaults** page, on the **Report as finished** tab, there is an option that is named **End-mark route**.</span></span> <span data-ttu-id="22c3d-108">في حاله تعيين هذا الموضوع علي *نعم*، يتم ترحيل دفتر يوميه بطاقة المسار عند استخدام العامل لجهاز بطاقة الوظيفة أو الوحدة الطرفية لبطاقة الوظيفة للإبلاغ عن العملية الاخيره.</span><span class="sxs-lookup"><span data-stu-id="22c3d-108">If this topic is set to *Yes*, a route card journal is posted when a worker uses the job card device or job card terminal to report the last operation.</span></span> <span data-ttu-id="22c3d-109">يقوم دفتر اليومية هذا بتمييز كافة العمليات كمكتملة وإنهاء كافة وظائف الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="22c3d-109">This journal marks all the operations as completed and ends all the production jobs.</span></span> <span data-ttu-id="22c3d-110">عند تعيين خيار **وضع علامة نهاية علي المسار** إلى القيمة *نعم*، لا يقوم النظام بمراعاه حاله المهمة التي قام العامل بتحديدها عند الإبلاغ عن آخر عمليه.</span><span class="sxs-lookup"><span data-stu-id="22c3d-110">When the **End-mark route** option is set to *Yes*, the system doesn't consider the job status that the worker selected when they reported the last operation.</span></span> <span data-ttu-id="22c3d-111">لا يقوم النظام أيضا بمراعاه ما إذا كان العامل يقوم بالإبلاغ عن الكمية الكاملة أو الجزئية.</span><span class="sxs-lookup"><span data-stu-id="22c3d-111">The system also doesn't consider whether the worker is reporting a full or partial quantity.</span></span>

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a><span data-ttu-id="22c3d-112">عند محاولة اجراء إغلاق سهم ، أتلقى رسالة التحذير التالية: "عدم تنفيذ حساب تحديد تكاليف التنفيذ الحديث بالتاريخ %1 الذي تم فيه تسجيل نهاية الفترة."</span><span class="sxs-lookup"><span data-stu-id="22c3d-112">When I attempt a stock closing, I receive the following warning message: "No execution of Backflush costing calculation with a date %1 matching period end has been registered."</span></span>

<span data-ttu-id="22c3d-113">في الإصدارات قبل إصدار 10.0.13 ، إذا كنت لا تستخدم تدفق تكلفه الإنتاج lean ، ستتلقى رسالة التحذير التالية اثناء اقفال المخزون:</span><span class="sxs-lookup"><span data-stu-id="22c3d-113">In releases before release 10.0.13, if you aren't using the lean production costing flow, you receive the following erroneous warning message during inventory closing:</span></span>

> <span data-ttu-id="22c3d-114">أنت علي وشك تنفيذ إغلاق المخزون بتاريخ %1.</span><span class="sxs-lookup"><span data-stu-id="22c3d-114">You are about to execute an Inventory close with a date %1.</span></span> <span data-ttu-id="22c3d-115">لا يوجد تنفيذ لحساب تكاليف الإصدار التلقائي %1 الذي تم تسجيل نهاية الفترة المطابقة.</span><span class="sxs-lookup"><span data-stu-id="22c3d-115">No execution of Backflush costing calculation with a date %1 matching period end has been registered.</span></span> <span data-ttu-id="22c3d-116">لا تنس تنفيذ حساب تكاليف الإصدار التلقائي بتاريخ %1 التي تطابق نهاية الفترة.</span><span class="sxs-lookup"><span data-stu-id="22c3d-116">Please remember to execute a Backflush costing calculation with a date of %1 matching period end.</span></span> <span data-ttu-id="22c3d-117">قد لا تكون تقييم المخزونات وتكلفه البضائع المبيعة والنسب التي تم بيعها بالأستاذ الفرعي أو دفتر الأستاذ العام حتى يتم تنفيذ ذلك.</span><span class="sxs-lookup"><span data-stu-id="22c3d-117">The valuation of inventories, cost of goods sold and variances might not be correct in Subledger or General ledger until this has been executed.</span></span>

<span data-ttu-id="22c3d-118">تم إصلاح هذه المشكلة في 10.0.13 الطرح والإصدارات الأحدث.</span><span class="sxs-lookup"><span data-stu-id="22c3d-118">This issue has been fixed in release 10.0.13 and later.</span></span> <span data-ttu-id="22c3d-119">للحصول على مزيد من المعلومات، راجع [قاعدة المعارف 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span><span class="sxs-lookup"><span data-stu-id="22c3d-119">For more information, see [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]