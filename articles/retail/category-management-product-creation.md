---
title: "إدارة وإنشاء فئات المنتجات"
description: "يصف هذا الموضوع التحسينات التي تم إدخالها على تجربة الإدارة لفئات منتجات البيع بالتجزئة. تسمح هذه التحسينات لمدراء البضائع بإنشاء ارتباط بين التدرج الهرمي لمنتجات البيع بالتجزئة وتفاصيل المنتجات الصادرة."
author: ashishmsft
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
ms.search.form: RetailCategoryAndProductWorkspace, RetailCategory
audience: Application User
ms.search.scope: Core, Retail
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: e269f6c3815cea55b69b7eb6a9a65bf7c9e15378
ms.contentlocale: ar-sa
ms.lasthandoff: 01/17/2018

---

# <a name="product-category-management-and-creation"></a><span data-ttu-id="a4fa3-104">إدارة وإنشاء فئات المنتجات</span><span class="sxs-lookup"><span data-stu-id="a4fa3-104">Product category management and creation</span></span>

[!include[banner](./includes/banner.md)]

<span data-ttu-id="a4fa3-105">إن التحسينات التي تم إدخالها على تجربة الإدارة لفئات منتجات البيع بالتجزئة تسمح لمدراء البضائع بإنشاء ارتباط بين التدرج الهرمي لمنتجات البيع بالتجزئة وتفاصيل المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="a4fa3-105">Enhancements that have been made to the management experience for Retail product categories let merchandising managers have a correlation between Retail product hierarchy and released product details.</span></span> <span data-ttu-id="a4fa3-106">لعرض هذه التحسينات في مساحة عمل **إدارة الفئات والمنتجات**، حدد **التدرج الهرمي لمنتجات البيع بالتجزئة‏‎** لفتح الصفحة **البنية الجديدة لفئة منتجات البيع بالتجزئة**.</span><span class="sxs-lookup"><span data-stu-id="a4fa3-106">To view these enhancements, in the **Category & product management**  workspace, select **Retail product hierarchy** to open the **New structure of Retail product category** page.</span></span> 

<span data-ttu-id="a4fa3-107">في الإصدارات السابقة، تم تقسيم خصائص المنتج إلى خصائص منتجات أساسية وخصائص منتجات البيع بالتجزئة، بالاستناد إلى نطاق إمكانية تطبيقها.</span><span class="sxs-lookup"><span data-stu-id="a4fa3-107">In previous releases, product properties were divided into Basic product properties and Retail product properties, based on the scope of their applicability.</span></span> <span data-ttu-id="a4fa3-108">كانت خصائص منتجات البيع بالتجزئة *عمومية*.</span><span class="sxs-lookup"><span data-stu-id="a4fa3-108">Retail product properties were *global*.</span></span> <span data-ttu-id="a4fa3-109">بمعنى آخر، بالنسبة إلى خاصية منتج معين، تتم مشاركة نفس القيمة عبر كافة الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="a4fa3-109">In other words, for a given product property, the same value is shared across all legal entities.</span></span> <span data-ttu-id="a4fa3-110">كانت خصائص المنتجات الأساسية *خاصة بكيان قانوني*.</span><span class="sxs-lookup"><span data-stu-id="a4fa3-110">Basic product properties were *legal entity–specific*.</span></span> <span data-ttu-id="a4fa3-111">بمعنى آخر، قد تختلف خاصية منتج معين عبر الكيانات القانونية، استنادًا إلى متطلبات العمل الفردية.</span><span class="sxs-lookup"><span data-stu-id="a4fa3-111">In other words, a given product property might differ across legal entities, based on individual business requirements.</span></span>

<span data-ttu-id="a4fa3-112">من خلال هذه التحسينات، لخصائص المنتجات في فئة منتجات البيع بالتجزئة، نستمر في فصل الحقول، استنادًا إلى إمكانية تطبيقها داخل مجموعة، لعكس بنية نموذج تفاصيل المنتجات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="a4fa3-112">With these enhancements, for product properties in the Retail product category, we continue to separate the fields, based on their applicability within a group, to reflect the released product details form structure.</span></span>

<span data-ttu-id="a4fa3-113">يمكنك التبديل بين إدارة خصائص خاصة بكيان قانوني عبر كافة الكيانات القانونية وإدارتها لكيان قانوني محدد.</span><span class="sxs-lookup"><span data-stu-id="a4fa3-113">You can switch between managing legal-entity specific properties across all legal entities and managing them for a specific legal entity.</span></span> <span data-ttu-id="a4fa3-114">حدد فقط **عرض/تحرير لكافة الكيانات القانونية** أو **عرض/تحرير لكيان قانوني محدد** كما تقتضي الحاجة.</span><span class="sxs-lookup"><span data-stu-id="a4fa3-114">Just select **View/Edit for all legal entities** or **View/Edit for a specific legal entity** as you require.</span></span>

<span data-ttu-id="a4fa3-115">باستطاعة مدراء البضائع أيضًا تحديد قيم افتراضية لمجموعة إضافية من خصائص المنتج على مستوى فئة فردية.</span><span class="sxs-lookup"><span data-stu-id="a4fa3-115">Merchandising managers can also define default values for an additional set of product properties at the level of an individual category.</span></span> <span data-ttu-id="a4fa3-116">يتم توارث قيم الخصائص هذه بواسطة منتج، استنادًا إلى اقترانها بفئة في وقت إنشاء المنتج.</span><span class="sxs-lookup"><span data-stu-id="a4fa3-116">These property values are inherited by a product, based on their association with a category at the time of product creation.</span></span>

## <a name="select-properties-to-update-products-from-the-retail-product-category-form"></a><span data-ttu-id="a4fa3-117">تحديد الخصائص لتحديث المنتجات من نموذج فئة منتجات البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="a4fa3-117">Select properties to update products from the Retail product category form</span></span>

<span data-ttu-id="a4fa3-118">يمكنك استخدام خصائص التجميع المنطقي لتحديد خصائص المنتجات المحدثة التي يجب دفعها إلى المنتجات المقترنة.</span><span class="sxs-lookup"><span data-stu-id="a4fa3-118">You can use logical grouping properties to select which updated product properties should be pushed to associated products.</span></span>

<span data-ttu-id="a4fa3-119">باستطاعة مدراء البضائع تعديل خصائص المنتجات المتوارثة هذه لكل منتج، لتلبية متطلبات العمل الفردية.</span><span class="sxs-lookup"><span data-stu-id="a4fa3-119">Merchandising managers can modify these inherited product properties for each product, to meet individual business requirements.</span></span>

