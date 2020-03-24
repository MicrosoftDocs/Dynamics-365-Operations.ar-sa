---
title: أصل العميل المتكامل
description: يوضح هذا الموضوع تكامل بيانات العملاء بين Finance and Operations وCommon Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 269346d38eeb3812c352d16f9d50fbcd09307c12
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124579"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="0d4a9-103">أصل العميل المتكامل</span><span class="sxs-lookup"><span data-stu-id="0d4a9-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="0d4a9-104">من المعتاد أن تتم عادة إدارة سجلات العملاء في أكثر من تطبيق واحد.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-104">It's typical for customer records to be mastered in more than one application.</span></span> <span data-ttu-id="0d4a9-105">على سبيل المثال، بإمكان نشاط المبيعات إحضار سجلات العملاء عبر تطبيق مبيعات، وبإمكان مبيعات التجزئة أو التجارة الإلكترونية إحضار سجلات العملاء عبر تطبيق Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-105">For example, sales activity can bring in commercial customer records through a Sales application, and e-Commerce or retail sales can bring in customer records through a Finance and Operations application.</span></span> <span data-ttu-id="0d4a9-106">بغض النظر عن مصدر سجلات العملاء، فهي تتكامل في الخلفية عبر حدود التطبيق واختلافات البنية التحتية.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-106">Regardless of where the customer record originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> <span data-ttu-id="0d4a9-107">تساعد إدارة العملاء المتكامل على التعامل مع سيناريوهات إدارة متعددة وتوفر طريقة عرض شاملة للعميل في مجموعة تطبيقات Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-107">Integrated customer mastering helps handle multi-mastering scenarios and provides a comprehensive view of the customer to the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="0d4a9-108">تدفق بيانات العميل</span><span class="sxs-lookup"><span data-stu-id="0d4a9-108">Customer data flow</span></span>

<span data-ttu-id="0d4a9-109">*العميل* هو مفهوم معرف بشكل دقيق في التطبيقات.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="0d4a9-110">ولذلك، فإن تكامل بيانات العميل ينطوي فقط على مواءمة مفهوم العميل بين التطبيقين.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="0d4a9-111">يبين الرسم التوضيحي التالي تدفق بيانات العميل.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-111">The following illustration shows the customer data flow.</span></span>

![تدفق بيانات العميل](media/dual-write-customer-data-flow.png)

<span data-ttu-id="0d4a9-113">يمكن تصنيف العملاء على نطاق واسع في نوعين: العملاء التجاريين/المؤسسيين والمستهلكين/المستخدمين النهائيين.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="0d4a9-114">يتم تخزين هذين النوعين من العملاء والتعامل معهما بطريقة مختلفة في Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="0d4a9-115">في Finance and Operations، تتم إدارة العملاء التجاريين/المؤسسيين والمستهلكين/المستخدمين النهائيين في جدول واحد يسمى **CustTable** (CustomerCustomerV3Entity)، ويتم تصنيفهم استنادًا إلى سمة **النوع**.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustomerCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="0d4a9-116">(إذا تم تعيين **النوع** إلى **مؤسسة**، فسيكون العميل تجاريًا/مؤسسيًا، وإذا تم تعيين **النوع** إلى **شخص**، فسيكون العميل مستهلكًا/مستخدمًا نهائيًا.) يتم التعامل مع معلومات جهة الاتصال الرئيسية عبر الكيان SMMContactPersonEntity.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="0d4a9-117">في Common Data Service، تتم إدارة العملاء التجاريين/المؤسسيين في كيان الحساب، ويتم تعريفهم كعملاء عند تعيين سمة **RelationshipType** إلى **عميل**.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="0d4a9-118">يتم تمثيل المستهلكين/المستخدمين النهائيين وشخص جهة الاتصال بواسطة كيان جهة الاتصال.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="0d4a9-119">للفصل بشكل واضح بين المستهلك/المستخدم النهائي وشخص جهة الاتصال، يتضمن كيان **جهة الاتصال** علامة منطقية تسمى **قابل للبيع**.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="0d4a9-120">عندما تكون قيمة **قابل للبيع** **صواب**، تكون جهة الاتصال عبارة عن عميل مستهلك/مستخدم نهائي، ولا يمكن إنشاء الأوامر وعروض الأسعار لجهة الاتصال هذه.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="0d4a9-121">عندما تكون قيمة **قابل للبيع** **خطأ**، تكون جهة الاتصال مجرد جهة اتصال رئيسية للعميل.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="0d4a9-122">عندما تشارك جهة اتصال غير قابلة للبيع في عملية عرض أسعار أو أمر، يتم تعيين قيمة **قابل للبيع** إلى **صواب** لوضع علامة على جهة الاتصال كجهة اتصال قابلة للبيع.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="0d4a9-123">جهة الاتصال التي أصبح جهة اتصال قابلة للبيع تبقى جهة اتصال قابلة للبيع.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="0d4a9-124">القوالب</span><span class="sxs-lookup"><span data-stu-id="0d4a9-124">Templates</span></span>

<span data-ttu-id="0d4a9-125">تتضمن بيانات العميل كافة المعلومات المتعلقة بالعميل، مثل مجموعة العملاء والعناوين ومعلومات الاتصال وملف تعريف الدفع وملف تعريف الفاتورة وحالة الولاء.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="0d4a9-126">تعمل مجموعة من مخططات الكيانات معًا أثناء تفاعل بيانات العميل، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="0d4a9-127">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0d4a9-127">Finance and Operations apps</span></span> | <span data-ttu-id="0d4a9-128">تطبيقات Dynamics 365 الأخرى</span><span class="sxs-lookup"><span data-stu-id="0d4a9-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="0d4a9-129">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="0d4a9-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="0d4a9-130">جهات اتصال CDS V2</span><span class="sxs-lookup"><span data-stu-id="0d4a9-130">CDS Contacts V2</span></span>             | <span data-ttu-id="0d4a9-131">جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="0d4a9-131">contacts</span></span>                        | <span data-ttu-id="0d4a9-132">يقوم هذا القالب بمزامنة كافة معلومات جهات الاتصال الاساسيه والثانوية والثلاثية لكل من العملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="0d4a9-133">مجموعات العملاء</span><span class="sxs-lookup"><span data-stu-id="0d4a9-133">Customer groups</span></span>             | <span data-ttu-id="0d4a9-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="0d4a9-134">msdyn_customergroups</span></span>            | <span data-ttu-id="0d4a9-135">يقوم هذا القالب بمزامنة معلومات مجموعة العملاء.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="0d4a9-136">طريقة دفع العميل</span><span class="sxs-lookup"><span data-stu-id="0d4a9-136">Customer payment method</span></span>     | <span data-ttu-id="0d4a9-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="0d4a9-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="0d4a9-138">يقوم هذا القالب بمزامنة معلومات طرق دفع العملاء.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="0d4a9-139">العملاء V3</span><span class="sxs-lookup"><span data-stu-id="0d4a9-139">Customers V3</span></span>                | <span data-ttu-id="0d4a9-140">الحسابات</span><span class="sxs-lookup"><span data-stu-id="0d4a9-140">accounts</span></span>                        | <span data-ttu-id="0d4a9-141">يقوم هذا القالب بمزامنة المعلومات الرئيسية للعميل للعملاء التجاريين والمؤسسين.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="0d4a9-142">العملاء V3</span><span class="sxs-lookup"><span data-stu-id="0d4a9-142">Customers V3</span></span>                | <span data-ttu-id="0d4a9-143">جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="0d4a9-143">contacts</span></span>                        | <span data-ttu-id="0d4a9-144">يقوم هذا القالب بمزامنة البيانات الرئيسية للعميل للعملاء والمستخدمين النهائيين.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="0d4a9-145">بطاقة الولاء</span><span class="sxs-lookup"><span data-stu-id="0d4a9-145">Loyalty card</span></span>                | <span data-ttu-id="0d4a9-146">msdyn_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="0d4a9-146">msdyn_loyaltycards</span></span>              | <span data-ttu-id="0d4a9-147">يقوم هذا القالب بمزامنة معلومات بطاقة ولاء العملاء.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-147">This template synchronizes customer loyalty card information.</span></span>
<span data-ttu-id="0d4a9-148">ملحقات الاسم</span><span class="sxs-lookup"><span data-stu-id="0d4a9-148">Name affixes</span></span>                | <span data-ttu-id="0d4a9-149">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="0d4a9-149">msdyn_nameaffixes</span></span>               | <span data-ttu-id="0d4a9-150">يقوم هذا القالب بمزامنة البيانات المرجعية لملصقات الأسماء، لكلٍّ من العملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-150">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="0d4a9-151">بنود يوم الدفع CDS V2</span><span class="sxs-lookup"><span data-stu-id="0d4a9-151">Payment day lines CDS V2</span></span>    | <span data-ttu-id="0d4a9-152">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="0d4a9-152">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="0d4a9-153">يقوم هذا القالب بمزامنة البيانات المرجعية لأسطر أيام الدفع لكلٍّ من العملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-153">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="0d4a9-154">أيام الدفع CDS</span><span class="sxs-lookup"><span data-stu-id="0d4a9-154">Payment days CDS</span></span>            | <span data-ttu-id="0d4a9-155">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="0d4a9-155">msdyn_paymentdays</span></span>               | <span data-ttu-id="0d4a9-156">يقوم هذا القالب بمزامنة البيانات المرجعية لأيام الدفع لكلٍّ من العملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-156">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="0d4a9-157">بنود جدول الدفع</span><span class="sxs-lookup"><span data-stu-id="0d4a9-157">Payment schedule lines</span></span>      | <span data-ttu-id="0d4a9-158">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="0d4a9-158">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="0d4a9-159">مزامنة البيانات المرجعية لأسطر جداول الدفع لكلٍّ من العملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-159">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="0d4a9-160">جدول الدفع</span><span class="sxs-lookup"><span data-stu-id="0d4a9-160">Payment schedule</span></span>            | <span data-ttu-id="0d4a9-161">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="0d4a9-161">msdyn_paymentschedules</span></span>          | <span data-ttu-id="0d4a9-162">يقوم هذا القالب بمزامنة البيانات المرجعية لجدول الدفع لكلٍّ من العملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-162">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="0d4a9-163">شروط الدفع</span><span class="sxs-lookup"><span data-stu-id="0d4a9-163">Terms of payment</span></span>            | <span data-ttu-id="0d4a9-164">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="0d4a9-164">msdyn_paymentterms</span></span>              | <span data-ttu-id="0d4a9-165">يقوم هذا القالب بمزامنة البيانات المرجعية لمدد الدفع (مدد الدفع) لكلٍّ من العملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="0d4a9-165">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
