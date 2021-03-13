---
title: تكوين فترات الانتظار
description: في Microsoft Dynamics 365 Human Resources، يُنشئ أيام الانتظار حدثا رئيسيًا يُستخدم في خطط الميزات.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 07ceed65a0346912d4be012a5cec502b0f0a6149
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111260"
---
# <a name="configure-waiting-periods"></a><span data-ttu-id="da9a6-103">تكوين فترات الانتظار</span><span class="sxs-lookup"><span data-stu-id="da9a6-103">Configure waiting periods</span></span>

<span data-ttu-id="da9a6-104">في Microsoft Dynamics 365 Human Resources، يُنشئ أيام الانتظار حدثا رئيسيًا يُستخدم في خطط الميزات.</span><span class="sxs-lookup"><span data-stu-id="da9a6-104">In Microsoft Dynamics 365 Human Resources, waiting days establish a milestone to use for benefit plans.</span></span> <span data-ttu-id="da9a6-105">على سبيل المثال، ثلاثة شهور من تاريخ التوظيف أو أول كل شهر أو ستة أشهر.</span><span class="sxs-lookup"><span data-stu-id="da9a6-105">For example, three months from hire date, the first of each month, or six months.</span></span>   

1. <span data-ttu-id="da9a6-106">في مساحة العمل **إدارة الميزات**، ضمن **إعداد**، حدد **فترات الانتظار**.</span><span class="sxs-lookup"><span data-stu-id="da9a6-106">In the **Benefits management** workspace, under **Setup**, select **Waiting periods**.</span></span>

2. <span data-ttu-id="da9a6-107">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="da9a6-107">Select **New**.</span></span>

3. <span data-ttu-id="da9a6-108">حدد قيمًا للحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="da9a6-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="da9a6-109">الحقل</span><span class="sxs-lookup"><span data-stu-id="da9a6-109">Field</span></span> | <span data-ttu-id="da9a6-110">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="da9a6-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="da9a6-111">**كود الانتظار**</span><span class="sxs-lookup"><span data-stu-id="da9a6-111">**Waiting code**</span></span> | <span data-ttu-id="da9a6-112">المعرف الفريد لفترة الانتظار.</span><span class="sxs-lookup"><span data-stu-id="da9a6-112">A unique identifier for the waiting period.</span></span> |
   | <span data-ttu-id="da9a6-113">**‏‏الوصف**</span><span class="sxs-lookup"><span data-stu-id="da9a6-113">**Description**</span></span> | <span data-ttu-id="da9a6-114">وصف فترة الانتظار.</span><span class="sxs-lookup"><span data-stu-id="da9a6-114">A description of the waiting period.</span></span> |
   | <span data-ttu-id="da9a6-115">**أسلوب الانتظار**</span><span class="sxs-lookup"><span data-stu-id="da9a6-115">**Waiting method**</span></span> | <span data-ttu-id="da9a6-116">حدد طريقة الانتظار المناسبة من قائمة القيم المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="da9a6-116">Select the appropriate waiting method from the drop-down list of values.</span></span> <span data-ttu-id="da9a6-117">الخيارات هي الصافي والشهر الحالي والربع الحالي والسنة الحالية والأسبوع الحالي.</span><span class="sxs-lookup"><span data-stu-id="da9a6-117">Options are Net, Current month, Current quarter, Current year, and Current week.</span></span> |
   | <span data-ttu-id="da9a6-118">**الأشهر**</span><span class="sxs-lookup"><span data-stu-id="da9a6-118">**Months**</span></span> | <span data-ttu-id="da9a6-119">أدخل عدد الأشهر لتتم إضافتها إلى أسلوب الانتظار لحساب تاريخ الانتظار.</span><span class="sxs-lookup"><span data-stu-id="da9a6-119">Enter the number of months to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="da9a6-120">**الأيام**</span><span class="sxs-lookup"><span data-stu-id="da9a6-120">**Days**</span></span> | <span data-ttu-id="da9a6-121">أدخل عدد الأيام لتتم إضافتها إلى أسلوب الانتظار لحساب تاريخ الانتظار.</span><span class="sxs-lookup"><span data-stu-id="da9a6-121">Enter the number of days to add to the waiting method to calculate the waiting date.</span></span> |
   | <span data-ttu-id="da9a6-122">**يوم الانتظار**</span><span class="sxs-lookup"><span data-stu-id="da9a6-122">**Waiting day**</span></span> | <span data-ttu-id="da9a6-123">حدد يوم الانتظار لاستخدامه لحساب تاريخ الانتظار.</span><span class="sxs-lookup"><span data-stu-id="da9a6-123">Select the waiting day to use to calculate the waiting date.</span></span> |

4. <span data-ttu-id="da9a6-124">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="da9a6-124">Select **Save**.</span></span>
