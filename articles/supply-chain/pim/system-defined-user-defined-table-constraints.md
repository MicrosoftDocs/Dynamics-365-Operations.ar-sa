---
title: "قيود الجدول المحددة بواسطة المستخدم أو المحددة بواسطة النظام"
description: "توضح هذه المقالة نوعي قيود الجدول للمكونات في نموذج تكوين منتج: القيود المحددة من قِبل المستخدم والقيود المحددة من قِبل النظام. تمثل قيود الجدول مقاييس مجموعات السمات المسموح بها، حيث يعرّف كل صف مجموعة واحدة من قيم السمات الممكنة."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 954c7bb6d9d78b1908331c2bb660fdfb35f5f986
ms.contentlocale: ar-sa
ms.lasthandoff: 01/17/2018

---

# <a name="system-defined-and-user-defined-table-constraints"></a><span data-ttu-id="4d8b9-104">قيود الجدول المحددة بواسطة المستخدم أو المحددة بواسطة النظام</span><span class="sxs-lookup"><span data-stu-id="4d8b9-104">System-defined and user-defined table constraints</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4d8b9-105">توضح هذه المقالة نوعي قيود الجدول للمكونات في نموذج تكوين منتج: القيود المحددة من قِبل المستخدم والقيود المحددة من قِبل النظام.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-105">This article explains the two types of table constraints for components in a product configuration model -  user-defined and system-defined.</span></span> <span data-ttu-id="4d8b9-106">تمثل قيود الجدول مقاييس مجموعات السمات المسموح بها، حيث يعرّف كل صف مجموعة واحدة من قيم السمات الممكنة.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-106">Table constraints represent matrices of the allowed attribute combinations, where each row defines one set of possible attribute values.</span></span>

<span data-ttu-id="4d8b9-107">تمثل قيود الجدول تمثل مقاييس مجموعات السمات المسموح بها للمكونات في نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-107">Table constraints represent matrices of the combinations of attributes that are allowed for components in a product configuration model.</span></span> <span data-ttu-id="4d8b9-108">يحدد كل صف في الجدول مجموعة من قيم السمات الممكنة.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-108">Each row in the table defines one set of possible attribute values.</span></span> <span data-ttu-id="4d8b9-109">يمكنك تعريف نوعين من القيود في نموذج تكوين منتج:</span><span class="sxs-lookup"><span data-stu-id="4d8b9-109">You can declare two types of constraints in a product configuration model:</span></span>

-   <span data-ttu-id="4d8b9-110">**قيد التعبير** – إنشاء تعبير يحدد العلاقات بين السمات لضمان أنه يمكن تحديد قيم متوافقة فقط أثناء تكوين المنتج.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-110">**Expression constraint** – Create an expression that defines relations between attributes to guarantee that only compatible values can be selected during product configuration.</span></span>
-   <span data-ttu-id="4d8b9-111">**قيد الجدول** -إنشاء جدول يحدد كافة المجموعات المسموح بها لمجموعة محددة من السمات.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-111">**Table constraint** – Create a table that defines all the combinations that are allowed for a specified set of attributes.</span></span> <span data-ttu-id="4d8b9-112">يتوفر نوعان من قيود الجدول: قيود الجدول المحددة من قِبل المستخدم وقيود الجدول المحددة من قِبل النظام.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-112">Two types of table constraints are available: user-defined table constraints and system-defined table constraints.</span></span>

<span data-ttu-id="4d8b9-113">توضح هذه المقالة قيود الجدول المحددة من قِبل المستخدم والمحددة من قِبل النظام للمكونات في نموذج تكوين منتج.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-113">This article describes user-defined and system-defined table constraints for components in a product configuration model.</span></span>

## <a name="user-defined-table-constraints"></a><span data-ttu-id="4d8b9-114">قيود الجدول المحددة من قِبل المستخدم</span><span class="sxs-lookup"><span data-stu-id="4d8b9-114">User-defined table constraints</span></span>
<span data-ttu-id="4d8b9-115">قيد الجدول المحدد بواسطة المستخدم هو نوع مصفوفة يتم استخدامها لتوضيح مجموعات قيم السمات المحددة التي تحددها أنواع السمات.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-115">A user-defined table constraint is a type of matrix that is used to describe the combinations of attribute values that are defined by attribute types.</span></span> <span data-ttu-id="4d8b9-116">على سبيل المثال، إذا قمت بإنتاج مكبرات الصوت، يمكنك تضمين أعمدة للون الكابينة والشبكة الأمامية في قيود الجدول المحدد من قِبل المستخدم.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-116">For example, if you produce speakers, you can include columns for the cabinet finish and the front grill in the user-defined table constraint.</span></span> <span data-ttu-id="4d8b9-117">ويشتمل نوع السمة للون الكابينة على أربع قيم، ويشتمل نوع السمة للشبكة الأمامية على ثلاث قيم.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-117">The attribute type for the cabinet finish has four values, and the attribute type for the front grill has three values.</span></span> <span data-ttu-id="4d8b9-118">ولذلك، إذا لم يتم استخدام القيود، هناك 4 × 3 = 12 مجموعة ممكنة.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-118">Therefore, if constraints aren't used, there are 4 × 3 = 12 possible combinations.</span></span> <span data-ttu-id="4d8b9-119">ومع ذلك، في هذا المثال، لا يثسمح بسوى ست مجموعات، كما هو موضح في الجدول التالي.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-119">However, in this example, only six combinations are allowed, as shown in the following table.</span></span> <span data-ttu-id="4d8b9-120">يتم عرض هذه المعلومات في علامة التبويب **المجموعات المسموح بها** في صفحة **تحرير قيود الجدول**.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-120">This information is displayed on the **Allowed combinations** tab on the **Edit table constraint** page.</span></span>

| <span data-ttu-id="4d8b9-121">لون الكابينة</span><span class="sxs-lookup"><span data-stu-id="4d8b9-121">Cabinet finish</span></span> | <span data-ttu-id="4d8b9-122">الشبكة الأمامية</span><span class="sxs-lookup"><span data-stu-id="4d8b9-122">Front grill</span></span> |
|----------------|-------------|
| <span data-ttu-id="4d8b9-123">أسود</span><span class="sxs-lookup"><span data-stu-id="4d8b9-123">Black</span></span>          | <span data-ttu-id="4d8b9-124">أسود</span><span class="sxs-lookup"><span data-stu-id="4d8b9-124">Black</span></span>       |
| <span data-ttu-id="4d8b9-125">أسود</span><span class="sxs-lookup"><span data-stu-id="4d8b9-125">Black</span></span>          | <span data-ttu-id="4d8b9-126">معدني</span><span class="sxs-lookup"><span data-stu-id="4d8b9-126">Metal</span></span>       |
| <span data-ttu-id="4d8b9-127">بلوطي</span><span class="sxs-lookup"><span data-stu-id="4d8b9-127">Oak</span></span>            | <span data-ttu-id="4d8b9-128">أسود</span><span class="sxs-lookup"><span data-stu-id="4d8b9-128">Black</span></span>       |
| <span data-ttu-id="4d8b9-129">روزوود</span><span class="sxs-lookup"><span data-stu-id="4d8b9-129">Rosewood</span></span>       | <span data-ttu-id="4d8b9-130">أبيض</span><span class="sxs-lookup"><span data-stu-id="4d8b9-130">White</span></span>       |
| <span data-ttu-id="4d8b9-131">أبيض</span><span class="sxs-lookup"><span data-stu-id="4d8b9-131">White</span></span>          | <span data-ttu-id="4d8b9-132">أسود</span><span class="sxs-lookup"><span data-stu-id="4d8b9-132">Black</span></span>       |
| <span data-ttu-id="4d8b9-133">أبيض</span><span class="sxs-lookup"><span data-stu-id="4d8b9-133">White</span></span>          | <span data-ttu-id="4d8b9-134">أبيض</span><span class="sxs-lookup"><span data-stu-id="4d8b9-134">White</span></span>       |

<span data-ttu-id="4d8b9-135">يتم تحديد قيود الجدول المحددة من قِبل المستخدم بإدخال جدول ثابت يعمل بنفس الطريقة كقيد تعبير.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-135">User-defined table constraints are defined by static table input that works the same way as an expression constraint.</span></span> <span data-ttu-id="4d8b9-136">وعند استخدام قيد الجدول المحدد من قِبل المستخدم، تتمثل الميزة في أن الجداول غالباً ما تكون أسهل في الإنشاء والفهم والحفظ من قيود التعبير الطويلة.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-136">When you use a user-defined table constraint, the advantage is that tables are often easier to create, understand, and maintain than long expression constraints.</span></span>

## <a name="system-defined-table-constraints"></a><span data-ttu-id="4d8b9-137">قيود الجدول المحدد بواسطة النظام</span><span class="sxs-lookup"><span data-stu-id="4d8b9-137">System-defined table constraints</span></span>
<span data-ttu-id="4d8b9-138">يُنشئ قيد الجدول المحدد بواسطة النظام تعيينًا ديناميكيًا بين نوع سمة وحقل في جدول.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-138">A system-defined table constraint creates a dynamic mapping between an attribute type and a field in a table.</span></span> <span data-ttu-id="4d8b9-139">وتم تضمين قيد جدول محدد من قِبل النظام في نموذج تكوين منتج، ويضمن التعيين إظهار البيانات في الجدول بدلاً من قيم نوع السمة.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-139">When a system-defined table constraint is included in a product configuration model, the mapping guarantees that the data in the table is shown instead of the values of the attribute type.</span></span> <span data-ttu-id="4d8b9-140">والنتيجة هي قيد ديناميكي، لأنه يمكن تعديل جدول المحتويات (على سبيل المثال، بالوحدات الأخرى).</span><span class="sxs-lookup"><span data-stu-id="4d8b9-140">The result is a dynamic constraint, because the table contents can be modified (for example, by other modules).</span></span>  

<span data-ttu-id="4d8b9-141">وعند إنشاء قيد جدول محدد من قِبل النظام، يمكنك تحديد جدول وتحديد الاستعلام المراد استخدامه اختياريًا، ثم إقران أنواع السمات بالحقول الموجودة في الجدول المحدد.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-141">When you create a system-defined table constraint, you select a table, optionally define the query to use, and then associate attribute types to the fields in the selected table.</span></span> <span data-ttu-id="4d8b9-142">ويجب أن تطابق أنواع الحقول أنواع السمات.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-142">The types of fields must match the types of attribute types.</span></span>  

<span data-ttu-id="4d8b9-143">‏‫وقبل سريان مفعول قيد جدول على نموذج تكوين منتج، يجب تضمين قيد الجدول في قيد في أحد مكونات النموذج.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-143">Before a table constraint can take effect on a product configuration model, the table constraint must be included in a constraint on one of the model's components.</span></span> <span data-ttu-id="4d8b9-144">والإجراء هو إنشاء قيد جديد، حدد نوع قيد الجدول، ثم حدد تعريف قيد الجدول المراد استخدامه.‬</span><span class="sxs-lookup"><span data-stu-id="4d8b9-144">The procedure is to create a new constraint, select the table constraint type, and then select the table constraint definition to use.</span></span> <span data-ttu-id="4d8b9-145">وأخيراً، يجب تعيين كافة الحقول في قيد الجدول إلى السمات في نموذج تكوين المنتج.</span><span class="sxs-lookup"><span data-stu-id="4d8b9-145">Finally, all fields in the table constraint must be mapped to attributes in the product configuration model.</span></span>

<a name="see-also"></a><span data-ttu-id="4d8b9-146">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="4d8b9-146">See also</span></span>
--------

[<span data-ttu-id="4d8b9-147">المفاهيم الأساسية في نماذج تكوين المنتجات</span><span class="sxs-lookup"><span data-stu-id="4d8b9-147">Key concepts in product configuration models</span></span>](product-configuration-models.md)




