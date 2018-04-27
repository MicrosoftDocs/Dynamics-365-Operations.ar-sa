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
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 699830ce6cd993f3dd3fd4ff744ce5a8b9645c32
ms.contentlocale: ar-sa
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a><span data-ttu-id="fe8e8-103">مزامنة المنتجات في Finance and Operations للمنتجات في Field Service</span><span class="sxs-lookup"><span data-stu-id="fe8e8-103">Synchronize products in Finance and Operations to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fe8e8-104">يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة منتجات من Microsoft Dynamics 365 for Finance and Operations إلى Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="fe8e8-104">This topic discusses the templates and underlying task that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="fe8e8-105">يستند قالب **منتجات Field Service ‏(Fin and Ops إلى Field Service)** إلى قالب **المنتجات (Fin and Ops إلى Sales) - مباشر** من العميل المتوقع إلى نقد.</span><span class="sxs-lookup"><span data-stu-id="fe8e8-105">The used **Field Service Products (Fin and Ops to Field Service)** template is based on the **Products (Fin and Ops to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="fe8e8-106">للحصول على مزيد من المعلومات، راجع [المنتجات (Fin and Ops إلى Sales) - مباشر](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="fe8e8-106">For more information, see [Products (Fin and Ops to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="fe8e8-107">يوضح هذا الموضوع فقط الاختلافات بين قالبي ** منتجات Field Service ‏(Fin and Ops إلى Field Service)** و**المنتجات (Fin and Ops إلى Sales) – مباشر**.</span><span class="sxs-lookup"><span data-stu-id="fe8e8-107">This topic only describes the differences between the **Field Service Products (Fin and Ops to Field Service)** and **Products (Fin and Ops to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="fe8e8-108">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="fe8e8-108">Templates and tasks</span></span>

<span data-ttu-id="fe8e8-109">**اسم القالب في تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="fe8e8-109">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="fe8e8-110">منتجات Field Service ‏(Fin and Ops إلى Field Service)</span><span class="sxs-lookup"><span data-stu-id="fe8e8-110">Field Service Products (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="fe8e8-111">**اسم المهمة في مشروع تكامل البيانات:**</span><span class="sxs-lookup"><span data-stu-id="fe8e8-111">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="fe8e8-112">المنتجات - المنتجات</span><span class="sxs-lookup"><span data-stu-id="fe8e8-112">Products - Products</span></span>

<span data-ttu-id="fe8e8-113">يشتمل قالب **منتجات Field Service ‏(Fin and Ops إلى Field Service)** على تعيين واحد غير مضمن في قالب **المنتجات (Fin and Ops إلى Sales) - مباشر**.</span><span class="sxs-lookup"><span data-stu-id="fe8e8-113">The **Field Service Products (Fin and Ops to Field Service)** template includes one mapping that isn't included in the **Products (Fin and Ops to Sales) – Direct** template.</span></span> <span data-ttu-id="fe8e8-114">يضمن هذا التعيين أن يتم تعيين الحقل المطلوب والخاص بـ Field Service **نوع منتج الخدمة** بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="fe8e8-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="fe8e8-115">يتم استخدام تعيين القيمة التالية.</span><span class="sxs-lookup"><span data-stu-id="fe8e8-115">The following value mapping is used.</span></span>

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="fe8e8-116">في Finance and Operations، يتم حساب قيمة **نوع منتج Field Service** في كيان بيانات **منتجات قابلة للبيع تم إصدارها‬** كما يلي:</span><span class="sxs-lookup"><span data-stu-id="fe8e8-116">In Finance and Operations, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="fe8e8-117">**المخزون:** نوع المنتج = مجموعة نماذج الأصناف والمنتجات، منتج مخزّن‬ = صحيح</span><span class="sxs-lookup"><span data-stu-id="fe8e8-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="fe8e8-118">**NonInventory:** نوع المنتج = مجموعة نماذج الأصناف والمنتجات، منتج مخزّن‬ = خطأ</span><span class="sxs-lookup"><span data-stu-id="fe8e8-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="fe8e8-119">**الخدمة:** نوع المنتج = الخدمة</span><span class="sxs-lookup"><span data-stu-id="fe8e8-119">**Service:** Product type = Service</span></span>

