--- 
title: "إعداد هيئات ضريبة المبيعات"
description: "إن هيئات ضريبة المبيعات‬ هي كيانات حيث يجب الإبلاغ عن ضريبة المبيعات المحصلة ودفعها."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f75ee28343161026a73dd889b345d65ecc345884
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-sales-tax-authorities"></a><span data-ttu-id="241fb-103">إعداد هيئات ضريبة المبيعات</span><span class="sxs-lookup"><span data-stu-id="241fb-103">Set up sales tax authorities</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="241fb-104">إن هيئات ضريبة المبيعات‬ هي كيانات حيث يجب الإبلاغ عن ضريبة المبيعات المحصلة ودفعها.</span><span class="sxs-lookup"><span data-stu-id="241fb-104">Sales tax authorities are entities to which collected sales tax needs to be reported and paid.</span></span> <span data-ttu-id="241fb-105">يمكنك دفع ضرائب المبيعات للهيئة مباشرة أو من خلال حساب مورّد تقوم بإنشائه لهيئة ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="241fb-105">You can pay sales taxes to the authority directly or through a vendor account that you create for the sales tax authority.</span></span> <span data-ttu-id="241fb-106">إذا قمت بذلك، فيمكن للشركة استخدام طرق الدفع المعتادة الخاصة بها للدفع إلى هيئة ضريبة المبيعات في الوقت المناسب.</span><span class="sxs-lookup"><span data-stu-id="241fb-106">If you do this, the company can use its usual payment routines to pay the sales tax authority on time.</span></span> <span data-ttu-id="241fb-107">إذا لم تقم بإعداد هيئة الضرائب كمورّد، فيجب على الشخص الدفع يدويًا لهيئة الضرائب في تاريخ الاستحقاق المناسب.</span><span class="sxs-lookup"><span data-stu-id="241fb-107">If you do not set up the tax authority as a vendor, someone must prepare a manual payment to the tax authority on the appropriate due date.</span></span> <span data-ttu-id="241fb-108">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="241fb-108">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="241fb-109">انتقل إلى الضريبة > الضرائب غير المباشرة > ضريبة المبيعات > هيئات ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="241fb-109">Go to Tax > Indirect taxes > Sales tax > Sales tax authorities.</span></span>
2. <span data-ttu-id="241fb-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="241fb-110">Click New.</span></span>
3. <span data-ttu-id="241fb-111">في الحقل "الهيئة‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="241fb-111">In the Authority field, type a value.</span></span>
4. <span data-ttu-id="241fb-112">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="241fb-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="241fb-113">في الحقل "حساب المورّد‬"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="241fb-113">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="241fb-114">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="241fb-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="241fb-115">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="241fb-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="241fb-116">حدد تخطيط التقرير للبلد/المنطقة حيث تتواجد، إذا كان متوفرًا.</span><span class="sxs-lookup"><span data-stu-id="241fb-116">Select the report layout for your country/region, if one is available.</span></span> <span data-ttu-id="241fb-117">إذا لم تتطابق تخطيطات التقارير مع متطلبات هيئة ضريبة المبيعات، فاستخدم التخطيط الافتراضي.</span><span class="sxs-lookup"><span data-stu-id="241fb-117">If the report layouts do not correspond to the requirements of the sales tax authority, use default layout.</span></span>
9. <span data-ttu-id="241fb-118">أدخل القيم في نموذج التقريب وحقول التقريب لتحديد كيف ينبغي تقريب المبلغ الإجمالي للضرائب المقرر دفعه.</span><span class="sxs-lookup"><span data-stu-id="241fb-118">Enter values in the Rounding form and the Round-off fields to specify how the tax total amount to be paid should be rounded.</span></span> <span data-ttu-id="241fb-119">سيتم ترحيل فروق التقريب إلى حسابات الحركات التلقائية‬ التي تم إعدادها في دفتر الأستاذ العام.</span><span class="sxs-lookup"><span data-stu-id="241fb-119">Any rounding differences will be posted to Accounts for automatic transactions set up in General ledger.</span></span>
10. <span data-ttu-id="241fb-120">في حقل "تقريب العلامات العشرية‬"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="241fb-120">In the Round-off field, enter a number.</span></span>
11. <span data-ttu-id="241fb-121">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="241fb-121">Click Save.</span></span>


