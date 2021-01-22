---
title: إعداد شيكات بتاريخ لاحق
description: يشرح هذا المقال كيفية تحديد ما إذا كان سيتم ترحيل إدخالات دفتر اليومية للشيكات ودفاتر يومية الترحيل أي لاستخدام مسح إدخالات ومدفوعات الموردين.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22e67aa051b5ea8267df7efac40e007d0f11a83d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141098"
---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="3f179-103">إعداد شيكات بتاريخ لاحق</span><span class="sxs-lookup"><span data-stu-id="3f179-103">Set up postdated checks</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f179-104">يشرح هذا المقال كيفية تحديد ما إذا كان سيتم ترحيل إدخالات دفتر اليومية للشيكات ودفاتر يومية الترحيل أي لاستخدام مسح إدخالات ومدفوعات الموردين.</span><span class="sxs-lookup"><span data-stu-id="3f179-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="3f179-105">يمكنك أيضا تحديد حسابات مقاصة للشيكات الصادرة والشيكات المستلمة وضريبة الخصم.</span><span class="sxs-lookup"><span data-stu-id="3f179-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="3f179-106">يتم إصدار الشيكات التي يتم تأخير تواريخها لإجراء مدفوعات واستلامها في تاريخ محدد في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="3f179-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="3f179-107">يمكنك تحديد ما إذا كان يجب ظهور الشيك في دفاتر المحاسبة قبل تاريخ استحقاقه أم لا.</span><span class="sxs-lookup"><span data-stu-id="3f179-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="3f179-108">ويتمثل دور هذا الإجراء في أمين الخزانة.</span><span class="sxs-lookup"><span data-stu-id="3f179-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="3f179-109">يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="3f179-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="3f179-110">إعداد شيكات بتاريخ لاحق</span><span class="sxs-lookup"><span data-stu-id="3f179-110">Set up postdated checks</span></span>
1. <span data-ttu-id="3f179-111">انتقل إلى إدارة النقد والبنك > الإعداد > معلمات إدارة النقد والبنوك.</span><span class="sxs-lookup"><span data-stu-id="3f179-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="3f179-112">انقر فوق علامة التبويب "الشيكات التي تم تأخير تواريخها".</span><span class="sxs-lookup"><span data-stu-id="3f179-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="3f179-113">حدد خانة الاختيار "تمكين الشيكات التي تم تأخير تواريخها" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="3f179-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="3f179-114">حدد خانة اختيار "ترحيل إدخالات دفتر اليومية للشيكات التي تم تأخير تواريخها" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="3f179-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="3f179-115">في الحقل "تسوية الحساب للشيكات الصادرة"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="3f179-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="3f179-116">في الحقل "تسوية الحساب للشيكات المستلمة"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="3f179-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="3f179-117">في الحقل "دفتر اليومية العام لإدخالات التسوية"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3f179-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="3f179-118">في الحقل "تحويل الشيكات التي تم تأخير تواريخها إلى دفتر يومية الدفع الخاص بهذا المورد"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3f179-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="3f179-119">في الحقل "حساب تسوية ضرائب الخصم"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="3f179-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="3f179-120">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="3f179-120">Click Save.</span></span>
11. <span data-ttu-id="3f179-121">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3f179-121">Close the page.</span></span>
12. <span data-ttu-id="3f179-122">انتقل إلى الحسابات المدينة > إعداد الدفع‬ > طرق الدفع.</span><span class="sxs-lookup"><span data-stu-id="3f179-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="3f179-123">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="3f179-123">Click New.</span></span>
14. <span data-ttu-id="3f179-124">في الحقل "طريقة الدفع"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="3f179-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="3f179-125">حدد الخيار "ترحيل تسوية الشيكات التي تم تأخير تواريخها" للإشارة إلى أن مبلغ الشيك سيتم ترحيله إلى حساب مقاصة".</span><span class="sxs-lookup"><span data-stu-id="3f179-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="3f179-126">في الحقل "نوع الحساب"، اكتب "البنك‬".</span><span class="sxs-lookup"><span data-stu-id="3f179-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="3f179-127">سيكون الحساب المقابل لطريقة الدفع بنكًا.</span><span class="sxs-lookup"><span data-stu-id="3f179-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="3f179-128">في الحقل "حساب الدفع"، حدد القيم المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="3f179-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="3f179-129">حدد الحساب البنكي المستخدم لخصم مبلغ الفاتورة.</span><span class="sxs-lookup"><span data-stu-id="3f179-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="3f179-130">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="3f179-130">Click Save.</span></span>
19. <span data-ttu-id="3f179-131">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="3f179-131">Close the page.</span></span>
