---
title: إنشاء كيانات قانونية
description: يصف هذا الموضوع كيفية إنشاء كيانات قانونية في Microsoft Dynamics 365 Commerce، يجب إنشاؤها وتكوينها قبل إنشاء القنوات.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 225fd6a07fee29414ac30a4602b4dfccdc4d742b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800604"
---
# <a name="create-legal-entities"></a><span data-ttu-id="42164-103">إنشاء كيانات قانونية</span><span class="sxs-lookup"><span data-stu-id="42164-103">Create legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="42164-104">يصف هذا الموضوع كيفية إنشاء كيانات قانونية في Microsoft Dynamics 365 Commerce، يجب إنشاؤها وتكوينها قبل إنشاء القنوات.</span><span class="sxs-lookup"><span data-stu-id="42164-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

<span data-ttu-id="42164-105">الكيان القانوني هو مؤسسة لديها هيكل قانوني مسجَّل أو مشرَّع.</span><span class="sxs-lookup"><span data-stu-id="42164-105">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="42164-106">يمكن إدخال الكيانات القانونية في العقود القانونية ويجب عليها إعداد كشوف حساب تقوم بالإبلاغ عن أدائها.</span><span class="sxs-lookup"><span data-stu-id="42164-106">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="42164-107">الشركة هي نوع من الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="42164-107">A company is a type of legal entity.</span></span> <span data-ttu-id="42164-108">وفي الوقت الحالي، تعتبر الشركات النوع الوحيد من الكيانات القانونية التي يمكنك إنشاؤها، ويقترن كل كيان قانوني بمعرّف شركة.</span><span class="sxs-lookup"><span data-stu-id="42164-108">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="42164-109">يوجد هذا الاقتران لأن بعض المناطق الوظيفية في البرنامج تستخدم معرف شركة أو *DataAreaId*، في نماذج بياناتها.</span><span class="sxs-lookup"><span data-stu-id="42164-109">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="42164-110">في هذه المجالات الوظيفية، تستخدم الشركات كحد لأمن البيانات.</span><span class="sxs-lookup"><span data-stu-id="42164-110">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="42164-111">يمكن للمستخدمين الوصول إلى البيانات فقط للشركة التي قاموا حاليًا بتسجيل الدخول إليها.</span><span class="sxs-lookup"><span data-stu-id="42164-111">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="42164-112">عند إنشاء قناة، يجب تحديد الكيان القانوني الذي تنتمي اليه القناة.</span><span class="sxs-lookup"><span data-stu-id="42164-112">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="42164-113">إنشاء كيان قانوني جديد</span><span class="sxs-lookup"><span data-stu-id="42164-113">Create a new legal entity</span></span>

<span data-ttu-id="42164-114">لإنشاء كيان قانوني جديد في Dynamics 365 Commerce، اتبع هذه الخطوات:</span><span class="sxs-lookup"><span data-stu-id="42164-114">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="42164-115">في جزء التنقل، انتقل إلى  **الوحدات \> إعداد المراكز الرئيسية ‬ \> الكيانات القانونية**.</span><span class="sxs-lookup"><span data-stu-id="42164-115">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="42164-116">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="42164-116">On the action pane, select **New**.</span></span> <span data-ttu-id="42164-117">يظهر الجزء **كيان قانوني جديد** إلى اليسار.</span><span class="sxs-lookup"><span data-stu-id="42164-117">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="42164-118">في حقل **الاسم**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="42164-118">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="42164-119">أدخل قيمة في حقل **الشركة**.</span><span class="sxs-lookup"><span data-stu-id="42164-119">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="42164-120">في الحقل **البلد/المنطقة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="42164-120">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="42164-121">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="42164-121">Select **OK**.</span></span> 

   ![إنشاء كيان قانوني](media/legal-entities.png)

1. <span data-ttu-id="42164-123">في القسم **عام**، أدخل المعلومات العامة التالية حول الكيان القانوني:</span><span class="sxs-lookup"><span data-stu-id="42164-123">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="42164-124">أدخل اسم بحث، إذا كان إدخال اسم البحث مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="42164-124">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="42164-125">اسم البحث هو اسم بديل يمكن استخدامه للبحث عن هذا الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="42164-125">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="42164-126">حدد ما إذا كان يتم استخدام هذا الكيان القانوني كشركة توحيد أم لا.</span><span class="sxs-lookup"><span data-stu-id="42164-126">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="42164-127">حدد ما إذا كان يتم استخدام هذا الكيان القانوني كشركة استبعاد أم لا.</span><span class="sxs-lookup"><span data-stu-id="42164-127">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="42164-128">حدد **اللغة الافتراضية** للكيان.</span><span class="sxs-lookup"><span data-stu-id="42164-128">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="42164-129">حدد **المنطقة الزمنية** للكيان.</span><span class="sxs-lookup"><span data-stu-id="42164-129">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="42164-130">في قسم **العناوين**، حدد **تحرير** لإدخال معلومات العنوان، مثل اسم الشارع ورقمه والرمز البريدي والمدينة.</span><span class="sxs-lookup"><span data-stu-id="42164-130">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="42164-131">في القسم **معلومات جهة الاتصال**، أدخل معلومات أساليب الاتصال، مثل عناوين البريد الإلكتروني وعناوين URL وأرقام الهاتف.</span><span class="sxs-lookup"><span data-stu-id="42164-131">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="42164-132">في القسم **إعداد التقارير التشريعية**، أدخل أرقام التسجيل التي يتم استخدامها لإعداد التقارير التشريعية.</span><span class="sxs-lookup"><span data-stu-id="42164-132">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="42164-133">في القسم **أرقام التسجيل**، أدخل أي معلومات مطلوبة من قبل الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="42164-133">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="42164-134">في المقطع **معلومات الحساب البنكي**، أدخل الحسابات البنكية وأرقام التوجيه الخاصة بالكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="42164-134">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="42164-135">في قسم **التجارة الخارجية واللوجستيات**، أدخل معلومات الشحن الخاصة بالكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="42164-135">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="42164-136">في القسم **التسلسلات الرقمية**، يمكنك عرض التسلسلات الرقمية المقترنة بالكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="42164-136">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="42164-137">سيكون هذا فارغًا عند البدء.</span><span class="sxs-lookup"><span data-stu-id="42164-137">This will be empty to start with.</span></span>
1. <span data-ttu-id="42164-138">في قسم **صورة لوحة المعلومات**، قم بتغيير أو عرض صورة الشعار وصورة لوحة المعلومات المرتبطة بالكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="42164-138">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="42164-139">في القسم **التسجيل الضريبي**، أدخل أرقام التسجيل التي يتم استخدامها لإبلاغ هيئات الضرائب.</span><span class="sxs-lookup"><span data-stu-id="42164-139">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="42164-140">في القسم **ضريبة 1099**، أدخل معلومات ضريبة 1099 للكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="42164-140">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="42164-141">في قسم **معلومات الضريبة**، أدخل معلومات الضريبة للكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="42164-141">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="42164-142">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="42164-142">Select **Save**.</span></span>

<span data-ttu-id="42164-143">تعرض الصورة التالية تفاصيل مثال عن كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="42164-143">The following image shows details of an example legal entity.</span></span>

![القسم العام للكيان القانوني](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="42164-145">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="42164-145">Additional resources</span></span>

[<span data-ttu-id="42164-146">نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="42164-146">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="42164-147">تخطيط التدرج الهرمي للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="42164-147">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="42164-148">التدرجات الهرمية للمؤسسات</span><span class="sxs-lookup"><span data-stu-id="42164-148">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="42164-149">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="42164-149">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="42164-150">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="42164-150">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
