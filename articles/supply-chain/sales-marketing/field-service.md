---
title: نظرة عامة على التكامل مع Microsoft Dynamics 365 Field Service
description: يوفر هذا الموضوع نظرة عامة على التكامل مع Microsoft Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 73d20958d0efadefc709db524fe16ed85d1ea33a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824884"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a><span data-ttu-id="5dd48-103">نظرة عامة على التكامل مع Microsoft Dynamics 365 Field Service</span><span class="sxs-lookup"><span data-stu-id="5dd48-103">Integration with Microsoft Dynamics 365 Field Service overview</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5dd48-104">يتيح Supply Chain Management مزامنة عمليات الأعمال بين Dynamics 365 Supply Chain Management وDynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="5dd48-104">Supply Chain Management enables synchronization of business processes between Dynamics 365 Supply Chain Management and Dynamics 365 Field Service.</span></span> <span data-ttu-id="5dd48-105">تم تكوين سيناريوهات التكامل باستخدام قوالب "موحد البيانات" القابلة للتوسعة وMicrosoft Dataverse لتمكين مزامنة عمليات الأعمال.</span><span class="sxs-lookup"><span data-stu-id="5dd48-105">The integration scenarios are configured by using extensible Data integrator templates and Microsoft Dataverse to enable the synchronization of business processes.</span></span>
<span data-ttu-id="5dd48-106">يمكن استخدام القوالب القياسية لإنشاء مشاريع تكامل مخصصة، حيث يمكن تعيين أعمدة وحداول مخصصة وقياسية إضافية لضبط التكامل والوفاء بمتطلبات أعمال معينة.</span><span class="sxs-lookup"><span data-stu-id="5dd48-106">Standard templates can be used to create custom integration projects, where additional standard and custom columns and tables can be mapped to adjust the integration and meet specific business needs.</span></span> 

<span data-ttu-id="5dd48-107">يستند تكامل Field Service إلى الوظيفة الموجودة "العميل المتوقع إلى النقدية‬".</span><span class="sxs-lookup"><span data-stu-id="5dd48-107">The field service integration builds on top of the existing prospect-to-cash functionality.</span></span>

![مزامنة عمليات الأعمال بين Supply Chain Management وField Service](./media/field-service-integration.png)

<span data-ttu-id="5dd48-109">تركز المرحلة الأولى من التكامل بين Field Service وSupply Chain Management على تمكين أوامر العمل والاتفاقيات في Field Service لفوترتها في Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5dd48-109">The first phase  of the integration between Field Service and Supply Chain Management is focused on enabling work orders and agreements in Field Service to be invoiced in Supply Chain Management.</span></span> <span data-ttu-id="5dd48-110">يبدأ التدفق المدعوم في Field Service، حيث تتم مزامنة المعلومات من أوامر العمل إلى Supply Chain Management كأوامر مبيعات.</span><span class="sxs-lookup"><span data-stu-id="5dd48-110">The supported flow starts in Field Service, where information from work orders is synchronized to Supply Chain Management as sales orders.</span></span> <span data-ttu-id="5dd48-111">في Supply Chain Management، تتم فوترة أوامر المبيعات لإنشاء مستندات الفواتير.</span><span class="sxs-lookup"><span data-stu-id="5dd48-111">In Supply Chain Management, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="5dd48-112">بالإضافة إلى ذلك، تتم مزامنة المعلومات من فواتير اتفاقيات Field Service إلى Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5dd48-112">In addition, the information from Field Service agreement invoices is synchronized to Supply Chain Management.</span></span> <span data-ttu-id="5dd48-113">يقوم موحد البيانات في Microsoft Dynamics 365 بمزامنة البيانات من خلال استخدام المشاريع القابلة للتخصيص.</span><span class="sxs-lookup"><span data-stu-id="5dd48-113">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="5dd48-114">يمكن استخدام القوالب القياسية لإنشاء مشاريع تكامل مخصصة حيث يمكن تعيين الأعمدة المخصصة والقياسية الإضافية، وكذلك الجداول، لتعديل التكامل والوفاء بالمتطلبات المحددة.</span><span class="sxs-lookup"><span data-stu-id="5dd48-114">Standard templates can be used to create custom integration projects where additional standard and custom columns, and also tables, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="5dd48-115">تعمل المرحلة الأولى من التكامل بين Field Service وSupply Chain Management على تمكين مزامنة العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="5dd48-115">The first phase of the integration between Field Service and Supply Chain Management enables synchronization of the following items:</span></span>

- [<span data-ttu-id="5dd48-116">مزامنة المنتجات في Supply Chain Management مع المنتجات في Field Service</span><span class="sxs-lookup"><span data-stu-id="5dd48-116">Synchronize products in Supply Chain Management to products in Field Service</span></span>](field-service-product.md)
- [<span data-ttu-id="5dd48-117">مزامنة أوامر العمل في Field Service مع أوامر المبيعات في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5dd48-117">Synchronize work orders in Field Service to sales orders in Supply Chain Management</span></span>](field-service-work-order.md)
- [<span data-ttu-id="5dd48-118">مزامنة فواتير الاتفاقيات في Field Service مع فواتير النص الحر في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5dd48-118">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>](field-service-invoice.md)

<span data-ttu-id="5dd48-119">للاطلاع على مثال حول الطريقة التي يمكنك من خلالها مزامنة أمر عمل بين Field Service وSupply Chain Management، شاهد مقطع فيديو YouTube القصير [كيفية مزامنة أمر عمل مع تكامل Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo).</span><span class="sxs-lookup"><span data-stu-id="5dd48-119">To see an example of how you can synchronize a work order between Field Service and Supply Chain Management, watch the short YouTube video [How to synchronize a work order with Microsoft Dynamics 365 Integration](https://www.youtube.com/watch?v=46ylO7raZAo).</span></span>

## <a name="integration-with-field-service-including-inventory-and-project-information"></a><span data-ttu-id="5dd48-120">التكامل مع Field Service، بما في ذلك معلومات حول المخزون والمشروع</span><span class="sxs-lookup"><span data-stu-id="5dd48-120">Integration with Field Service, including inventory and project information</span></span>

<span data-ttu-id="5dd48-121">تركز الوظيفة الإضافية في هذه المرحلة الثانية على تقديم معلومات لفنيي الخدمة حول معلومات المخزون من Supply Chain Management، مما يسمح لهم بتحديث مستويات المخزون وإجراء عمليات تحويل المواد.</span><span class="sxs-lookup"><span data-stu-id="5dd48-121">The additional functionality in this second phase focused on giving field technicians insight about the inventory information from Supply Chain Management, allowing them to update inventory levels and do material transfers.</span></span> <span data-ttu-id="5dd48-122">بالإضافة إلى ذلك، فإن الشركات التي تقوم بتثبيت أو صيانة السلع المباعة تستفيد من إمكانية تحكم أفضل بالإضافة إلى رؤية أوضح لعملية البيع والخدمة الكاملة مع التكامل من المشاريع.</span><span class="sxs-lookup"><span data-stu-id="5dd48-122">In addition, companies installing or servicing sold goods will benefit from better control and visibility to the full sales and service process with integration from projects.</span></span>

### <a name="functionality-includes-integration-of"></a><span data-ttu-id="5dd48-123">تتضمن الوظيفة تكامل:</span><span class="sxs-lookup"><span data-stu-id="5dd48-123">Functionality includes integration of:</span></span>
- <span data-ttu-id="5dd48-124">معلومات المستودع</span><span class="sxs-lookup"><span data-stu-id="5dd48-124">Warehouse information</span></span>
- <span data-ttu-id="5dd48-125">معلومات المخزون المتاح</span><span class="sxs-lookup"><span data-stu-id="5dd48-125">On-hand inventory information</span></span>
- <span data-ttu-id="5dd48-126">عمليات تحويل المخزون</span><span class="sxs-lookup"><span data-stu-id="5dd48-126">Inventory transfers</span></span>
- <span data-ttu-id="5dd48-127">تعديلات المخزون</span><span class="sxs-lookup"><span data-stu-id="5dd48-127">Inventory adjustments</span></span>
- <span data-ttu-id="5dd48-128">ربط مشاريع Supply Chain Management مع أوامر عمل Dynamics 365 Field Service</span><span class="sxs-lookup"><span data-stu-id="5dd48-128">Supply Chain Management projects connected with Dynamics 365 Field Service work orders</span></span>
- <span data-ttu-id="5dd48-129">تقوم أوامر عمل Dynamics 365 Field Service التي لديها ارتباط مع مشاريع Supply Chain Management بتطبيق رقم المشروع هذا على أمر مبيعات للسماح بالفوترة من المشروع.</span><span class="sxs-lookup"><span data-stu-id="5dd48-129">Dynamics 365 Field Service work orders with link to Supply Chain Management projects, apply this project number to the sales order to allow invoicing from the project.</span></span> 

![مزامنة عمليات الأعمال بين Supply Chain Management وField Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a><span data-ttu-id="5dd48-131">تعمل المرحلة الثانية من التكامل بين Field Service وSupply Chain Management على تمكين المزامنة مع القوالب التالية:</span><span class="sxs-lookup"><span data-stu-id="5dd48-131">The second phase of the integration between Field Service and Supply Chain Management enables synchronization with the following templates:</span></span>
- <span data-ttu-id="5dd48-132">المستودعات (Supply Chain Management إلى Field Service) - المستودعات من Supply Chain Management إلى Field Service [استعلام متقدم]</span><span class="sxs-lookup"><span data-stu-id="5dd48-132">Warehouses (Supply Chain Management to Field Service) - Warehouses from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="5dd48-133">مخزون المنتجات (Supply Chain Management إلى Field Service) - معلومات مستوى المخزون من Supply Chain Management إلى Field Service [استعلام متقدم]</span><span class="sxs-lookup"><span data-stu-id="5dd48-133">Product Inventory (Supply Chain Management to Field Service) - Inventory level information from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="5dd48-134">تسوية المخزون (Field Service إلى Supply Chain Management) - تسويات المخزون من Field Service إلى Supply Chain Management [استعلام متقدم]</span><span class="sxs-lookup"><span data-stu-id="5dd48-134">Inventory Adjustment (Field Service to Supply Chain Management) - Inventory adjustments from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="5dd48-135">عمليات تحويل المخزون‬ (Field Service إلى Supply Chain Management) - عمليات تحويل المخزون‬ من Field Service إلى Supply Chain Management [استعلام متقدم]</span><span class="sxs-lookup"><span data-stu-id="5dd48-135">Inventory Transfers (Field Service to Supply Chain Management) - Inventory transfers from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="5dd48-136">المشاريع (Supply Chain Management إلى Field Service) - قائمة المشاريع من Supply Chain Management إلى Field Service</span><span class="sxs-lookup"><span data-stu-id="5dd48-136">Projects (Supply Chain Management to Field Service) - Project list from Supply Chain Management to Field Service</span></span> 
- <span data-ttu-id="5dd48-137">أوامر العمل مع المشروع (Field Service إلى Supply Chain Management) - أوامر العمل في Field Service إلى أوامر المبيعات في Supply Chain Management، مع دعم للمشروع [استعلام متقدم]</span><span class="sxs-lookup"><span data-stu-id="5dd48-137">Work Orders with Project (Field Service to Supply Chain Management) - Work orders in Field Service to Sales orders  in Supply Chain Management, with support for Project [Advanced Query]</span></span> 
- <span data-ttu-id="5dd48-138">منتجات Field Service مع وحدة المخزون (Supply Chain Management إلى Sales)‏ - "منتجات قابلة للبيع تم إصدارها‬" في Supply Chain Management إلى "منتجات" Sales لـ Field Service، بما في ذلك وحدة المخزون</span><span class="sxs-lookup"><span data-stu-id="5dd48-138">Field Service Products with Inventory unit (Supply Chain Management to Sales) - Supply Chain Management 'Sellable released products' to Sales 'Products' for Field Service, including Inventory unit</span></span> 

## <a name="system-requirements"></a><span data-ttu-id="5dd48-139">متطلبات النظام</span><span class="sxs-lookup"><span data-stu-id="5dd48-139">System requirements</span></span>

### <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="5dd48-140">متطلبات النظام في Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="5dd48-140">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="5dd48-141">يدعم تكامل Field Service الإصدارات التالية:</span><span class="sxs-lookup"><span data-stu-id="5dd48-141">Field Service integration supports the following versions:</span></span>

- <span data-ttu-id="5dd48-142">تم طرح الإصدار 8.1.2 من Dynamics 365 for Finance and Operations (ديسمبر 2018) في شهر ديسمبر 2018 وله رقم إصدار التطبيق 8.1.195 مع Platform update 22 (7.0.5095).</span><span class="sxs-lookup"><span data-stu-id="5dd48-142">Dynamics 365 for Finance and Operations version 8.1.2 (December 2018) was released in December 2018 and has an application build number 8.1.195 with Platform update 22 (7.0.5095).</span></span> 

### <a name="system-requirements-for-field-service"></a><span data-ttu-id="5dd48-143">متطلبات النظام لـ Field Service</span><span class="sxs-lookup"><span data-stu-id="5dd48-143">System requirements for Field Service</span></span>
<span data-ttu-id="5dd48-144">لاستخدام حل تكامل Field Service، يجب عليك تثبيت المكونات التالية:</span><span class="sxs-lookup"><span data-stu-id="5dd48-144">To use the Field Service integration solution, you must install the following components:</span></span>

- <span data-ttu-id="5dd48-145">Field Service (الإصدار 8.2.0.286) أو إصدار لاحق على Dynamics 365 9.1.x - تم إطلاقه في شهر نوفمبر 2018</span><span class="sxs-lookup"><span data-stu-id="5dd48-145">Field Service (version 8.2.0.286) or a later version on Dynamics 365 9.1.x - Released November 2018</span></span>
- <span data-ttu-id="5dd48-146">حل العميل المتوقع إلى النقدية (P2C) لتطبيق Dynamics 365، الإصدار 1.15.0.1 أو إصدار أحدث.</span><span class="sxs-lookup"><span data-stu-id="5dd48-146">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="5dd48-147">الحل متوفر للتنزيل من [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="5dd48-147">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="5dd48-148">حل 'تكامل Field Service، والمشروع والمخزون' لبرنامج Dynamics 365، الإصدار 2.0.0.0 أو إصدار لاحق.</span><span class="sxs-lookup"><span data-stu-id="5dd48-148">'Field Service Integration, Project and Inventory' solution for Dynamics 365, version 2.0.0.0 or a later version.</span></span> <span data-ttu-id="5dd48-149">الحل متوفر للتنزيل من [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span><span class="sxs-lookup"><span data-stu-id="5dd48-149">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]