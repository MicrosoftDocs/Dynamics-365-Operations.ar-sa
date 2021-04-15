---
title: SPLITLISTBYLIMIT ER وظيفة
description: يوفر هذا الموضوع معلومات حول كيفية استخدام وظيفة إعداد التقارير الإلكترونية SPLITLISTBYLIMIT (ER).
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb492560a453ec59bb82d24dd6717f409bd8b257
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745535"
---
# <a name="splitlistbylimit-er-function"></a><span data-ttu-id="0295c-103">SPLITLISTBYLIMIT ER وظيفة</span><span class="sxs-lookup"><span data-stu-id="0295c-103">SPLITLISTBYLIMIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0295c-104">تقسم الوظيفة `SPLITLISTBYLIMIT` القائمة المُحددة إلى قائمة جديدة من القوائم الفرعية (دفعات).</span><span class="sxs-lookup"><span data-stu-id="0295c-104">The `SPLITLISTBYLIMIT` function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="0295c-105">يتم حساب عدد السجلات في كل دفعة بشكل ديناميكي.</span><span class="sxs-lookup"><span data-stu-id="0295c-105">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="0295c-106">ثم تُرجع الوظيفة النتيجة كقيمة *قائمة سجلات* جديدة التي تتكون من الدفعات.</span><span class="sxs-lookup"><span data-stu-id="0295c-106">The function then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="0295c-107">بناء الجملة</span><span class="sxs-lookup"><span data-stu-id="0295c-107">Syntax</span></span>

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a><span data-ttu-id="0295c-108">الوسائط</span><span class="sxs-lookup"><span data-stu-id="0295c-108">Arguments</span></span>

<span data-ttu-id="0295c-109">`list`: *قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="0295c-109">`list`: *Record list*</span></span>

<span data-ttu-id="0295c-110">مسار صالح لمصدر بيانات من نوع البيانات *قائمة السجلات*.</span><span class="sxs-lookup"><span data-stu-id="0295c-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="0295c-111">`limit value`: *عدد صحيح* أو *حقيقي*</span><span class="sxs-lookup"><span data-stu-id="0295c-111">`limit value`: *Integer* or *Real*</span></span>

<span data-ttu-id="0295c-112">الحد الأقصى لقيمة الحد المستخدم لتقسيم القائمة الأصلية إلى دفعات.</span><span class="sxs-lookup"><span data-stu-id="0295c-112">The maximum value of the limit that is used to split the original list into batches.</span></span>

<span data-ttu-id="0295c-113">`limit source`: *الحقل*</span><span class="sxs-lookup"><span data-stu-id="0295c-113">`limit source`: *Field*</span></span>

<span data-ttu-id="0295c-114">المسار الصالح لحقل من النوع *عدد صحيح* أو *حقيقي* في القائمة المُحددة.</span><span class="sxs-lookup"><span data-stu-id="0295c-114">The valid path of a field of the *Integer* or *Real* type in the specified list.</span></span> <span data-ttu-id="0295c-115">تُحدد قيمة هذا الحقل الخطوة التي يتم فيها زيادة إجمالي المجموع.</span><span class="sxs-lookup"><span data-stu-id="0295c-115">The value of this field defines the step that the total sum is increased on.</span></span>

## <a name="return-values"></a><span data-ttu-id="0295c-116">إرجاع القيم</span><span class="sxs-lookup"><span data-stu-id="0295c-116">Return values</span></span>

<span data-ttu-id="0295c-117">*قائمة السجلات*</span><span class="sxs-lookup"><span data-stu-id="0295c-117">*Record list*</span></span>

<span data-ttu-id="0295c-118">قائمة السجلات الناتجة.</span><span class="sxs-lookup"><span data-stu-id="0295c-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0295c-119">ملاحظات الاستخدام</span><span class="sxs-lookup"><span data-stu-id="0295c-119">Usage notes</span></span>

<span data-ttu-id="0295c-120">تحتوي قائمة الدفعات التي تم إرجاعها على العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="0295c-120">The list of batches that is returned contains the following elements:</span></span>

- <span data-ttu-id="0295c-121">**القيمة**: *القائمة*</span><span class="sxs-lookup"><span data-stu-id="0295c-121">**Value**: *List*</span></span>

    <span data-ttu-id="0295c-122">قائمة السجلات التي تخص الدفعة الحالية.</span><span class="sxs-lookup"><span data-stu-id="0295c-122">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="0295c-123">**BatchNumber**: *عدد صحيح*</span><span class="sxs-lookup"><span data-stu-id="0295c-123">**BatchNumber**: *Integer*</span></span>

    <span data-ttu-id="0295c-124">عدد الدفعات الحالية في القائمة المُرتجعة.</span><span class="sxs-lookup"><span data-stu-id="0295c-124">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="0295c-125">لا يتم تطبيق الحد على صنف واحد من القائمة الأصلية عندما يقوم مصدر الحد بتجاوز الحد المعرّف.</span><span class="sxs-lookup"><span data-stu-id="0295c-125">The limit isn't applied to a single item of the original list if the limit source exceeds the defined limit.</span></span>

## <a name="example"></a><span data-ttu-id="0295c-126">مثال</span><span class="sxs-lookup"><span data-stu-id="0295c-126">Example</span></span>

<span data-ttu-id="0295c-127">يوضح الرسم التوضيحي التالي تنسيق التقارير الإلكترونية (ER).</span><span class="sxs-lookup"><span data-stu-id="0295c-127">The following illustration shows an Electronic reporting (ER) format.</span></span>

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

<span data-ttu-id="0295c-128">يبين الرسم التوضيحي التالي مصادر البيانات التي يتم استخدامها للتنسيق.</span><span class="sxs-lookup"><span data-stu-id="0295c-128">The following illustration shows the data sources that are used for the format.</span></span>

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

<span data-ttu-id="0295c-129">يعرض الرسم التوضيحي التالي النتيجة عند تشغيل التنسيق.</span><span class="sxs-lookup"><span data-stu-id="0295c-129">The following illustration shows the result when the format is run.</span></span> <span data-ttu-id="0295c-130">في هذه الحالة، الإخراج عبارة عن قائمة مسطحة بأصناف السلع.</span><span class="sxs-lookup"><span data-stu-id="0295c-130">In this case, the output is a flat list of commodity items.</span></span>

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

<span data-ttu-id="0295c-131">في الرسوم التوضيحية التالية، تم تعديل التنسيق نفسه بحيث يقدم قائمة أصناف السلع في دُفعات إذا كانت الدفعة الواحدة يجب أن تتضمن سلعًا ويجب ألا يتجاوز الوزن الإجمالي الحد 9.</span><span class="sxs-lookup"><span data-stu-id="0295c-131">In the following illustrations, the same format has been adjusted so that it presents the list of commodity items in batches if a single batch must include commodities and the total weight should not exceed a limit of 9.</span></span>

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

<span data-ttu-id="0295c-132">يعرض الرسم التوضيحي التالي النتيجة عند تشغيل التنسيق المعدَّل.</span><span class="sxs-lookup"><span data-stu-id="0295c-132">The following illustration shows the result when the adjusted format is run.</span></span>

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> <span data-ttu-id="0295c-133">لا يتم تطبيق الحد على الصنف الأخير من القائمة الأصلية لأن القيمة (**11**) لمصدر الحد (**الوزن**) تتجاوز الحد المُعرف (**9**).</span><span class="sxs-lookup"><span data-stu-id="0295c-133">The limit isn't applied to the last item of the original list, because the value (**11**) of the limit source (**weight**) exceeds the defined limit (**9**).</span></span> <span data-ttu-id="0295c-134">لتجاهل القوائم الفرعية خلال إنشاء التقرير، استخدم إما وظيفة `WHERE` أو تعبير **مُمكّن** لعنصر التنسيق المناظر، عند الحاجة.</span><span class="sxs-lookup"><span data-stu-id="0295c-134">To ignore sublists during report generation, use either the `WHERE` function or the **Enabled** expression of the corresponding format element, as you require.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0295c-135">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="0295c-135">Additional resources</span></span>

[<span data-ttu-id="0295c-136">دالات القائمة</span><span class="sxs-lookup"><span data-stu-id="0295c-136">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]