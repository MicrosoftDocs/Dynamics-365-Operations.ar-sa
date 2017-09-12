--- 
title: "إعداد ملفات تعريف الترحيل والتسهيلات البنكية لخطاب الاعتماد"
description: "يوضح هذا الإجراء إنشاء تسهيلات بنك وترحيل ملف التعريف المطلوب لمعالجة خطابات الاعتماد."
author: kweekley
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
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a5c68feeb163e09f183c49afea24d2f9e5999594
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a><span data-ttu-id="5cd53-103">إعداد ملفات تعريف الترحيل والتسهيلات البنكية لخطاب الاعتماد</span><span class="sxs-lookup"><span data-stu-id="5cd53-103">Set up bank facilities and posting profiles for letter of credit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5cd53-104">يوضح هذا الإجراء إنشاء تسهيلات بنك وترحيل ملف التعريف المطلوب لمعالجة خطابات الاعتماد.</span><span class="sxs-lookup"><span data-stu-id="5cd53-104">This procedure walks through creating a Bank facility and posting profile required to process Letters of credit.</span></span> 

<span data-ttu-id="5cd53-105">تستخدم هذه المهمة شركة العرض التجريبي "USMF".</span><span class="sxs-lookup"><span data-stu-id="5cd53-105">This tasks uses the demo company 'USMF'.</span></span>






## <a name="general-ledger-parameter"></a><span data-ttu-id="5cd53-106">معلمة دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="5cd53-106">General ledger parameter</span></span>
1. <span data-ttu-id="5cd53-107">انتقل إلى إدارة النقد والبنك > الإعداد > معلمات إدارة النقد والبنوك.</span><span class="sxs-lookup"><span data-stu-id="5cd53-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="5cd53-108">قم بتوسيع القسم "المستند البنكي".</span><span class="sxs-lookup"><span data-stu-id="5cd53-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="5cd53-109">حدد الخيار "تمكين استيراد خطاب الاعتماد".</span><span class="sxs-lookup"><span data-stu-id="5cd53-109">Select the Enable import letter of credit option.</span></span>
4. <span data-ttu-id="5cd53-110">حدد الخيار "تمكين تصدير خطاب الاعتماد".</span><span class="sxs-lookup"><span data-stu-id="5cd53-110">Select the Enable export letter of credit option.</span></span>
5. <span data-ttu-id="5cd53-111">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="5cd53-111">Click Save.</span></span>
6. <span data-ttu-id="5cd53-112">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5cd53-112">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="5cd53-113">إنشاء تسهيل بنكي</span><span class="sxs-lookup"><span data-stu-id="5cd53-113">Create Bank facility</span></span>
1. <span data-ttu-id="5cd53-114">انتقل إلى إدارة النقد والبنك > الإعداد > التسهيلات البنكية.</span><span class="sxs-lookup"><span data-stu-id="5cd53-114">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="5cd53-115">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="5cd53-115">Click New.</span></span>
3. <span data-ttu-id="5cd53-116">في الحقل "مجموعة التسهيلات"، أدخل اسم مجموعة التسهيلات البنكية.</span><span class="sxs-lookup"><span data-stu-id="5cd53-116">In the Facility group field, enter the bank facility group name.</span></span>
4. <span data-ttu-id="5cd53-117">في الحقل "الوصف"، أدخل وصف مجموعة التسهيلات البنكية.</span><span class="sxs-lookup"><span data-stu-id="5cd53-117">In the Description field, enter the bank facility group description.</span></span>
5. <span data-ttu-id="5cd53-118">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="5cd53-118">Click Save.</span></span>
6. <span data-ttu-id="5cd53-119">انقر فوق علامة التبويب "أنواع التسهيلات".</span><span class="sxs-lookup"><span data-stu-id="5cd53-119">Click the Facility types tab.</span></span>
7. <span data-ttu-id="5cd53-120">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="5cd53-120">Click New.</span></span>
8. <span data-ttu-id="5cd53-121">في الحقل "نوع التسهيل"، أدخل رمزًا فريدًا.</span><span class="sxs-lookup"><span data-stu-id="5cd53-121">In the Facility type field, enter a unique code.</span></span>
9. <span data-ttu-id="5cd53-122">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="5cd53-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="5cd53-123">في الحقل "مجموعة التسهيلات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5cd53-123">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="5cd53-124">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5cd53-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="5cd53-125">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5cd53-125">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="5cd53-126">في الحقل "طبيعة التسهيل"، حدد طبيعة التسهيل البنكي.</span><span class="sxs-lookup"><span data-stu-id="5cd53-126">In the Facility nature field, select the nature of the bank facility.</span></span>
14. <span data-ttu-id="5cd53-127">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="5cd53-127">Click Save.</span></span>
15. <span data-ttu-id="5cd53-128">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5cd53-128">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="5cd53-129">ملفات تعريف ترحيل بنكي</span><span class="sxs-lookup"><span data-stu-id="5cd53-129">Bank posting profile</span></span>
1. <span data-ttu-id="5cd53-130">انتقل إلى إدارة النقد والبنك > الإعداد > ملف تعريف ترحيل المستندات البنكية.</span><span class="sxs-lookup"><span data-stu-id="5cd53-130">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="5cd53-131">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="5cd53-131">Click New.</span></span>
3. <span data-ttu-id="5cd53-132">في الحقل "رقم الحساب/المجموعة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="5cd53-132">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5cd53-133">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="5cd53-133">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="5cd53-134">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="5cd53-134">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5cd53-135">حد الحساب الرئيسي للتسوية.</span><span class="sxs-lookup"><span data-stu-id="5cd53-135">Select the main account for settlement.</span></span>
    * <span data-ttu-id="5cd53-136">يُستخدم هذا الحساب عند حساب تقدير التدفق النقدي.</span><span class="sxs-lookup"><span data-stu-id="5cd53-136">This account is used when calculating cash flow forecast.</span></span>  
7. <span data-ttu-id="5cd53-137">في الحقل "المصاريف"، حدد حساب حركات المصروفات.</span><span class="sxs-lookup"><span data-stu-id="5cd53-137">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="5cd53-138">في الحقل "حساب الهامش"، حدد حساب حركات الهامش.</span><span class="sxs-lookup"><span data-stu-id="5cd53-138">In the Margin account field, select the account for margin transactions.</span></span>
    * <span data-ttu-id="5cd53-139">يتم خصم هذا الحساب عند ترحيل هامش الافتتاح واعتماده عند نشر الدفع.</span><span class="sxs-lookup"><span data-stu-id="5cd53-139">This account is debited when the opening margin is posted and credited when the payment is posted.</span></span>  
9. <span data-ttu-id="5cd53-140">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="5cd53-140">Click Save.</span></span>


