---
title: مزامنة المنتجات في Supply Chain Management مع المنتجات في Field Service
description: يصف هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 04/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: ffa0616d51127a024bea526c5926a182c0449971
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996716"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a><span data-ttu-id="5474c-103">مزامنة المنتجات في Supply Chain Management مع المنتجات في Field Service</span><span class="sxs-lookup"><span data-stu-id="5474c-103">Synchronize products in Supply Chain Management to products in Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5474c-104">يناقش هذا الموضوع القوالب والمهمة الأساسية التي يتم استخدامها لمزامنة المنتجات من Dynamics 365 Supply Chain Management إلى Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="5474c-104">This topic discusses the templates and underlying task that are used to synchronize products from Dynamics 365 Supply Chain Management to Dynamics 365  Field Service.</span></span>

<span data-ttu-id="5474c-105">يستند قالب **منتجات Field Service ‏(Supply Chain Management إلى Field Service)** إلى قالب **المنتجات (Supply Chain Management إلى Sales) - مباشر** من العميل المتوقع إلى النقدية.</span><span class="sxs-lookup"><span data-stu-id="5474c-105">The used **Field Service Products (Supply Chain Management to Field Service)** template is based on the **Products (Supply Chain Management to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="5474c-106">للحصول على مزيد من المعلومات، راجع [المنتجات (Supply Chain Management إلى Sales) - مباشر](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="5474c-106">For more information, see [Products (Supply Chain Management to Sales) – Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="5474c-107">يوضح هذا الموضوع فقط الاختلافات بين قالبي **منتجات Field Service ‏(Supply Chain Management إلى Field Service)** و **المنتجات (Supply Chain Management إلى Sales) – مباشر**.</span><span class="sxs-lookup"><span data-stu-id="5474c-107">This topic only describes the differences between the **Field Service Products (Supply Chain Management to Field Service)** and **Products (Supply Chain Management to Sales) – Direct** templates.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="5474c-108">القوالب والمهام</span><span class="sxs-lookup"><span data-stu-id="5474c-108">Templates and tasks</span></span>

<span data-ttu-id="5474c-109">**اسم القالب في تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="5474c-109">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="5474c-110">منتجات Field Service ‏(Supply Chain Management إلى Field Service)</span><span class="sxs-lookup"><span data-stu-id="5474c-110">Field Service Products (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="5474c-111">**اسم المهمة في مشروع تكامل البيانات**</span><span class="sxs-lookup"><span data-stu-id="5474c-111">**Name of the task in the Data integration project**</span></span>

- <span data-ttu-id="5474c-112">المنتجات - المنتجات</span><span class="sxs-lookup"><span data-stu-id="5474c-112">Products - Products</span></span>

<span data-ttu-id="5474c-113">يتضمن قالب **منتجات Field Service ‏(Supply Chain Management إلى Field Service)** تعيينًا غير مضمن في قالب **المنتجات (Supply Chain Management إلى Sales) - مباشر**.</span><span class="sxs-lookup"><span data-stu-id="5474c-113">The **Field Service Products (Supply Chain Management to Field Service)** template includes one mapping that isn't included in the **Products (Supply Chain Management to Sales) – Direct** template.</span></span> <span data-ttu-id="5474c-114">يضمن هذا التعيين أن يتم تعيين الحقل المطلوب والخاص بـ Field Service **نوع منتج الخدمة** بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="5474c-114">This mapping ensures that the required Field Service-specific field **Service Product Type** is set correctly.</span></span>

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

<span data-ttu-id="5474c-115">يتم استخدام تعيين القيمة التالية.</span><span class="sxs-lookup"><span data-stu-id="5474c-115">The following value mapping is used.</span></span>

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

<span data-ttu-id="5474c-116">في Supply Chain Management، يتم حساب قيمة **نوع منتج Field Service** في كيان بيانات **منتجات قابلة للبيع تم إصدارها‬** كما يلي:</span><span class="sxs-lookup"><span data-stu-id="5474c-116">In Supply Chain Management, the **Field Service product type** value on the **Sellable released products** data entity is calculated as follows:</span></span>

- <span data-ttu-id="5474c-117">**المخزون:** نوع المنتج = مجموعة نماذج الأصناف والمنتجات، منتج مخزّن‬ = صحيح</span><span class="sxs-lookup"><span data-stu-id="5474c-117">**Inventory:** Product type = Product and Item model group, Stocked product = True</span></span>
- <span data-ttu-id="5474c-118">**NonInventory:** نوع المنتج = مجموعة نماذج الأصناف والمنتجات، منتج مخزّن‬ = خطأ</span><span class="sxs-lookup"><span data-stu-id="5474c-118">**NonInventory:** Product type = Product and Item model group, Stocked product = False</span></span>
- <span data-ttu-id="5474c-119">**الخدمة:** نوع المنتج = الخدمة</span><span class="sxs-lookup"><span data-stu-id="5474c-119">**Service:** Product type = Service</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5474c-120">تعيين القالب في تكامل البيانات</span><span class="sxs-lookup"><span data-stu-id="5474c-120">Template mapping in Data integration</span></span>

<span data-ttu-id="5474c-121">تبين الأشكال التوضيحية التالية تعيين القالب في تكامل البيانات.</span><span class="sxs-lookup"><span data-stu-id="5474c-121">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a><span data-ttu-id="5474c-122">منتجات Field Service ‏(Supply Chain Management إلى Field Service): المنتجات - المنتجات</span><span class="sxs-lookup"><span data-stu-id="5474c-122">Field Service Products (Supply Chain Management to Field Service): Products - Products</span></span>

<span data-ttu-id="5474c-123">[![تعيين القالب في تكامل البيانات](./media/FSProduct.png)](./media/FSProduct.png)</span><span class="sxs-lookup"><span data-stu-id="5474c-123">[![Template mapping in Data integration](./media/FSProduct.png)](./media/FSProduct.png)</span></span>
