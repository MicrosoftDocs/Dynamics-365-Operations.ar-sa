---
title: "لن يتم تحديث تقارير التحليل"
description: "يوضح هذا الموضوع ما يجب عليك القيام به إذا لم تظهر التغييرات في بيانات العميل في أيًا من مساحات العمل الخاصة بالعميل."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.contentlocale: ar-sa
ms.lasthandoff: 12/04/2018

---

# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="78511-103">لن يتم تحديث تقارير التحليل</span><span class="sxs-lookup"><span data-stu-id="78511-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="78511-104">**المشكلة**</span><span class="sxs-lookup"><span data-stu-id="78511-104">**Issue**</span></span>

<span data-ttu-id="78511-105">لا تظهر التغييرات في بيانات العميل على علامات تبويب **التحليلات** الخاصة بأيًا من مساحات عمل العميل.</span><span class="sxs-lookup"><span data-stu-id="78511-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="78511-106">**السبب**</span><span class="sxs-lookup"><span data-stu-id="78511-106">**Cause**</span></span>

<span data-ttu-id="78511-107">بشكل افتراضي، يتم تحديث تقارير Microsoft Power BI كل أربع ساعات، وفقًا لجدول الوظيفة الدفعية لقياس النشر.</span><span class="sxs-lookup"><span data-stu-id="78511-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="78511-108">**‏‏الدقة**</span><span class="sxs-lookup"><span data-stu-id="78511-108">**Resolution**</span></span>

<span data-ttu-id="78511-109">وقد تكون هذه المشكلة مُجرد مسألة توقيت فقط.</span><span class="sxs-lookup"><span data-stu-id="78511-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="78511-110">اتبع هذه الخطوات لبدء الوظيفة الدفعية وتحديث مساحات عمل التحليلات.</span><span class="sxs-lookup"><span data-stu-id="78511-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="78511-111">افتح صفحة **الوظائف الدفعية** في **إدارة النظام \>الارتباطات \>الوظائف الدفعية \>الوظائف الدفعية**.</span><span class="sxs-lookup"><span data-stu-id="78511-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="78511-112">بدلاً من ذلك، استخدم بحث، ثم أدخل **الوظائف الدفعية**.</span><span class="sxs-lookup"><span data-stu-id="78511-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="78511-113">ابحث عن وظيفة**توزيع القياس** في القائمة.</span><span class="sxs-lookup"><span data-stu-id="78511-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="78511-114">حدد **تحرير** في أعلى الصفحة، ثم قم بتعيين وقت/تاريخ البدء المجدول للقيمة التي سوف تقوم بتحديث التحليلات لوقت أقرب إلى الوقت الحالي.</span><span class="sxs-lookup"><span data-stu-id="78511-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![الوظائف الدفعية](media/batch-jobs.png)

