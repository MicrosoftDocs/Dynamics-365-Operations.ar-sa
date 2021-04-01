---
title: إيداع مدفوعات العميل
description: إيداع مدفوعات العميل.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7357683e46df04c3dedd7e22607748512c9de94a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220241"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="02bab-103">إيداع مدفوعات العميل</span><span class="sxs-lookup"><span data-stu-id="02bab-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02bab-104">إيداع مدفوعات العميل.</span><span class="sxs-lookup"><span data-stu-id="02bab-104">Deposit customer payments.</span></span> <span data-ttu-id="02bab-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="02bab-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="02bab-106">انتقل إلى **جزء التنقل > الوحدات النمطية > الحسابات المدينة > المدفوعات > دفتر يومية المدفوعات‬**.</span><span class="sxs-lookup"><span data-stu-id="02bab-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="02bab-107">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="02bab-107">Select **New**.</span></span>
3. <span data-ttu-id="02bab-108">في حقل **الاسم**، حدد‏‎ **CustPay** في القائمة المنسدلة</span><span class="sxs-lookup"><span data-stu-id="02bab-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="02bab-109">حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="02bab-109">Select **Lines**.</span></span>
5. <span data-ttu-id="02bab-110">في الحقل **الحساب**، حدد العميل الذي تقوم بتسجيل الدفعة له.</span><span class="sxs-lookup"><span data-stu-id="02bab-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="02bab-111">في الحقل **الدائن**، أدخل مبلغ الدفع.</span><span class="sxs-lookup"><span data-stu-id="02bab-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="02bab-112">يمكنك اختيار ترك المبلغ فارغًا والسماح للنظام بحسابه عن طريق تحديد الفواتير التي تم دفعها.</span><span class="sxs-lookup"><span data-stu-id="02bab-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="02bab-113">في حقل **مرجع الدفع**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="02bab-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="02bab-114">قد يكون مرجع الدفع رقم الشيك للدفعة التي تقوم بإدخاله.</span><span class="sxs-lookup"><span data-stu-id="02bab-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="02bab-115">يكون مرجع الدفع مطلوبًا لتضمين الدفعة في إيصال إيداع.</span><span class="sxs-lookup"><span data-stu-id="02bab-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="02bab-116">ضع علامة على المربع "استخدام إيصال إيداع‬".</span><span class="sxs-lookup"><span data-stu-id="02bab-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="02bab-117">إذا كان يجب تضمين الدفع في الإيداع فيمكنك تغيير هذا الإعداد إلى "نعم".</span><span class="sxs-lookup"><span data-stu-id="02bab-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="02bab-118">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="02bab-118">Select **New**.</span></span>
10. <span data-ttu-id="02bab-119">في الحقل **الحساب**، حدد العميل للدفعة التالية.</span><span class="sxs-lookup"><span data-stu-id="02bab-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="02bab-120">في الحقل **الدائن**، أدخل مبلغ الدفع.</span><span class="sxs-lookup"><span data-stu-id="02bab-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="02bab-121">في حقل **مرجع الدفع**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="02bab-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="02bab-122">ضع علامة على المربع **استخدام إيصال إيداع‬**.</span><span class="sxs-lookup"><span data-stu-id="02bab-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="02bab-123">حدد **ترحيل**.</span><span class="sxs-lookup"><span data-stu-id="02bab-123">Select **Post**.</span></span> <span data-ttu-id="02bab-124">يجب ترحيل المدفوعات قبل التمكن من إنشاء إيصال الإيداع.</span><span class="sxs-lookup"><span data-stu-id="02bab-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="02bab-125">وهذا للتأكد من أن المدفوعات لا تتغير بعد إنشاء إيصال الإيداع.</span><span class="sxs-lookup"><span data-stu-id="02bab-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="02bab-126">حدد **الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="02bab-126">Select **Functions**.</span></span>
16. <span data-ttu-id="02bab-127">حدد **إيصال الإيداع**.</span><span class="sxs-lookup"><span data-stu-id="02bab-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="02bab-128">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="02bab-128">Select **OK**.</span></span> <span data-ttu-id="02bab-129">يتم استخدام الصفحة الأولى لإنشاء إيصال الإيداع.</span><span class="sxs-lookup"><span data-stu-id="02bab-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="02bab-130">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="02bab-130">Select **OK**.</span></span> <span data-ttu-id="02bab-131">تتعلق الخطوة الثانية بطباعة إيصال الإيداع، ولكن هذه الخطوة غير مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="02bab-131">The second step is to print the deposit slip, but this step is not required.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]