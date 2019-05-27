---
title: تطبيق نقطة البيع (POS) وإعدادات لغة المستخدم
description: يصف هذا الموضوع كيفية تغيير إعدادات اللغة في Retail Modern POS (MPOS) وCloud POS.
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
ms.openlocfilehash: faf8cdcee70b55842072298b51789f6cd7a577af
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545090"
---
# <a name="point-of-sale-pos-application-and-user-language-settings"></a><span data-ttu-id="a9837-103">تطبيق نقطة البيع (POS) وإعدادات لغة المستخدم</span><span class="sxs-lookup"><span data-stu-id="a9837-103">Point of sale (POS) application and user language settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a9837-104">يصف هذا الموضوع كيفية تغيير إعدادات اللغة في Retail Modern POS (MPOS) وCloud POS.</span><span class="sxs-lookup"><span data-stu-id="a9837-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

## <a name="overview"></a><span data-ttu-id="a9837-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="a9837-105">Overview</span></span>

<span data-ttu-id="a9837-106">تدعم Retail Modern POS (MPOS) وCloud POS البيئات التي يمكن أن تختلف بها إعدادات اللغة والتحويلات بين المتجر وإعدادات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="a9837-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="a9837-107">على سبيل المثال، يمكن أن يكون المتجر موجوداً في منطقة حيث تكون اللغة الإنجليزية الأكثر شيوعًا للعملاء، ولكن بعض العاملين يفضلون استخدام التطبيق بالترجمات الفرنسية.‬</span><span class="sxs-lookup"><span data-stu-id="a9837-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="a9837-108">لغة البيانات</span><span class="sxs-lookup"><span data-stu-id="a9837-108">Data language</span></span>

<span data-ttu-id="a9837-109">‏‫بغض النظر عن إعدادات المستخدم، سوف تستخدم MPOS وCloud POS دائمًا إعدادات لغة المتجر لتحديد الترجمات المستخدمة للبيانات.</span><span class="sxs-lookup"><span data-stu-id="a9837-109">Regardless of the user's settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="a9837-110">وهذا سيضمن أن كافة المستخدمين والعملاء سيكون لديهم تجربة متناسقة.</span><span class="sxs-lookup"><span data-stu-id="a9837-110">This will ensure that all users and customers will have a consistent experience.</span></span> <span data-ttu-id="a9837-111">تتضمن أمثلة البيانات:‬</span><span class="sxs-lookup"><span data-stu-id="a9837-111">Examples of data include:</span></span>

- <span data-ttu-id="a9837-112">المنتجات</span><span class="sxs-lookup"><span data-stu-id="a9837-112">Products</span></span>
- <span data-ttu-id="a9837-113">السمات والقيم</span><span class="sxs-lookup"><span data-stu-id="a9837-113">Attributes and values</span></span>
- <span data-ttu-id="a9837-114">أسماء الفئة</span><span class="sxs-lookup"><span data-stu-id="a9837-114">Category names</span></span>
- <span data-ttu-id="a9837-115">إيصالات حركة المطبوعة أو مرسلة عبر البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="a9837-115">Printed or emailed transaction receipts</span></span>
- <span data-ttu-id="a9837-116">أسماء طريقة الدفع</span><span class="sxs-lookup"><span data-stu-id="a9837-116">Payment method names</span></span>
- <span data-ttu-id="a9837-117">رسائل شاشة عرض سطرية</span><span class="sxs-lookup"><span data-stu-id="a9837-117">Line display messages</span></span>

<span data-ttu-id="a9837-118">سيتم استخدام لغة المتجر أيضًا لشاشة تسجيل الدخول إلى نقطة البيع الرئيسية، لأن المستخدم غير معروف قبل تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="a9837-118">The store's language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="a9837-119">إذا لم تتوفر ترجمة للغة المتجر، فإن نقطة البيع ستعود إلى لغة الشركة.‬</span><span class="sxs-lookup"><span data-stu-id="a9837-119">If a translation is not available for the store's language, the POS will revert to the company's language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="a9837-120">تكوين إعدادات لغة المتجر</span><span class="sxs-lookup"><span data-stu-id="a9837-120">Configuring the store's language setting</span></span>

<span data-ttu-id="a9837-121">يتم تعيين إعداد لغة المتجر من **كافة متاجر البيع بالتجزئة‬** في صفحة **متجر البيع بالتجزئة** ضمن **عام &gt; الإعدادات الإقليمية &gt; اللغة**.</span><span class="sxs-lookup"><span data-stu-id="a9837-121">The store's language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language**.</span></span> <span data-ttu-id="a9837-122">استخدم القائمة المنسدلة لاختيار لغة لكل متجر.‬</span><span class="sxs-lookup"><span data-stu-id="a9837-122">Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="a9837-123">لغة واجهة المستخدم</span><span class="sxs-lookup"><span data-stu-id="a9837-123">User interface language</span></span>

<span data-ttu-id="a9837-124">يحدد إعداد لغة مستخدم نقطة البيع الترجمات المستخدمة في واجهة مستخدم التطبيق.</span><span class="sxs-lookup"><span data-stu-id="a9837-124">The POS user's language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="a9837-125">وهذا يتضمن كافة التسميات والقوائم التي لا تعتبر بيانات.‬</span><span class="sxs-lookup"><span data-stu-id="a9837-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="a9837-126">‏‫يتمثل أحد الاستثناءات في النص المعروض على شبكات أزرار نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="a9837-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="a9837-127">لا تدعم شبكات الأزرار الترجمات، لذلك فإنها سوف تُظهر النص دائمًا كما هو محدد على الزر.</span><span class="sxs-lookup"><span data-stu-id="a9837-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="a9837-128">ولدعم الأزرار المترجمة، فإنه يجب عليك نسخ شبكات الأزرار المنفصلة وصيانها وتعيينها إلى المستخدمين حسب الاقتضاء.‬</span><span class="sxs-lookup"><span data-stu-id="a9837-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="a9837-129">تكوين إعدادات لغة المستخدم</span><span class="sxs-lookup"><span data-stu-id="a9837-129">Configuring the user's language setting</span></span>

<span data-ttu-id="a9837-130">يتم تعيين إعداد لغة مستخدم نقطة البيع من **جميع العاملين** في صفحة **العامل** ضمن **البيع بالتجزئة &gt; اللغة**.</span><span class="sxs-lookup"><span data-stu-id="a9837-130">The POS user's language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span> <span data-ttu-id="a9837-131">لا يتم تعيينها على علامة تبويب ملف التعريف الأساسي. لا يتم استخدام هذا الإعداد بواسطة نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="a9837-131">It is not set on the main Profile tab. This setting is not used by POS.</span></span> <span data-ttu-id="a9837-132">إذا لم يتم تعيين لغة المستخدم أو إذا تم تعيينها إلى لغة لا تتوفر فيها ترجمات، ستعود نقطة البيع إلى لغة المتجر.</span><span class="sxs-lookup"><span data-stu-id="a9837-132">If the user's language is not set or it is set to a language where translations are not available, the POS will revert to the store's language.</span></span>

|             | <span data-ttu-id="a9837-133">لغة واجهة المستخدم   </span><span class="sxs-lookup"><span data-stu-id="a9837-133">UI language</span></span>                | <span data-ttu-id="a9837-134">لغة البيانات (المنتجات، تنسيقات الإيصالات، عرض الخط، إلخ)</span><span class="sxs-lookup"><span data-stu-id="a9837-134">Data language (products, receipt formats, line display, etc.)</span></span> |
|-------------|----------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a9837-135">**الشركة**</span><span class="sxs-lookup"><span data-stu-id="a9837-135">**Company**</span></span> | <span data-ttu-id="a9837-136">افتراضي</span><span class="sxs-lookup"><span data-stu-id="a9837-136">Default</span></span>                    | <span data-ttu-id="a9837-137">افتراضي</span><span class="sxs-lookup"><span data-stu-id="a9837-137">Default</span></span>                                                       |
| <span data-ttu-id="a9837-138">**المتجر**</span><span class="sxs-lookup"><span data-stu-id="a9837-138">**Store**</span></span>   | <span data-ttu-id="a9837-139">يتجاوز الشركة</span><span class="sxs-lookup"><span data-stu-id="a9837-139">Overrides company</span></span>          | <span data-ttu-id="a9837-140">يتجاوز الشركة</span><span class="sxs-lookup"><span data-stu-id="a9837-140">Overrides company</span></span>                                             |
| <span data-ttu-id="a9837-141">**المستخدم**</span><span class="sxs-lookup"><span data-stu-id="a9837-141">**User**</span></span>    | <span data-ttu-id="a9837-142">يتجاوز المتجر أو الشركة</span><span class="sxs-lookup"><span data-stu-id="a9837-142">Overrides store or company</span></span> | <span data-ttu-id="a9837-143">أبدًا</span><span class="sxs-lookup"><span data-stu-id="a9837-143">Never</span></span>                                                         |
