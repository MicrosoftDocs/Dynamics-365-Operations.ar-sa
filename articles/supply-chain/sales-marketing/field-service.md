---
title: التكامل مع Microsoft Dynamics 365 for Field Service
description: يوفر هذا الموضوع نظرة عامة على التكامل مع Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 02/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 111ed3257af3caf8e90844b9a6e1475ef931b674
ms.sourcegitcommit: 2b14f15487f19c10fce4bfa24de70cdb3fab05ab
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/05/2019
ms.locfileid: "375036"
---
# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="763a1-103">التكامل مع Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="763a1-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="763a1-104">يمكّن Microsoft Dynamics 365 for Finance and Operations مزامنة عمليات الأعمال بين Finance and Operations وMicrosoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="763a1-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="763a1-105">تم تكوين سيناريوهات التكامل باستخدام قوالب موحد البيانات القابلة للتوسيع وCommon Data Service (CDS) لتمكين مزامنة عمليات الأعمال.</span><span class="sxs-lookup"><span data-stu-id="763a1-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>
<span data-ttu-id="763a1-106">يمكن استخدام القوالب القياسية لإنشاء مشاريع تكامل مخصصة، حيث يمكن تعيين حقول وكيانات مخصصة وقياسية إضافية لضبط التكامل والوفاء بمتطلبات أعمال معينة.</span><span class="sxs-lookup"><span data-stu-id="763a1-106">Standard templates can be used to create custom integration projects, where additional standard and custom fields and entities can be mapped to adjust the integration and meet specific business needs.</span></span> 

<span data-ttu-id="763a1-107">يستند تكامل Field Service إلى الوظيفة الموجودة "العميل المتوقع إلى النقدية‬".</span><span class="sxs-lookup"><span data-stu-id="763a1-107">The field service integration builds on top of the existing prospect-to-cash functionality.</span></span>

![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/field-service-integration.png)

<span data-ttu-id="763a1-109">تنصب المرحلة الأولى من التكامل بين Field Service وFinance and Operations على تمكين أوامر العمل والاتفاقيات في Field Service لفوترتها في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="763a1-109">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="763a1-110">يبدأ التدفق المدعوم في Field Service، حيث تتم مزامنة المعلومات من أوامر العمل لـ Finance and Operations كأوامر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="763a1-110">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="763a1-111">في Finance and Operations، تتم فوترة أوامر المبيعات لإنشاء مستندات الفواتير.</span><span class="sxs-lookup"><span data-stu-id="763a1-111">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="763a1-112">بالإضافة إلى ذلك، تتم مزامنة المعلومات من فواتير اتفاقيات Field Service لـ Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="763a1-112">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="763a1-113">يقوم موحد البيانات في Microsoft Dynamics 365 بمزامنة البيانات من خلال استخدام المشاريع القابلة للتخصيص.</span><span class="sxs-lookup"><span data-stu-id="763a1-113">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="763a1-114">يمكن استخدام القوالب القياسية لإنشاء مشاريع تكامل مخصصة حيث يمكن تعيين الحقول المخصصة والقياسية الإضافية، وكذلك الكيانات، لتعديل التكامل والوفاء بالمتطلبات المحددة.</span><span class="sxs-lookup"><span data-stu-id="763a1-114">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="763a1-115">تعمل المرحلة الأولى من التكامل بين Field Service وFinance and Operations على تمكين مزامنة العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="763a1-115">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="763a1-116">المنتجات في Finance and Operations للمنتجات في Field Service التي تشمل معلومات نوع المنتج</span><span class="sxs-lookup"><span data-stu-id="763a1-116">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="763a1-117">أوامر العمل في Field Service لأوامر المبيعات في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="763a1-117">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="763a1-118">الفواتير في Field Service لفواتير النص الحر في Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="763a1-118">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="763a1-119">للاطلاع على مثال حول الطريقة التي يمكنك من خلالها مزامنة أمر عمل بين Field Service وFinance and Operations، شاهد فيديو YouTube القصير [كيفية مزامنة أمر عمل مع تكامل Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo).</span><span class="sxs-lookup"><span data-stu-id="763a1-119">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video [How to synchronize a work order with Microsoft Dynamics 365 Integration](https://www.youtube.com/watch?v=46ylO7raZAo).</span></span>

# <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a><span data-ttu-id="763a1-120">التكامل مع Microsoft Dynamics 365 for Field Service، بما في ذلك معلومات حول المخزون والمشروع</span><span class="sxs-lookup"><span data-stu-id="763a1-120">Integration with Microsoft Dynamics 365 for Field Service, including inventory and project information</span></span>

<span data-ttu-id="763a1-121">تركز الوظيفة الإضافية في هذه المرحلة الثانية على تقديم معلومات لفنيي الخدمة حول معلومات المخزون من Finance and Operations، مما يسمح لهم بتحديث مستويات المخزون وإجراء عمليات تحويل المواد.</span><span class="sxs-lookup"><span data-stu-id="763a1-121">The additional functionality in this second phase focused on giving field technicians insight about the inventory information from Finance and Operations, allowing them to update inventory levels and do material transfers.</span></span> <span data-ttu-id="763a1-122">بالإضافة إلى ذلك، فإن الشركات التي تقوم بتثبيت أو صيانة السلع المباعة تستفيد من إمكانية تحكم أفضل بالإضافة إلى رؤية أوضح لعملية البيع والخدمة الكاملة مع التكامل من المشاريع.</span><span class="sxs-lookup"><span data-stu-id="763a1-122">In addition, companies installing or servicing sold goods will benefit from better control and visibility to the full sales and service process with integration from projects.</span></span>

### <a name="functionality-includes-integration-of"></a><span data-ttu-id="763a1-123">تتضمن الوظيفة تكامل:</span><span class="sxs-lookup"><span data-stu-id="763a1-123">Functionality includes integration of:</span></span>
- <span data-ttu-id="763a1-124">معلومات المستودع</span><span class="sxs-lookup"><span data-stu-id="763a1-124">Warehouse information</span></span>
- <span data-ttu-id="763a1-125">معلومات المخزون المتاح</span><span class="sxs-lookup"><span data-stu-id="763a1-125">On-hand inventory information</span></span>
- <span data-ttu-id="763a1-126">عمليات تحويل المخزون</span><span class="sxs-lookup"><span data-stu-id="763a1-126">Inventory transfers</span></span>
- <span data-ttu-id="763a1-127">تعديلات المخزون</span><span class="sxs-lookup"><span data-stu-id="763a1-127">Inventory adjustments</span></span>
- <span data-ttu-id="763a1-128">مشاريع Dynamics 365 for Finance and Operations المتصلة بأوامر عمل Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="763a1-128">Dynamics 365 for Finance and Operations projects connected with Dynamics 365 for Field Service work orders</span></span>
- <span data-ttu-id="763a1-129">تقوم أوامر عمل Dynamics 365 for Field Service التي لديها ارتباط إلى مشاريع Dynamics 365 for Finance and Operations بتطبيق المشروع هذا على أمر مبيعات Dynamics 365 for Finance and Operations للسماح بالفوترة من المشروع.</span><span class="sxs-lookup"><span data-stu-id="763a1-129">Dynamics 365 for Field Service work orders with link to Dynamics 365 for Finance and Operations projects, apply this project number to the Dynamics 365 for Finance and Operations sales order to allow invoicing from the project.</span></span> 

![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a><span data-ttu-id="763a1-131">تعمل المرحلة الثانية من التكامل بين Field Service وFinance and Operations على تمكين المزامنة مع القوالب التالية:</span><span class="sxs-lookup"><span data-stu-id="763a1-131">The second phase of the integration between Field Service and Finance and Operations enables synchronization with the following templates:</span></span>
- <span data-ttu-id="763a1-132">المستودعات (Fin and Ops إلى Field Service) - المستودعات من Finance and Operations إلى Field Service [استعلام متقدم]</span><span class="sxs-lookup"><span data-stu-id="763a1-132">Warehouses (Fin and Ops to Field Service) - Warehouses from Finance and Operations to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="763a1-133">مخزون المنتج (Fin and Ops إلى Field Service) - معلومات مستوى المخزون من Finance and Operations إلى Field Service [استعلام متقدم]</span><span class="sxs-lookup"><span data-stu-id="763a1-133">Product Inventory (Fin and Ops to Field Service) - Inventory level information from Finance and Operations to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="763a1-134">تسوية المخزون (Field Service إلى Fin and Ops) - تسويات المخزون من Field Service إلى Finance and Operations [استعلام متقدم]</span><span class="sxs-lookup"><span data-stu-id="763a1-134">Inventory Adjustment (Field Service to Fin and Ops) - Inventory adjustments from Field Service to Finance and Operations [Advanced Query]</span></span> 
- <span data-ttu-id="763a1-135">عمليات تحويل المخزون (Field Service إلى Fin and Ops) - عمليات تحويل المخزون من Field Service إلى Finance and Operations [استعلام متقدم]</span><span class="sxs-lookup"><span data-stu-id="763a1-135">Inventory Transfers (Field Service to Fin and Ops) - Inventory transfers from Field Service to Finance and Operations [Advanced Query]</span></span> 
- <span data-ttu-id="763a1-136">المشاريع (Fin and Ops إلى Field Service) - قائمة المشاريع من Finance and Operations إلى Field Service</span><span class="sxs-lookup"><span data-stu-id="763a1-136">Projects (Fin and Ops to Field Service) - Project list from Finance and Operations to Field Service</span></span> 
- <span data-ttu-id="763a1-137">أوامر العمل مع المشروع (Field Service إلى Fin and Ops) - أوامر العمل في Field Service إلى أوامر المبيعات في Finance and Operations، مع دعم للمشروع [استعلام متقدم]</span><span class="sxs-lookup"><span data-stu-id="763a1-137">Work Orders with Project (Field Service to Fin and Ops) - Work orders in Field Service to Sales orders  in Finance and Operations, with support for Project [Advanced Query]</span></span> 
- <span data-ttu-id="763a1-138">منتجات Field Service مع وحدة المخزون (Fin and Ops إلى Sales)‏ - "منتجات قابلة للبيع تم إصدارها‬" في Finance and Operations إلى "منتجات" Sales لـ Field Service، بما في ذلك وحدة المخزون</span><span class="sxs-lookup"><span data-stu-id="763a1-138">Field Service Products with Inventory unit (Fin and Ops to Sales) - Finance and Operations 'Sellable released products' to Sales 'Products' for Field Service, including Inventory unit</span></span> 

# <a name="system-requirements"></a><span data-ttu-id="763a1-139">متطلبات النظام</span><span class="sxs-lookup"><span data-stu-id="763a1-139">System requirements</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="763a1-140">متطلبات النظام لـ Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="763a1-140">System requirements for Finance and Operations</span></span>
<span data-ttu-id="763a1-141">يدعم تكامل Field Service الإصدارات التالية:</span><span class="sxs-lookup"><span data-stu-id="763a1-141">Field Service integration supports the following versions:</span></span>

- <span data-ttu-id="763a1-142">تم طرح الإصدار 8.1.2 من Dynamics 365 for Finance and Operations (ديسمبر 2019) في شهر ديسمبر 2019 وله رقم إصدار التطبيق 8.1.195 مع Platform Update 22 (7.0.5095).</span><span class="sxs-lookup"><span data-stu-id="763a1-142">Dynamics 365 for Finance and Operations version 8.1.2 (December 2019) was released in December 2019 and has an application build number 8.1.195 with Platform Update 22 (7.0.5095).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="763a1-143">متطلبات النظام لـ Field Service</span><span class="sxs-lookup"><span data-stu-id="763a1-143">System requirements for Field Service</span></span>
<span data-ttu-id="763a1-144">لاستخدام حل تكامل Field Service، يجب عليك تثبيت المكونات التالية:</span><span class="sxs-lookup"><span data-stu-id="763a1-144">To use the Field Service integration solution, you must install the following components:</span></span>

- <span data-ttu-id="763a1-145">Field Service for Dynamics 365 (الإصدار 8.2.0.286) أو إصدار لاحق على Dynamics 365 9.1.x - تم إطلاقه في شهر نوفمبر 2018</span><span class="sxs-lookup"><span data-stu-id="763a1-145">Field Service for Dynamics 365 (version 8.2.0.286) or a later version on Dynamics 365 9.1.x - Released November 2018</span></span>
- <span data-ttu-id="763a1-146">حل العميل المتوقع إلى النقدية (P2C) لتطبيق Dynamics 365، الإصدار 1.15.0.1 أو إصدار أحدث.</span><span class="sxs-lookup"><span data-stu-id="763a1-146">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="763a1-147">الحل متوفر للتنزيل من [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="763a1-147">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="763a1-148">حل 'تكامل Field Service، والمشروع والمخزون' لبرنامج Dynamics 365، الإصدار 2.0.0.0 أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="763a1-148">'Field Service Integration, Project and Inventory' solution for Dynamics 365, version 2.0.0.0 or a later version.</span></span> <span data-ttu-id="763a1-149">الحل متوفر للتنزيل من [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span><span class="sxs-lookup"><span data-stu-id="763a1-149">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span></span>
