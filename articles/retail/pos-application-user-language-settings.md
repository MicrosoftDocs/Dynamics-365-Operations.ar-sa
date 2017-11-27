---
title: "تطبيق نقطة البيع وإعدادات اللغة المستخدمة"
description: "يصف هذا الموضوع كيفية تغيير إعدادات اللغة في نقطة بيع التجزئة الحديثة (MPOS) و نقاط بيع المجموعة."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: dacc072ab5c070010d86302fa08a3066125b23a6
ms.contentlocale: ar-sa
ms.lasthandoff: 11/03/2017

---

# <a name="pos-application-and-user-language-settings"></a><span data-ttu-id="835d2-103">تطبيق نقطة البيع وإعدادات اللغة المستخدمة</span><span class="sxs-lookup"><span data-stu-id="835d2-103">POS application and user language settings</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="835d2-104">يصف هذا الموضوع كيفية تغيير إعدادات اللغة في نقطة بيع التجزئة الحديثة (MPOS) و نقاط بيع المجموعة.</span><span class="sxs-lookup"><span data-stu-id="835d2-104">This topic describes how to change language settings in Retail Modern POS (MPOS) and Cloud POS.</span></span>

<a name="overview"></a><span data-ttu-id="835d2-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="835d2-105">Overview</span></span>
========

<span data-ttu-id="835d2-106">‏‫تدعم ‏‫نقطة البيع الحديثة للبيع بالتجزئة (MPOS) ونقطة بيع المجموعة البيئات التي يمكن أن تختلف بها إعدادات اللغة والتحويلات بين المتجر وإعدادات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="835d2-106">Retail Modern POS (MPOS) and Cloud POS support environments where language settings and translations can vary between the store and user settings.</span></span> <span data-ttu-id="835d2-107">على سبيل المثال، يمكن أن يكون المتجر موجوداً في منطقة حيث تكون اللغة الإنجليزية الأكثر شيوعًا للعملاء، ولكن بعض العاملين يفضلون استخدام التطبيق بالترجمات الفرنسية.‬</span><span class="sxs-lookup"><span data-stu-id="835d2-107">For example, the store could be located in a region where English is most common for their customers, but some workers prefer to use the application with French translations.</span></span>

## <a name="data-language"></a><span data-ttu-id="835d2-108">لغة البيانات</span><span class="sxs-lookup"><span data-stu-id="835d2-108">Data language</span></span>
<span data-ttu-id="835d2-109">‏‫بغض النظر عن إعدادات المستخدم، ستستخدم نقطة البيع بالتجزئة الحديثة ونقطة بيع المجموعة إعدادات لغة المتاجر لتحديد الترجمات المستخدمة للبيانات.</span><span class="sxs-lookup"><span data-stu-id="835d2-109">Regardless of the user’s settings, MPOS and Cloud POS will always use the store's language settings to determine the translations used for data.</span></span> <span data-ttu-id="835d2-110">وهذا سيضمن أن كافة المستخدمين والعملاء سيكون لديهم تجربة متناسقة.</span><span class="sxs-lookup"><span data-stu-id="835d2-110">This will ensure that all users and customers will have a consistent experience.</span></span>  <span data-ttu-id="835d2-111">تتضمن أمثلة البيانات:‬</span><span class="sxs-lookup"><span data-stu-id="835d2-111">Examples of data include:</span></span>

-   <span data-ttu-id="835d2-112">المنتجات</span><span class="sxs-lookup"><span data-stu-id="835d2-112">Products</span></span>
-   <span data-ttu-id="835d2-113">السمات والقيم</span><span class="sxs-lookup"><span data-stu-id="835d2-113">Attributes and values</span></span>
-   <span data-ttu-id="835d2-114">أسماء الفئة</span><span class="sxs-lookup"><span data-stu-id="835d2-114">Category names</span></span>
-   <span data-ttu-id="835d2-115">إيصالات حركة المطبوعة أو مرسلة عبر البريد الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="835d2-115">Printed or emailed transaction receipts</span></span>
-   <span data-ttu-id="835d2-116">أسماء طريقة الدفع</span><span class="sxs-lookup"><span data-stu-id="835d2-116">Payment method names</span></span>
-   <span data-ttu-id="835d2-117">رسائل شاشة عرض سطرية</span><span class="sxs-lookup"><span data-stu-id="835d2-117">Line display messages</span></span>

<span data-ttu-id="835d2-118">سيتم استخدام لغة المتجر أيضًا لشاشة تسجيل الدخول إلى نقطة البيع الرئيسية، لأن المستخدم غير معروف قبل تسجيل الدخول.</span><span class="sxs-lookup"><span data-stu-id="835d2-118">The store’s language will also be used for the main POS login screen, since the user is not known before logging in.</span></span> <span data-ttu-id="835d2-119">إذا لم تتوفر ترجمة للغة المتجر، فإن نقطة البيع ستعود إلى اللغة الخاصة بالشركة.‬</span><span class="sxs-lookup"><span data-stu-id="835d2-119">If a translation is not available for the store’s language, the POS will revert to the company’s language.</span></span>

### <a name="configuring-the-stores-language-setting"></a><span data-ttu-id="835d2-120">تكوين إعدادات لغة المتجر</span><span class="sxs-lookup"><span data-stu-id="835d2-120">Configuring the store’s language setting</span></span>

<span data-ttu-id="835d2-121">يتم تعيين إعداد لغة المتجر من **جميع متاجر التجزئة** على الصفحة **متجر البيع بالتجزئة** ضمن **عام &gt; الإعدادات الإقليمية &gt; اللغة.</span><span class="sxs-lookup"><span data-stu-id="835d2-121">The store’s language setting is set from **All retail stores** on the **Retail Store** page under **General &gt; Regional Settings &gt; Language.</span></span> <span data-ttu-id="835d2-122">**استخدم القائمة المنسدلة لاختيار لغة لكل متجر.‬</span><span class="sxs-lookup"><span data-stu-id="835d2-122">**Use the drop down to choose the language for each store.</span></span>

## <a name="user-interface-language"></a><span data-ttu-id="835d2-123">لغة واجهة المستخدم</span><span class="sxs-lookup"><span data-stu-id="835d2-123">User interface language</span></span>
<span data-ttu-id="835d2-124">يحدد إعداد لغة مستخدم نقطة البيع الترجمات المستخدمة في واجهة مستخدم التطبيق.</span><span class="sxs-lookup"><span data-stu-id="835d2-124">The POS user’s language setting determines the translations used in the application user interface.</span></span> <span data-ttu-id="835d2-125">وهذا يتضمن كافة التسميات والقوائم التي لا تعتبر بيانات.‬</span><span class="sxs-lookup"><span data-stu-id="835d2-125">This includes all labels, menus, and lists that are not considered data.</span></span> <span data-ttu-id="835d2-126">‏‫يتمثل أحد الاستثناءات في النص المعروض على شبكات أزرار نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="835d2-126">One exception is the text that is displayed on POS button grids.</span></span> <span data-ttu-id="835d2-127">لا تدعم شبكات الأزرار الترجمات، لذلك فإنها سوف تُظهر النص دائمًا كما هو محدد على الزر.</span><span class="sxs-lookup"><span data-stu-id="835d2-127">The button grids don't support translations, so they will always show the text as defined on the button.</span></span> <span data-ttu-id="835d2-128">ولدعم الأزرار المترجمة، فإنه يجب عليك نسخ شبكات الأزرار المنفصلة وصيانها وتعيينها إلى المستخدمين حسب الاقتضاء.‬</span><span class="sxs-lookup"><span data-stu-id="835d2-128">In order to support translated buttons, you'll have to copy and maintain separate button grids and assign them to the users as appropriate.</span></span>

### <a name="configuring-the-users-language-setting"></a><span data-ttu-id="835d2-129">تكوين إعدادات لغة المستخدم</span><span class="sxs-lookup"><span data-stu-id="835d2-129">Configuring the user’s language setting</span></span>

<span data-ttu-id="835d2-130">يتم تعيين إعداد لغة مستخدم نقاط البيع من **جميع العمال** بصفحة **العامل** ضمن **‎البيع بالتجزئة &gt; اللغة**.</span><span class="sxs-lookup"><span data-stu-id="835d2-130">The POS user’s language setting is set from **All workers** on the **Worker** page under **Retail &gt; Language**.</span></span>  <span data-ttu-id="835d2-131">لم يتم التعيين إلى لا على علامة التبويب ملف التعريف الأساسي.  لا يتم استخدام هذا الإعداد بواسطة نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="835d2-131">It is not set on the main Profile tab.  This setting is not used by POS.</span></span> <span data-ttu-id="835d2-132">إذا لم يتم تعيين لغة المستخدم أو إذا تم تعيينها إلى لغة لا تتوفر فيها ترجمات، ستعود نقطة البيع إلى لغة المتجر.</span><span class="sxs-lookup"><span data-stu-id="835d2-132">If the user’s language is not set or it is set to a language where translations are not available, the POS will revert to the store’s language.</span></span>  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="835d2-133">** **</span><span class="sxs-lookup"><span data-stu-id="835d2-133">** **</span></span>       | <span data-ttu-id="835d2-134">**لغة واجهة المستخدم** ** **</span><span class="sxs-lookup"><span data-stu-id="835d2-134">**UI language** ** **</span></span>      | <span data-ttu-id="835d2-135">**لغة البيانات (المنتجات، تنسيقات الإيصالات، عرض الخط، إلخ)**</span><span class="sxs-lookup"><span data-stu-id="835d2-135">**Data language (products, receipt formats, line display, etc.)**</span></span> |
| <span data-ttu-id="835d2-136">**الشركة**</span><span class="sxs-lookup"><span data-stu-id="835d2-136">**Company**</span></span> | <span data-ttu-id="835d2-137">افتراضي</span><span class="sxs-lookup"><span data-stu-id="835d2-137">Default</span></span>                    | <span data-ttu-id="835d2-138">افتراضي</span><span class="sxs-lookup"><span data-stu-id="835d2-138">Default</span></span>                                                           |
| <span data-ttu-id="835d2-139">**المتجر**</span><span class="sxs-lookup"><span data-stu-id="835d2-139">**Store**</span></span>   | <span data-ttu-id="835d2-140">يتجاوز الشركة</span><span class="sxs-lookup"><span data-stu-id="835d2-140">Overrides company</span></span>          | <span data-ttu-id="835d2-141">يتجاوز الشركة</span><span class="sxs-lookup"><span data-stu-id="835d2-141">Overrides company</span></span>                                                 |
| <span data-ttu-id="835d2-142">**المستخدم**</span><span class="sxs-lookup"><span data-stu-id="835d2-142">**User**</span></span>    | <span data-ttu-id="835d2-143">يتجاوز المتجر أو الشركة</span><span class="sxs-lookup"><span data-stu-id="835d2-143">Overrides store or company</span></span> | <span data-ttu-id="835d2-144">أبدًا</span><span class="sxs-lookup"><span data-stu-id="835d2-144">Never</span></span>                                                             |






