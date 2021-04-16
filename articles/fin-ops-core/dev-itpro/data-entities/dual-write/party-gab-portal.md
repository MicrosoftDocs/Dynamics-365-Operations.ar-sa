---
title: استخدام Power Portal مع نموذج بيانات الطرف
description: يصف هذا الموضوع التغييرات التي تم إجراؤها على أدوار ويب Power Portal بسبب نموذج بيانات الطرف في الكتابة المزدوجة.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833080"
---
# <a name="using-power-portal-with-the-party-data-model"></a><span data-ttu-id="c1edd-103">استخدام Power Portal مع نموذج بيانات الطرف</span><span class="sxs-lookup"><span data-stu-id="c1edd-103">Using Power Portal with the Party data model</span></span>

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c1edd-104">يتضمن الإصدار 2.0.999.0 من حل تزامن تطبيق الكتابة المزدوجة والإصدارات الأحدث تغييرات نموذج البيانات إلى دفتر العناوين العام والحزب لجدولي الحساب وجهات الاتصال.</span><span class="sxs-lookup"><span data-stu-id="c1edd-104">The Dual-write application orchestration solution version 2.0.999.0 and later includes data model changes to party and global address book for the Account and Contact tables.</span></span> <span data-ttu-id="c1edd-105">تسمح التغييرات بعلاقات أطراف بأطراف تدعم سيناريوهات الأعمال المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="c1edd-105">The changes allow many-to-many relationships that support advanced business scenarios.</span></span> <span data-ttu-id="c1edd-106">لا تدعم أدوار موقع البوابة الإلكترونية على الويب هذه التغييرات، بما في ذلك مدخل العميل، التي يتم شحنها خارج الصندوق أو التي كانت موجودة في بيئتك قبل تثبيت الكتابة المزدوجة.</span><span class="sxs-lookup"><span data-stu-id="c1edd-106">These changes are not supported by portal web roles, including the customer portal, that are shipped out-of-the-box or that existed in your environment before you installed dual-write.</span></span> <span data-ttu-id="c1edd-107">لكي تعمل أدوار الويب كما هو متوقع، تحتاج إلى إنشاء أدوار ويب جديدة باستخدام نموذج البيانات الجديد.</span><span class="sxs-lookup"><span data-stu-id="c1edd-107">For the web roles to work as expected, you need to create new web roles using the new data model.</span></span> 

<span data-ttu-id="c1edd-108">باختصار، لقد تغيرت طريقة تفاعل الجداول، لكن أذونات الجدول في مدخل العميل لم تتغير.</span><span class="sxs-lookup"><span data-stu-id="c1edd-108">In summary, the way the tables interact has changed, but the table permissions in the customer portal haven't changed.</span></span> <span data-ttu-id="c1edd-109">يشرح هذا الموضوع كيفية إنشاء أدوار ويب جديدة تعمل مع نموذج البيانات المتقدم الجديد.</span><span class="sxs-lookup"><span data-stu-id="c1edd-109">This topic explains how to create new web roles that work with the new advanced data model.</span></span>

<span data-ttu-id="c1edd-110">يعرض هذا الرسم التخطيطي علاقة الجدول **دون** نموذج بيانات دفتر العناوين العمومي والطرف:</span><span class="sxs-lookup"><span data-stu-id="c1edd-110">This diagram shows the table relationship **without** the party and global address book data model:</span></span>

   ![دون نموذج الطرف](media/without-party-model.PNG)

<span data-ttu-id="c1edd-112">يعرض هذا الرسم التخطيطي علاقة الجدول **مع** نموذج بيانات دفتر العناوين العمومي والطرف:</span><span class="sxs-lookup"><span data-stu-id="c1edd-112">This diagram shows the table relationship **with** the party and global address book data model:</span></span>

   ![مع نموذج الطرف](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a><span data-ttu-id="c1edd-114">إنشاء إذن جدول جديد</span><span class="sxs-lookup"><span data-stu-id="c1edd-114">Create a new table permission</span></span>

<span data-ttu-id="c1edd-115">لإنشاء أذونات الجداول الجديدة هذه، اتبع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="c1edd-115">To create these new table permissions, follow these steps:</span></span>

1. <span data-ttu-id="c1edd-116">قم بتسجيل الدخول إلى [Power Apps](https://make.powerapps.com)، وانتقل إلى تطبيقاتك.</span><span class="sxs-lookup"><span data-stu-id="c1edd-116">Sign in to [Power Apps](https://make.powerapps.com), and go to your apps.</span></span>
2. <span data-ttu-id="c1edd-117">حدد تطبيق إدارة المدخل.</span><span class="sxs-lookup"><span data-stu-id="c1edd-117">Select your Portal Management app.</span></span>
3. <span data-ttu-id="c1edd-118">في الشريط الجانبي، حدد **الأمان> أذونات الجداول**.</span><span class="sxs-lookup"><span data-stu-id="c1edd-118">In the side bar, select **Security > Table permissions**.</span></span>

    <span data-ttu-id="c1edd-119">يجب إنشاء ثلاثة أذونات جديدة:</span><span class="sxs-lookup"><span data-stu-id="c1edd-119">You must create three new permissions:</span></span>

    + <span data-ttu-id="c1edd-120">اتصال جهة الاتصال بالطرف</span><span class="sxs-lookup"><span data-stu-id="c1edd-120">Contact to Party connection</span></span>
    + <span data-ttu-id="c1edd-121">اتصال الطرف بالحساب</span><span class="sxs-lookup"><span data-stu-id="c1edd-121">Party to Account connection</span></span>
    + <span data-ttu-id="c1edd-122">اتصال الحساب بالأمر</span><span class="sxs-lookup"><span data-stu-id="c1edd-122">Account to Order connection</span></span>

4. <span data-ttu-id="c1edd-123">قم بإنشاء وحفظ إذن جديد لاتصال جهة الاتصال بالطرف، مع تعيين هذه المعلمات:</span><span class="sxs-lookup"><span data-stu-id="c1edd-123">Create and save a new permission for the Contact to Party connection, setting these parameters:</span></span>

    + <span data-ttu-id="c1edd-124">**الاسم**: اتصال الطرف بالحساب (أو اختيارك)</span><span class="sxs-lookup"><span data-stu-id="c1edd-124">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="c1edd-125">**اسم الجدول**: msdyn_contactforparty</span><span class="sxs-lookup"><span data-stu-id="c1edd-125">**Table Name**: msdyn_contactforparty</span></span>
    + <span data-ttu-id="c1edd-126">**موقع الويب**: مدخل العملاء</span><span class="sxs-lookup"><span data-stu-id="c1edd-126">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="c1edd-127">**النطاق**: جهة الاتصال</span><span class="sxs-lookup"><span data-stu-id="c1edd-127">**Scope**: Contact</span></span>
    + <span data-ttu-id="c1edd-128">**الامتيازات**: تحديد الكل</span><span class="sxs-lookup"><span data-stu-id="c1edd-128">**Privileges**: Select all</span></span>
    + <span data-ttu-id="c1edd-129">**أدوار الويب**: مستخدمون مصادقون، ممثل العملاء (أو اختيارك)</span><span class="sxs-lookup"><span data-stu-id="c1edd-129">**Web roles**: Authenticated Users, Customer Representative (or your choice)</span></span>

5. <span data-ttu-id="c1edd-130">قم بإنشاء وحفظ إذن جديد لاتصال الطرف بالحساب، مع تعيين هذه المعلمات:</span><span class="sxs-lookup"><span data-stu-id="c1edd-130">Create and save a new permission for the Party to Account connection, setting these parameters:</span></span>

    + <span data-ttu-id="c1edd-131">**الاسم**: اتصال الطرف بالحساب (أو اختيارك)</span><span class="sxs-lookup"><span data-stu-id="c1edd-131">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="c1edd-132">**اسم الجدول**: الحساب</span><span class="sxs-lookup"><span data-stu-id="c1edd-132">**Table Name**: account</span></span>
    + <span data-ttu-id="c1edd-133">**موقع الويب**: مدخل العملاء</span><span class="sxs-lookup"><span data-stu-id="c1edd-133">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="c1edd-134">**النطاق**: الأصل</span><span class="sxs-lookup"><span data-stu-id="c1edd-134">**Scope**: Parent</span></span>
    + <span data-ttu-id="c1edd-135">**الامتيازات**: تحديد الكل</span><span class="sxs-lookup"><span data-stu-id="c1edd-135">**Privileges**: Select all</span></span>
    + <span data-ttu-id="c1edd-136">**إذن الجدول الأصل**: اتصال جهة الاتصال بالطرف</span><span class="sxs-lookup"><span data-stu-id="c1edd-136">**Parent Table Permission**: Contact to Party Connection</span></span>

6. <span data-ttu-id="c1edd-137">قم بإنشاء وحفظ إذن جديد لاتصال الحساب بالأمر، مع تعيين هذه المعلمات:</span><span class="sxs-lookup"><span data-stu-id="c1edd-137">Create and save a new permission for the Account to Order connection, setting these parameters:</span></span>

    + <span data-ttu-id="c1edd-138">**الاسم**: اتصال الحساب بالأمر (أو اختيارك)</span><span class="sxs-lookup"><span data-stu-id="c1edd-138">**Name**: Account to Order Connection (or your choice)</span></span>
    + <span data-ttu-id="c1edd-139">**اسم الجدول**: أمر المبيعات</span><span class="sxs-lookup"><span data-stu-id="c1edd-139">**Table Name**: salesorder</span></span>
    + <span data-ttu-id="c1edd-140">**موقع الويب**: مدخل العملاء</span><span class="sxs-lookup"><span data-stu-id="c1edd-140">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="c1edd-141">**النطاق**: الأصل</span><span class="sxs-lookup"><span data-stu-id="c1edd-141">**Scope**: Parent</span></span>
    + <span data-ttu-id="c1edd-142">**الامتيازات**: تحديد الكل</span><span class="sxs-lookup"><span data-stu-id="c1edd-142">**Privileges**: Select all</span></span>
    + <span data-ttu-id="c1edd-143">**إذن الجدول الأصل**: اتصال الطرف بالحساب</span><span class="sxs-lookup"><span data-stu-id="c1edd-143">**Parent Table Permission**: Party to Account Connection</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
