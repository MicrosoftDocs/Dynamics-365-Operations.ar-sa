---
title: معالجة الخصومات للدفع
description: يوضح هذا الإجراء كيفية تحويل خصومات العميل المعتمدة التي تمت معالجتها لإشعارات دائنة.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 617b5d99973e630cca2973227c2e54a63bd1ec4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263290"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="c486b-103">معالجة الخصومات للدفع</span><span class="sxs-lookup"><span data-stu-id="c486b-103">Process rebates for payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c486b-104">يوضح هذا الإجراء كيفية تحويل خصومات العميل المعتمدة التي تمت معالجتها لإشعارات دائنة.</span><span class="sxs-lookup"><span data-stu-id="c486b-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="c486b-105">يمكن استخدام هذا الدليل في شركة العرض التقديمي USMF.</span><span class="sxs-lookup"><span data-stu-id="c486b-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="c486b-106">الشرط المسبق لهذا الدليل هو وجود مطالبة واحدة أو أكثر من مطالبات الخصم في حالة"تمييز".</span><span class="sxs-lookup"><span data-stu-id="c486b-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="c486b-107">إذا كنت تستخدم USMF، يجب عليك تشغيل الدليل "إنشاء خصومات العميل ومعالجتها" قبل تشغيل في هذا الدليل.</span><span class="sxs-lookup"><span data-stu-id="c486b-107">If you're using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="c486b-108">تحويل مطالبات الخصم لإشعار دائن</span><span class="sxs-lookup"><span data-stu-id="c486b-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="c486b-109">انتقل إلى "جميع العملاء".</span><span class="sxs-lookup"><span data-stu-id="c486b-109">Go to All customers.</span></span>
2. <span data-ttu-id="c486b-110">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c486b-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c486b-111">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c486b-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c486b-112">في جزء الإجراءات، انقر فوق "تحصيل".</span><span class="sxs-lookup"><span data-stu-id="c486b-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="c486b-113">انقر فوق "تسوية الحركات".</span><span class="sxs-lookup"><span data-stu-id="c486b-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="c486b-114">انقر فوق "الوظائف".</span><span class="sxs-lookup"><span data-stu-id="c486b-114">Click Functions.</span></span>
7. <span data-ttu-id="c486b-115">انقر فوق "برنامج الخصم".</span><span class="sxs-lookup"><span data-stu-id="c486b-115">Click Rebate program.</span></span>
    * <span data-ttu-id="c486b-116">تسرد صفحة الخصومات قائمة بمطالبات الخصم التي قمت بمعالجتها في منضدة عمل خصم العميل والتي تكون في حالة "التمييز".</span><span class="sxs-lookup"><span data-stu-id="c486b-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="c486b-117">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="c486b-117">Click Edit.</span></span>
    * <span data-ttu-id="c486b-118">قم بتعيين علامات الاختيار الموجودة في الحقل "تمييز" للمطالبات التي تريد تضمينها في إشعار الدائن.</span><span class="sxs-lookup"><span data-stu-id="c486b-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="c486b-119">انقر فوق "الوظائف".</span><span class="sxs-lookup"><span data-stu-id="c486b-119">Click Functions.</span></span>
10. <span data-ttu-id="c486b-120">انقر فوق "إنشاء إشعار دائن".</span><span class="sxs-lookup"><span data-stu-id="c486b-120">Click Create credit note.</span></span>
    * <span data-ttu-id="c486b-121">تظهر رسالة لإعلامك بأنه قد تم ترحيل دفتر يومية (هذا هو دفتر يومية استهلاك الحسابات المدينة، كما هو محدد في صفحة معلمات الحسابات المدينة).</span><span class="sxs-lookup"><span data-stu-id="c486b-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="c486b-122">يؤدي هذا لنقل مبلغ الالتزام الحقيقي (المبلغ الدائن) إلى رصيد العميل.</span><span class="sxs-lookup"><span data-stu-id="c486b-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="c486b-123">ويعني هذا أنه تمت إضافة حساب العميل وخصم حساب استحقاق الخصم.</span><span class="sxs-lookup"><span data-stu-id="c486b-123">This means that the customer's account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="c486b-124">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c486b-124">Close the page.</span></span>
12. <span data-ttu-id="c486b-125">انقر فوق "إلغاء".</span><span class="sxs-lookup"><span data-stu-id="c486b-125">Click Cancel.</span></span>
    * <span data-ttu-id="c486b-126">يؤدي هذا لتحديث الصفحة بحيث يمكنك أن ترى التحديثات.</span><span class="sxs-lookup"><span data-stu-id="c486b-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="c486b-127">في جزء الإجراءات، انقر فوق "تحصيل".</span><span class="sxs-lookup"><span data-stu-id="c486b-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="c486b-128">انقر فوق "تسوية الحركات".</span><span class="sxs-lookup"><span data-stu-id="c486b-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="c486b-129">لاحظ أنه تمت إضافة حركة لمبلغ سالب لرصيد العميل، تمثل إجمالي مبلغ الخصم، دون مرجع فاتورة.</span><span class="sxs-lookup"><span data-stu-id="c486b-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="c486b-130">انقر فوق "إلغاء".</span><span class="sxs-lookup"><span data-stu-id="c486b-130">Click Cancel.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]