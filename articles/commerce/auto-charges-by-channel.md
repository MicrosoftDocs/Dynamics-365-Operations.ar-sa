---
title: تمكين التكاليف التلقائية وتكوينها حسب القناة
description: يوضح هذا الموضوع كيفية تمكين التكاليف التلقائية وتكوينها حسب القناة في Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 23d02cf96faf3753303435acc148bf71e487d791
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799892"
---
# <a name="enable-and-configure-auto-charges-by-channel"></a><span data-ttu-id="0f2c5-103">تمكين التكاليف التلقائية وتكوينها حسب القناة</span><span class="sxs-lookup"><span data-stu-id="0f2c5-103">Enable and configure auto charges by channel</span></span>

<span data-ttu-id="0f2c5-104">يوضح هذا الموضوع كيفية تمكين التكاليف التلقائية وتكوينها حسب القناة في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-104">This topic explains how to enable and configure automatic charges (auto charges) by channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0f2c5-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="0f2c5-105">Overview</span></span>

<span data-ttu-id="0f2c5-106">وقد تواجه وحدات سيناريو حيث يجب تطبيق رسوم التدوير أو رسوم أخرى على مجموعة من المنتجات التي يتم بيعها في جميع المتاجر أو بعضها في ولاية معينة (على سبيل المثال، كاليفورنيا).</span><span class="sxs-lookup"><span data-stu-id="0f2c5-106">You might have scenarios where recycling fees or other fees must be applied to a group of products that are sold in all or some stores in a specific state (for example, California).</span></span> <span data-ttu-id="0f2c5-107">تتيح لك ميزة **تمكين تصفية التكاليف التلقائية حسب القناة** في Commerce تحديد التكاليف التلقائية حسب القناة (على سبيل المثال، قناة تقليدية معينة).</span><span class="sxs-lookup"><span data-stu-id="0f2c5-107">The **Enable filter auto charges by channel** feature in Commerce lets you specify auto charges by channel (for example, a specific brick-and-mortar channel).</span></span> <span data-ttu-id="0f2c5-108">هذه الميزة متوفرة في Dynamics 365 Commerce الإصدار 10.0.10 والإصدارات الأحدث.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-108">This feature is available in Dynamics 365 Commerce version 10.0.10 and later.</span></span>

<span data-ttu-id="0f2c5-109">لتمكين التكاليف التلقائية حسب القناة وتكوينها، يجب إكمال المهام التالية:</span><span class="sxs-lookup"><span data-stu-id="0f2c5-109">To enable and configure auto charges by channel, you must complete the following tasks:</span></span>

- <span data-ttu-id="0f2c5-110">قم بتشغيل ميزة **تمكين تصفية التكاليف التلقائية حسب القناة**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-110">Turn on the **Enable filter auto charges by channel** feature.</span></span>
- <span data-ttu-id="0f2c5-111">قم بتكوين غرض التدرج الهرمي للمؤسسة</span><span class="sxs-lookup"><span data-stu-id="0f2c5-111">Configure the organization hierarchy purpose.</span></span>
- <span data-ttu-id="0f2c5-112">حدد التكاليف التلقائية حسب القناة.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-112">Define auto charges by channel.</span></span>

> [!NOTE]
> <span data-ttu-id="0f2c5-113">تعمل ميزة **تمكين تصفية التكاليف التلقائية حسب القناة** فقط إذا تم تشغيل ميزة التكاليف التلقائية المتقدمة أيضًا.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-113">The **Enable filter auto charges by channel** feature works only if the advanced auto charges feature is also turned on.</span></span> <span data-ttu-id="0f2c5-114">للحصول على معلومات حول كيفية تشغيل ميزة التكاليف التلقائية المتقدمة، راجع [التكاليف التلقائية المتقدمة ‬للقناة متعددة الاتجاهات](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="0f2c5-114">For information about how to turn on the advanced auto charges feature, see [Omni-channel advanced auto charges](omni-auto-charges.md).</span></span>

## <a name="turn-on-the-enable-filter-auto-charges-by-channel-feature"></a><span data-ttu-id="0f2c5-115">قم بتشغيل ميزة تمكين تصفية التكاليف التلقائية حسب القناة.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-115">Turn on the Enable filter auto charges by channel feature</span></span>

<span data-ttu-id="0f2c5-116">لتمكين التكاليف التلقائية حسب القناة في Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-116">To enable auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="0f2c5-117">انتقل إلى **إدارة النظام \> مساحات العمل \> إدارة الميزات**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-117">Go to **System administrator \> Workspaces \> Feature management**.</span></span>
1. <span data-ttu-id="0f2c5-118">في علامة التبويب **غير ممكّن**، في قائمة **اسم الميزة**، ابحث عن **تمكين تصفية التكاليف التلقائية حسب القناة** وحددها.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-118">On the **Not enabled** tab, in the **Feature name** list, find and select **Enable filter auto charges by channel**.</span></span>
1. <span data-ttu-id="0f2c5-119">في الزاوية اليمنى السفلية اليمنى، حدد **تمكين الآن**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-119">In the lower-right corner, select **Enable now**.</span></span> <span data-ttu-id="0f2c5-120">بعد تشغيل الميزة، ستظهر في القائمة الموجودة ضمن علامة التبويب **الكل**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-120">After the feature has been turned on, it will appear in the list on the **All** tab.</span></span>
1. <span data-ttu-id="0f2c5-121">انتقل إلى **البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> جدول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-121">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="0f2c5-122">في الجزء الأيمن، ابحث عن وظيفة **1110** (**التكوين العمومي**) وحددها.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-122">In the left pane, find and select the **1110** (**Global configuration**) job.</span></span>
1. <span data-ttu-id="0f2c5-123">في جزء الإجراء، حدد **التشغيل الآن** لنشر تغييرات التكوين.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-123">On the Action Pane, select **Run now** to propagate the configuration changes.</span></span>

> [!WARNING]
> <span data-ttu-id="0f2c5-124">إذا قمت بإيقاف تشغيل ميزة **تمكين تصفية التكاليف التلقائية حسب القناة** بعد استخدامها بالفعل، سوف لن يظهر حقل **علاقة قناة البيع بالتجزئة** تحت **التكاليف التلقائية** بعد الآن، وستفقد كافة التكوينات الموجودة.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-124">If you turn off the **Enable filter auto charges by channel** feature after you've already used it, the **Retail channel relation** field under **Auto charges** will no longer appear, and you will lose all existing configurations.</span></span> <span data-ttu-id="0f2c5-125">إذا كانت عملية إزالة تكوينات **علاقة قناة البيع بالتجزئة** ستسبب تكرار قواعد التكاليف التلقائية، ستفشل محاولة إيقاف تشغيل هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-125">If removal of the **Retail channel relation** configurations will cause auto charges rules to be duplicated, an attempt to turn off the feature will fail.</span></span> <span data-ttu-id="0f2c5-126">قبل إيقاف تشغيل الميزة، تأكد من مراجعة كافة قواعد التكاليف التلقائية وإجراء أي تغييرات مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-126">Before you turn off the feature, be sure to review all auto charges rules and make any required changes.</span></span>

## <a name="configure-the-organization-hierarchy-purpose"></a><span data-ttu-id="0f2c5-127">تكوين غرض التدرج الهرمي للمؤسسة</span><span class="sxs-lookup"><span data-stu-id="0f2c5-127">Configure the organization hierarchy purpose</span></span>

<span data-ttu-id="0f2c5-128">تم إنشاء غرض التدرج الهرمي للمؤسسة الذي يسمى **التكلفة التلقائية للبيع بالتجزئة** لإدارة التدرج الهرمي للتكاليف التلقائية حسب القناة.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-128">A new organization hierarchy purpose that is named **Retail auto charge** has been created to manage the hierarchy for auto charges by channel.</span></span>

<span data-ttu-id="0f2c5-129">لتعيين تدرج هرمي افتراضي لغرض التدرج الهرمي للمؤسسة في Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-129">To assign a default hierarchy to an organization hierarchy purpose in Commerce, follow these steps.</span></span>
        
1. <span data-ttu-id="0f2c5-130">انتقل إلى **إدارة المؤسسة** \> المؤسسات \> أغراض التدرج الهرمي للمؤسسات.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-130">Go to **Organization administration \> Organizations \> Organization hierarchy purposes**.</span></span>
1. <span data-ttu-id="0f2c5-131">في الجزء الأيمن، حدد **التكلفة التلقائية للبيع بالتجزئة**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-131">In the left pane, select **Retail auto charge**.</span></span>
1. <span data-ttu-id="0f2c5-132">تحت **التدرجات الهرمية المعينة**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-132">Under **Assigned hierarchies**, select **Add**.</span></span>
1. <span data-ttu-id="0f2c5-133">في مربع الحوار **التدرجات الهرمية للمؤسسات**، حدد تدرجًا هرميًا للمؤسسة (على سبيل المثال، **متاجر البيع بالتجزئة حسب المنطقة**)، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-133">In the **Organization hierarchies** dialog box, select an organization hierarchy (for example, **Retail Stores by Region**), and then select **OK**.</span></span>
1. <span data-ttu-id="0f2c5-134">تحت **التدرجات الهرمية المعينة**، حدد **تعيين كافتراضي**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-134">Under **Assigned hierarchies**, select **Set as default**.</span></span>
1. <span data-ttu-id="0f2c5-135">انتقل إلى **البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> جدول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="0f2c5-136">في الجزء الأيمن، ابحث عن وظيفة **1040** (**المنتجات**) وحددها.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-136">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="0f2c5-137">في جزء الإجراءات، حدد **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-137">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="0f2c5-138">كرر الخطوتين السابقتين لتشغيل الوظيفتين **1070** (**تكوين القناة**) و **1110** (**التكوين العمومي**).</span><span class="sxs-lookup"><span data-stu-id="0f2c5-138">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>

![تكوين غرض التدرج الهرمي لمؤسسة للتكلفة التلقائية للبيع بالتجزئة](media/Auto-charges-org-hierarchy-purpose.png)

## <a name="define-auto-charges-by-channel"></a><span data-ttu-id="0f2c5-140">تحديد التكاليف التلقائية حسب القناة</span><span class="sxs-lookup"><span data-stu-id="0f2c5-140">Define auto charges by channel</span></span>

<span data-ttu-id="0f2c5-141">بعد تشغيل ميزة **تمكين تصفية التكاليف التلقائية حسب القناة** وتكوين غرض التدرج المؤسسة لـ **التكلفة التلقائية للبيع بالتجزئة**، يمكن تحديد التكاليف التلقائية حسب القناة إما على مستوى عنوان الأمر أو على مستوى بند الأمر.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-141">After you've turned on the **Enable filter auto charges by channel** feature and configured the **Retail auto charge** organization hierarchy purpose, auto charges by channel can be defined at either the order header level or the order line level.</span></span>

<span data-ttu-id="0f2c5-142">لتحديد التكاليف التلقائية حسب القناة في Commerce، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-142">To define auto charges by channel in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="0f2c5-143">انتقل إلى **الحسابات المدينة \> إعداد التكاليف \> التكاليف التلقائية**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-143">Go to **Accounts receivable \> Charges setup \> Auto charges**.</span></span>
1. <span data-ttu-id="0f2c5-144">في الجزء الأيمن، في حقل **المستوي**، حدد إما **رأس** أو **بند**، وفقًا لمتطلبات العمل.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-144">In the left pane, in the **Level** field, select either **Header** or **Line**, depending on your business requirements.</span></span>
1. <span data-ttu-id="0f2c5-145">في الحقل **كود قناة البيع بالتجزئة**، حدد كود القناة المناسب (على سبيل المثال، **جدول** أو **مجموعة**).</span><span class="sxs-lookup"><span data-stu-id="0f2c5-145">In the **Retail channel code** field, select the appropriate channel code (for example, **Table** or **Group**).</span></span> <span data-ttu-id="0f2c5-146">في حال استخدام الإعداد الافتراضي **الكل**، يتم تطبيق قواعد التكلفة على كافة القنوات.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-146">If the default setting, **All**, is used, charge rules are applied to all channels.</span></span>

    - <span data-ttu-id="0f2c5-147">ذا قمت بتحديد **مجموعة‏‎**، فتأكد من إنشاء مجموعة تكاليف قناة البيع بالتجزئة في **Retail and Commerce \> إعداد القناة \> التكاليف \> مجموعات تكاليف قنوات البيع بالتجزئة**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-147">If you select **Group**, make sure that a retail channel charges group is created at **Retail and Commerce \> Channel setup \> Charges \> Retail channel charge groups**.</span></span>
    - <span data-ttu-id="0f2c5-148">إذا قمت بتحديد **جدول**، يمكنك تحديد قناة معينة (على سبيل المثال، **سان فرانسيسكو**) في الحقل **علاقة قناة البيع بالتجزئة**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-148">If you select **Table**, you can select a specific channel (for example, **San Francisco**) in the **Retail channel relation** field.</span></span>

1. <span data-ttu-id="0f2c5-149">انتقل إلى **البيع بالتجزئة والتجارة \> تكنولوجيا معلومات البيع بالتجزئة والتجارة \> جدول التوزيع**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-149">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="0f2c5-150">في الجزء الأيمن، ابحث عن وظيفة **1040** (**المنتجات**) وحددها.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-150">In the left pane, find and select the **1040** (**Products**) job.</span></span>
1. <span data-ttu-id="0f2c5-151">في جزء الإجراءات، حدد **تشغيل الآن**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-151">On the Action Pane, select **Run now**.</span></span>
1. <span data-ttu-id="0f2c5-152">كرر الخطوتين السابقتين لتشغيل الوظيفتين **1070** (**تكوين القناة**) و **1110** (**التكوين العمومي**).</span><span class="sxs-lookup"><span data-stu-id="0f2c5-152">Repeat the previous two steps to run the **1070** (**Channel configuration**) and **1110** (**Global configuration**) jobs.</span></span>
    
![التكاليف التلقائية المحددة حسب القناة](media/Auto-charges-line-charge-by-channel.png)

## <a name="example-scenario"></a><span data-ttu-id="0f2c5-154">سيناريو كمثال</span><span class="sxs-lookup"><span data-stu-id="0f2c5-154">Example scenario</span></span>

<span data-ttu-id="0f2c5-155">يوضح المثال التالي الخطوات المطلوبة لتكوين منتج بحيث يتم فرض رسوم إعادة التدوير عند بيع المنتج من خلال قناة سان فرانسيسكو التقليدية.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-155">The following example outlines the steps that are required to configure a product so that recycling fees are charged when the product is sold through a San Francisco brick-and-mortar channel.</span></span> <span data-ttu-id="0f2c5-156">يوضح المثال أيضًا كيفية ظهور التكاليف التلقائية في تطبيق نقطة البيع في Commerce.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-156">The example also shows how the auto charges appear in the Commerce point of sale (POS) application.</span></span>

<span data-ttu-id="0f2c5-157">تقوم المؤسسة بتحديد كود التكاليف المسماة **إعادة التدوير**، كما هو مبين في الرسم التوضيحي التالي.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-157">The organization defines a charges code that is named **RECYCLE**, as shown in the following illustration.</span></span>

![كود تكاليف إعادة التدوير](media/Auto-charges-charge-code.png)

<span data-ttu-id="0f2c5-159">يتم إنشاء تكلفة تلقائية على مستوى البند.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-159">An auto charge is created at the line level.</span></span> <span data-ttu-id="0f2c5-160">لها التكوين التالي:</span><span class="sxs-lookup"><span data-stu-id="0f2c5-160">It has the following configuration:</span></span>

- <span data-ttu-id="0f2c5-161">يتم تعيين‏‎ حقل **كود الحساب** إلى **الكل**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-161">The **Account code** field is set to **All**.</span></span>
- <span data-ttu-id="0f2c5-162">يتم تعيين‏‎ حقل **كود الصنف** إلى **جدول**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-162">The **Item code** field is set to **Table**.</span></span>
- <span data-ttu-id="0f2c5-163">يتم تعيين **علاقة الصنف** إلى معرف المنتج **91001**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-163">The **Item relation** field is set to product ID **91001**.</span></span>
- <span data-ttu-id="0f2c5-164">يتم تعيين‏‎ حقل **كود وضع التسليم** إلى **الكل**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-164">The **Mode of delivery code** field is set to **All**.</span></span>
- <span data-ttu-id="0f2c5-165">يتم تعيين‏‎ حقل **كود قناة البيع بالتجزئة** إلى **جدول**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-165">The **Retail channel code** field is set to **Table**.</span></span>
- <span data-ttu-id="0f2c5-166">يتم تعيين حقل **علاقة قناه البيع بالتجزئة** إلى متجر  **سان فرانسيسكو**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-166">The **Retail channel relation** field is set to the **San Francisco** store.</span></span>

<span data-ttu-id="0f2c5-167">يتم إنشاء بند التكاليف التلقائية.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-167">An auto charges line is created.</span></span> <span data-ttu-id="0f2c5-168">لها التكوين التالي:</span><span class="sxs-lookup"><span data-stu-id="0f2c5-168">It has the following configuration:</span></span>

- <span data-ttu-id="0f2c5-169">يتم تعيين حقل **العملة** إلى **دولار أمريكي**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-169">The **Currency** field is set to **USD**.</span></span>
- <span data-ttu-id="0f2c5-170">يتم تعيين‏‎ حقل **كود التكاليف** إلى **إعادة التدوير**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-170">The **Charges code** field is set to **RECYCLE**.</span></span>
- <span data-ttu-id="0f2c5-171">يتم تعيين‏‎ حقل **الفئة** إلى **ثابت**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-171">The **Category** field is set to **Fixed**.</span></span>
- <span data-ttu-id="0f2c5-172">ويتم تعيين حقل **التكاليف** إلى **6.25$**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-172">The **Charges** field is set to **$6.25**.</span></span>

![تكوين التكلفة التلقائية على مستوى البند وبند التكاليف التلقائية](media/Auto-charges-recyclingfee-line-fee.png)

<span data-ttu-id="0f2c5-174">في تطبيق نقطه البيع POS، يتم إنشاء أمر مبيعات في قناة متجر **سان فرانسيسكو**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-174">In the POS application, a sales order is created in the **San Francisco** store channel.</span></span> <span data-ttu-id="0f2c5-175">يعرض بند **التكاليف** رسوم إعادة التدوير **$6.25**.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-175">The **Charges** line shows the recycling fee of **$6.25**.</span></span>

<span data-ttu-id="0f2c5-176">ومن خلال تحديد **خيارات الحركة \> التكاليف \> إدارة التكاليف** في تطبيق POS نقطه البيع، يمكنك عرض كود التكاليف ووصف رسوم إعادة التدوير.</span><span class="sxs-lookup"><span data-stu-id="0f2c5-176">By selecting **Transaction options \> Charges \> Manage charges** in the POS application, you can view the charges code and description for the recycling fee.</span></span>

![رسوم إعادة التدوير في تطبيق نقطة البيع POS](media/pos-auto-charges-recyclingfee-line-fee.png)

## <a name="additional-resources"></a><span data-ttu-id="0f2c5-178">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0f2c5-178">Additional resources</span></span>

[<span data-ttu-id="0f2c5-179">التكاليف التلقائية المتقدمة ‬للقناة متعددة الاتجاهات</span><span class="sxs-lookup"><span data-stu-id="0f2c5-179">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="0f2c5-180">توزيع تكاليف الرأس لمطابقة بنود المبيعات</span><span class="sxs-lookup"><span data-stu-id="0f2c5-180">Prorate header charges to matching sales lines</span></span>](pro-rate-charges-matching-lines.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]