---
title: "مزامنة المنتجات في Finance and Operations للمنتجات في Field Service"
description: "يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة منتجات من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: ace66c037953f4b1b2e8b93a315faefdb090b1eb
ms.openlocfilehash: bf5de13fee6db1b467c1cf4d5cc65b46c67b29fe
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="ce8ef-103">مزامنة المنتجات في Finance and Operations للمنتجات في Field Service</span><span class="sxs-lookup"><span data-stu-id="ce8ef-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ce8ef-104">يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة منتجات من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="ce8ef-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="ce8ef-105">يستند قالب **منتجات Field Service ‏(Fin and Ops إلى Field Service)** إلى قالب **المنتجات (Fin and Ops إلى Sales) - مباشر** من العميل المتوقع إلى نقد.</span><span class="sxs-lookup"><span data-stu-id="ce8ef-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="ce8ef-106">للحصول على مزيد من المعلومات، راجع [المنتجات (Fin and Ops إلى Sales) - مباشر](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="ce8ef-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="ce8ef-107">يوضح هذا الموضوع فقط الاختلافات بين قالبي **منتجات Field Service ‏(Fin and Ops إلى Field Service)** و**المنتجات (Fin and Ops إلى Sales) – مباشر**.</span><span class="sxs-lookup"><span data-stu-id="ce8ef-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ce8ef-108">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="ce8ef-108">Templates and tasks</span></span>

<span data-ttu-id="ce8ef-109">**اسم القالب في تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="ce8ef-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="ce8ef-110">منتجات Field Service ‏(Fin and Ops إلى Field Service)</span><span class="sxs-lookup"><span data-stu-id="ce8ef-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="ce8ef-111">**اسم المهمة في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="ce8ef-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="ce8ef-112">المنتجات - المنتجات</span><span class="sxs-lookup"><span data-stu-id="ce8ef-112">Products - Products</span></span>

<span data-ttu-id="ce8ef-113">يشتمل قالب **منتجات Field Service ‏(Fin and Ops إلى Field Service)** على تعيين واحد غير مضمن في قالب **المنتجات (Fin and Ops إلى Sales) - مباشر**.</span><span class="sxs-lookup"><span data-stu-id="ce8ef-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="ce8ef-114">يضمن هذا التعيين أن يتم تعيين الحقل المطلوب والخاص بـ Field Service **نوع منتج الخدمة** بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="ce8ef-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="ce8ef-115">يتم استخدام تعيين القيمة التالية.</span><span class="sxs-lookup"><span data-stu-id="ce8ef-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="ce8ef-116">في Finance and Operations، يتم حساب قيمة **نوع منتج Field Service** في كيان بيانات **منتجات قابلة للبيع تم إصدارها‬** كما يلي:</span><span class="sxs-lookup"><span data-stu-id="ce8ef-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="ce8ef-117">**المخزون:** نوع المنتج = مجموعة نماذج الأصناف والمنتجات، منتج مخزّن‬ = صحيح</span><span class="sxs-lookup"><span data-stu-id="ce8ef-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="ce8ef-118">**NonInventory:** نوع المنتج = مجموعة نماذج الأصناف والمنتجات، منتج مخزّن‬ = خطأ</span><span class="sxs-lookup"><span data-stu-id="ce8ef-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="ce8ef-119">**الخدمة:** نوع المنتج = الخدمة</span><span class="sxs-lookup"><span data-stu-id="ce8ef-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ce8ef-120">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="ce8ef-120">Template mapping in Data integration</span></span>

<span data-ttu-id="ce8ef-121">تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="ce8ef-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a><span data-ttu-id="ce8ef-122">منتجات Field Service ‏(Fin and Ops إلى Field Service): المنتجات - المنتجات</span><span class="sxs-lookup"><span data-stu-id="ce8ef-122">Field Service Products (Fin and Ops to Field Service): Products - Products</span></span>

<span data-ttu-id="ce8ef-123">[![تعيين القالب في تكامل البيانات](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="ce8ef-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>

