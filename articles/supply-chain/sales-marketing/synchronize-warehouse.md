---
title: "مزامنة المستودعات من Finance and Operations إلى Field Service"
description: "يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المستودعات من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: ar-sa
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="a5a43-103">مزامنة المستودعات من Finance and Operations إلى Field Service</span><span class="sxs-lookup"><span data-stu-id="a5a43-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a5a43-104">يناقش هذا الموضوع القوالب والمهام الأساسية التي يتم استخدامها لمزامنة المستودعات من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="a5a43-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="a5a43-105">[![مزامنة عمليات الأعمال بين Finance and Operations وField Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="a5a43-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a5a43-106">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="a5a43-106">Templates and tasks</span></span>
<span data-ttu-id="a5a43-107">يُستخدم القالب التالي والمهام الأساسية التالية لتشغيل مزامنة المستودعات من Microsoft Dynamics 365 for Field Service إلى Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a5a43-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="a5a43-108">**اسم القالب في تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="a5a43-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="a5a43-109">المستودعات (Finance and Operations إلى Field Service)</span><span class="sxs-lookup"><span data-stu-id="a5a43-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="a5a43-110">**أسماء المهام في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="a5a43-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="a5a43-111">المستودع</span><span class="sxs-lookup"><span data-stu-id="a5a43-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="a5a43-112">مجموعة الكيانات</span><span class="sxs-lookup"><span data-stu-id="a5a43-112">Entity set</span></span>
| <span data-ttu-id="a5a43-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="a5a43-113">Field Service</span></span>    | <span data-ttu-id="a5a43-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a5a43-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="a5a43-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="a5a43-115">msdyn_warehouses</span></span> | <span data-ttu-id="a5a43-116">المستودعات</span><span class="sxs-lookup"><span data-stu-id="a5a43-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="a5a43-117">تدفق الكيان</span><span class="sxs-lookup"><span data-stu-id="a5a43-117">Entity flow</span></span>
<span data-ttu-id="a5a43-118">يمكن مزامنة المستودعات التي يتم إنشاؤها وصيانتها في Finance and Operations إلى Field Service عبر مشروع تكامل بيانات Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="a5a43-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="a5a43-119">يمكن التحكم في المستودعات المطلوبة التي تتزامن مع Field Service بواسطة وظائف الاستعلام والتصفية المتقدمة على المشروع.</span><span class="sxs-lookup"><span data-stu-id="a5a43-119">The desired warehouses that synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="a5a43-120">ويتم إنشاء المستودعات التي تتزامن من Finance and Operations في Field Service مع تعيين الحقل "تتم المحافظة عليه خارجيًا‬" إلى "نعم" والسجل محدد للقراءة فقط.</span><span class="sxs-lookup"><span data-stu-id="a5a43-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the field Is maintained externally set to Yes and the record is made read only.</span></span>
<span data-ttu-id="a5a43-121">حل Field Service CRM لدعم التكامل بين Field Service وFinance and Operations، يلزم وجود وظيفة إضافية من حل Field Service CRM.</span><span class="sxs-lookup"><span data-stu-id="a5a43-121">Field Service CRM solution To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="a5a43-122">يشتمل الحل على التغييرات التالية.</span><span class="sxs-lookup"><span data-stu-id="a5a43-122">The solution includes the following changes.</span></span>
<span data-ttu-id="a5a43-123">تمت إضافة الحقل **تتم المحافظة عليه خارجيًا** إلى كيان **المستودع (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="a5a43-123">The field **Is Maintained Externally** has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="a5a43-124">يساعد هذا الحقل في تحديد ما إذا كانت معالجة المستودع من Operations أو إذا كان موجودًا فقط في Field Service.</span><span class="sxs-lookup"><span data-stu-id="a5a43-124">This field helps to identify If the Warehouse is handled from Operations or if It only exists in Field Service.</span></span>
- <span data-ttu-id="a5a43-125">نعم - نشأ المستودع من Finance and Operations ولن يكون قابلاً للتحرير في Sales.</span><span class="sxs-lookup"><span data-stu-id="a5a43-125">Yes – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="a5a43-126">لا – تم إدخال المستودع مباشرة في Field Service ويتم الاحتفاظ به هنا.</span><span class="sxs-lookup"><span data-stu-id="a5a43-126">No – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="a5a43-127">يساعد الحقل **تتم المحافظة عليه خارجيًا** في التحكم في مزامنة مستويات المخزون والتسويات وعمليات التحويل والاستخدام في أوامر العمل.</span><span class="sxs-lookup"><span data-stu-id="a5a43-127">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers and usage on work orders.</span></span> <span data-ttu-id="a5a43-128">وحدها المستودعات حيث **تتم المحافظة عليها خارجيًا‬‏‫** = نعم يمكن استخدامها للمزامنة مباشرة إلى نفس المستودع في النظام الآخر.</span><span class="sxs-lookup"><span data-stu-id="a5a43-128">Only warehouses with **Is Externally Maintained** = Yes can be used to synchronize directly to the same warehouse in the other system.</span></span> 

<span data-ttu-id="a5a43-129">ملاحظة: من الممكن إنشاء عدة مستودعات في Field Services (باستخدام **تتم المحافظة عليها خارجيًا‬‏‫** = لا") ثم تعيينها إلى مستودع واحد في Finance and Operations، باستخدام وظائف التصفية والاستعلام المتقدمة.</span><span class="sxs-lookup"><span data-stu-id="a5a43-129">Note: It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="a5a43-130">يتم استخدام هذا الإجراء في الحالات التي تريد فيها أن تعمل Field service كأساس على مستوى المخزون المفصل وفقط إرسال تحديثات إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a5a43-130">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="a5a43-131">في هذه الحالة، لن تحصل Field service على تحديثات مستوى المخزون من Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a5a43-131">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="a5a43-132">اطلع على معلومات إضافية في "مزامنة عمليات تسوية المخزون من Field Service إلى Finance and Operations‬" و"مزامنة أوامر العمل في Field Service إلى أوامر المبيعات المرتبطة بالمشروع في Finance and Operations‬".</span><span class="sxs-lookup"><span data-stu-id="a5a43-132">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="a5a43-133">المتطلبات الأساسية وإعداد التعيين</span><span class="sxs-lookup"><span data-stu-id="a5a43-133">Prerequisites and mapping setup</span></span>
### <a name="in-the-data-integration-project"></a><span data-ttu-id="a5a43-134">في مشروع تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="a5a43-134">In the Data Integration project</span></span>
<span data-ttu-id="a5a43-135">قبل مزامنة المستودعات، تأكد من تحديث وظائف الاستعلام والتصفية المتقدمة بحيث تتضمن فقط المستودعات التي تريد إحضارها من Finance and Operations إلى Field Service.</span><span class="sxs-lookup"><span data-stu-id="a5a43-135">Before synchronization of the warehouses make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="a5a43-136">لاحظ أنك ستحتاج إلى المستودع في Field Service لتطبيقه على أوامر العمل والتسويات وعمليات التحويل.</span><span class="sxs-lookup"><span data-stu-id="a5a43-136">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments and transfers.</span></span>  

<span data-ttu-id="a5a43-137">تأكد من وجود **مفتاح تكامل** لـ **msdyn_warehouses**</span><span class="sxs-lookup"><span data-stu-id="a5a43-137">Ensure the **Integration key** exist for **msdyn_warehouses**</span></span>
1. <span data-ttu-id="a5a43-138">اذهب إلى تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="a5a43-138">Go to Data Integration</span></span>
2. <span data-ttu-id="a5a43-139">حدد علامة التبويب **مجموعة الاتصال**</span><span class="sxs-lookup"><span data-stu-id="a5a43-139">Select **Connection Set** tab</span></span>
3. <span data-ttu-id="a5a43-140">حدد مجموعة الاتصال المستخدمة لمزامنة أمر العمل</span><span class="sxs-lookup"><span data-stu-id="a5a43-140">Select the Connection set used for Work order synchronization</span></span>
4. <span data-ttu-id="a5a43-141">حدد علامة التبويب **مفتاح التكامل**</span><span class="sxs-lookup"><span data-stu-id="a5a43-141">Select **Integration key** tab</span></span>
5. <span data-ttu-id="a5a43-142">ابحث عن msdyn_warehouses وتأكد نت إضافة المفتاح **msdyn_name (الاسم)**.</span><span class="sxs-lookup"><span data-stu-id="a5a43-142">Find msdyn_warehouses and check that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="a5a43-143">إذا كان غير معروض، فأضفه بالنقر فوق **إضافة مفتاح**، ثم انقر فوق **حفظ** في الجزء العلوي من الصفحة</span><span class="sxs-lookup"><span data-stu-id="a5a43-143">If it is not shown, add it by click **Add key** and click **Save** in the top of the page</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a5a43-144">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="a5a43-144">Template mapping in Data integration</span></span>

<span data-ttu-id="a5a43-145">تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="a5a43-145">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="a5a43-146">المستودعات (Finance and Operations إلى Field Service): المستودع</span><span class="sxs-lookup"><span data-stu-id="a5a43-146">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="a5a43-147">[![تعيين القالب في تكامل البيانات](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="a5a43-147">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>

