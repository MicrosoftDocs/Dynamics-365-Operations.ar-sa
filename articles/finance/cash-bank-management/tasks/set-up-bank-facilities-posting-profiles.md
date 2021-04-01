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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b72a412aaaf1c70b4414d00e99b923380f7dd86
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225287"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a><span data-ttu-id="7a14c-103">إعداد ملفات تعريف الترحيل والتسهيلات البنكية لخطابات الضمان</span><span class="sxs-lookup"><span data-stu-id="7a14c-103">Set up bank facilities and posting profiles for letters of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7a14c-104">تنشئ هذه المهمة تسهيلاً بنكيًا وملف تعريف ترحيل مطلوب لمعالجة خطاب ضمان.</span><span class="sxs-lookup"><span data-stu-id="7a14c-104">This task creates a Bank facility and posting profile that is needed to process a letter of guarantee.</span></span>



<span data-ttu-id="7a14c-105">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="7a14c-105">This task uses the USMF demo company.</span></span> 




## <a name="general-ledger-parameter"></a><span data-ttu-id="7a14c-106">معلمة دفتر الأستاذ العام</span><span class="sxs-lookup"><span data-stu-id="7a14c-106">General ledger parameter</span></span>
1. <span data-ttu-id="7a14c-107">انتقل إلى إدارة النقد والبنك > الإعداد > معلمات إدارة النقد والبنوك.</span><span class="sxs-lookup"><span data-stu-id="7a14c-107">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="7a14c-108">قم بتوسيع القسم "المستند البنكي".</span><span class="sxs-lookup"><span data-stu-id="7a14c-108">Expand the Bank document section.</span></span>
3. <span data-ttu-id="7a14c-109">حدد الخيار "تمكين خطاب الضمان".</span><span class="sxs-lookup"><span data-stu-id="7a14c-109">Select the Enable letter of guarantee option.</span></span>
4. <span data-ttu-id="7a14c-110">في الحقل "دفتر يومية الحركات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="7a14c-110">In the Transaction journal field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7a14c-111">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7a14c-111">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="7a14c-112">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7a14c-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="7a14c-113">انقر فوق علامة التبويب "التسلسلات الرقمية".</span><span class="sxs-lookup"><span data-stu-id="7a14c-113">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="7a14c-114">تعريف كود التسلسل الرقمي لرقم خطاب الضمان ومراجع حركات خطابات الضمان</span><span class="sxs-lookup"><span data-stu-id="7a14c-114">Define number sequence code for Letter of guarantee number and Letter of guarantee transaction references</span></span>  
8. <span data-ttu-id="7a14c-115">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7a14c-115">Click Save.</span></span>
9. <span data-ttu-id="7a14c-116">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7a14c-116">Close the page.</span></span>

## <a name="create-bank-facility"></a><span data-ttu-id="7a14c-117">إنشاء تسهيل بنكي</span><span class="sxs-lookup"><span data-stu-id="7a14c-117">Create Bank facility</span></span>
1. <span data-ttu-id="7a14c-118">انتقل إلى إدارة النقد والبنك > الإعداد > التسهيلات البنكية.</span><span class="sxs-lookup"><span data-stu-id="7a14c-118">Go to Cash and bank management > Setup > Bank facilities.</span></span>
2. <span data-ttu-id="7a14c-119">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="7a14c-119">Click New.</span></span>
3. <span data-ttu-id="7a14c-120">في الحقل "مجموعة التسهيلات"، أدخل اسم مجموعة التسهيلات البنكية الخاصة بحركة خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="7a14c-120">In the Facility group field, enter the bank facility group name for the letter of guarantee transaction.</span></span>
4. <span data-ttu-id="7a14c-121">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7a14c-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7a14c-122">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7a14c-122">Click Save.</span></span>
6. <span data-ttu-id="7a14c-123">انقر فوق علامة التبويب "أنواع التسهيلات".</span><span class="sxs-lookup"><span data-stu-id="7a14c-123">Click the Facility types tab.</span></span>
7. <span data-ttu-id="7a14c-124">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="7a14c-124">Click New.</span></span>
8. <span data-ttu-id="7a14c-125">في الحقل "نوع التسهيل"، أدخل اسم نوع التسهيل البنكي المرتبط باتفاقية التسهيلات البنكية.</span><span class="sxs-lookup"><span data-stu-id="7a14c-125">In the Facility type field, enter the name of the bank facility type that is related to the bank facility agreement.</span></span>
9. <span data-ttu-id="7a14c-126">في حقل "الوصف"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="7a14c-126">In the Description field, type a value.</span></span>
10. <span data-ttu-id="7a14c-127">في الحقل "مجموعة التسهيلات"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="7a14c-127">In the Facility group field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="7a14c-128">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7a14c-128">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="7a14c-129">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7a14c-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="7a14c-130">في الحقل "طبيعة التسهيل"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="7a14c-130">In the Facility nature field, select an option.</span></span>
14. <span data-ttu-id="7a14c-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="7a14c-131">Click Save.</span></span>
15. <span data-ttu-id="7a14c-132">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7a14c-132">Close the page.</span></span>

## <a name="bank-posting-profile"></a><span data-ttu-id="7a14c-133">ملفات تعريف ترحيل بنكي</span><span class="sxs-lookup"><span data-stu-id="7a14c-133">Bank posting profile</span></span>
1. <span data-ttu-id="7a14c-134">انتقل إلى إدارة النقد والبنك > الإعداد > ملف تعريف ترحيل المستندات البنكية.</span><span class="sxs-lookup"><span data-stu-id="7a14c-134">Go to Cash and bank management > Setup > Bank documents posting profile.</span></span>
2. <span data-ttu-id="7a14c-135">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="7a14c-135">Click New.</span></span>
3. <span data-ttu-id="7a14c-136">في الحقل "رقم الحساب/المجموعة"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="7a14c-136">In the Account/Group number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="7a14c-137">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="7a14c-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="7a14c-138">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="7a14c-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="7a14c-139">في الحقل "حساب التسوية"، حدد الحساب الرئيسي للتسوية.</span><span class="sxs-lookup"><span data-stu-id="7a14c-139">In the Settle account field, select the main account for settlement.</span></span>
7. <span data-ttu-id="7a14c-140">في الحقل "المصاريف"، حدد حساب حركات المصروفات.</span><span class="sxs-lookup"><span data-stu-id="7a14c-140">In the Charges account field, select the account for expense transactions.</span></span>
8. <span data-ttu-id="7a14c-141">في الحقل "حساب الهامش"، حدد الحساب لحركة الهامش.</span><span class="sxs-lookup"><span data-stu-id="7a14c-141">In the Margin account field, select the account for the margin transaction.</span></span>
9. <span data-ttu-id="7a14c-142">في الحقل "حساب التصفية"، حدد حساب التصفية لحركة خطاب الضمان.</span><span class="sxs-lookup"><span data-stu-id="7a14c-142">In the Liquidation account field, select the liquidation account for the letter of guarantee transaction.</span></span> 
10. <span data-ttu-id="7a14c-143">انقر فوق حفظ.</span><span class="sxs-lookup"><span data-stu-id="7a14c-143">Click Save.</span></span>
11. <span data-ttu-id="7a14c-144">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="7a14c-144">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]