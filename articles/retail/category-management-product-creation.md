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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 106beb8c2c69f8cef2abf0db9015b079248e0a66
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---

# <a name="manage-retail-product-categories-and-products"></a><span data-ttu-id="363ea-103">إدارة منتجات وفئات منتج Retail</span><span class="sxs-lookup"><span data-stu-id="363ea-103">Manage Retail product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="363ea-104">يصف هذا الموضوع طريقة محسنة لإدارة فئات منتجات Retail والمنتجات في Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="363ea-104">This topic describes an enhanced way to manage Retail product categories and products in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="363ea-105">تسمح التحسينات لمُدراء ترويج السلع بعرض بنية خصائص المنتجات المشتركة بين التدرج الهرمي لمنتج Retail وتفاصيل المنتجات المُصدرة.</span><span class="sxs-lookup"><span data-stu-id="363ea-105">The enhancements let merchandising managers view a structure of product properties that is shared between the Retail product hierarchy and released product details.</span></span>

<span data-ttu-id="363ea-106">لمزيد من المعلومات حول كيفية إدارة فئات منتج Retail، في مساحة عمل **إدارة الفئات والمنتجات**، حدد تجانب **التدرج الهرمي لمنتجات Retail**.</span><span class="sxs-lookup"><span data-stu-id="363ea-106">To learn more about how to manage Retail product categories, in the **Category and product management** workspace, select the **Retail product hierarchy** tile.</span></span>

<span data-ttu-id="363ea-107">لاحظ البنية المحسَّنة لصفحة **التدرج الهرمي لمنتجات Retail** التي تظهر.</span><span class="sxs-lookup"><span data-stu-id="363ea-107">Notice the enhanced structure of the **Retail product hierarchy** page that appears.</span></span> <span data-ttu-id="363ea-108">في الإصدارات السابقة لـ Retail، تم تقسيم خصائص المنتجات إلى *خصائص المنتجات الأساسية* و*خصائص منتجات Retail*، بناءً على نطاق إمكانية تطبيقها.</span><span class="sxs-lookup"><span data-stu-id="363ea-108">In previous versions of Retail, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="363ea-109">خصائص منتجات Retail *عمومية* في نطاق إمكانية تطبيقها.</span><span class="sxs-lookup"><span data-stu-id="363ea-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="363ea-110">بمعنى آخر، بالنسبة إلى خاصية منتج Retail معين، تتم مشاركة نفس القيمة عبر كافة الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="363ea-110">In other words, for a given Retail product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="363ea-111">وفي المقابل، خصائص المنتجات الأساسية هي *خاصة بكيان قانوني*.</span><span class="sxs-lookup"><span data-stu-id="363ea-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="363ea-112">بمعنى آخر، بالنسبة لخاصية منتج أساسي محدد، قد تختلف القيمة عبر الكيانات القانونية، استنادًا إلى متطلبات العمل الفردية لكل كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="363ea-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="363ea-113">في بنية فئة منتج Retail المُحسنة، يتم فصل خصائص المنتجات بصورة منطقية استنادًا إلى إمكانية تطبيقها في مجموعة، لتعكس بنية تفاصيل المنتجات المُصدرة من البنية.</span><span class="sxs-lookup"><span data-stu-id="363ea-113">In the enhanced Retail product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![الحقول المجمعة بناءً على نطاق إمكانية تطبيق الخصائص](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="363ea-115">يمكنك التبديل بين إدارة خصائص خاصة بكيان قانوني عبر كافة الكيانات القانونية وإدارتها لكيان قانوني محدد.</span><span class="sxs-lookup"><span data-stu-id="363ea-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="363ea-116">لإدارة خصائص عبر جميع الكيانات القانونية، حدد **طريقة عرض لكافة الكيانات القانونية** (أو **التحرير لكافة الكيانات القانونية**).</span><span class="sxs-lookup"><span data-stu-id="363ea-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![عرض/تحرير لكافة الكيانات القانونية](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="363ea-118">لإدارة الخصائص لأحد الكيانات القانونية المحددة، حدد **طريقة عرض لكيان قانوني محدد** (أو **تحرير لكيان قانوني محدد**).</span><span class="sxs-lookup"><span data-stu-id="363ea-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![عرض/تحرير لكيان قانوني محدد](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="363ea-120">بالإضافة إلى ذلك، في بنية محسَّنة لفئة منتج Retail، يمكن لمُدير ترويج الآن تحديد القيم الافتراضية لمجموعة إضافية من خصائص المنتجات عند مستوى الفئة الفردية.</span><span class="sxs-lookup"><span data-stu-id="363ea-120">Additionally, in the enhanced Retail product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="363ea-121">وعندما يتم إنشاء المنتجات بعد ذلك، فإنها تورث القيم الافتراضية لخضائص منتجاتها، بناءً على اقتران هذه الخصائص بفئة فردية من التدرج الهرمي لمنتج Retail.</span><span class="sxs-lookup"><span data-stu-id="363ea-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in Retail product hierarchy.</span></span> <span data-ttu-id="363ea-122">يمكن أيضًا تعديل خصائص المنتجات المتوارثة لكل منتج لتلبية متطلبات العمل الفردية.</span><span class="sxs-lookup"><span data-stu-id="363ea-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a><span data-ttu-id="363ea-123">تحديد الخصائص لتحديث المنتجات في صفحة التدرج الهرمي لمنتجات Retail</span><span class="sxs-lookup"><span data-stu-id="363ea-123">Selecting properties to update products on the Retail product hierarchy page</span></span>

<span data-ttu-id="363ea-124">يمكنك استخدام هذه البنية المُحسنة الجديدة لخصائص المنتج لتحديد خصائص منتجات مُحدثة يجب دفعها إلى المنتجات المقترنة.</span><span class="sxs-lookup"><span data-stu-id="363ea-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="363ea-125">في صفحة **التدرج الهرمي لمنتجات Retail**، في "جزء الإجراءات"، حدد **فئة**، ثم حدد **تحديث المنتجات** لفتح مربع الحوار **تحديث المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="363ea-125">On the **Retail product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![مربع الحوار تحديث المنتجات](media/NewUpdateProductsEnhancedView.PNG)


