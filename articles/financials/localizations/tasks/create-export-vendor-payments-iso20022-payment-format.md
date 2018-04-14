--- 
title: "إنشاء وتصدير دفعات المورّد باستخدام تنسيق الدفع ISO20022"
description: "يوضح هذا الإجراء كيفية إنشاء بنود الدفع في دفتر يومية دفع المورّد وإنشاء ملف دفع المورّد باستخدام مثال تحوي الائتمان ISO2022."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5787edc4a041e4b571c7ab6f056f4bd0a17cf2d7
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="a657d-103">إنشاء وتصدير دفعات المورّد باستخدام تنسيق الدفع ISO20022</span><span class="sxs-lookup"><span data-stu-id="a657d-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a657d-104">يوضح هذا الإجراء كيفية إنشاء بنود الدفع في دفتر يومية دفع المورّد وإنشاء ملف دفع المورّد باستخدام مثال تحوي الائتمان ISO2022.</span><span class="sxs-lookup"><span data-stu-id="a657d-104">This procedure shows how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span> 

<span data-ttu-id="a657d-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي DEMF.</span><span class="sxs-lookup"><span data-stu-id="a657d-105">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="a657d-106">هذا هو الإجراء الخامس من ضمن الإجراءات الخمسة، هدفه توضيح عملية معالجة مدفوعات المورّد باستخدام تكوينات التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a657d-106">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="a657d-107">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="a657d-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-payment-lines"></a><span data-ttu-id="a657d-108">إنشاء بنود الدفع</span><span class="sxs-lookup"><span data-stu-id="a657d-108">Create payment lines</span></span>
1. <span data-ttu-id="a657d-109">انتقل إلى الحسابات الدائنة > المدفوعات‬ > دفتر يومية المدفوعات‬‬.</span><span class="sxs-lookup"><span data-stu-id="a657d-109">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="a657d-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="a657d-110">Click New.</span></span>
3. <span data-ttu-id="a657d-111">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="a657d-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a657d-112">في الحقل "الاسم"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a657d-112">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="a657d-113">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="a657d-113">Click Lines.</span></span>
6. <span data-ttu-id="a657d-114">انقر فوق "مقترح الدفع".</span><span class="sxs-lookup"><span data-stu-id="a657d-114">Click Payment proposal.</span></span>
7. <span data-ttu-id="a657d-115">انقر فوق "إنشاء مقترح دفع".</span><span class="sxs-lookup"><span data-stu-id="a657d-115">Click Create payment proposal.</span></span>
8. <span data-ttu-id="a657d-116">وسّع المقطع "السجلات المطلوب تضمينها‬".</span><span class="sxs-lookup"><span data-stu-id="a657d-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="a657d-117">انقر فوق "عامل التصفية".</span><span class="sxs-lookup"><span data-stu-id="a657d-117">Click Filter.</span></span>
10. <span data-ttu-id="a657d-118">في القائمة، حدد الصف الخاص بجدول "المورّدون" وحقل "حساب المورّد".</span><span class="sxs-lookup"><span data-stu-id="a657d-118">In the list, select the row for Vendors table and Vendor account field.</span></span>
11. <span data-ttu-id="a657d-119">في الحقل "المعايير‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="a657d-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="a657d-120">يمكنك تطبيق أي معايير لتحديد حركات المورّد للدفع، لهذا لمثال استخدم DE-001 كحساب مورّد.</span><span class="sxs-lookup"><span data-stu-id="a657d-120">You can apply any criteria for selecting vendor transactions to pay, for this example use DE-001 as a vendor account.</span></span>  
12. <span data-ttu-id="a657d-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a657d-121">Click OK.</span></span>
13. <span data-ttu-id="a657d-122">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="a657d-122">Click OK.</span></span>
14. <span data-ttu-id="a657d-123">انقر فوق "إنشاء مدفوعات".</span><span class="sxs-lookup"><span data-stu-id="a657d-123">Click Create payments.</span></span>

## <a name="generate-an-iso20022-payment-file"></a><span data-ttu-id="a657d-124">إنشاء ملف دفع ISO20022</span><span class="sxs-lookup"><span data-stu-id="a657d-124">Generate an ISO20022 payment file</span></span>


