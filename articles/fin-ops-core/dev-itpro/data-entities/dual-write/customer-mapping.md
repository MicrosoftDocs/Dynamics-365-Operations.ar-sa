---
title: أصل العميل المتكامل
description: يوضح هذا الموضوع تكامل بيانات العملاء بين Finance and Operations وDataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 402342b459c366d0e198e3d0e946deb1f9e81739
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568116"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="5a07e-103">أصل العميل المتكامل</span><span class="sxs-lookup"><span data-stu-id="5a07e-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="5a07e-104">يمكن إدارة بيانات العملاء في أكثر من تطبيق Dynamics 365 واحد.</span><span class="sxs-lookup"><span data-stu-id="5a07e-104">Customer data can be mastered in more than one Dynamics 365 application.</span></span> <span data-ttu-id="5a07e-105">علي سبيل المثال، يمكن أن ينشأ صف العميل إذا كان نشاط المبيعات في Dynamics 365 Sales (تطبيق يستند إلى النموذج في Dynamics 365)، أو يمكن أن صف من خلال نشاط بيع بالتجزئة في Dynamics 365 Commerce (تطبيق Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="5a07e-105">For example, a customer row can originate though sales activity in Dynamics 365 Sales (a model-driven app in Dynamics 365), or a row can originate through retail activity in Dynamics 365 Commerce (a Finance and Operations app).</span></span> <span data-ttu-id="5a07e-106">بغض النظر عن المكان الذي تنشأ فيه البيانات الخاصة بالعميل، فإنها تتكامل خلف المشاهد.</span><span class="sxs-lookup"><span data-stu-id="5a07e-106">No matter where where the customer data originates, it is integrated behind the scenes.</span></span> <span data-ttu-id="5a07e-107">يوفر أصل العميل المتكامل المرونة لبيانات العميل الرئيسية في أي تطبيق Dynamics 365 ويوفر طريقة عرض شاملة للعميل عبر مجموعة تطبيقات Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5a07e-107">Integrated customer master gives you the flexibility to master customer data in any Dynamics 365 application and provides a comprehensive view of the customer across the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="5a07e-108">تدفق بيانات العميل</span><span class="sxs-lookup"><span data-stu-id="5a07e-108">Customer data flow</span></span>

<span data-ttu-id="5a07e-109">*العميل* هو مفهوم معرف بشكل دقيق في التطبيقات.</span><span class="sxs-lookup"><span data-stu-id="5a07e-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="5a07e-110">ولذلك، فإن تكامل بيانات العميل ينطوي فقط على مواءمة مفهوم العميل بين التطبيقين.</span><span class="sxs-lookup"><span data-stu-id="5a07e-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="5a07e-111">يبين الرسم التوضيحي التالي تدفق بيانات العميل.</span><span class="sxs-lookup"><span data-stu-id="5a07e-111">The following illustration shows the customer data flow.</span></span>

![تدفق بيانات العميل](media/dual-write-customer-data-flow.png)

<span data-ttu-id="5a07e-113">يمكن تصنيف العملاء على نطاق واسع في نوعين: العملاء التجاريين/المؤسسيين والمستهلكين/المستخدمين النهائيين.</span><span class="sxs-lookup"><span data-stu-id="5a07e-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="5a07e-114">يتم تخزين هذين النوعين من العملاء والتعامل معهما بطريقة مختلفة في Finance and Operations وDataverse.</span><span class="sxs-lookup"><span data-stu-id="5a07e-114">These two types of customers are stored and handled differently in Finance and Operations and Dataverse.</span></span>

<span data-ttu-id="5a07e-115">في Finance and Operations، تتم إدارة العملاء التجاريين/المؤسسيين والمستهلكين/المستخدمين النهائيين في جدول واحد يسمى **CustTable** (CustCustomerV3Entity)، ويتم تصنيفهم استنادًا إلى سمة **النوع**.</span><span class="sxs-lookup"><span data-stu-id="5a07e-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="5a07e-116">(إذا تم تعيين **النوع** إلى **مؤسسة**، فسيكون العميل تجاريًا/مؤسسيًا، وإذا تم تعيين **النوع** إلى **شخص**، فسيكون العميل مستهلكًا/مستخدمًا نهائيًا.) يتم التعامل مع معلومات جهة الاتصال الرئيسية عبر الجدول SMMContactPersonEntity.</span><span class="sxs-lookup"><span data-stu-id="5a07e-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity table.</span></span>

<span data-ttu-id="5a07e-117">في Dataverse، تتم إدارة العملاء التجاريين/المؤسسيين في جدول الحساب، ويتم تعريفهم كعملاء عند تعيين سمة **RelationshipType** إلى **عميل**.</span><span class="sxs-lookup"><span data-stu-id="5a07e-117">In Dataverse, commercial/organizational customers are mastered in the Account table and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="5a07e-118">يتم تمثيل المستهلكين/المستخدمين النهائيين وشخص جهة الاتصال بواسطة جدول جهة الاتصال.</span><span class="sxs-lookup"><span data-stu-id="5a07e-118">Both consumers/end users and the contact person are represented by the Contact table.</span></span> <span data-ttu-id="5a07e-119">للفصل بشكل واضح بين المستهلك/المستخدم النهائي وشخص جهة الاتصال، يتضمن جدول **جهة الاتصال** علامة منطقية تسمى **قابل للبيع**.</span><span class="sxs-lookup"><span data-stu-id="5a07e-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** table has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="5a07e-120">عندما تكون قيمة **قابل للبيع** **صواب**، تكون جهة الاتصال عبارة عن عميل مستهلك/مستخدم نهائي، ولا يمكن إنشاء الأوامر وعروض الأسعار لجهة الاتصال هذه.</span><span class="sxs-lookup"><span data-stu-id="5a07e-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="5a07e-121">عندما تكون قيمة **قابل للبيع** **خطأ**، تكون جهة الاتصال مجرد جهة اتصال رئيسية للعميل.</span><span class="sxs-lookup"><span data-stu-id="5a07e-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="5a07e-122">عندما تشارك جهة اتصال غير قابلة للبيع في عملية عرض أسعار أو أمر، يتم تعيين قيمة **قابل للبيع** إلى **صواب** لوضع علامة على جهة الاتصال كجهة اتصال قابلة للبيع.</span><span class="sxs-lookup"><span data-stu-id="5a07e-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="5a07e-123">جهة الاتصال التي أصبح جهة اتصال قابلة للبيع تبقى جهة اتصال قابلة للبيع.</span><span class="sxs-lookup"><span data-stu-id="5a07e-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="5a07e-124">القوالب</span><span class="sxs-lookup"><span data-stu-id="5a07e-124">Templates</span></span>

<span data-ttu-id="5a07e-125">تتضمن بيانات العميل كافة المعلومات المتعلقة بالعميل، مثل مجموعة العملاء والعناوين ومعلومات الاتصال وملف تعريف الدفع وملف تعريف الفاتورة وحالة الولاء.</span><span class="sxs-lookup"><span data-stu-id="5a07e-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="5a07e-126">تعمل مجموعة من مخططات الجداول معًا أثناء تفاعل بيانات العميل، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="5a07e-126">A collection of table maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="5a07e-127">تطبيقات Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5a07e-127">Finance and Operations apps</span></span> | <span data-ttu-id="5a07e-128">تطبيقات Dynamics 365 الأخرى</span><span class="sxs-lookup"><span data-stu-id="5a07e-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="5a07e-129">‏‏الوصف</span><span class="sxs-lookup"><span data-stu-id="5a07e-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="5a07e-130">جهات اتصال CDS V2</span><span class="sxs-lookup"><span data-stu-id="5a07e-130">CDS Contacts V2</span></span>             | <span data-ttu-id="5a07e-131">جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="5a07e-131">contacts</span></span>                        | <span data-ttu-id="5a07e-132">يقوم هذا القالب بمزامنة كافة معلومات جهات الاتصال الاساسيه والثانوية والثلاثية لكل من العملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="5a07e-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="5a07e-133">مجموعات العملاء</span><span class="sxs-lookup"><span data-stu-id="5a07e-133">Customer groups</span></span>             | <span data-ttu-id="5a07e-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="5a07e-134">msdyn_customergroups</span></span>            | <span data-ttu-id="5a07e-135">يقوم هذا القالب بمزامنة معلومات مجموعة العملاء.</span><span class="sxs-lookup"><span data-stu-id="5a07e-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="5a07e-136">طريقة دفع العميل</span><span class="sxs-lookup"><span data-stu-id="5a07e-136">Customer payment method</span></span>     | <span data-ttu-id="5a07e-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="5a07e-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="5a07e-138">يقوم هذا القالب بمزامنة معلومات طرق دفع العملاء.</span><span class="sxs-lookup"><span data-stu-id="5a07e-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="5a07e-139">العملاء V3</span><span class="sxs-lookup"><span data-stu-id="5a07e-139">Customers V3</span></span>                | <span data-ttu-id="5a07e-140">الحسابات</span><span class="sxs-lookup"><span data-stu-id="5a07e-140">accounts</span></span>                        | <span data-ttu-id="5a07e-141">يقوم هذا القالب بمزامنة المعلومات الرئيسية للعميل للعملاء التجاريين والمؤسسين.</span><span class="sxs-lookup"><span data-stu-id="5a07e-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="5a07e-142">العملاء V3</span><span class="sxs-lookup"><span data-stu-id="5a07e-142">Customers V3</span></span>                | <span data-ttu-id="5a07e-143">جهات الاتصال</span><span class="sxs-lookup"><span data-stu-id="5a07e-143">contacts</span></span>                        | <span data-ttu-id="5a07e-144">يقوم هذا القالب بمزامنة البيانات الرئيسية للعميل للعملاء والمستخدمين النهائيين.</span><span class="sxs-lookup"><span data-stu-id="5a07e-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="5a07e-145">ملحقات الاسم</span><span class="sxs-lookup"><span data-stu-id="5a07e-145">Name affixes</span></span>                | <span data-ttu-id="5a07e-146">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="5a07e-146">msdyn_nameaffixes</span></span>               | <span data-ttu-id="5a07e-147">يقوم هذا القالب بمزامنة البيانات المرجعية لملصقات الأسماء، لكلٍّ من العملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="5a07e-147">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="5a07e-148">بنود يوم الدفع CDS V2</span><span class="sxs-lookup"><span data-stu-id="5a07e-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="5a07e-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="5a07e-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="5a07e-150">يقوم هذا القالب بمزامنة البيانات المرجعية لأسطر أيام الدفع لكلٍّ من العملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="5a07e-150">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="5a07e-151">أيام الدفع CDS</span><span class="sxs-lookup"><span data-stu-id="5a07e-151">Payment days CDS</span></span>            | <span data-ttu-id="5a07e-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="5a07e-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="5a07e-153">يقوم هذا القالب بمزامنة البيانات المرجعية لأيام الدفع لكلٍّ من العملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="5a07e-153">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="5a07e-154">بنود جدول الدفع</span><span class="sxs-lookup"><span data-stu-id="5a07e-154">Payment schedule lines</span></span>      | <span data-ttu-id="5a07e-155">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="5a07e-155">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="5a07e-156">مزامنة البيانات المرجعية لأسطر جداول الدفع لكلٍّ من العملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="5a07e-156">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="5a07e-157">جدول الدفع</span><span class="sxs-lookup"><span data-stu-id="5a07e-157">Payment schedule</span></span>            | <span data-ttu-id="5a07e-158">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="5a07e-158">msdyn_paymentschedules</span></span>          | <span data-ttu-id="5a07e-159">يقوم هذا القالب بمزامنة البيانات المرجعية لجدول الدفع لكلٍّ من العملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="5a07e-159">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="5a07e-160">شروط الدفع</span><span class="sxs-lookup"><span data-stu-id="5a07e-160">Terms of payment</span></span>            | <span data-ttu-id="5a07e-161">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="5a07e-161">msdyn_paymentterms</span></span>              | <span data-ttu-id="5a07e-162">يقوم هذا القالب بمزامنة البيانات المرجعية لمدد الدفع (مدد الدفع) لكلٍّ من العملاء والموردين.</span><span class="sxs-lookup"><span data-stu-id="5a07e-162">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]