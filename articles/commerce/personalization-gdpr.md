---
title: إلغاء الاشتراك في التوصيات المخصصة
description: يشرح هذا الموضوع كيفية السماح للعملاء بالانسحاب من تلقي التوصيات المخصصة في Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e65fc54f87664caec95b2bc2c579d0820ae08c0f
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477674"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="ea0a7-103">إلغاء الاشتراك في التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="ea0a7-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ea0a7-104">يشرح هذا الموضوع كيفية السماح للعملاء بالانسحاب من تلقي التوصيات المخصصة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ea0a7-105">واثناء إنشاء الحساب، يتم إعداد العملاء الجدد تلقائيا لتلقي التوصيات المخصصة.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-105">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="ea0a7-106">ومع ذلك، يوفر Dynamics 365 Commerce يوفر طرقا متنوعة لبائعي التجزئة السماح للمستخدمين بالخروج من هذه التوصيات وتقييد معالجه البيانات الشخصية الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-106">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="ea0a7-107">سوف يتوقف المستخدمون المصادقون الذين يرفضوا الخروج من التوصيات المخصصة فورا من مشاهده القوائم الشخصية.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-107">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="ea0a7-108">بالإضافة إلى ذلك، ستتم أزاله كافة البيانات الشخصية التي تم تجميعها لإضفاء طابع شخصي من نماذج التوصيات المخصصة.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-108">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="ea0a7-109">لمزيد من المعلومات حول توصيات المنتجات المخصصة، راجع [تمكين التوصيات المخصصة](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="ea0a7-109">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="ea0a7-110">طرق لبائعي التجزئة لتنفيذ تجربه للغاء الاشتراك</span><span class="sxs-lookup"><span data-stu-id="ea0a7-110">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="ea0a7-111">لدى بائعي التجزئة ثلاث طرق لتنفيذ تجربه إلغاء الاشتراك.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-111">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="ea0a7-112">إلغاء الاشتراك نيابةً عن المستخدمين</span><span class="sxs-lookup"><span data-stu-id="ea0a7-112">Opting out on behalf of users</span></span>

<span data-ttu-id="ea0a7-113">في أداره الحساب في مكتب التجارة التجارية، يمكن لبائعي التجزئة إلغاء الاشتراك بالنيابة عن المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-113">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="ea0a7-114">من الصفحة الرئيسية للمكتب الخلفي، ابحث عن **جميع العملاء**.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-114">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="ea0a7-115">ابحث عن عميل وحدده، ثم حدد علامة التبويب السريع **Retail**.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-115">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![علامة التبويب السريع Retail](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="ea0a7-117">ضمن **الخصوصية**، قم بتعيين خيار **تعطيل التخصيص** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-117">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![إعدادات الخصوصية](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="ea0a7-119">حدد **حفظ** ثم أغلق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-119">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="ea0a7-120">تجربه إلغاء الاشتراك المستند إلى الوحدة النمطية</span><span class="sxs-lookup"><span data-stu-id="ea0a7-120">Module-based opt-out experience</span></span>

<span data-ttu-id="ea0a7-121">يمكن لبائعي التجزئة السماح للمستخدمين المصادقين بالاشتراك في التوصيات المخصصة بأنفسهم.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-121">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="ea0a7-122">لتوفير تجربه إلغاء الاشتراك هذه، أضف الوحدة النمطية للغاء اشتراك المستخدم إلى صفحات ملف تعريف حساب العميل.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-122">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="ea0a7-123">الملحقات المخصصة</span><span class="sxs-lookup"><span data-stu-id="ea0a7-123">Custom extensions</span></span>

<span data-ttu-id="ea0a7-124">يمكن لبائعي التجزئة إنشاء الملحقات الخاصة بهم لأداره تجربه الرفض للمستخدمين.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-124">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="ea0a7-125">لمزيد من المعلومات، راجع [استدعاء واجهات برمجة تطبيقات Retail Server](e-commerce-extensibility/call-retail-server-apis.md) و[توسعة القنوات على الإنترنت](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="ea0a7-125">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="ea0a7-126">الحصول على نسخه رقميه من التوصيات الشخصية البيانات نيابة عن مستخدم تمت مصادقته</span><span class="sxs-lookup"><span data-stu-id="ea0a7-126">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="ea0a7-127">قد يرغب العملاء في الحصول على نسخه رقميه من بياناتهم الشخصية ويظهر أيضا عرضا مصدرا لنتائج التوصيات الخاصة بهم.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-127">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="ea0a7-128">إذا طلب أحد العملاء هذه المعلومات، فيجب ان يقوم بائع التجزئة بإنشاء ملحق مخصص يقوم باستدعاء واجهه برمجه تطبيق خادم البيع بالتجزئة واستعلامات عن النتائج الكاملة من **العناصر المقترحة لك**، وذلك استنادا إلى معرف العميل الخاص بالعميل.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-128">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="ea0a7-129">ويمكن بعد ذلك تصدير النتائج بتنسيق قيم مفصوله بفواصل (CSV) ومشاركتها مع العميل.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-129">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="ea0a7-130">يوضح المثال التالي كيف يمكن لبائع التجزئة إنجاز هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-130">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="ea0a7-131">يقوم بائع التجزئة بإنشاء ملحق مخصص لجذب التوصيات الشخصية بالبيانات نيابة عن المستخدم.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-131">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="ea0a7-132">للحصول على معلومات حول كيفيه إنشاء الوحدات النمطية، واستنساخ الوحدات النمطية، واستدعاء واجهات برمجة تطبيقات Retail Server، واستدعاء إجراءات البيانات، راجع [توسيع القنوات على الإنترنت](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="ea0a7-132">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="ea0a7-133">يقوم الملحق المخصص باستدعاء إجراء بيانات **الحصول على التوصيات** الأساسي للحصول على توصيات ويقوم بتمرير المعلومات المطلوبة اليه، وذلك استنادا إلى متطلبات القائمة.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-133">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="ea0a7-134">في حاله قائمة **العناصر المقترحة لك**، يجب ان يقوم الامتداد بتمرير اسم القائمة الصحيحة ومعرف العميل إلى إجراء البيانات.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-134">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="ea0a7-135">أحدي الطرق لإنشاء الملحق المخصص هي استنساخ الوحدة النمطية لمجموعه المنتجات الموجودة والتي تستخدم لإرجاع نتائج التوصيات.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-135">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="ea0a7-136">ومن خلال استنساخ هذه الوحدة النمطية الموجودة، يمكن لبائع التجزئة تعديل التعليمات البرمجية الموجودة وأضافه زر جديد يصدر نتائج التوصيات إلى ملف CSV.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-136">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="ea0a7-137">لمزيد من المعلومات، راجع [استنساخ وحدة مكتبة وحدات نمطية](e-commerce-extensibility/clone-starter-module.md) و[الوحدات النمطية لمجموعة المنتجات](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ea0a7-137">For more information, see [Clone a module library module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="ea0a7-138">للحصول على عرض كامل لمكتبه واجهه برمجه تطبيقات Retail Server، راجع [عميل Retail Server وواجهة برمجة تطبيقات العملاؤ](dev-itpro/retail-server-customer-consumer-api.md).</span><span class="sxs-lookup"><span data-stu-id="ea0a7-138">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="ea0a7-139">بعد إنشاء الملحق المخصص، يمكن لبائع التجزئة تصدير ملف CSV من كافة نتائج التوصيات، استنادا إلى معرف العميل الفريد للمستخدم الذي تمت مصادقته.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-139">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="ea0a7-140">يمكن لبائع التجزئة مشاركه ملف CSV الذي تم تصديره والذي يحتوي على القائمة الشخصية الكاملة للمنتجات الموصي بها مع المستخدم المصادق عليه.</span><span class="sxs-lookup"><span data-stu-id="ea0a7-140">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea0a7-141">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="ea0a7-141">Additional resources</span></span>

[<span data-ttu-id="ea0a7-142">نظرة عامة على توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="ea0a7-142">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ea0a7-143">تمكين Azure Data Lake Storage في بيئة Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ea0a7-143">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="ea0a7-144">تمكين توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="ea0a7-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="ea0a7-145">تمكين التوصيات المخصصة</span><span class="sxs-lookup"><span data-stu-id="ea0a7-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="ea0a7-146">تمكين توصيات "تسوق منتجات تبدو مماثلة"</span><span class="sxs-lookup"><span data-stu-id="ea0a7-146">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="ea0a7-147">إضافة توصيات المنتجات على نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="ea0a7-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="ea0a7-148">إضافة توصيات إلى شاشة المعاملة</span><span class="sxs-lookup"><span data-stu-id="ea0a7-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="ea0a7-149">إدارة نتائج توصيات الذكاء الاصطناعي والتعلم الآلي (AI-ML)</span><span class="sxs-lookup"><span data-stu-id="ea0a7-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="ea0a7-150">إنشاء توصيات مختارة يدويًا</span><span class="sxs-lookup"><span data-stu-id="ea0a7-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="ea0a7-151">إنشاء توصيات بواسطة بيانات العرض التوضيحي</span><span class="sxs-lookup"><span data-stu-id="ea0a7-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="ea0a7-152">الأسئلة المتداولة حول توصيات المنتجات</span><span class="sxs-lookup"><span data-stu-id="ea0a7-152">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
