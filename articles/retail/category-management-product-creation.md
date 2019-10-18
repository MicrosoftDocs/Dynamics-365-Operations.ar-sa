---
title: إدارة منتجات وفئات منتج Retail
description: يصف هذا الموضوع كيف يمكن لمديري ترويج السلع استخدام فئات منتجات Retail لإدارة العلاقات بين التدرج الهرمي لمنتج Retail وتفاصيل المنتجات المُصدرة.
author: ashishmsft
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: ''
ms.assetid: c7ed2ba5-87c6-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 27870fe6172479b891b885d9e84ca10b250e3399
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019491"
---
# <a name="manage-retail-product-categories-and-products"></a><span data-ttu-id="6ece4-103">إدارة فئات منتجات Retail والمنتجات</span><span class="sxs-lookup"><span data-stu-id="6ece4-103">Manage Retail product categories and products</span></span>

[!include [banner](./includes/banner.md)]

<span data-ttu-id="6ece4-104">يصف هذا الموضوع طريقة محسنة لإدارة فئات المنتجات والمنتجات في Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="6ece4-104">This topic describes an enhanced way to manage product categories and products in Dynamics 365 Retail.</span></span> <span data-ttu-id="6ece4-105">تسمح التحسينات لمُدراء ترويج السلع بعرض بنية خصائص المنتجات المشتركة بين التدرج الهرمي للمنتج وتفاصيل المنتجات المُصدرة.</span><span class="sxs-lookup"><span data-stu-id="6ece4-105">The enhancements let merchandising managers view a structure of product properties that is shared between the product hierarchy and released product details.</span></span>

<span data-ttu-id="6ece4-106">لمزيد من المعلومات حول كيفية إدارة فئات المنتجات، في مساحة عمل **إدارة الفئات والمنتجات**، حدد تجانب **التسلسل الهرمي لمنتج البيع بالتجزئة‬**.</span><span class="sxs-lookup"><span data-stu-id="6ece4-106">To learn more about how to manage product categories, in the **Category and product management** workspace, select the **Retail product hierarchy** tile.</span></span>

<span data-ttu-id="6ece4-107">لاحظ البنية المحسَّنة لصفحة **التدرج الهرمي لمنتجات Retail** التي تظهر.</span><span class="sxs-lookup"><span data-stu-id="6ece4-107">Notice the enhanced structure of the **Retail product hierarchy** page that appears.</span></span> <span data-ttu-id="6ece4-108">في الإصدارات السابقة لـ Retail، تم تقسيم خصائص المنتجات إلى *خصائص المنتجات الأساسية* و*خصائص منتجات Retail*، بناءً على نطاق إمكانية تطبيقها.</span><span class="sxs-lookup"><span data-stu-id="6ece4-108">In previous versions of Retail, product properties were divided into *basic product properties* and *Retail product properties*, based on the scope of their applicability.</span></span> <span data-ttu-id="6ece4-109">خصائص منتجات Retail *عمومية* في نطاق إمكانية تطبيقها.</span><span class="sxs-lookup"><span data-stu-id="6ece4-109">Retail product properties are *global* in their scope of applicability.</span></span> <span data-ttu-id="6ece4-110">بمعنى آخر، بالنسبة إلى خاصية منتج معين، تتم مشاركة نفس القيمة عبر كافة الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="6ece4-110">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="6ece4-111">وفي المقابل، خصائص المنتجات الأساسية هي *خاصة بكيان قانوني*.</span><span class="sxs-lookup"><span data-stu-id="6ece4-111">By contrast, basic product properties are *legal entity–specific*.</span></span> <span data-ttu-id="6ece4-112">بمعنى آخر، بالنسبة لخاصية منتج أساسي محدد، قد تختلف القيمة عبر الكيانات القانونية، استنادًا إلى متطلبات العمل الفردية لكل كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="6ece4-112">In other words, for a given basic product property, the value can differ across legal entities, depending on the individual business requirements of each legal entity.</span></span>

<span data-ttu-id="6ece4-113">في بنية فئة المنتجات المُحسنة، يتم فصل خصائص المنتجات بصورة منطقية استنادًا إلى إمكانية تطبيقها في مجموعة، لتعكس بنية تفاصيل المنتجات المُصدرة من البنية.</span><span class="sxs-lookup"><span data-stu-id="6ece4-113">In the enhanced product category structure, product properties are logically separated based on their applicability in a group, to reflect the structure of the released product details form structure.</span></span>

![الحقول المجمعة بناءً على نطاق إمكانية تطبيق الخصائص](media/NoticeGroupingOfFieldsBasedOnTheirScope.PNG)

<span data-ttu-id="6ece4-115">يمكنك التبديل بين إدارة خصائص خاصة بكيان قانوني عبر كافة الكيانات القانونية وإدارتها لكيان قانوني محدد.</span><span class="sxs-lookup"><span data-stu-id="6ece4-115">You can switch between managing legal entity–specific properties across all legal entities and managing them for a specific legal entity.</span></span>

<span data-ttu-id="6ece4-116">لإدارة خصائص عبر جميع الكيانات القانونية، حدد **طريقة عرض لكافة الكيانات القانونية** (أو **التحرير لكافة الكيانات القانونية**).</span><span class="sxs-lookup"><span data-stu-id="6ece4-116">To manage properties across all legal entities, select **View for all legal entities** (or **Edit for all legal entities**).</span></span>

![عرض/تحرير لكافة الكيانات القانونية](media/ToggleBackToEditForSpecificLegalEntity.PNG)

<span data-ttu-id="6ece4-118">لإدارة الخصائص لأحد الكيانات القانونية المحددة، حدد **طريقة عرض لكيان قانوني محدد** (أو **تحرير لكيان قانوني محدد**).</span><span class="sxs-lookup"><span data-stu-id="6ece4-118">To manage properties for a specific legal entity, select **View for a specific legal entity** (or **Edit for a specific legal entity**).</span></span>

![عرض/تحرير لكيان قانوني محدد](media/ToggleToEditForAllLegalEntities.PNG)

<span data-ttu-id="6ece4-120">بالإضافة إلى ذلك، في بنية محسَّنة لفئة منتج Retail، يمكن لمُدير ترويج الآن تحديد القيم الافتراضية لمجموعة إضافية من خصائص المنتجات عند مستوى الفئة الفردية.</span><span class="sxs-lookup"><span data-stu-id="6ece4-120">Additionally, in the enhanced Retail product category structure, a merchandising manager can now define default values for an additional set of product properties at the level of the individual category.</span></span> <span data-ttu-id="6ece4-121">وعندما يتم إنشاء المنتجات بعد ذلك، فإنها تورث القيم الافتراضية لخصائص منتجاتها، بناءً على اقتران هذه الخصائص بفئة فردية من التدرج الهرمي للمنتجات.</span><span class="sxs-lookup"><span data-stu-id="6ece4-121">Then, when products are created, they inherit default values for their product properties, based on the association of those properties with an individual category in the product hierarchy.</span></span> <span data-ttu-id="6ece4-122">يمكن أيضًا تعديل خصائص المنتجات المتوارثة لكل منتج لتلبية متطلبات العمل الفردية.</span><span class="sxs-lookup"><span data-stu-id="6ece4-122">These inherited product properties can also be modified for each product to meet individual business requirements.</span></span>

## <a name="selecting-properties-to-update-products-on-the-retail-product-hierarchy-page"></a><span data-ttu-id="6ece4-123">تحديد الخصائص لتحديث المنتجات في صفحة التدرج الهرمي لمنتجات Retail</span><span class="sxs-lookup"><span data-stu-id="6ece4-123">Selecting properties to update products on the Retail product hierarchy page</span></span>

<span data-ttu-id="6ece4-124">يمكنك استخدام هذه البنية المُحسنة الجديدة لخصائص المنتج لتحديد خصائص منتجات مُحدثة يجب دفعها إلى المنتجات المقترنة.</span><span class="sxs-lookup"><span data-stu-id="6ece4-124">You can use the new enhanced structure for product properties to select updated product properties that must be pushed to the associated products.</span></span> <span data-ttu-id="6ece4-125">في صفحة **التدرج الهرمي لمنتجات Retail**، في "جزء الإجراءات"، حدد **فئة**، ثم حدد **تحديث المنتجات** لفتح مربع الحوار **تحديث المنتجات**.</span><span class="sxs-lookup"><span data-stu-id="6ece4-125">On the **Retail product hierarchy** page, on the Action Pane, select **Category**, and then select **Update products** to open the **Update products** dialog box.</span></span>

![مربع الحوار تحديث المنتجات](media/NewUpdateProductsEnhancedView.PNG)
