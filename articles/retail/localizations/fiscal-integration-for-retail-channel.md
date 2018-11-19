---
title: "التكامل المالي لقناة البيع بالتجزئة"
description: "يوفر هذا الموضوع نظرة عامة على تكامل Retail POS المالي."
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: ar-sa
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a><span data-ttu-id="3fc3f-103">التكامل المالي لقناة البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="3fc3f-103">Fiscal integration for Retail channel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fc3f-104">يقدم هذا الموضوع نظرة عامة على وظائف التكامل المالي المتوفرة في Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-104">This topic is an overview of the fiscal integration functionality that is available in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="3fc3f-105">وتعتبر وظيفة التكامل المالي إطار عمل تم تصميمه لدعم القوانين المالية المحلية التي تهدف إلى لمنع الاحتيال في مجال البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-105">The fiscal integration functionality is a framework designed to support local fiscal laws that are aimed to prevent fraud in the Retail industry.</span></span> <span data-ttu-id="3fc3f-106">تتضمن السيناريوهات النموذجية التي يمكن تغطيتها باستخدام التكامل المالي:</span><span class="sxs-lookup"><span data-stu-id="3fc3f-106">Typical scenarios that could be covered by using fiscal integration include:</span></span>

- <span data-ttu-id="3fc3f-107">طباعة إيصال مالي وتقديمه للعميل.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-107">Printing a fiscal receipt and giving it to the customer.</span></span>
- <span data-ttu-id="3fc3f-108">حماية عملية إرسال المعلومات المتعلقة بالمبيعات والمرتجعات التي يتم تنفيذها في نقطة بيع إلى خدمة خارجية توفرها الهيئة المختصة.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-108">Securing the submission of the information related to sales and returns performed on POS to an external service provided by the authority.</span></span>
- <span data-ttu-id="3fc3f-109">استخدام حماية البيانات بواسطة توقيع رقمي معتمد من قبل الهيئة المختصة.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-109">Using data protection with a digital signature authorized by the authority.</span></span>

<span data-ttu-id="3fc3f-110">يوفر هذا الموضوع إرشادات لإعداد التكامل المالي لتمكين المستخدمين تنفيذ المهام التالية.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-110">This topic provides guidelines for setting up fiscal integration so users can perform the following tasks.</span></span> 

- <span data-ttu-id="3fc3f-111">تكوين الموصلات المالية‬، وهي أو خدمات مالية تُستخدم لأغراض التسجيل المالي مثل حفظ التواقيع الرقمية وإرسال البيانات المالية بطريقة آمنة.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-111">Configure fiscal connectors, which are fiscal devices or services used for fiscal registration purposes like saving, digital signatures, and secured submission of fiscal data.</span></span>
- <span data-ttu-id="3fc3f-112">تكوين موفر المستندات، الذي يقوم بتعريف أسلوب إخراج وخوارزمية تتعلق بإنشاء المستندات المالية.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-112">Configure the document provider, which defines an output method and an algorithm of fiscal document generation.</span></span>
- <span data-ttu-id="3fc3f-113">تكوين عملية التسجيل المالي التي تحدد سلسلة من الخطوات ومجموعة من الموصلات المستخدمة في كل خطوة.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-113">Configure the fiscal registration process, which is defines a sequence of steps and a group of connectors used on each step.</span></span>
- <span data-ttu-id="3fc3f-114">تعيين عمليات التسجيل المالي لملفات تعريف وظائف نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-114">Assign fiscal registration processes to POS functionality profiles.</span></span>
- <span data-ttu-id="3fc3f-115">قم بتعيين ملفات التعريف التقنية للموصلات‬، إما إلى ملفات تعريف الأجهزة (للموصلات المالية المحلية) أو إلى ملفات تعريف وظائف نقطة البيع (لأنواع الموصلات المالية الأخرى).</span><span class="sxs-lookup"><span data-stu-id="3fc3f-115">Assign connector technical profiles, either to hardware profiles (for the local fiscal connectors) or to POS functionality profiles (for other fiscal connector types).</span></span>

## <a name="fiscal-integration-execution-flow"></a><span data-ttu-id="3fc3f-116">سير عمل تنفيذ التكامل المالي</span><span class="sxs-lookup"><span data-stu-id="3fc3f-116">Fiscal integration execution flow</span></span>
<span data-ttu-id="3fc3f-117">يوضح السيناريو التالي سير العمل الشائع لتنفيذ التكامل المالي.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-117">The following scenario shows the common fiscal integration execution flow.</span></span>

1. <span data-ttu-id="3fc3f-118">تهيئة عملية التسجيل المالي.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-118">Initialization of the fiscal registration process.</span></span>
  
   <span data-ttu-id="3fc3f-119">بعد تنفيذ بعض الإجراءات التي تتطلب التسجيل المالي، مثلاً بعد تنفيذ حركة بيع بالتجزئة، ترتبط عملية التسجيل المالي بملف التعريف الحالي لوظائف نقطة البيع‬.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-119">After performing some actions where fiscal registration is required, such as after a retail transaction has been concluded, the fiscal registration process is associated with the current POS functionality profile.</span></span>

1. <span data-ttu-id="3fc3f-120">البحث عن موصل مالي.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-120">Search for a fiscal connector.</span></span>
   
   <span data-ttu-id="3fc3f-121">لكل خطوة تسجيل مالي مضمنة في عملية التسجيل المالي، يقوم النظام بمطابقة قائمة الموصلات المالية.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-121">For each fiscal registration step included in the fiscal registration process, the system matches the list of fiscal connectors.</span></span> <span data-ttu-id="3fc3f-122">تتضمن هذه الموصلات ملف تعريف وظيفيًا في مجموعة الموصلات المحددة، مع قائمة بالموصلات التي لديها ملف تعريف تقني يرتبط بملف تعريف الأجهزة الحالي (لنوع موصل يساوي **محلي** فقط) أو بملف تعريف وظائف نقطة البيع‬ الحالي (لأنواع الموصلات الأخرى).</span><span class="sxs-lookup"><span data-stu-id="3fc3f-122">These connectors have a functional profile included in the specified connector group, with a list of connectors that have a technical profile associated with the current hardware profile (for a connector type that equals **Local** only) or with the current POS functionality profile (for other connector types).</span></span>
   
1. <span data-ttu-id="3fc3f-123">تنفيذ التكامل المالي.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-123">Perform the fiscal integration.</span></span>

   <span data-ttu-id="3fc3f-124">يقوم النظام بتنفيذ كافة الإجراءات الضرورية المحددة بواسطة تجميع يرتبط بالموصل الذي تم العثور عليه.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-124">The system executes all necessary actions defined by an assembly linked with the found connector.</span></span> <span data-ttu-id="3fc3f-125">ويتم ذلك وفقًا لإعدادات ملف التعريف الوظيفي وملف التعريف التقني التي تم العثور عليها في الخطوة السابقة لهذا الموصل.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-125">This is done in accordance with the settings of the functional profile and technical profile that were found on the previous step for this connector.</span></span>

## <a name="setup-needed-before-using-fiscal-integration"></a><span data-ttu-id="3fc3f-126">الإعداد المطلوب قبل استخدام التكامل المالي</span><span class="sxs-lookup"><span data-stu-id="3fc3f-126">Setup needed before using fiscal integration</span></span>
<span data-ttu-id="3fc3f-127">قبل استخدام وظيفة التكامل المالي، يجب تحديد الإعدادات التالية:</span><span class="sxs-lookup"><span data-stu-id="3fc3f-127">Before using the fiscal integration functionality, you should define the following settings:</span></span>

- <span data-ttu-id="3fc3f-128">تعريف التسلسل الرقمي في صفحة **معلمات البيع بالتجزئة‬** لرقم ملف تعريف الوظائف المالية.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-128">Define the number sequence on the **Retail parameters** page for the fiscal functional profile number.</span></span>
  
- <span data-ttu-id="3fc3f-129">تعريف التسلسلات الرقمية في صفحة **المعلمات المشتركة للبيع بالتجزئة‬** للمراجع التالية:</span><span class="sxs-lookup"><span data-stu-id="3fc3f-129">Define the number sequences on the **Retail shared parameters** page for the following references:</span></span>
  
  - <span data-ttu-id="3fc3f-130">رقم ملف التعريف التقني المالي</span><span class="sxs-lookup"><span data-stu-id="3fc3f-130">Fiscal technical profile number</span></span>
  - <span data-ttu-id="3fc3f-131">رقم مجموعة الموصل المالي</span><span class="sxs-lookup"><span data-stu-id="3fc3f-131">Fiscal connector group number</span></span>
  - <span data-ttu-id="3fc3f-132">رقم عملية التسجيل</span><span class="sxs-lookup"><span data-stu-id="3fc3f-132">Registration process number</span></span>

- <span data-ttu-id="3fc3f-133">إنشاء **موصل مالي** في **البيع بالتجزئة > إعداد القناة > التكامل المالي > الموصلات المالية** لكل جهاز أو خدمة تريد استخدامها لأغراض التكامل المالي.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-133">Create a **Fiscal connector** in **Retail > Channel setup > Fiscal integration > Fiscal connectors** for each device or service that you plan to use for fiscal integration purposes.</span></span>

-  <span data-ttu-id="3fc3f-134">إنشاء **موفر المستندات المالية** في **البيع بالتجزئة > إعداد القناة > التكامل المالي > موفرو المستندات المالية‬** لكافة الموصلات المالية.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-134">Create a **Fiscal document provider** in **Retail > Channel setup > Fiscal integration > Fiscal document providers** for all fiscal connectors.</span></span> <span data-ttu-id="3fc3f-135">يعتبر تعيين البيانات جزءًا من موفر المستندات المالية.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-135">Data mapping is considered a part of the fiscal document provider.</span></span> <span data-ttu-id="3fc3f-136">لإعداد تعيينات بيانات مختلفة للموصل نفسه (مثل القواعد الخاصة بالولاية)، يجب عليك إنشاء موفرين مختلفين للمستندات المالية.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-136">To set up different data mappings for the same connector (like state-specific regulations), you should create different fiscal document providers.</span></span>

- <span data-ttu-id="3fc3f-137">إنشاء **ملف التعريف الوظيفي للموصل‬** في **البيع بالتجزئة > إعداد القناة > التكامل المالي > ملفات التعريف الوظيفية للموصلات‬** لكل موفر مستندات مالي.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-137">Create a **Connector functional profile** in **Retail > Channel setup > Fiscal integration > Connector functional profiles** for each fiscal document provider.</span></span>
  - <span data-ttu-id="3fc3f-138">حدد اسم موصل.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-138">Select a connector name.</span></span>
  - <span data-ttu-id="3fc3f-139">حدد موفر المستندات.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-139">Select a document provider.</span></span>
  - <span data-ttu-id="3fc3f-140">حدد إعدادات معدلات ضريبة القيمة المضافة على علامة التبويب **إعداد الخدمة**.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-140">Specify VAT rates settings on the **Service setup** tab.</span></span>
  - <span data-ttu-id="3fc3f-141">حدد تعيين أكواد ضريبة القيمة المضافة وتعيين نوع طريقة الدفع على علامة التبويب **تعيين البيانات**.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-141">Specify VAT codes mapping and tender type mapping on the **Data mapping** tab.</span></span>

  #### <a name="examples"></a><span data-ttu-id="3fc3f-142">أمثلة</span><span class="sxs-lookup"><span data-stu-id="3fc3f-142">Examples</span></span> 

  |  | <span data-ttu-id="3fc3f-143">التنسيق</span><span class="sxs-lookup"><span data-stu-id="3fc3f-143">Format</span></span> | <span data-ttu-id="3fc3f-144">مثال</span><span class="sxs-lookup"><span data-stu-id="3fc3f-144">Example</span></span> | 
  |--------|--------|--------|
  | <span data-ttu-id="3fc3f-145">إعدادات معدلات ضريبة القيمة المضافة</span><span class="sxs-lookup"><span data-stu-id="3fc3f-145">VAT rates settings</span></span> | <span data-ttu-id="3fc3f-146">القيمة: VATrate</span><span class="sxs-lookup"><span data-stu-id="3fc3f-146">value : VATrate</span></span> | <span data-ttu-id="3fc3f-147">1 : 2000, 2 : 1800</span><span class="sxs-lookup"><span data-stu-id="3fc3f-147">1 : 2000, 2 : 1800</span></span> |
  | <span data-ttu-id="3fc3f-148">تعيين أكواد ضريبة القيمة المضافة</span><span class="sxs-lookup"><span data-stu-id="3fc3f-148">VAT codes mapping</span></span> | <span data-ttu-id="3fc3f-149">VATcode : القيمة</span><span class="sxs-lookup"><span data-stu-id="3fc3f-149">VATcode : value</span></span> | <span data-ttu-id="3fc3f-150">vat20 : 1, vat18 : 2</span><span class="sxs-lookup"><span data-stu-id="3fc3f-150">vat20 : 1, vat18 : 2</span></span> |
  | <span data-ttu-id="3fc3f-151">تعيين أنواع طرق الدفع</span><span class="sxs-lookup"><span data-stu-id="3fc3f-151">Tender types mapping</span></span> | <span data-ttu-id="3fc3f-152">TenderTyp : قيمة</span><span class="sxs-lookup"><span data-stu-id="3fc3f-152">TenderTyp : value</span></span> | <span data-ttu-id="3fc3f-153">النقد : 1، البطاقة : 2</span><span class="sxs-lookup"><span data-stu-id="3fc3f-153">Cash : 1, Card : 2</span></span> |

- <span data-ttu-id="3fc3f-154">إنشاء **مجموعات موصلات مالية** في **البيع بالتجزئة > إعداد القناة > التكامل المالي > مجموعة الموصلات المالية**.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-154">Create **Fiscal connector groups** in **Retail > Channel setup > Fiscal integration > Fiscal connector group**.</span></span> <span data-ttu-id="3fc3f-155">مجموعة الموصلات هي مجموعة فرعية من ملفات التعريف الوظيفية المرتبطة بالموصلات المالية التي تؤدي وظائف مماثلة وتُستخدم في المرحلة نفسها في عملية التسجيل المالي.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-155">A connector group is a subset of functional profiles linked with fiscal connectors that perform identical functions and are used at the same stage within a fiscal registration process.</span></span>

   - <span data-ttu-id="3fc3f-156">أضف ملفات تعريف وظيفية إلى مجموعة الموصلات.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-156">Add functional profiles to the connector group.</span></span> <span data-ttu-id="3fc3f-157">انقر فوق **إضافة** في صفحة **ملفات التعريف الوظيفية** وحدد رقم ملف تعريف.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-157">Click **Add** on the **Functional profiles** page and select a profile number.</span></span>
   - <span data-ttu-id="3fc3f-158">إذا أردت تعليق استخدام ملف التعريف الوظيفي، فقم بتعيين **تعطيل** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-158">If you want to suspend usage of the functional profile, set **Disable** to **Yes**.</span></span> 
   
     <span data-ttu-id="3fc3f-159">يؤثر هذا التغيير على مجموعة الموصلات الحالية فقط.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-159">This change affects the current connector group only.</span></span> <span data-ttu-id="3fc3f-160">يمكنك متابعة استخدام ملف التعريف الوظيفي نفسه في مجموعات موصلات أخرى.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-160">You can continue using the same functional profile in other connector groups.</span></span>

     >[!NOTE]
     > <span data-ttu-id="3fc3f-161">ضمن مجموعة موصلات، يتوفر ملف تعريف وظيفي واحد لكل موصل مالي.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-161">Within a connector group, each fiscal connector can only have one functional profile.</span></span>

- <span data-ttu-id="3fc3f-162">إنشاء **ملف التعريف التقني للموصل‬** في **البيع بالتجزئة > إعداد القناة > التكامل المالي > ملفات التعريف التقنية للموصلات‬** لكل موصل مالي.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-162">Create a **Connector technical profile** in **Retail > Channel setup > Fiscal integration > Connector technical profiles** for each fiscal connector.</span></span>
  - <span data-ttu-id="3fc3f-163">حدد اسم موصل.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-163">Select a connector name.</span></span>
  - <span data-ttu-id="3fc3f-164">حدد اسم موصل:</span><span class="sxs-lookup"><span data-stu-id="3fc3f-164">Select a connector type:</span></span> 
      - <span data-ttu-id="3fc3f-165">**محلي** - عيّن هذا النوع للأجهزة أو التطبيقات المثبتة على جهاز محلي.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-165">**Local** - Set this type for physical devices or applications installed on a local machine.</span></span>
      - <span data-ttu-id="3fc3f-166">**داخلي**- عيّن هذا النوع للأجهزة المالية والخدمات المتصلة بخادم البيع بالتجزئة.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-166">**Internal** - Set this type for fiscal devices and services connected to Retail Server.</span></span>
      - <span data-ttu-id="3fc3f-167">**خارجي** - للخدمات المالية الخارجية مثل مدخل ويب الذي توفره هيئة ضرائب.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-167">**External** - For external fiscal services like a web-portal provided by a tax authority.</span></span>
    
  - <span data-ttu-id="3fc3f-168">تحديد الإعدادات على علامة التبويب **الاتصال**.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-168">Specify settings on the **Connection** tab.</span></span>

      
 >[!NOTE]
 > <span data-ttu-id="3fc3f-169">سيتم تحميل إصدار محدث من تكوين تم تحميله في السابق لملفات التعريف الوظيفية والتقنية على حدٍ سواء.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-169">An updated version of a configuration that was loaded earlier will be loaded for both functional and technical profiles.</span></span> <span data-ttu-id="3fc3f-170">إذا كان موصل أو موفر مستندات ملائم قيد التشغيل، فسيتم إعلامك بذلك.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-170">If an appropriate connector or document provider is already in use, you will be notified.</span></span> <span data-ttu-id="3fc3f-171">بشكل افتراضي، يتم تخزين كافة التغييرات التي تم إدخالها يدويًا في ملفات التعريف الوظيفية والتقنية.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-171">By default, all changes that have been made manually in functional and technical profiles will be stored.</span></span> <span data-ttu-id="3fc3f-172">من أجل تجاوز ملفات التعريف هذه باستخدام المجموعة الافتراضية للمعلمات من تكوين ما، انقر فوق **تحديث** في صفحة **ملفات التعريف الوظيفية للموصلات‬** وصفحة **ملفات التعريف التقنية للموصلات‬**.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-172">In order to override these profiles with the default set of parameters from a configuration, click **Update** on the **Connector functional profiles** page and **Connector technical profiles** page.</span></span>
 
- <span data-ttu-id="3fc3f-173">إنشاء **عملية التسجيل المالي** في **البيع بالتجزئة > إعداد القناة > التكامل المالي > عمليات التسجيل المالي** لكل عملية فريدة للتكامل المالي.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-173">Create a **Fiscal registration process** in **Retail > Channel setup > Fiscal integration > Fiscal registration processes** for each unique process of the fiscal integration.</span></span> <span data-ttu-id="3fc3f-174">يتم تعريف عملية التسجيل بواسطة تسلسل خطوات التسجيل ومجموعة الموصلات المستخدمة في كل خطوة.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-174">A registration process is defined by the sequence of the registration steps and the connector group used on each step.</span></span> 
  
  - <span data-ttu-id="3fc3f-175">إضافة خطوات التسجيل للعملية:</span><span class="sxs-lookup"><span data-stu-id="3fc3f-175">Add registration steps to the process:</span></span>
      - <span data-ttu-id="3fc3f-176">النقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-176">Click **Add**.</span></span>
      - <span data-ttu-id="3fc3f-177">حدد نوع موصل.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-177">Select a connector type.</span></span>
      
      >[!NOTE]
      > <span data-ttu-id="3fc3f-178">يحدد هذا الحقل المكان حيث سيبحث النظام في ملف تعريف تقني للموصل، إما في ملفات تعريف الأجهزة لنوع الموصل **المحلي**، أو في ملفات تعريف وظائف نقطة البيع لأنواع موصلات مالية أخرى.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-178">This field defines where the system will search in a technical profile for the connector, either in hardware profiles for connector type **Local**, or in POS functionality profiles for other fiscal connector types.</span></span>
      
   - <span data-ttu-id="3fc3f-179">حدد مجموعة موصلات.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-179">Select a connector group.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="3fc3f-180">انقر فوق **التحقق من الصحة** للتحقق من تكامل بنية عملية التسجيل.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-180">Click **Validate** to check the integrity of the registration process structure.</span></span> <span data-ttu-id="3fc3f-181">من المستحسن إجراء عمليات التحقق من الصحة في الحالات التالية:</span><span class="sxs-lookup"><span data-stu-id="3fc3f-181">It’s recommended that validations be made in the following cases:</span></span>
       >- <span data-ttu-id="3fc3f-182">لإجراء عملية تسجيل جديدة بعد استكمال جميع الإعدادات، بما في ذلك الربط بملفات تعريف وظائف نقطة البيع وملفات تعريف الأجهزة.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-182">For a new registration process after all the settings are completed, including binding to POS functionality profiles and hardware profiles.</span></span>
       >- <span data-ttu-id="3fc3f-183">بعد إجراء تحديثات لعملية تسجيل موجودة.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-183">After making updates to an existing registration process.</span></span>

-  <span data-ttu-id="3fc3f-184">ربط عمليات التسجيل المالي بملفات تعريف وظائف نقطة البيع في **البيع بالتجزئة > إعداد القناة > إعداد نقطة البيع > ملفات تعريف نقطة البيع > ملفات تعريف الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-184">Bind fiscal registration processes to POS functionality profiles in **Retail > Channel setup > POS setup > POS profiles > Functionality profiles**.</span></span>
   - <span data-ttu-id="3fc3f-185">انقر فوق **تحرير** وحدد **رقم العملية‬** على علامة التبويب **عملية تسجيل مالي**.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-185">Click **Edit** and select a **Process number** on the **Fiscal registration process** tab.</span></span>
- <span data-ttu-id="3fc3f-186">ربط ملفات التعريف التقنية للموصلات‬ بملفات تعريف الأجهزة في **البيع بالتجزئة > إعداد القناة > إعداد نقطة البيع > ملفات تعريف نقطة البيع > ملفات تعريف الأجهزة**.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-186">Bind the connector technical profiles to the hardware profiles in **Retail > Channel setup > POS setup > POS profiles > Hardware profiles**.</span></span>
   - <span data-ttu-id="3fc3f-187">انقر فوق **تحرير**، ثم فوق **جديد** على علامة تبويب **‏‫ملف التعريف التقني المالي**.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-187">Click **Edit**, then click **New** on the **Fiscal technical profile** tab.</span></span>
   - <span data-ttu-id="3fc3f-188">حدد ‏‫ملف التعريف التقني للموصل في الحقل **رقم ملف التعريف**.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-188">Select a connector technical profile in the **Profile number** field.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="3fc3f-189">يمكنك إضافة العديد من ملفات التعريف التقنية إلى ملف تعريف الأجهزة.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-189">You can add several technical profiles to a hardware profile.</span></span> <span data-ttu-id="3fc3f-190">ومع ذلك، هذا الأمر غير مدعوم إذا تضمن ملف تعريف الأجهزة‬ أكثر من تقاطع واحد مع أي مجموعة موصلات.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-190">However, this is not supported if a hardware profile has more than one intersection with any connector group.</span></span> <span data-ttu-id="3fc3f-191">لتجنب الإعدادات غير الصحيحة، من المستحسن التحقق من صحة عملية التسجيل بعد تحديث كافة ملفات تعريف الأجهزة‬.</span><span class="sxs-lookup"><span data-stu-id="3fc3f-191">To avoid incorrect settings, it’s recommended that you validate the registration process after updating all the hardware profiles.</span></span>

