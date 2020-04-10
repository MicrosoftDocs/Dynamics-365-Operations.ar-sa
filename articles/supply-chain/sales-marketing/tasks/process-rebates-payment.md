---
title: معالجة الخصومات للدفع
description: يوضح هذا الإجراء كيفية تحويل خصومات العميل المعتمدة التي تمت معالجتها لإشعارات دائنة.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 412e7df299a419642018a62e6e8febd5d59c65e1
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148426"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="b5f66-103">معالجة الخصومات للدفع</span><span class="sxs-lookup"><span data-stu-id="b5f66-103">Process rebates for payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5f66-104">يوضح هذا الإجراء كيفية تحويل خصومات العميل المعتمدة التي تمت معالجتها لإشعارات دائنة.</span><span class="sxs-lookup"><span data-stu-id="b5f66-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="b5f66-105">يمكن استخدام هذا الدليل في شركة العرض التقديمي USMF.</span><span class="sxs-lookup"><span data-stu-id="b5f66-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="b5f66-106">الشرط المسبق لهذا الدليل هو وجود مطالبة واحدة أو أكثر من مطالبات الخصم في حالة"تمييز".</span><span class="sxs-lookup"><span data-stu-id="b5f66-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="b5f66-107">إذا كنت تستخدم USMF، يجب عليك تشغيل الدليل "إنشاء خصومات العميل ومعالجتها" قبل تشغيل في هذا الدليل.</span><span class="sxs-lookup"><span data-stu-id="b5f66-107">If you're using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="b5f66-108">تحويل مطالبات الخصم لإشعار دائن</span><span class="sxs-lookup"><span data-stu-id="b5f66-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="b5f66-109">انتقل إلى "جميع العملاء".</span><span class="sxs-lookup"><span data-stu-id="b5f66-109">Go to All customers.</span></span>
2. <span data-ttu-id="b5f66-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="b5f66-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b5f66-111">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="b5f66-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b5f66-112">في جزء الإجراءات، انقر فوق "تحصيل".</span><span class="sxs-lookup"><span data-stu-id="b5f66-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="b5f66-113">انقر فوق "تسوية الحركات".</span><span class="sxs-lookup"><span data-stu-id="b5f66-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="b5f66-114">انقر فوق "الوظائف".</span><span class="sxs-lookup"><span data-stu-id="b5f66-114">Click Functions.</span></span>
7. <span data-ttu-id="b5f66-115">انقر فوق "برنامج الخصم".</span><span class="sxs-lookup"><span data-stu-id="b5f66-115">Click Rebate program.</span></span>
    * <span data-ttu-id="b5f66-116">تسرد صفحة الخصومات قائمة بمطالبات الخصم التي قمت بمعالجتها في منضدة عمل خصم العميل والتي تكون في حالة "التمييز".</span><span class="sxs-lookup"><span data-stu-id="b5f66-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="b5f66-117">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="b5f66-117">Click Edit.</span></span>
    * <span data-ttu-id="b5f66-118">قم بتعيين علامات الاختيار الموجودة في الحقل "تمييز" للمطالبات التي تريد تضمينها في إشعار الدائن.</span><span class="sxs-lookup"><span data-stu-id="b5f66-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="b5f66-119">انقر فوق "الوظائف".</span><span class="sxs-lookup"><span data-stu-id="b5f66-119">Click Functions.</span></span>
10. <span data-ttu-id="b5f66-120">انقر فوق "إنشاء إشعار دائن".</span><span class="sxs-lookup"><span data-stu-id="b5f66-120">Click Create credit note.</span></span>
    * <span data-ttu-id="b5f66-121">تظهر رسالة لإعلامك بأنه قد تم ترحيل دفتر يومية (هذا هو دفتر يومية استهلاك الحسابات المدينة، كما هو محدد في صفحة معلمات الحسابات المدينة).</span><span class="sxs-lookup"><span data-stu-id="b5f66-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="b5f66-122">يؤدي هذا لنقل مبلغ الالتزام الحقيقي (المبلغ الدائن) إلى رصيد العميل.</span><span class="sxs-lookup"><span data-stu-id="b5f66-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="b5f66-123">ويعني هذا أنه تمت إضافة حساب العميل وخصم حساب استحقاق الخصم.</span><span class="sxs-lookup"><span data-stu-id="b5f66-123">This means that the customer's account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="b5f66-124">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b5f66-124">Close the page.</span></span>
12. <span data-ttu-id="b5f66-125">انقر فوق "إلغاء".</span><span class="sxs-lookup"><span data-stu-id="b5f66-125">Click Cancel.</span></span>
    * <span data-ttu-id="b5f66-126">يؤدي هذا لتحديث الصفحة بحيث يمكنك أن ترى التحديثات.</span><span class="sxs-lookup"><span data-stu-id="b5f66-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="b5f66-127">في جزء الإجراءات، انقر فوق "تحصيل".</span><span class="sxs-lookup"><span data-stu-id="b5f66-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="b5f66-128">انقر فوق "تسوية الحركات".</span><span class="sxs-lookup"><span data-stu-id="b5f66-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="b5f66-129">لاحظ أنه تمت إضافة حركة لمبلغ سالب لرصيد العميل، تمثل إجمالي مبلغ الخصم، دون مرجع فاتورة.</span><span class="sxs-lookup"><span data-stu-id="b5f66-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="b5f66-130">انقر فوق "إلغاء".</span><span class="sxs-lookup"><span data-stu-id="b5f66-130">Click Cancel.</span></span>

