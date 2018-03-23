---
title: "إدارة فئات المنتج"
description: "يصف هذا الموضوع كيف يمكن لمديري ترويج السلع استخدام فئات منتجات Retail لإدارة العلاقات بين التدرج الهرمي لمنتج Retail وتفاصيل المنتجات المُصدرة."
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 25fa39dc81fc721d7593a25a102ce47041ebc5f0
ms.openlocfilehash: 4b7ef962b777a31e1da238a8ec1be9a42ec5bb5f
ms.contentlocale: ar-sa
ms.lasthandoff: 03/13/2018

---


# <a name="enhanced-product-and-category-management"></a><span data-ttu-id="81b4c-103">إدارة الفئات والمنتجات المُحسنة</span><span class="sxs-lookup"><span data-stu-id="81b4c-103">Enhanced product and category management</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="81b4c-104">يصف هذا الموضوع طريقة محسنة لإدارة فئات منتجات Retail والمنتجات في Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="81b4c-104">This topic describes an enhanced way to manage Retail product categories and products in Dynamics 365 for Retail.</span></span> <span data-ttu-id="81b4c-105">تسمح هذه التحسينات لمُدراء ترويج السلع عرض بنية عامة لخصائص المنتجات بين التدرج الهرمي لمنتج Retail وتفاصيل المنتجات المُصدرة.</span><span class="sxs-lookup"><span data-stu-id="81b4c-105">These enhancements let merchandising managers view a common structure of product properties between Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="81b4c-106">لمزيد من المعلومات حول إدارة فئات منتج Retail، انتقل إلى **التدرج الهرمي لمنتجات Retail** من مساحة عمل **إدارة الفئات والمنتجات**، ولاحظ البنية المُحسنة لصفحة **فئة منتج Retail**.</span><span class="sxs-lookup"><span data-stu-id="81b4c-106">To learn more about managing Retail product categories, go to **Retail product hierarchy** from the **Category and product management** workspace, and note the enhanced structure of the **Retail product category** page.</span></span>

![مساحة عمل إدارة الفئات والمنتجات](media/LaunchRetailProductHierarchy.png)

<span data-ttu-id="81b4c-108">في الإصدارات السابقة، تم تقسيم خصائص المنتجات إلى **خصائص منتجات أساسية** و**خصائص منتجات Retail**، بناءً على نطاق إمكانية تطبيقها.</span><span class="sxs-lookup"><span data-stu-id="81b4c-108">In previous versions, product properties were divided into **Basic product properties** and **Retail product properties**, based on the scope of their applicability.</span></span> <span data-ttu-id="81b4c-109">كانت **خصائص منتجات Retail** *عمومية* بحسب نطاق إمكانية التطبيق، مما يعني أنه بالنسبة لـ **خصائص منتج Retail**، تتم مشاركة نفس القيمة عبر كافة الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="81b4c-109">**Retail product properties** were *global* by scope of applicability, which means that for a given **Retail product property**, the same value is shared across all legal entities.</span></span> <span data-ttu-id="81b4c-110">**خصائص المنتجات الأساسية** هي *خاصة بكيان قانوني*.</span><span class="sxs-lookup"><span data-stu-id="81b4c-110">**Basic product properties** are *legal entity specific*.</span></span> <span data-ttu-id="81b4c-111">بمعنى آخر، بالنسبة لـ **خصائص المنتجات الأساسية** قد تختلف القيمة عبر الكيانات القانونية استنادًا إلى متطلبات العمل الفردية.</span><span class="sxs-lookup"><span data-stu-id="81b4c-111">In other words, for a given **Basic product property** the value can differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="81b4c-112">في بنية فئة منتج Retail المُحسنة، يتم فصل خصائص المنتجات بصورة منطقية استنادًا إلى إمكانية تطبيقها داخل مجموعة، لتعكس تفاصيل المنتجات المُصدرة من البنية.</span><span class="sxs-lookup"><span data-stu-id="81b4c-112">In the enhanced Retail product category structure, product properties are logically separated based on their applicability within a group, to reflect the released product details form structure.</span></span>

![تجميع الحقول بناءً على نطاق قابلية تطبيقها](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="81b4c-114">يمكنك التبديل بين إدارة خصائص خاصة بكيان قانوني عبر كافة الكيانات القانونية وإدارتها لكيان قانوني محدد.</span><span class="sxs-lookup"><span data-stu-id="81b4c-114">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="81b4c-115">وللقيام بهذا، حدد إما **عرض/تحرير لكافة الكيانات القانونية** أو **عرض/تحرير لكيان قانوني محدد**.</span><span class="sxs-lookup"><span data-stu-id="81b4c-115">To do this, select either **View/Edit for all legal entities** or **View/Edit for a specific legal entity**.</span></span>

![تبديل طريقة العرض بين شخص وكافة الكيانات القانونية](media/ToggleBackToEditForSpecificLegalEntity.PNG)

![تبديل طريقة العرض بين شخص وكافة الكيانات القانونية](media/ToggleToEditForAllLegalEntities.PNG)  

<span data-ttu-id="81b4c-118">بالمقارنة بالإصدارات السابقة، في بنية فئة منتج Retail الجديدة، يمكن لمُديري الترويج للسلع أيضًا تحديد القيم الافتراضية لمجموعة إضافية من خصائص المنتجات عند مستوى فئة فردية.</span><span class="sxs-lookup"><span data-stu-id="81b4c-118">Compared to previous versions, in the new Retail product category structure a merchandising manager can also define default values for an additional set of product properties at an individual category level.</span></span> <span data-ttu-id="81b4c-119">في وقت إنشاء المنتج، يتم توريث قيم خصائص المنتجات الافتراضية بحسب المنتج، بناءً على اقترانها بفئة فردية من التدرج الهرمي لمنتج Retail.</span><span class="sxs-lookup"><span data-stu-id="81b4c-119">At the time of product creation, these default product property values are inherited by a product, based on their association with an individual category from Retail product hierarchy.</span></span> <span data-ttu-id="81b4c-120">يمكن أيضًا تعديل خصائص المنتجات المتوارثة لكل منتج لتلبية متطلبع العمل الفردية.</span><span class="sxs-lookup"><span data-stu-id="81b4c-120">These inherited product properties can also be modified for each product, to meet individual business requirements.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="81b4c-121">تحديد الخصائص لتحديث المنتجات من نموذج فئة منتجات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="81b4c-121">Select properties to update products from the Retail product category form</span></span> 
 
<span data-ttu-id="81b4c-122">يمكنك استخدام هذه البنية المُحسنة الجديدة لخصائص المنتج لتحديد أي خصائص منتجات مُحدثة يجب دفعها إلى المنتجات المقترنة.</span><span class="sxs-lookup"><span data-stu-id="81b4c-122">You can use this new enhanced structure for product properties to select which updated product properties must be pushed to associated products.</span></span> 

![طريقة العرض الجديدة المحسنة للمنتجات المُحسنة](media/NewUpdateProductsEnhancedView.PNG) 

<span data-ttu-id="81b4c-124">باستطاعة مدراء البضائع تعديل خصائص المنتجات المتوارثة هذه لكل منتج، لتلبية متطلبات العمل الفردية.</span><span class="sxs-lookup"><span data-stu-id="81b4c-124">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>


