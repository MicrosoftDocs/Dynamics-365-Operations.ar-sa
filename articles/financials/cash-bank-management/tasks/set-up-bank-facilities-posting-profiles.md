---
title: إعداد ملفات تعريف الترحيل والتسهيلات البنكية لخطابات الضمان
description: تنشئ هذه المهمة تسهيلاً بنكيًا وملف تعريف ترحيل مطلوب لمعالجة خطاب ضمان.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f696f5aa809692a0cc2c4ff559945a301480d7e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566008"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="d5766-103">إعداد ملفات تعريف الترحيل والتسهيلات البنكية لخطابات الضمان</span><span class="sxs-lookup"><span data-stu-id="d5766-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d5766-104">تنشئ هذه المهمة تسهيلاً بنكيًا وملف تعريف ترحيل مطلوب لمعالجة خطاب ضمان.</span><span class="sxs-lookup"><span data-stu-id="d5766-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="d5766-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="d5766-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="d5766-106">معلمة دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="d5766-106">General ledger parameter</span></span>
1. <span data-ttu-id="d5766-107">انتقل إلى إدارة النقد والبنك > الإعداد > معلمات إدارة النقد والبنوك.</span><span class="sxs-lookup"><span data-stu-id="d5766-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="d5766-108">قم بتوسيع القسم "المستند البنكي".</span><span class="sxs-lookup"><span data-stu-id="d5766-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="d5766-109">حدد الخيار "تمكين خطاب الضمان".</span><span class="sxs-lookup"><span data-stu-id="d5766-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="d5766-110">في الحقل "دفتر يومية الحركات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d5766-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d5766-111">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d5766-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="d5766-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d5766-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d5766-113">انقر فوق علامة التبويب "التسلسلات الرقمية".</span><span class="sxs-lookup"><span data-stu-id="d5766-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="d5766-114">تعريف كود التسلسل الرقمي لرقم خطاب الضمان ومراجع حركات خطابات الضمان</span><span class="sxs-lookup"><span data-stu-id="d5766-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="d5766-115">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d5766-115">Click Save.</span></span>
9. <span data-ttu-id="d5766-116">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d5766-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="d5766-117">إنشاء تسهيل بنكي</span><span class="sxs-lookup"><span data-stu-id="d5766-117">Create Bank facility</span></span>
1. <span data-ttu-id="d5766-118">انتقل إلى إدارة النقد والبنك > الإعداد > التسهيلات البنكية.</span><span class="sxs-lookup"><span data-stu-id="d5766-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="d5766-119">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d5766-119">Click New.</span></span>
3. <span data-ttu-id="d5766-120">في الحقل "مجموعة التسهيلات"، أدخل اسم مجموعة التسهيلات البنكية الخاصة بحركة خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="d5766-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="d5766-121">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d5766-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d5766-122">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d5766-122">Click Save.</span></span>
6. <span data-ttu-id="d5766-123">انقر فوق علامة التبويب "أنواع التسهيلات".</span><span class="sxs-lookup"><span data-stu-id="d5766-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="d5766-124">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d5766-124">Click New.</span></span>
8. <span data-ttu-id="d5766-125">في الحقل "نوع التسهيل"، أدخل اسم نوع التسهيل البنكي المرتبط باتفاقية التسهيلات البنكية.</span><span class="sxs-lookup"><span data-stu-id="d5766-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="d5766-126">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d5766-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="d5766-127">في الحقل "مجموعة التسهيلات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d5766-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="d5766-128">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d5766-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="d5766-129">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d5766-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="d5766-130">في الحقل "طبيعة التسهيل"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="d5766-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="d5766-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="d5766-131">Click Save.</span></span>
15. <span data-ttu-id="d5766-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d5766-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="d5766-133">ملفات تعريف ترحيل بنكي</span><span class="sxs-lookup"><span data-stu-id="d5766-133">Bank posting profile</span></span>
1. <span data-ttu-id="d5766-134">انتقل إلى إدارة النقد والبنك > الإعداد > ملف تعريف ترحيل المستندات البنكية.</span><span class="sxs-lookup"><span data-stu-id="d5766-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="d5766-135">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="d5766-135">Click New.</span></span>
3. <span data-ttu-id="d5766-136">في الحقل "رقم الحساب/المجموعة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d5766-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d5766-137">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d5766-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d5766-138">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="d5766-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d5766-139">في الحقل "حساب التسوية"، حدد الحساب الرئيسي للتسوية.</span><span class="sxs-lookup"><span data-stu-id="d5766-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="d5766-140">في الحقل "المصاريف"، حدد حساب حركات المصروفات.</span><span class="sxs-lookup"><span data-stu-id="d5766-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="d5766-141">في الحقل "حساب الهامش"، حدد الحساب لحركة الهامش.</span><span class="sxs-lookup"><span data-stu-id="d5766-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="d5766-142">في الحقل "حساب التصفية"، حدد حساب التصفية لحركة خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="d5766-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="d5766-143">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="d5766-143">Click Save.</span></span>
11. <span data-ttu-id="d5766-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="d5766-144">Close the page.</span></span>

