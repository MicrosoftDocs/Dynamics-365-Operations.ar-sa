---
title: استكشاف أخطاء التقارير التحليلية وإصلاحها
description: يوضح هذا المقال ما يجب عليك القيام به إذا لم تظهر التغييرات في بيانات العميل في أيًا من مساحات العمل الخاصة بالعميل.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
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
ms.openlocfilehash: c5e1a1d7044567a07acedf71e65ed244275acfd9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111340"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="680f9-103">استكشاف أخطاء التقارير التحليلية وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="680f9-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="680f9-104">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="680f9-104">**Issue**</span></span>

<span data-ttu-id="680f9-105">لا تظهر التغييرات في بيانات العميل على علامات تبويب **التحليلات** الخاصة بأيًا من مساحات عمل العميل.</span><span class="sxs-lookup"><span data-stu-id="680f9-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="680f9-106">**السبب**</span><span class="sxs-lookup"><span data-stu-id="680f9-106">**Cause**</span></span>

<span data-ttu-id="680f9-107">بشكل افتراضي، يتم تحديث تقارير Microsoft Power BI كل أربع ساعات، وفقًا لجدول الوظيفة الدفعية لقياس النشر.</span><span class="sxs-lookup"><span data-stu-id="680f9-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="680f9-108">**‏‏الدقة**</span><span class="sxs-lookup"><span data-stu-id="680f9-108">**Resolution**</span></span>

<span data-ttu-id="680f9-109">وقد تكون هذه المشكلة مُجرد مسألة توقيت فقط.</span><span class="sxs-lookup"><span data-stu-id="680f9-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="680f9-110">اتبع هذه الخطوات لبدء الوظيفة الدفعية وتحديث مساحات عمل التحليلات.</span><span class="sxs-lookup"><span data-stu-id="680f9-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="680f9-111">افتح صفحة **الوظائف الدفعية** في **إدارة النظام \>الارتباطات \>الوظائف الدفعية \>الوظائف الدفعية**.</span><span class="sxs-lookup"><span data-stu-id="680f9-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="680f9-112">بدلاً من ذلك، استخدم بحث، ثم أدخل **الوظائف الدفعية**.</span><span class="sxs-lookup"><span data-stu-id="680f9-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="680f9-113">ابحث عن وظيفة **توزيع القياس** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="680f9-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="680f9-114">حدد **تحرير** في أعلى الصفحة، ثم قم بتعيين وقت/تاريخ البدء المجدول للقيمة التي سوف تقوم بتحديث التحليلات لوقت أقرب إلى الوقت الحالي.</span><span class="sxs-lookup"><span data-stu-id="680f9-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![الوظائف الدفعية](media/batch-jobs.png)
