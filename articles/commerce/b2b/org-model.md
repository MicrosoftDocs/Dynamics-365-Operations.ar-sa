---
title: إنشاء تدرجات هرمية لتصميم المؤسسة لمؤسسات B2B
description: يصف هذا الموضوع كيفية إنشاء تدرجات هرمية لتصميم المؤسسة لمؤسسات الأعمال بين الشركات (B2B).
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 487af939f92ece8bc3e543b3beeffa239baa1863
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799819"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a><span data-ttu-id="085fe-103">إنشاء تدرجات هرمية لتصميم المؤسسة لمؤسسات B2B</span><span class="sxs-lookup"><span data-stu-id="085fe-103">Create org modeling hierarchies for B2B organizations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="085fe-104">يصف هذا الموضوع كيفية إنشاء تدرجات هرمية لتصميم المؤسسة لمؤسسات الأعمال بين الشركات (B2B) في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="085fe-104">This topic describes how to create organizational modeling hierarchies for business-to-business (B2B) organizations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="085fe-105">في المركز الرئيسي لـ Commerce، يتم تمثيل مؤسسات شركاء الأعمال بواسطة العميل وكيانات التدرج الهرمي للعميل.</span><span class="sxs-lookup"><span data-stu-id="085fe-105">In Commerce headquarters, business partner organizations are represented by customer and customer hierarchy entities.</span></span> <span data-ttu-id="085fe-106">يتم تمثيل مؤسسة شريك الأعمال ومستخدميها كعملاء، ويتم استخدام التدرجات الهرمية للعملاء لربط هؤلاء العملاء مع بعضهم البعض.</span><span class="sxs-lookup"><span data-stu-id="085fe-106">The business partner organization and its users are represented as customers, and customer hierarchies are used to associate those customers with each other.</span></span>

<span data-ttu-id="085fe-107">عندما يتم اعتماد طلب شريك الأعمال بالانضمام إلى موقع تجارة إلكترونية بيبن الشركات B2B، يتم تنفيذ الإجراءات التالية:</span><span class="sxs-lookup"><span data-stu-id="085fe-107">When a business partner request to join a B2B e-commerce site is approved, the following actions are performed:</span></span>

- <span data-ttu-id="085fe-108">يتم إنشاء سجلين عميلين جديدين في النظام: سجل عميل **من نوع مؤسسة** لمؤسسة شريك العمل وسجل عميل **من نوع شخص** للطالب (أي مستخدم شريك الأعمال الذي أرسل الطلب).</span><span class="sxs-lookup"><span data-stu-id="085fe-108">Two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor (that is, the business partner user who submitted the request).</span></span>
- <span data-ttu-id="085fe-109">يتم إنشاء سجل التدرج الهرمي للعميل الجديد ضمن **العميل \> التدرج الهرمي للعميل**.</span><span class="sxs-lookup"><span data-stu-id="085fe-109">A new customer hierarchy record is created under **Customer \> Customer hierarchy**.</span></span> <span data-ttu-id="085fe-110">يتضمن هذا السجل خصائص الرأس التالية:</span><span class="sxs-lookup"><span data-stu-id="085fe-110">This record has the following header properties:</span></span>

    - <span data-ttu-id="085fe-111">**معرف التدرج الهرمي للعميل** - معرف فريد للتسلسل الهرمي للعميل.</span><span class="sxs-lookup"><span data-stu-id="085fe-111">**Customer hierarchy ID** – A unique ID for the customer hierarchy.</span></span> <span data-ttu-id="085fe-112">يستخدم هذا المعرف التسلسل الرقمي المحدد في المعلمات المشتركة لـ Commerce في المركز الرئيسي لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="085fe-112">This ID uses the number sequence that is defined in Commerce shared parameters in Commerce headquarters.</span></span>
    - <span data-ttu-id="085fe-113">**الاسم** – اسم المؤسسة الخاصة بشريك الأعمل، كما هو محدد في طلب الانضمام.</span><span class="sxs-lookup"><span data-stu-id="085fe-113">**Name** – The organization name of the business partner, as specified in the onboarding request.</span></span>
    - <span data-ttu-id="085fe-114">**الغرض** – يتم تعيين هذه الخاصية على القيمة المحددة مسبقًا **مؤسسة B2B**.</span><span class="sxs-lookup"><span data-stu-id="085fe-114">**Purpose** – This property is set to the predefined value **B2B organization**.</span></span>
    - <span data-ttu-id="085fe-115">**المؤسسة** – معرف العميل الخاص بشريك الأعمال.</span><span class="sxs-lookup"><span data-stu-id="085fe-115">**Organization** – The customer ID of the business partner.</span></span>

<span data-ttu-id="085fe-116">فيما يلي تفاصيل سجل التدرج الهرمي للعميل:</span><span class="sxs-lookup"><span data-stu-id="085fe-116">Here are the details of the customer hierarchy record:</span></span>

- <span data-ttu-id="085fe-117">يتم إقران سجل العميل الخاص بالطالب بالتدرج الهرمي للعميل.</span><span class="sxs-lookup"><span data-stu-id="085fe-117">The customer record of the requestor is associated with the customer hierarchy.</span></span>
- <span data-ttu-id="085fe-118">يتم ربط دور المسؤول بالطالب.</span><span class="sxs-lookup"><span data-stu-id="085fe-118">The administrator role is associated with the requestor.</span></span>

<span data-ttu-id="085fe-119">عندما يضيف المسؤول مزيدًا من المستخدمين إلى مؤسسة شركاء الأعمال في موقع B2B، يتم إنشاء سجل عميل جديد لكل مستخدم في المركز الرئيسي لـ Commerce.</span><span class="sxs-lookup"><span data-stu-id="085fe-119">When the administrator adds more users are to the business partner organization on a B2B site, a new customer record for each user is created in Commerce headquarters.</span></span> <span data-ttu-id="085fe-120">وتتم أيضًا إضافة سجل العميل هذا إلى سجل التدرج الهرمي للعميل المناسب لشريك الأعمال ويكون له دور "المستخدم".</span><span class="sxs-lookup"><span data-stu-id="085fe-120">This customer record is also added to the relevant customer hierarchy record for the business partner and has the role of a "user."</span></span>

> [!NOTE]
> <span data-ttu-id="085fe-121">في معظم الحالات، يجب أن تتطابق قيم الخصائص المقابلة لكافة سجلات العملاء في التدرج الهرمي.</span><span class="sxs-lookup"><span data-stu-id="085fe-121">In most cases, the corresponding property values of all customer records in a hierarchy should match.</span></span> <span data-ttu-id="085fe-122">على سبيل المثال، نظرًا لأن كافة مستخدمي شريك الأعمال يجب أن يحصلو على أسعار مماثلة للمنتجات، فيجب أن تتطابق مجموعات الأسعار والتكوينات المقترنة بها.</span><span class="sxs-lookup"><span data-stu-id="085fe-122">For example, because all business partner users should get similar prices for products, their price group and associated configurations should match.</span></span> <span data-ttu-id="085fe-123">ومع ذلك، لا يفرض النظام هذا التناسق.</span><span class="sxs-lookup"><span data-stu-id="085fe-123">However, the system doesn't enforce this consistency.</span></span> <span data-ttu-id="085fe-124">لذلك، فإن يكون مستخدمو المركز الرئيسي لـ Commerce المتعلقون مسؤولين عن ضمان مطابقة قيم الخصائص والتكوينات لكافة العملاء في تدرج هرمي المُعطى.</span><span class="sxs-lookup"><span data-stu-id="085fe-124">Therefore, the relevant Commerce headquarters users are responsible for ensuring that the property values and configurations match for all customers in a given hierarchy.</span></span>

<span data-ttu-id="085fe-125">يمكن لمستخدمي المركز الرئيسي لـ Commerce الاطلاع على قيم الخصائص لكافة سجلات العملاء في التدرج الهرمي من طريقة عرض جنبا إلى جنب.</span><span class="sxs-lookup"><span data-stu-id="085fe-125">Commerce headquarters users can look at the property values for all customer records in the hierarchy in a side-by-side view.</span></span> <span data-ttu-id="085fe-126">حدد خصائص سجل العميل ذات الصلة من خلال تحديد أسماء علامات التبويب في القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="085fe-126">Select the relevant customer record properties by selecting the tab names on the drop-down menu.</span></span> <span data-ttu-id="085fe-127">يمكن للمستخدمين عرض قيم الخصائص وتحريرها من طريقة العرض هذه مباشرة.</span><span class="sxs-lookup"><span data-stu-id="085fe-127">Users can directly view and edit the property values from this view.</span></span> <span data-ttu-id="085fe-128">وبدلا من ذلك، إذا كنت ترغب في تطبيق كافة القيم من سجل العميل الخاص بالمسؤول إلى كافة سجلات عملاء المستخدم، فحدد **تجاوز** في تفاصيل التدرج الهرمي للعميل.</span><span class="sxs-lookup"><span data-stu-id="085fe-128">Alternatively, if you want to apply all the values from the administrator customer record to all the user customer records, select **Override** in the customer hierarchy details.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="085fe-129">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="085fe-129">Additional resources</span></span>

[<span data-ttu-id="085fe-130">إعداد موقع تجارة إلكترونية بين الشركات B2B</span><span class="sxs-lookup"><span data-stu-id="085fe-130">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="085fe-131">إدارة مستخدمي شركاء الأعمال على مواقع التجارة الإلكترونية بين الشركات B2B</span><span class="sxs-lookup"><span data-stu-id="085fe-131">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="085fe-132">تكوين طريقة دفع حساب العميل لمواقع التجارة الإلكترونية بين الشركات B2B</span><span class="sxs-lookup"><span data-stu-id="085fe-132">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="085fe-133">تعيين حدود كمية المنتج لمواقع التجارة الإلكترونية بين الشركات B2B</span><span class="sxs-lookup"><span data-stu-id="085fe-133">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]