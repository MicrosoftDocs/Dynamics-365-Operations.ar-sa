---
title: استكشاف أخطاء التقارير التحليلية وإصلاحها
description: يوضح هذا المقال ما يجب عليك القيام به إذا لم تظهر التغييرات في بيانات العميل في أيًا من مساحات العمل الخاصة بالعميل.
author: andreabichsel
ms.date: 02/03/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b500d519d61edfd20456355376e3fc81f16517a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794963"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="24925-103">استكشاف أخطاء التقارير التحليلية وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="24925-103">Troubleshoot analytic reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="24925-104">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="24925-104">**Issue**</span></span>

<span data-ttu-id="24925-105">لا تظهر التغييرات في بيانات العميل على علامات تبويب **التحليلات** الخاصة بأيًا من مساحات عمل العميل.</span><span class="sxs-lookup"><span data-stu-id="24925-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="24925-106">**السبب**</span><span class="sxs-lookup"><span data-stu-id="24925-106">**Cause**</span></span>

<span data-ttu-id="24925-107">بشكل افتراضي، يتم تحديث تقارير Microsoft Power BI كل أربع ساعات، وفقًا لجدول الوظيفة الدفعية لقياس النشر.</span><span class="sxs-lookup"><span data-stu-id="24925-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="24925-108">**‏‏الدقة**</span><span class="sxs-lookup"><span data-stu-id="24925-108">**Resolution**</span></span>

<span data-ttu-id="24925-109">وقد تكون هذه المشكلة مُجرد مسألة توقيت فقط.</span><span class="sxs-lookup"><span data-stu-id="24925-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="24925-110">اتبع هذه الخطوات لبدء الوظيفة الدفعية وتحديث مساحات عمل التحليلات.</span><span class="sxs-lookup"><span data-stu-id="24925-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="24925-111">افتح صفحة **الوظائف الدفعية** في **إدارة النظام \>الارتباطات \>الوظائف الدفعية \>الوظائف الدفعية**.</span><span class="sxs-lookup"><span data-stu-id="24925-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="24925-112">بدلاً من ذلك، استخدم بحث، ثم أدخل **الوظائف الدفعية**.</span><span class="sxs-lookup"><span data-stu-id="24925-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="24925-113">ابحث عن وظيفة **توزيع القياس** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="24925-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="24925-114">حدد **تحرير** في أعلى الصفحة، ثم قم بتعيين وقت/تاريخ البدء المجدول للقيمة التي سوف تقوم بتحديث التحليلات لوقت أقرب إلى الوقت الحالي.</span><span class="sxs-lookup"><span data-stu-id="24925-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![الوظائف الدفعية](media/batch-jobs.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]