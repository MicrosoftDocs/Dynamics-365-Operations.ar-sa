---
title: تسجيل شيك بتاريخ لاحق لمورد وترحيله
description: يمكنك تسجيل تفاصيل شيك بتاريخ لاحق قبل أن تقوم بإصدار الشيك لمورد، وذلك باستخدام ‏‫إيصال دفتر اليومية.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5788948c40f20e686565198c84facd68a935d9c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566054"
---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="c3816-103">تسجيل شيك بتاريخ لاحق لمورد وترحيله</span><span class="sxs-lookup"><span data-stu-id="c3816-103">Register and post a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c3816-104">يمكنك تسجيل تفاصيل شيك بتاريخ لاحق قبل أن تقوم بإصدار الشيك لمورد، وذلك باستخدام ‏‫إيصال دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="c3816-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="c3816-105">ويمكنك أيضا ترحيل الشيك الذي تم تأخير تاريخه وإنشاء الحركات المالية.</span><span class="sxs-lookup"><span data-stu-id="c3816-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="c3816-106">قبل تسجيل شيك بتاريخ لاحق مستلم من العميل وترحيله، يجب إكمال المهمة التالية:</span><span class="sxs-lookup"><span data-stu-id="c3816-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="c3816-107">إعداد شيكات بتاريخ لاحق‬ في صفحة إدارة النقد والبنوك.</span><span class="sxs-lookup"><span data-stu-id="c3816-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="c3816-108">ويتمثل دور دلائل المهام هذه في أمين الخزانة.</span><span class="sxs-lookup"><span data-stu-id="c3816-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="c3816-109">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="c3816-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="c3816-110">انتقل إلى الحسابات الدائنة > المدفوعات > دفتر يومية المدفوعات‬‬</span><span class="sxs-lookup"><span data-stu-id="c3816-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="c3816-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="c3816-111">Click New.</span></span>
3. <span data-ttu-id="c3816-112">في حقل "الاسم"، اكتب "VendPay".</span><span class="sxs-lookup"><span data-stu-id="c3816-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="c3816-113">انقر فوق البنود.</span><span class="sxs-lookup"><span data-stu-id="c3816-113">Click Lines.</span></span>
5. <span data-ttu-id="c3816-114">في حقل "الحساب"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="c3816-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="c3816-115">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c3816-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="c3816-116">في الحقل "مدين"، أدخل رقمًا.</span><span class="sxs-lookup"><span data-stu-id="c3816-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="c3816-117">في الحقل "طريقة الدفع"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="c3816-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c3816-118">حدد طريقة دفع الشيك الذي تم تأخير تاريخه.</span><span class="sxs-lookup"><span data-stu-id="c3816-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="c3816-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c3816-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="c3816-120">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c3816-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="c3816-121">انقر فوق علامة التبويب "الشيكات التي تم تأخير تواريخها".</span><span class="sxs-lookup"><span data-stu-id="c3816-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="c3816-122">في الحقل "رقم الشيك"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c3816-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="c3816-123">أدخل رقم الشيك بتاريخ لاحق أو قم بتعديله.</span><span class="sxs-lookup"><span data-stu-id="c3816-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="c3816-124">في الحقل "اسم بنك الإصدار"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="c3816-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="c3816-125">أدخل تفاصيل البنك عن بنك الإصدار.</span><span class="sxs-lookup"><span data-stu-id="c3816-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="c3816-126">انقر فوق علامة التبويب "القائمة".</span><span class="sxs-lookup"><span data-stu-id="c3816-126">Click the List tab.</span></span>
15. <span data-ttu-id="c3816-127">انقر فوق "ترحيل".</span><span class="sxs-lookup"><span data-stu-id="c3816-127">Click Post.</span></span>
16. <span data-ttu-id="c3816-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c3816-128">Close the page.</span></span>
17. <span data-ttu-id="c3816-129">انقر فوق علامة التبويب "الشيكات التي تم تأخير تواريخها".</span><span class="sxs-lookup"><span data-stu-id="c3816-129">Click the Postdated checks tab.</span></span>

