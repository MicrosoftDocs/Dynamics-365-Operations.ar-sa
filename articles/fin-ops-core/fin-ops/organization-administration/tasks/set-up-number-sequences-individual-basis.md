---
title: إعداد التسلسلات الرقمية على أساس فردي
description: يشرح هذا الموضوع كيفية إعداد التسلسلات الرقمية على أساس فردي.
author: sericks007
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceDetails
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db662eb407fbcf3587f3fcb03347a3f14e83b879
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140482"
---
# <a name="set-up-number-sequences-on-an-individual-basis"></a><span data-ttu-id="08f12-103">إعداد التسلسلات الرقمية على أساس فردي</span><span class="sxs-lookup"><span data-stu-id="08f12-103">Set up number sequences on an individual basis</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="08f12-104">يشرح هذا الموضوع كيفية إعداد التسلسلات الرقمية على أساس فردي.</span><span class="sxs-lookup"><span data-stu-id="08f12-104">This topic explains how to set up number sequences on an individual basis.</span></span> <span data-ttu-id="08f12-105">تُستخدم التسلسلات الرقمية لإنشاء معرفات فريدة قابلة للقراءة لسجلات البيانات الرئيسية وسجلات الحركات التي تتطلب وجودها.</span><span class="sxs-lookup"><span data-stu-id="08f12-105">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="08f12-106">ويشار إلى البيانات الرئيسية أو سجل الحركة الذي يتطلب معرفًا بمرجع.</span><span class="sxs-lookup"><span data-stu-id="08f12-106">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="08f12-107">قبل إنشاء سجلات جديدة لأحد المراجع، يجب أن تقوم بإعداد تسلسل رقمي وإقرانه بالمرجع.</span><span class="sxs-lookup"><span data-stu-id="08f12-107">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="08f12-108">يمكنك إعداد كافة التسلسلات الرقمية المطلوبة في نفس الوقت باستخدام المعالج **تعيين التسلسلات الرقمية‬**، أو يمكنك إنشاء تسلسلات رقمية فردية أو تعديلها باستخدام الصفحة **التسلسلات الرقمية‬**.</span><span class="sxs-lookup"><span data-stu-id="08f12-108">You can set up all required number sequences at the same time by using the **Set up number sequences** wizard, or you can create or modify individual number sequences by using the **Number sequences** page.</span></span>

1. <span data-ttu-id="08f12-109">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المؤسسة > التسلسلات الرقمية > التسلسلات الرقمية**.</span><span class="sxs-lookup"><span data-stu-id="08f12-109">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="08f12-110">حدد **التسلسل الرقمي**.</span><span class="sxs-lookup"><span data-stu-id="08f12-110">Select **Number sequence**.</span></span>
3. <span data-ttu-id="08f12-111">في الحقل **كود التسلسل الرقمي‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="08f12-111">In the **Number sequence code** field, type a value.</span></span>
4. <span data-ttu-id="08f12-112">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="08f12-112">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="08f12-113">من علامة التبويب السريعة **محددات النطاق**، حدد نطاقًا للتسلسل الرقمي، ثم حدد قيم النطاق من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="08f12-113">On the **Scope parameters** FastTab, select a scope for the number sequence and select scope values from the drop-down list.</span></span> <span data-ttu-id="08f12-114">يحدد النطاق أي من المؤسسات تستخدم التسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="08f12-114">The scope defines which organizations use the number sequence.</span></span> <span data-ttu-id="08f12-115">علاوةً على ذلك، بإمكان التسلسلات الرقمية التي لديها نطاق آخر غير **المشترك** أن تتضمن شرائح تتوافق مع نطاقها.</span><span class="sxs-lookup"><span data-stu-id="08f12-115">In addition, number sequences that have a scope other than **Shared** can have segments that correspond to their scope.</span></span> <span data-ttu-id="08f12-116">فعلى سبيل المثال، بإمكان تسلسل أرقام لديه النطاق **كيان قانوني** أن يتضمن شريحة تسلسل رقمي.</span><span class="sxs-lookup"><span data-stu-id="08f12-116">For example, a number sequence with a scope of **Legal entity** can have a legal entity segment.</span></span> <span data-ttu-id="08f12-117">لمزيد من المعلومات حول النطاقات، راجع [نظرة عامة على التسلسلات الرقمية](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview).</span><span class="sxs-lookup"><span data-stu-id="08f12-117">For more information about scopes, see [Number sequence overview](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview).</span></span> 
6. <span data-ttu-id="08f12-118">وسّع قسم **الشرائح**.</span><span class="sxs-lookup"><span data-stu-id="08f12-118">Expand the **Segments** section.</span></span>
    - <span data-ttu-id="08f12-119">حدد تنسيق التسلسل الرقمي عن طريق إضافة شرائح أو إزالتها أو إعادة ترتيبها.</span><span class="sxs-lookup"><span data-stu-id="08f12-119">Define the format for the number sequence by adding, removing, and rearranging segments.</span></span>  
    - <span data-ttu-id="08f12-120">بإمكان التسلسلات الرقمية لجميع النطاقات أن تحتوي على *شرائح ثابتة* و*شرائح أبجدية رقمية*.</span><span class="sxs-lookup"><span data-stu-id="08f12-120">Number sequences of all scopes can contain *Constant segments* and *Alphanumeric segments*.</span></span> <span data-ttu-id="08f12-121">تحتوي المقاطع الثابتة على مجموعة من الأحرف الأبجدية الرقمية التي لا تتغير.</span><span class="sxs-lookup"><span data-stu-id="08f12-121">Constant segments contain a set of alphanumeric characters that do not change.</span></span> <span data-ttu-id="08f12-122">استخدم هذا النوع من المقاطع لإضافة واصلة أو فواصل أخرى بين شرائح تسلسل الرقم.</span><span class="sxs-lookup"><span data-stu-id="08f12-122">Use this segment type to add a hyphen or other separators between number sequence segments.</span></span> <span data-ttu-id="08f12-123">تحتوي المقاطع الأبجدية الرقمية على مجموعة من علامات الأرقام (#) وعلامات العطف (&).</span><span class="sxs-lookup"><span data-stu-id="08f12-123">Alphanumeric segments contain a combination of number signs (#) and ampersands (&).</span></span> <span data-ttu-id="08f12-124">تمثل هذه الأحرف الحروف والأرقام التي تزداد كل مرة يُستخدم فيها رقم من التسلسل.</span><span class="sxs-lookup"><span data-stu-id="08f12-124">These characters represent letters and numbers that increment every time that a number from the sequence is used.</span></span> <span data-ttu-id="08f12-125">استخدم علامة الرقم (#) للإشارة إلى زيادة الأرقام وعلامة العطف (&) للإشارة إلى زيادة الحروف.</span><span class="sxs-lookup"><span data-stu-id="08f12-125">Use a number sign (#) to indicate incrementing numbers and an ampersand (&) to indicate incrementing letters.</span></span> <span data-ttu-id="08f12-126">على سبيل المثال، ينشئ التنسيق `#####_2014` التسلسل `00001_2014` و`00002_2014` وغير ذلك.</span><span class="sxs-lookup"><span data-stu-id="08f12-126">For example, the format `#####_2014` creates the sequence `00001_2014`, `00002_2014`, and so on.</span></span> <span data-ttu-id="08f12-127">يجب وجود شريحة هجائية رقمية واحدة على الأقل.</span><span class="sxs-lookup"><span data-stu-id="08f12-127">At least one alphanumeric segment must be present.</span></span> <span data-ttu-id="08f12-128">شرائح النطاق، مثل الشركة أو الكيان القانوني، غير مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="08f12-128">Scope segments, such as company or legal entity, are not required.</span></span> <span data-ttu-id="08f12-129">إلا أنه إذا لم تكن شرائح النطاق متضمنة في التنسيق، يستمر إنشاء الأرقام للمرجع المحدد في كل نطاق.</span><span class="sxs-lookup"><span data-stu-id="08f12-129">However, if you do not include scope segments in the format, numbers for the selected reference are still generated per scope.</span></span>  
7. <span data-ttu-id="08f12-130">قم بتوسيع القسم **المراجع**.</span><span class="sxs-lookup"><span data-stu-id="08f12-130">Expand the **References** section.</span></span> <span data-ttu-id="08f12-131">حدد نوع المستند أو السجل لتعيين هذا التسلسل الرقمي إليه.</span><span class="sxs-lookup"><span data-stu-id="08f12-131">Select the document type or record to assign this number sequence to.</span></span> <span data-ttu-id="08f12-132">هذه الخطوة اختيارية بالنسبة للتسلسلات المحددة لأنماط استخدام التطبيق الخاصة.</span><span class="sxs-lookup"><span data-stu-id="08f12-132">This step is optional for sequences that are defined for special application usage patterns.</span></span> <span data-ttu-id="08f12-133">في هذه السيناريوهات، يتم إنشاء رقم جديد باستخدام قيمة كود تسلسل رقمي أو معرف بدون استخدام مرجع.</span><span class="sxs-lookup"><span data-stu-id="08f12-133">In these scenarios, a new number is generated by using the value of a number sequence code or ID, without using a reference.</span></span> <span data-ttu-id="08f12-134">ومن أمثلة نمط استخدام التطبيق الخاص مسلسل الإيصال المستخدم لأسماء دفتر اليومية الخاصة.</span><span class="sxs-lookup"><span data-stu-id="08f12-134">An example of a special application usage pattern is a voucher series that is used for specific journal names.</span></span> <span data-ttu-id="08f12-135">إلا أننا لا نوصي باستخدام مثل هذه الأنماط.</span><span class="sxs-lookup"><span data-stu-id="08f12-135">However, we do not recommend that you use such patterns.</span></span>  
8. <span data-ttu-id="08f12-136">قم بتوسيع القسم **عام**.</span><span class="sxs-lookup"><span data-stu-id="08f12-136">Expand the **General** section.</span></span> <span data-ttu-id="08f12-137">من علامة التبويب السريعة "عام"، حدد ما إذا كان التسلسل الرقمي يدويًا أم مستمرًا أم غير مستمر.</span><span class="sxs-lookup"><span data-stu-id="08f12-137">On the General FastTab, specify whether the number sequence is manual, and continuous or non-continuous.</span></span> <span data-ttu-id="08f12-138">بالإضافة إلى ذلك، أدخل أدنى أرقام وأعلاها التي يمكن استخدامها في التسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="08f12-138">In addition, enter the lowest and highest numbers that can be used in the number sequence.</span></span> <span data-ttu-id="08f12-139">ولا نوصي بتغيير تسلسل رقمي غير مستمر إلى تسلسل رقمي مستمر.</span><span class="sxs-lookup"><span data-stu-id="08f12-139">We do not recommend changing a non-continuous number sequence to a continuous number sequence.</span></span> <span data-ttu-id="08f12-140">نظرًا لأن التسلسل الرقمي لا يكون مستمرًا فعلاً.</span><span class="sxs-lookup"><span data-stu-id="08f12-140">The number sequence will not be truly continuous.</span></span> <span data-ttu-id="08f12-141">كما أن هذا التغيير قد يسبب في اختراقات المفاتيح المكررة في قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="08f12-141">This change may also cause duplicate key violations in the database.</span></span> <span data-ttu-id="08f12-142">بالإضافة إلى أن التسلسلات الرقمية المستمرة لها تأثير أكبر على الأداء.</span><span class="sxs-lookup"><span data-stu-id="08f12-142">In addition, continuous number sequences have a larger effect on performance.</span></span>   
9. <span data-ttu-id="08f12-143">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="08f12-143">Click **Save**.</span></span>
