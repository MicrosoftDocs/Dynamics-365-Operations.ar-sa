---
title: تسجيل أصناف لصنف ممكَّن للتخزين المتقدم باستخدام دفتر يومية وصول الصنف
description: يقدم هذا الموضوع سيناريو يوضح كيفية تسجيل الأصناف باستخدام دفتر يومية وصول الصنف عند استخدام عمليات إدارة المستودعات المتقدمة.
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830824"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="cbdf8-103">تسجيل أصناف لصنف ممكَّن للتخزين المتقدم باستخدام دفتر يومية وصول الصنف</span><span class="sxs-lookup"><span data-stu-id="cbdf8-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cbdf8-104">يقدم هذا الموضوع سيناريو يوضح كيفية تسجيل الأصناف باستخدام دفتر يومية وصول الصنف عند استخدام عمليات إدارة المستودعات المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-104">This topic presents a scenario that shows how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="cbdf8-105">يتم ذلك عادة عن طريق موظف الاستقبال.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-105">This would usually be done by a receiving clerk.</span></span>

## <a name="enable-sample-data"></a><span data-ttu-id="cbdf8-106">تمكين عينة البيانات</span><span class="sxs-lookup"><span data-stu-id="cbdf8-106">Enable sample data</span></span>

<span data-ttu-id="cbdf8-107">للعمل من خلال هذا السيناريو باستخدام نماذج السجلات والقيم المحددة في هذا الموضوع، يجب أن تستخدم نظامًا حيث تم تثبيت البيانات التجريبية القياسية، ويجب عليك تحديد اكيان القانوني *USMF* قبل البدء.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-107">To work through this scenario using the sample records and values specified in this topic, you must be using a system where the standard demo data is installed, and you must select the *USMF* legal entity before you begin.</span></span>

<span data-ttu-id="cbdf8-108">يمكنك بدلا من ذلك العمل عبر هذا السيناريو باستبدال القيم من البيانات الخاصة بك بشرط ان تكون البيانات التالية متوفرة:</span><span class="sxs-lookup"><span data-stu-id="cbdf8-108">You can instead work through this scenario by substituting values from your own data provided that you have the following data available:</span></span>

- <span data-ttu-id="cbdf8-109">يجب ان يكون لديك أمر شراء مؤكد مع بند أمر شراء مفتوح.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-109">You must have a confirmed purchase order with an open purchase order line.</span></span>
- <span data-ttu-id="cbdf8-110">يجب أن يكون الصنف على البند صنفًا مخزنًا.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-110">The item on the line must be stocked.</span></span> <span data-ttu-id="cbdf8-111">ويجب الا يستخدم متغيرات المنتج، ويجب الا يكون له ابعاد تعقب.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-111">It must not use product variants, and must not have tracking dimensions.</span></span>
- <span data-ttu-id="cbdf8-112">يجب أن يقترن الصنف بمجموعة أبعاد التخزين التي تم تمكين عملية إدارة المستودعات بها.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-112">The item must be associated with a storage dimension group that has warehouse management process enabled.</span></span>
- <span data-ttu-id="cbdf8-113">يجب تمكين المستودع الذي يتم استخدامه لعمليات إدارة المستودع ويجب أن يكون الموقع الذي تستخدمَه يتم التحكم به بواسطة لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-113">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span>

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a><span data-ttu-id="cbdf8-114">إنشاء راس دفتر يوميه وصول الصنف الذي يستخدم أداره المستودعات</span><span class="sxs-lookup"><span data-stu-id="cbdf8-114">Create an item arrival journal header that uses warehouse management</span></span>

<span data-ttu-id="cbdf8-115">يوضح السيناريو التالي كيفيه إنشاء راس دفتر يوميه وصول الصنف الذي يستخدم أداره المستودعات:</span><span class="sxs-lookup"><span data-stu-id="cbdf8-115">The following scenario shows how to create an item arrival journal header that uses warehouse management:</span></span>

1. <span data-ttu-id="cbdf8-116">تاكد من ان النظام الخاص بك يحتوي علي أمر شراء مؤكد يحقق المتطلبات الموضحة في القسم السابق.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-116">Make sure your system contains a confirmed purchase order that fulfils the requirements outlined in the previous section.</span></span> <span data-ttu-id="cbdf8-117">يستخدم هذا السيناريو أمر شراء للشركة *USMF*، حساب المورد *1001*، المستودع *51*، مع بند أمر لـ *10 PL* (10 نقالات) من رقم الصنف *M9200*.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-117">This scenario uses a purchase order for company *USMF*, vendor account *1001*, warehouse *51*, with an order line for *10 PL* (10 pallets) of item number *M9200*.</span></span>
1. <span data-ttu-id="cbdf8-118">قم بتدوين رقم أمر الشراء الذي ستستخدمه.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-118">Make a note of the purchase order number that you will use.</span></span>
1. <span data-ttu-id="cbdf8-119">انتقل إلى **إدارة المخزون \> إدخالات دفاتر اليومية \> وصول الصنف \> وصول الصنف**.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-119">Go to **Inventory management \> Journal entries \> Item arrival \> Item arrival**.</span></span>
1. <span data-ttu-id="cbdf8-120">حدد **جديد** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-120">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="cbdf8-121">يفتح مربع الحوار **إنشاء دفتر يومية إدارة المستودع**.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-121">The **Create warehouse management journal** dialog box opens.</span></span> <span data-ttu-id="cbdf8-122">حدد اسم دفتر يومية في حقل **الاسم**.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-122">Select a journal name in the **Name** field.</span></span>
    - <span data-ttu-id="cbdf8-123">إذا كنت تستخدم بيانات نموذج *USMF*، حدد *WHS*.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-123">If you are using *USMF* sample data, select *WHS*.</span></span>
    - <span data-ttu-id="cbdf8-124">إذا كنت تستخدم البيانات الخاصة بك، فيجب ان يكون دفتر اليومية الذي اخترته قد تم تعيين **التحقق من موقع الانتقاء** له إلى *لا* و **إدارة العزل** إلى *لا*.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-124">If you're using your own data, the journal you choose must have **Check picking location** set to *No* and **Quarantine management** set to *No*.</span></span>
1. <span data-ttu-id="cbdf8-125">قم بتعيين **المرجع** إلى *أمر الشراء*.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-125">Set **Reference** to *Purchase order*.</span></span>
1. <span data-ttu-id="cbdf8-126">قم بتعيين **رقم الحساب** إلى *1001*.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-126">Set **Account number** to *1001*.</span></span>
1. <span data-ttu-id="cbdf8-127">قم بتعيين **رقم** لرقم أمر الشراء الذي قمت بتحديده لهذا التدريب.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-127">Set **Number** to the number of the purchase order that you identified for this exercise.</span></span>

    <span data-ttu-id="cbdf8-128">![دفتر يومية وصول الصنف](../media/item-arrival-journal-header.png "دفتر يومية وصول الصنف")</span><span class="sxs-lookup"><span data-stu-id="cbdf8-128">![Item arrival journal](../media/item-arrival-journal-header.png "Item arrival journal")</span></span>

1. <span data-ttu-id="cbdf8-129">حدد **موافق** لإنشاء راس دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-129">Select the **OK** to create the journal header.</span></span>
1. <span data-ttu-id="cbdf8-130">في قسم **بنود دفتر اليومية**، حدد **إضافة بند** وأدخل البيانات التالية:</span><span class="sxs-lookup"><span data-stu-id="cbdf8-130">In the **Journal lines** section, select **Add line** and enter the following data:</span></span>
    - <span data-ttu-id="cbdf8-131">**رقم الصنف** – قم بالتعيين إلى *M9200*.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-131">**Item number** – Set to *M9200*.</span></span> <span data-ttu-id="cbdf8-132">سيتم تعيين **الموقع**، و **المستودع**، و **الكمية** على أساس بيانات حركة المخزون لعدد 10 نقالات (1000 لكل منها).</span><span class="sxs-lookup"><span data-stu-id="cbdf8-132">The **Site**, **Warehouse**, and **Quantity** will get set based on the inventory transaction data for the 10 pallets (1000 ea.).</span></span>
    - <span data-ttu-id="cbdf8-133">**الموقع** – قم بالتعيين إلى *001*.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-133">**Location** – Set to  *001*.</span></span> <span data-ttu-id="cbdf8-134">لا يتعقب هذا الموقع المحدد لوحات الترخيص.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-134">This specific location does not track license plates.</span></span>

    <span data-ttu-id="cbdf8-135">![بند دفتر يومية وصول الصنف](../media/item-arrival-journal-line.png "بند دفتر يومية وصول الصنف")</span><span class="sxs-lookup"><span data-stu-id="cbdf8-135">![Item arrival journal line](../media/item-arrival-journal-line.png "Item arrival journal line")</span></span>

    > [!NOTE]
    > <span data-ttu-id="cbdf8-136">يحدد حقل **التاريخ** التاريخ الذي سيتم فيه تسجيل الكمية المتاحة من هذا الصنف في المخزون.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-136">The **Date** field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    >
    > <span data-ttu-id="cbdf8-137">سيتم ملء **معرف الشحنة** بواسطة النظام إذا أمكن تعريفه بشكل فريد من المعلومات المقدمة.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-137">The **Lot ID** will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="cbdf8-138">وإلا ستحتاجُ لإدخال هذا المعرف يدوياً.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-138">Otherwise you will have to enter this manually.</span></span> <span data-ttu-id="cbdf8-139">هذا حقل مطلوب يربط هذا التسجيل ببند مستند مصدر محدد.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-139">This is a required field, which links this registration to a specific source document line.</span></span>  

1. <span data-ttu-id="cbdf8-140">حدد **التحقق** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-140">Select **Validate** on the Action Pane.</span></span> <span data-ttu-id="cbdf8-141">يتحقق هذا من دفتر اليومية الجاهز للترحيل.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-141">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="cbdf8-142">إذا فشلت عملية التحقق، فستحتاجُ لتصحيح الأخطاء قبل أن تتمكن من ترحيل دفتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-142">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
1. <span data-ttu-id="cbdf8-143">يفتح مربع الحوار **التحقق من دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-143">The **Check journal** dialog box opens.</span></span> <span data-ttu-id="cbdf8-144">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-144">Select **OK**.</span></span>
1. <span data-ttu-id="cbdf8-145">راجع شريط الرسالة.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-145">Review the message bar.</span></span> <span data-ttu-id="cbdf8-146">من المفترض أن تظهر رسالة تفيد باكتمال العملية.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-146">There should be a message denoting that the operation was completed.</span></span>  
1. <span data-ttu-id="cbdf8-147">حدد **ترحيل** في جزء الإجراء.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-147">Select **Post** on the Action Pane.</span></span>
1. <span data-ttu-id="cbdf8-148">يفتح مربع الحوار **ترحيل دفتر اليومية**.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-148">The **Post journal** dialog box opens.</span></span> <span data-ttu-id="cbdf8-149">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-149">Select **OK**.</span></span>
1. <span data-ttu-id="cbdf8-150">راجع شريط الرسالة.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-150">Review the message bar.</span></span> <span data-ttu-id="cbdf8-151">من المفترض أن تظهر رسالة تشير إلى اكتمال العملية.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-151">There should be messages denoting that the operation completed.</span></span>
1. <span data-ttu-id="cbdf8-152">حدد **الوظائف > إيصال استلام المنتجات** في جزء الإجراءات لتحديث بند أمر الشراء وترحيل إيصال استلام المنتجات.</span><span class="sxs-lookup"><span data-stu-id="cbdf8-152">Select **Functions > Product receipt** on the Action Pane to update the purchase order line and post a product receipt.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
