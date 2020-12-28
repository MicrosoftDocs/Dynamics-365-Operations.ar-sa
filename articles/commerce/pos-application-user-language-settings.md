---
title: تطبيق نقطة البيع (POS) وإعدادات لغة المستخدم
description: يصف هذا الموضوع كيفية تغيير إعدادات اللغة في نقطة البيع الحديثة (MPOS) ونقاط بيع المجموعة.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 49bfcaa4c05ea8e6cc6bf0a8f855f2474cea35bc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410004"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a><span data-ttu-id="d24c8-103">تطبيق نقطة البيع (POS) وإعدادات لغة المستخدم</span><span class="sxs-lookup"><span data-stu-id="d24c8-103">Point of sale (POS) application and user language settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d24c8-104">يصف هذا الموضوع كيفية تغيير إعدادات اللغة في نقطة البيع الحديثة (MPOS) ونقاط بيع المجموعة.</span><span class="sxs-lookup"><span data-stu-id="d24c8-104">This topic describes how to change language settings in Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="d24c8-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="d24c8-105">Overview</span></span>
<span data-ttu-id="d24c8-106">‏‫تدعم ‏‫نقطة البيع الحديثة (MPOS) ونقطة بيع المجموعة البيئات التي يمكن أن تختلف بها إعدادات اللغة والتحويلات بين المتجر وإعدادات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="d24c8-106">Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="d24c8-107">على سبيل المثال، يمكن أن يكون المتجر موجوداً في منطقة حيث تكون اللغة الإنجليزية الأكثر شيوعًا للعملاء، ولكن بعض العاملين يفضلون استخدام التطبيق بالترجمات الفرنسية.‬</span><span class="sxs-lookup"><span data-stu-id="d24c8-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="d24c8-108">لغة البيانات</span><span class="sxs-lookup"><span data-stu-id="d24c8-108">Data language</span></span>

<span data-ttu-id="d24c8-109">‏‫بغض النظر عن إعدادات المستخدم، سوف تستخدم MPOS وCloud POS دائمًا إعدادات لغة المتجر لتحديد الترجمات المستخدمة للبيانات.</span><span class="sxs-lookup"><span data-stu-id="d24c8-109">Regardless of the user's settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="d24c8-110">وهذا سيضمن أن كافة المستخدمين والعملاء سيكون لديهم تجربة متناسقة.</span><span class="sxs-lookup"><span data-stu-id="d24c8-110">This will ensure that all users and customers will have a consistent experience.</span></span> <span data-ttu-id="d24c8-111">تتضمن أمثلة البيانات:‬</span><span class="sxs-lookup"><span data-stu-id="d24c8-111">Examples of data include:</span></span>

- <span data-ttu-id="d24c8-112">المنتجات</span><span class="sxs-lookup"><span data-stu-id="d24c8-112">Products</span></span>
- <span data-ttu-id="d24c8-113">السمات والقيم</span><span class="sxs-lookup"><span data-stu-id="d24c8-113">Attributes and values</span></span>
- <span data-ttu-id="d24c8-114">أسماء الفئة</span><span class="sxs-lookup"><span data-stu-id="d24c8-114">Category names</span></span>
- <span data-ttu-id="d24c8-115">إيصالات حركة المطبوعة أو مرسلة عبر البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="d24c8-115">Printed or emailed transaction receipts</span></span>
- <span data-ttu-id="d24c8-116">أسماء طريقة الدفع</span><span class="sxs-lookup"><span data-stu-id="d24c8-116">Payment method names</span></span>
- <span data-ttu-id="d24c8-117">رسائل شاشة عرض سطرية</span><span class="sxs-lookup"><span data-stu-id="d24c8-117">Line display messages</span></span>

<span data-ttu-id="d24c8-118">سيتم استخدام لغة المتجر أيضًا لشاشة تسجيل الدخول إلى نقطة البيع الرئيسية، لأن المستخدم غير معروف قبل تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="d24c8-118">The store's language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="d24c8-119">إذا لم تتوفر ترجمة للغة المتجر، فإن نقطة البيع ستعود إلى لغة الشركة.‬</span><span class="sxs-lookup"><span data-stu-id="d24c8-119">If a translation is not available for the store's language, the POS will revert to the company's language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="d24c8-120">تكوين إعدادات لغة المتجر</span><span class="sxs-lookup"><span data-stu-id="d24c8-120">Configuring the store's language setting</span></span>

<span data-ttu-id="d24c8-121">يتم تعيين إعداد لغة المتجر من **كافة المتاجر‬** في صفحة **المتجر** ضمن **عام &gt; الإعدادات الإقليمية &gt; اللغة**.</span><span class="sxs-lookup"><span data-stu-id="d24c8-121">The store's language setting is set from **All stores** on the **Store** page under **General &gt; Regional Settings &gt; Language**.</span></span> <span data-ttu-id="d24c8-122">استخدم القائمة المنسدلة لاختيار لغة لكل متجر.‬</span><span class="sxs-lookup"><span data-stu-id="d24c8-122">Use the drop-down list to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="d24c8-123">لغة واجهة المستخدم</span><span class="sxs-lookup"><span data-stu-id="d24c8-123">User interface language</span></span>

<span data-ttu-id="d24c8-124">يحدد إعداد لغة مستخدم نقطة البيع الترجمات المستخدمة في واجهة مستخدم التطبيق.</span><span class="sxs-lookup"><span data-stu-id="d24c8-124">The POS user's language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="d24c8-125">وهذا يتضمن كافة التسميات والقوائم التي لا تعتبر بيانات.‬</span><span class="sxs-lookup"><span data-stu-id="d24c8-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="d24c8-126">‏‫يتمثل أحد الاستثناءات في النص المعروض على شبكات أزرار نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="d24c8-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="d24c8-127">لا تدعم شبكات الأزرار الترجمات، لذلك فإنها سوف تُظهر النص دائمًا كما هو محدد على الزر.</span><span class="sxs-lookup"><span data-stu-id="d24c8-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="d24c8-128">ولدعم الأزرار المترجمة، فإنه يجب عليك نسخ شبكات الأزرار المنفصلة وصيانها وتعيينها إلى المستخدمين حسب الاقتضاء.‬</span><span class="sxs-lookup"><span data-stu-id="d24c8-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="d24c8-129">تكوين إعدادات لغة المستخدم</span><span class="sxs-lookup"><span data-stu-id="d24c8-129">Configuring the user's language setting</span></span>

<span data-ttu-id="d24c8-130">يتم تعيين إعداد لغة مستخدم نقطة البيع من **جميع العاملين** في صفحة **العامل** ضمن **البيع بالتجزئة والتجارة &gt; اللغة**.</span><span class="sxs-lookup"><span data-stu-id="d24c8-130">The POS user's language setting is set from **All workers** on the **Worker** page under **Retail and Commerce &gt; Language**.</span></span> <span data-ttu-id="d24c8-131">لا يتم تعيينها على علامة تبويب ملف التعريف الأساسي. لا يتم استخدام هذا الإعداد بواسطة نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="d24c8-131">It is not set on the main Profile tab. This setting is not used by POS.</span></span> <span data-ttu-id="d24c8-132">إذا لم يتم تعيين لغة المستخدم أو إذا تم تعيينها إلى لغة لا تتوفر فيها ترجمات، ستعود نقطة البيع إلى لغة المتجر.</span><span class="sxs-lookup"><span data-stu-id="d24c8-132">If the user's language is not set or it is set to a language where translations are not available, the POS will revert to the store's language.</span></span>

|             | <span data-ttu-id="d24c8-133">لغة واجهة المستخدم   </span><span class="sxs-lookup"><span data-stu-id="d24c8-133">UI language</span></span>                | <span data-ttu-id="d24c8-134">لغة البيانات (المنتجات، تنسيقات الإيصالات، عرض الخط، إلخ)</span><span class="sxs-lookup"><span data-stu-id="d24c8-134">Data language (products, receipt formats, line display, etc.)</span></span> |
|-------------|----------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d24c8-135">**الشركة**</span><span class="sxs-lookup"><span data-stu-id="d24c8-135">**Company**</span></span> | <span data-ttu-id="d24c8-136">افتراضي</span><span class="sxs-lookup"><span data-stu-id="d24c8-136">Default</span></span>                    | <span data-ttu-id="d24c8-137">افتراضي</span><span class="sxs-lookup"><span data-stu-id="d24c8-137">Default</span></span>                                                       |
| <span data-ttu-id="d24c8-138">**المتجر**</span><span class="sxs-lookup"><span data-stu-id="d24c8-138">**Store**</span></span>   | <span data-ttu-id="d24c8-139">يتجاوز الشركة</span><span class="sxs-lookup"><span data-stu-id="d24c8-139">Overrides company</span></span>          | <span data-ttu-id="d24c8-140">يتجاوز الشركة</span><span class="sxs-lookup"><span data-stu-id="d24c8-140">Overrides company</span></span>                                             |
| <span data-ttu-id="d24c8-141">**المستخدم**</span><span class="sxs-lookup"><span data-stu-id="d24c8-141">**User**</span></span>    | <span data-ttu-id="d24c8-142">يتجاوز المتجر أو الشركة</span><span class="sxs-lookup"><span data-stu-id="d24c8-142">Overrides store or company</span></span> | <span data-ttu-id="d24c8-143">أبدًا</span><span class="sxs-lookup"><span data-stu-id="d24c8-143">Never</span></span>                                                         |
