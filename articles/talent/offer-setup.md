---
title: إعداد إدارة العروض في Attract
description: يصف هذا الموضوع كيفية إعداد العروض في Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bc91a83afd5ce1627376685bcf612d6998ddbc02
ms.sourcegitcommit: 5022d63a81c3715c9a3dcf2a68217bb6b17c7805
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2019
ms.locfileid: "2890545"
---
# <a name="set-up-offer-management-in-attract"></a><span data-ttu-id="84613-103">إعداد إدارة العروض في Attract</span><span class="sxs-lookup"><span data-stu-id="84613-103">Set up offer management in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="84613-104">عند نقل أحد المرشحين إلى مرحلة العرض في Dynamics 365 Talent: Attract، يجب أن تتأكد من إمكانية إنشاء العروض بسرعة لهذا المرشح، والموافقة عليها كما تقتضي الحاجة، ثم إرسالها إلى المرشح.</span><span class="sxs-lookup"><span data-stu-id="84613-104">When a candidate is moved to the offer stage in Dynamics 365 Talent: Attract, you need to ensure that the offers can be quickly created for the candidate, approved as necessary, and sent out to the candidate.</span></span> <span data-ttu-id="84613-105">وبما أن معظم العروض تعتبر قياسية، يمكن إنشاؤها من قوالب قابلة لإعادة الاستخدام.</span><span class="sxs-lookup"><span data-stu-id="84613-105">Because most offers are standard, they can be created from reusable templates.</span></span> <span data-ttu-id="84613-106">في Attract، تكون جميع العروض مجمعة في حزمة عرض، وهي عبارة عن مجموعة تتضمن مستند عرض أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="84613-106">In Attract, all offers are rolled into an offer package, which is a collection of one or more offer documents.</span></span> 

<span data-ttu-id="84613-107">يسرد هذا الموضوع جميع الخطوات التي يجب على مسؤول Attract اتباعها لإعداد قوالب حزم عروض مختلفة كجزء من إمكانية إدارة العروض في Attract.</span><span class="sxs-lookup"><span data-stu-id="84613-107">This topic lists all the steps that an Attract administrator would follow to set up different offer package templates as part of the offer management capability in Attract.</span></span> <span data-ttu-id="84613-108">لن يتمكن المستخدمون الذين لا يؤدون أدوار المسؤول من الوصول إلى هذه الإمكانيات.</span><span class="sxs-lookup"><span data-stu-id="84613-108">Users with non-administrator roles will not have access to these capabilities.</span></span>

>[!NOTE]
> <span data-ttu-id="84613-109">تتوفر إمكانيات إدارة العروض كجزء من المكون الإضافي "التوظيف الشامل".</span><span class="sxs-lookup"><span data-stu-id="84613-109">Offer management capabilities are available as part of the Comprehensive Hiring Add-On.</span></span>

## <a name="offer-data"></a><span data-ttu-id="84613-110">بيانات العرض</span><span class="sxs-lookup"><span data-stu-id="84613-110">Offer data</span></span> 

<span data-ttu-id="84613-111">تعتبر بيانات العرض أصغر وحدة في قالب حزمة العرض.</span><span class="sxs-lookup"><span data-stu-id="84613-111">Offer data is the smallest unit inside the offer package template.</span></span> <span data-ttu-id="84613-112">يتكوّن العرض النموذجي من نص قياسي ومجموعة من القيم.</span><span class="sxs-lookup"><span data-stu-id="84613-112">A typical offer consists of standard text and a set of values.</span></span> <span data-ttu-id="84613-113">وتعتبر مجموعات القيم العناصر الوحيدة التي يمكنها أن تتغير بين العروض.</span><span class="sxs-lookup"><span data-stu-id="84613-113">The sets of values are the only pieces that could change between offers.</span></span> <span data-ttu-id="84613-114">أثناء إنشاء العرض، يعتبر الجانب الأهم الذي يمكن لمنشئ العرض التركيز عليه قائمة العناصر النائبة لبيانات العرض الموجودة في قالب حزمة العرض.</span><span class="sxs-lookup"><span data-stu-id="84613-114">During the offer creation, the most important aspect that the offer creator can focus on is the list of offer data placeholders present in an offer package template.</span></span> <span data-ttu-id="84613-115">لإعداد بيانات العرض، قم بما يلي.</span><span class="sxs-lookup"><span data-stu-id="84613-115">To set up offer data, do the following.</span></span>

1.  <span data-ttu-id="84613-116">انتقل إلى **إدارة العروض**.</span><span class="sxs-lookup"><span data-stu-id="84613-116">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="84613-117">قم بتوسيع قسم **المكتبة** في جزء التنقل الأيمن، ثم انتقل إلى **بيانات العرض**.</span><span class="sxs-lookup"><span data-stu-id="84613-117">Expand the **Library** section in the left navigation pane, then go to **Offer data**.</span></span>

    >[!NOTE]
    > <span data-ttu-id="84613-118">تتضمن صفحة **بيانات العرض** القسمين **تفاصيل المرشح** و**تفاصيل الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="84613-118">On the **Offer data** page are the **Candidate details** and **Job details** sections.</span></span> <span data-ttu-id="84613-119">يوفر Attract بعض العناصر النائبة الجاهزة لبيانات العرض.</span><span class="sxs-lookup"><span data-stu-id="84613-119">Attract provides a few offer data placeholders out-of-the-box.</span></span>
    > 
    > <span data-ttu-id="84613-120">تتضمن الصفحة أقسامًا لتنظيم مختلف العناصر النائبة لبيانات العرض في مجموعات منطقية.</span><span class="sxs-lookup"><span data-stu-id="84613-120">There are sections on the page to organize different offer data placeholders together in logical groups.</span></span> <span data-ttu-id="84613-121">بإمكان هذه الأقسام المساعدة في الحفاظ على بيانات العرض وتعبئة البيانات أثناء عملية إنشاء عرض.</span><span class="sxs-lookup"><span data-stu-id="84613-121">These sections can help with maintenance of offer data and population of data during the offer creation process.</span></span>
    > 
    > <span data-ttu-id="84613-122">لإنشاء قائمة قيم لعنصر نائب، قم بتحميل ورقة عمل Excel تحتوي على عمود واحد بعنوان لعنصر النائب وقائمة الاختيارات في الصفوف المدرجة بأسفل.</span><span class="sxs-lookup"><span data-stu-id="84613-122">To create a list of values for a placeholder, upload an Excel spreadsheet that has one column with the placeholder as the column title and the list of choices in the rows underneath.</span></span> <span data-ttu-id="84613-123">إذا تمت الإشارة إلى العنصر النائب نفسه في مجموعة قاعدة بيانات أخرى، تأكد من أن لديهم مجموعة مشتركة من القيم.</span><span class="sxs-lookup"><span data-stu-id="84613-123">If the same placeholder is referenced in another data rule set, ensure they have a common set of values.</span></span>
    
1.  <span data-ttu-id="84613-124">لإنشاء قسم جديد لبيانات العرض، انقر فوق **إضافة قسم** وأدخل اسمًا فريدًا للقسم.</span><span class="sxs-lookup"><span data-stu-id="84613-124">To create a new offer data section, click **Add a section** and enter a unique name for the section.</span></span>

1.  <span data-ttu-id="84613-125">لإضافة العناصر النائبة لبيانات العرض إلى أي قسم، انقر فوق **إضافة بيانات العرض** وأدخل اسمًا فريدًا للعنصر النائب.</span><span class="sxs-lookup"><span data-stu-id="84613-125">To add offer data placeholders to any section, click **Add offer data** and enter a unique name for the placeholder.</span></span>

1.  <span data-ttu-id="84613-126">لتحرير اسم أي مقطع، يمكنك تمرير الماوس فوق اسم القسم وتحديث الاسم.</span><span class="sxs-lookup"><span data-stu-id="84613-126">To edit the name of any section, hover over the section name and update the name.</span></span>

1.  <span data-ttu-id="84613-127">لتحرير اسم أي عنصر نائب موجود لبيانات العرض، تأكد أولاً من أن العنصر النائب ليس عبارة عن جزء من أي قالب.</span><span class="sxs-lookup"><span data-stu-id="84613-127">To edit the name of any existing offer data placeholder, first make sure that the placeholder is not already part of any template.</span></span> <span data-ttu-id="84613-128">وبعد ذلك، قم بتمرير الماوس فوق اسم العنصر النائب لبيانا العرض، ثم حدّث الاسم حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="84613-128">Then, hover over the name of the offer data placeholder and update the name as needed.</span></span>

1. <span data-ttu-id="84613-129">لحذف عنصر نائب موجود لبيانات العرض، تأكد أولاً من أن العنصر النائب ليس عبارة عن جزء من أي قالب آخر.</span><span class="sxs-lookup"><span data-stu-id="84613-129">To delete an existing offer data placeholder, first make sure that the placeholder is not part of any other template.</span></span> <span data-ttu-id="84613-130">وبعد ذلك، قم بتمرير الماوس فوق العنصر النائب وعند ظهور أيقونة سلة المهملات، انقر فوقها لحذف العنصر النائب لبيانات العرض.</span><span class="sxs-lookup"><span data-stu-id="84613-130">Then, hover over the placeholder and when the trash can icon appears, click the trash can to delete the offer data placeholder.</span></span>
    >[!NOTE]
    > <span data-ttu-id="84613-131">يدل مؤشر الرقم الموجود إلى جانب بيانات كل عرض إلى عدد القوالب التي يعتبر العنصر النائب لبيانات العرض جزءًا منها.</span><span class="sxs-lookup"><span data-stu-id="84613-131">You can see how many templates an offer data placeholder is part of by the number indicator next to each offer data.</span></span> 

1. <span data-ttu-id="84613-132">لحذف أي قسم، قم بتمرير الماوس فوق الاسم.</span><span class="sxs-lookup"><span data-stu-id="84613-132">To delete any section, hover over the name.</span></span> <span data-ttu-id="84613-133">إذا لم يظهر أي واحد من العناصر النائبة لبيانات العرض داخل القسم في أي قالب، يمكنك النقر فوق أيقونة سلة المهملات لحذفه.</span><span class="sxs-lookup"><span data-stu-id="84613-133">If none of the offer data placeholders inside the section appear in any template, you can click the trash can icon to delete it.</span></span> 
    >[!NOTE]
    > <span data-ttu-id="84613-134">سيؤدي حذف المقطع إلى حذف كافة العناصر النائبة لبيانات العرض الموجودة داخله.</span><span class="sxs-lookup"><span data-stu-id="84613-134">Deleting the section will also delete all the offer data placeholders inside that section.</span></span>

<span data-ttu-id="84613-135">بعد إعداد العناصر النائبة لبيانات العرض، يمكنك استخدامها عبر أي قالب المستند.</span><span class="sxs-lookup"><span data-stu-id="84613-135">After the offer data placeholders have been set up, you can use them across any document template.</span></span> <span data-ttu-id="84613-136">لا تقتصر العناصر النائبة لبيانات العرض على قالب معين، إذ يمكن استخدام المجموعة نفسها عبر كافة القوالب.</span><span class="sxs-lookup"><span data-stu-id="84613-136">Offer data placeholders are not restricted to a specific template -- the same set can be used across all templates.</span></span>

## <a name="offer-data-rules"></a><span data-ttu-id="84613-137">قواعد بيانات العرض</span><span class="sxs-lookup"><span data-stu-id="84613-137">Offer data rules</span></span>

<span data-ttu-id="84613-138">وضعت معظم المؤسسات قواعد تتناول كيفية إنشاء العروض.</span><span class="sxs-lookup"><span data-stu-id="84613-138">Most organization have rules for how offers must be created.</span></span> <span data-ttu-id="84613-139">على سبيل المثال، قد تطالب إحدى المؤسسات بأن يكون عرض الراتب السنوي الأقصى لموقع معين ومستوى الرتبة معًا ضمن نطاق معين، أو أن يكون هناك بعض القيم المعينة الممكنة لمستوى العرض المقدم للموظف الجديد.</span><span class="sxs-lookup"><span data-stu-id="84613-139">For example, an organization may want to require that the maximum annual salary offer for a specific location and seniority level combination has to be within a certain range, or that there are only a few specific values possible for the offer level for the new hire.</span></span> <span data-ttu-id="84613-140">يدعم Attract حاليًا جميع قواعد البيانات هذه باستخدام ملف CSV.</span><span class="sxs-lookup"><span data-stu-id="84613-140">Attract currently supports all such data rules using a CSV file.</span></span>

<span data-ttu-id="84613-141">لتحضير ملف CSV لقواعد البيانات، قم بما يلي.</span><span class="sxs-lookup"><span data-stu-id="84613-141">To prepare the data rules CSV file, do the following.</span></span>

1.  <span data-ttu-id="84613-142">حدد العنصر النائب لبيانات العرض لمجموعة القواعد.</span><span class="sxs-lookup"><span data-stu-id="84613-142">Determine the offer data placeholder for the rule set.</span></span> <span data-ttu-id="84613-143">على سبيل المثال، **الراتب السنوية**.</span><span class="sxs-lookup"><span data-stu-id="84613-143">For example, **Annual Salary**.</span></span>

1.  <span data-ttu-id="84613-144">حدد قيم العنصر النائب لبيانات العرض التابعة.</span><span class="sxs-lookup"><span data-stu-id="84613-144">Identify the dependent offer data placeholder values.</span></span> <span data-ttu-id="84613-145">على سبيل المثال، **موقع الوظيفة** و**المستوى**.</span><span class="sxs-lookup"><span data-stu-id="84613-145">For example, **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="84613-146">حدد العمودين 1 و2 على أنهما **موقع الوظيفة** و **المستوى**.</span><span class="sxs-lookup"><span data-stu-id="84613-146">Specify columns 1 and 2 as **Job Location** and **Level**.</span></span>

1.  <span data-ttu-id="84613-147">لتحميل قيمة المجموعة، اجعل العمودين 3 و4 **الراتب السنوي**.</span><span class="sxs-lookup"><span data-stu-id="84613-147">To upload a range value, make columns 3 and 4 **Annual Salary**.</span></span> <span data-ttu-id="84613-148">لتحميل قيمة معينة بدلاً من مجموعة، اجعل العمود 3 **الراتب السنوي**.</span><span class="sxs-lookup"><span data-stu-id="84613-148">To upload a specific value instead of a range, only make column 3 **Annual Salary**.</span></span>

1.  <span data-ttu-id="84613-149">قم بتعبئة ملف Microsoft Excel استنادًا إلى أدوارك المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="84613-149">Populate the Microsoft Excel file based on your required roles.</span></span>

1.  <span data-ttu-id="84613-150">تأكد من أن كل صف عبارة عن تركيبة فريدة من كافة القيم التي تم جمعها معًا.</span><span class="sxs-lookup"><span data-stu-id="84613-150">Ensure that each row is a unique combination of all the values put together.</span></span>

1.  <span data-ttu-id="84613-151">احفظ الملف بتنسيق CSV.</span><span class="sxs-lookup"><span data-stu-id="84613-151">Save the file as a CSV format.</span></span>

<span data-ttu-id="84613-152">لتحميل ملف قواعد بيانات العرض، قم بما يلي.</span><span class="sxs-lookup"><span data-stu-id="84613-152">To upload the offer data rules file, do the following.</span></span>

1.  <span data-ttu-id="84613-153">انتقل إلى **إدارة العروض**.</span><span class="sxs-lookup"><span data-stu-id="84613-153">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="84613-154">قم بتوسيع قسم **المكتبة** في جزء التنقل الأيمن، ثم انتقل إلى **قواعد بيانات العرض**.</span><span class="sxs-lookup"><span data-stu-id="84613-154">Expand the **Library** section in the left navigation panel, then go to **Offer data rules**.</span></span>

1.  <span data-ttu-id="84613-155">انقر فوق **مجموعة بيانات جديدة** لعرض مربع الحوار **تحميل**.</span><span class="sxs-lookup"><span data-stu-id="84613-155">Click **New data set** to display the **Upload** dialog box.</span></span>

1.  <span data-ttu-id="84613-156">حدد اسمًا فريدًا لمجموعة القواعد وقم بتحميل ملف CSV المحفوظ.</span><span class="sxs-lookup"><span data-stu-id="84613-156">Specify a unique name for the rule set and then upload the saved CSV file.</span></span>

1.  <span data-ttu-id="84613-157">النقر فوق **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="84613-157">Click **Add**.</span></span>
    <span data-ttu-id="84613-158">ستتم معالجة مجموعة القواعد في الخلفية وسيتم إعلامك داخل التطبيق وعبر البريد الإلكتروني فور اكتمالها.</span><span class="sxs-lookup"><span data-stu-id="84613-158">The rule set will be processed in the background and you will be notified in-app and via email once it completes.</span></span>

    <span data-ttu-id="84613-159">سيتم إعلامك إن كان هناك أي أخطاء أثناء معالجة التحميل.</span><span class="sxs-lookup"><span data-stu-id="84613-159">You will be notified if there are errors while processing the upload.</span></span> <span data-ttu-id="84613-160">يمكنك عندئذٍ تنزيل سجل الأخطاء وإصلاح الملف وتحميله مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="84613-160">You can then download the error log, fix the file, and upload it again.</span></span>

1.  <span data-ttu-id="84613-161">استخدم زر علامة القطع (**…**) إذا أردت تنزيل مجموعة القواعد وتحديث مجموعة القيم.</span><span class="sxs-lookup"><span data-stu-id="84613-161">Use the ellipses button (**…**) option if you want to download the rule set and update the set of values.</span></span> <span data-ttu-id="84613-162">يمكنك تحميل الملف مرة أخرى بعد التحديث.</span><span class="sxs-lookup"><span data-stu-id="84613-162">After updating, you can upload the file again.</span></span>

1.  <span data-ttu-id="84613-163">يمكنك حذف مجموعة قواعد موجودة تم تحميله في حالة عدم استخدام العنصر النائب الذي تم تعريفه في قالب مستند آخر.</span><span class="sxs-lookup"><span data-stu-id="84613-163">You can delete an existing rule set upload if the placeholder being defined is not being used in another document template.</span></span>

>[!NOTE]
> - <span data-ttu-id="84613-164">يتضمن كل عنصر نائب مجموعة فريدة من الأعمدة التي يعتمد عليها.</span><span class="sxs-lookup"><span data-stu-id="84613-164">Each placeholder can only have one unique set of columns that it is dependent on.</span></span> <span data-ttu-id="84613-165">على سبيل المثال، إذا كان **الراتب السنوي** يعتمد على **موقع الوظيفة** و**المستوى**، فلا يمكنك تحميل مجموعة قواعد أخرى حيث يعتمد **الراتب السنوي** على مجموعة مختلفة من الأعمدة.</span><span class="sxs-lookup"><span data-stu-id="84613-165">For example, if **Annual Salary** is dependent on **Job Location** and **Level**, you can't upload another rule set where **Annual Salary** is dependent on a different set of columns.</span></span>

> - <span data-ttu-id="84613-166">يمكنك تنزيل مجموعات قواعد بيانات العرض على علامة تبويب **النماذج‬** في صفحة **قواعد بيانات العرض**.</span><span class="sxs-lookup"><span data-stu-id="84613-166">You can download sample offer data rule sets on the **Samples** tab on the **Offer data rules** page.</span></span>

> - <span data-ttu-id="84613-167">عندما يقوم منشئ العرض بإبطال القيم التي توصي بها قواعد بيانات العرض، توضع علامة على العرض على أنه غير قياسي وسيتم تعيين سير عمل الموافقة على العرض.</span><span class="sxs-lookup"><span data-stu-id="84613-167">When an offer creator overrides the values that are recommended by the offer data rules, the offer is flagged as non-standard and offer approval workflow will be mandated.</span></span>

## <a name="document-templates"></a><span data-ttu-id="84613-168">قوالب المستندات</span><span class="sxs-lookup"><span data-stu-id="84613-168">Document templates</span></span>

<span data-ttu-id="84613-169">بإمكان قالب مستند العرض مساعدة المسؤولين على إنشاء رسائل العرض.</span><span class="sxs-lookup"><span data-stu-id="84613-169">An offer document template can help administrators create offer letters.</span></span> <span data-ttu-id="84613-170">يعتبر قالب مستند العرض خليطًا من النص الذي سيشكل جزءًا من العرض بالإضافة إلى العناصر النائبة لبيانات العرض المعرّفة.</span><span class="sxs-lookup"><span data-stu-id="84613-170">The offer document template is a combination of the text that will be part of the offer as well as the defined offer data placeholders.</span></span> 

<span data-ttu-id="84613-171">لإنشاء قالب مستند العرض، قم بما يلي.</span><span class="sxs-lookup"><span data-stu-id="84613-171">To create an offer document template, do the following.</span></span>

1.  <span data-ttu-id="84613-172">انتقل إلى **إدارة العروض**.</span><span class="sxs-lookup"><span data-stu-id="84613-172">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="84613-173">قم بتوسيع قسم **المكتبة** في جزء التنقل الأيمن، ثم انتقل إلى **القوالب**.</span><span class="sxs-lookup"><span data-stu-id="84613-173">Expand the **Library** section in the left navigation pane and go to **Templates**.</span></span>

    <span data-ttu-id="84613-174">تعرض صفحة **القوالب** قائمة بقوالب المستندات التي تم تعريفها.</span><span class="sxs-lookup"><span data-stu-id="84613-174">The **Templates** page will display a list of document templates that have already been defined.</span></span>

1.  <span data-ttu-id="84613-175">لإنشاء قالب مستند جديد، انقر فوق **قالب جديد**.</span><span class="sxs-lookup"><span data-stu-id="84613-175">To create a new document template, click **New Template**.</span></span>

1.  <span data-ttu-id="84613-176">أدخل اسمًا فريدًا للقالب، وانقر فوق **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="84613-176">Enter a unique name for the template and click **Create**.</span></span>

1.  <span data-ttu-id="84613-177">استخدم محرر النص المنسق لإدراج محتوى مستند العرض أو تحريره.</span><span class="sxs-lookup"><span data-stu-id="84613-177">Use the rich text editor to insert or edit the offer document content.</span></span> <span data-ttu-id="84613-178">يمكنك إدراج جداول وصور وارتباطات تشعبية باستخدام الخيارات المتوفرة في الجزء العلوي من محرر النص.</span><span class="sxs-lookup"><span data-stu-id="84613-178">You can insert tables, images, and hyperlinks using the options available at the top of the text editor.</span></span>

1.  <span data-ttu-id="84613-179">يمكنك إدراج العناصر النائبة لبيانات العرض في مستند القالب من خلال:</span><span class="sxs-lookup"><span data-stu-id="84613-179">You can insert offer data placeholders in the offer template document by:</span></span>

    - <span data-ttu-id="84613-180">السحب والإفلات من الجزء الأيسر.</span><span class="sxs-lookup"><span data-stu-id="84613-180">Dragging and dropping from the right pane.</span></span>

    - <span data-ttu-id="84613-181">وضع علامة كلمة رئيسية على العنصر النائب لبيانات العرض مباشرةً في الموضع.</span><span class="sxs-lookup"><span data-stu-id="84613-181">Hashtag the offer data placeholder directly into position.</span></span> <span data-ttu-id="84613-182">كتابة **\#** ثم بدء كتابة اسم العنصر النائب لبيانات العرض.</span><span class="sxs-lookup"><span data-stu-id="84613-182">Type **\#** and then start typing the name of the offer data placeholder.</span></span> <span data-ttu-id="84613-183">ستظهر الخيارات في القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="84613-183">Options will appear in the drop-down list.</span></span> <span data-ttu-id="84613-184">انقر أو اضغط على **Enter‎** لإدراج العنصر النائب لبيانات العرض.</span><span class="sxs-lookup"><span data-stu-id="84613-184">Click or press **Enter** to insert the offer data placeholder.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="84613-185">لربط عنصر نائب بقالب مستند العرض من دون عرض قيمته للمرشح، قم بتمرير الماوس فوق العنصر النائب لبيانات العرض وانقر فوق الأيقونة **تثبيت**.</span><span class="sxs-lookup"><span data-stu-id="84613-185">To associate a placeholder to the offer document template without exposing its value to the candidate, hover over the offer data placeholder and click the **Pin** icon.</span></span> <span data-ttu-id="84613-186">سيؤدي ذلك إلى دفع العنصر النائب إلى قسم **بيانات العرض المثبتة** في قالب مستند العرض.</span><span class="sxs-lookup"><span data-stu-id="84613-186">This will push the placeholder to the **Pinned offer data** section of the offer document template.</span></span> <span data-ttu-id="84613-187">لإزالة التثبيت، اتبع نفس الخطوات ولكن انقر فوق **إزالة تثبيت** في قائمة العناصر النائبة لبيانات العرض.</span><span class="sxs-lookup"><span data-stu-id="84613-187">To unpin, follow the same steps but click **Unpin** in the list of offer data placeholders.</span></span>

    > - <span data-ttu-id="84613-188">لعرض قائمة بالعناصر النائبة لبيانات العرض النشطة، قم بالتبديل إلى علامة التبويب **نشطة** في الجزء الأيسر.</span><span class="sxs-lookup"><span data-stu-id="84613-188">To view the list of active offer data placeholders, switch to the **Active** tab in the right pane.</span></span>

    > - <span data-ttu-id="84613-189">إذا أدخلت عنصرًا نائبًا يعتمد على مجموعة قواعد بيانات عرض، فيمكنك رؤية تبعية هذا العنصر النائب لبيانات العرض على قيم أخرى.</span><span class="sxs-lookup"><span data-stu-id="84613-189">If you insert a placeholder that is driven by an offer data rule set, you can see the dependency of that offer data placeholder on other values.</span></span>

    > - <span data-ttu-id="84613-190">أو، يمكنك **استيراد** المحتوى من ملف docx. على جهازك المحلي وتحريره كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="84613-190">Alternatively, you can **Import** the content from a .docx file on your local machine and edit as required.</span></span> <span data-ttu-id="84613-191">وبهذه الطريقة، لا تحتاج إلى كتابة المحتوى الكامل في المحرر.</span><span class="sxs-lookup"><span data-stu-id="84613-191">That way, you don’t have to type in all the content in the editor.</span></span>

1. <span data-ttu-id="84613-192">لمعاينة مستند العرض، استخدم الخيار **معاينة** في أعلى الصفحة.</span><span class="sxs-lookup"><span data-stu-id="84613-192">To preview the offer document, use the **Preview** option at the top of the page.</span></span>

1. <span data-ttu-id="84613-193">للتحكم في قدرة منشئ العرض على تحرير محتوى مستند العرض، استخدم الخيار **إدارة الأذونات** في أعلى الصفحة.</span><span class="sxs-lookup"><span data-stu-id="84613-193">To control whether an offer creator can edit the offer document content, use the **Manage permission** option at the top of the page.</span></span> <span data-ttu-id="84613-194">إذا أردت أن يقوم منشئ العرض بإدراج قيم العناصر النائبة فقط من دون تحرير النص، فيمكنك تعيين قيمة الإذن إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="84613-194">If you want the offer creator to only insert placeholder values and not edit text, set the permission value to **No**.</span></span>

1. <span data-ttu-id="84613-195">انقر فوق **حفظ** لحفظ التقدم الذي حققته.</span><span class="sxs-lookup"><span data-stu-id="84613-195">Click **Save** to save your progress.</span></span> <span data-ttu-id="84613-196">سيتم حفظ القالب في حالة المسودة.</span><span class="sxs-lookup"><span data-stu-id="84613-196">The template will be saved in a draft state.</span></span>

1. <span data-ttu-id="84613-197">لإنجاز العملية ووضع علامة على المستند كمنشور، انقر فوق **إنهاء**.</span><span class="sxs-lookup"><span data-stu-id="84613-197">To finalize and mark the document as published, click **Finish**.</span></span>

1. <span data-ttu-id="84613-198">يمكنك الاطلاع على قوالب المستندات النشطة حاليًا، في وضع المسودة، والتي تمت أرشفتها ولم تعد قيد الاستخدام في تجربة الوصول إلى مكتبة قوالب المستندات.</span><span class="sxs-lookup"><span data-stu-id="84613-198">You can see which document templates are currently active, in draft mode, and have been archived and are no longer in use on the document templates library landing experience.</span></span>

>[!NOTE]
> <span data-ttu-id="84613-199">يمكنك حذف أي قالب مستند عرض ليس جزءًا من قالب حزمة عرض موجود.</span><span class="sxs-lookup"><span data-stu-id="84613-199">You can delete any offer document template that is not part of an existing offer package template.</span></span>


## <a name="offer-package-templates"></a><span data-ttu-id="84613-200">قوالب حزم العروض</span><span class="sxs-lookup"><span data-stu-id="84613-200">Offer package templates</span></span>

<span data-ttu-id="84613-201">حزم العروض هي النتائج الملموسة للعرض التي تتم مشاركتها وتتكون من تركيبة تضم قالب مستند عرض أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="84613-201">Offer packages are the offer artifacts that are shared with the candidate and consist of a combination of one or more offer document templates.</span></span> <span data-ttu-id="84613-202">لإنشاء حزمة العرض، قم بما يلي.</span><span class="sxs-lookup"><span data-stu-id="84613-202">To create an offer package, do the following.</span></span>

1.  <span data-ttu-id="84613-203">انتقل إلى **إدارة العروض**.</span><span class="sxs-lookup"><span data-stu-id="84613-203">Go to **Offer management**.</span></span>

1.  <span data-ttu-id="84613-204">انتقل إلى **الحزم** من جزء التنقل الأيمن.</span><span class="sxs-lookup"><span data-stu-id="84613-204">Go to **Packages** from the left navigation pane.</span></span>

    <span data-ttu-id="84613-205">تظهر قائمة بقوالب الحزم النشطة المتوفرة لمنشئي العروض.</span><span class="sxs-lookup"><span data-stu-id="84613-205">A list of active package templates that are available for offer creators to use is displayed.</span></span>

1.  <span data-ttu-id="84613-206">لإنشاء حزمة عرض جديدة، انقر فوق **حزمة جديدة**.</span><span class="sxs-lookup"><span data-stu-id="84613-206">To create a new offer package, click **New Package**.</span></span>

1.  <span data-ttu-id="84613-207">أدخل اسمًا فريدًا، وانقر فوق **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="84613-207">Enter a unique name and click **Create**.</span></span>

1.  <span data-ttu-id="84613-208">انقر فوق **إضافة قالب**.</span><span class="sxs-lookup"><span data-stu-id="84613-208">Click **Add template**.</span></span>

    >[!NOTE]
    > - <span data-ttu-id="84613-209">يمكن أن تختار إنشاء قالب جديد أو الاختيار من ضمن قالب موجود.</span><span class="sxs-lookup"><span data-stu-id="84613-209">You can choose to create a new template or choose from an existing one.</span></span>

    > - <span data-ttu-id="84613-210">إذا اخترت الإضافة إلى قالب موجود، فيجب أن تتأكد من حفظ قالب مستند العرض وإنجازه ووضع علامة نشط عليه.</span><span class="sxs-lookup"><span data-stu-id="84613-210">If you choose to add an existing template, you need to make sure that the   offer document template was saved, finalized, and marked as   active.</span></span>
    
    > - <span data-ttu-id="84613-211">يمكنك اختيار العدد الذي تريده من قوالب المستندات.</span><span class="sxs-lookup"><span data-stu-id="84613-211">You can choose as many document templates as you want.</span></span> 
    
1.  <span data-ttu-id="84613-212">انقر فوق **تم** للعودة إلى **إدارة الحزم**.</span><span class="sxs-lookup"><span data-stu-id="84613-212">Click **Done** to return to **Package management**.</span></span>

    <span data-ttu-id="84613-213">يمكنك تكوين تسلسل للمستندات وأيضًا تحديد ما إذا كان مستند العرض المعين مطلوبًا اثناء إنشاء العرض.</span><span class="sxs-lookup"><span data-stu-id="84613-213">You can configure the sequence of the documents and also mark whether the specific offer document is required during offer creation.</span></span> <span data-ttu-id="84613-214">سيتوفر لمنشئ العرض خيار حذف المستندات التي تم وضع علامة **غير مطلوب** عليها.</span><span class="sxs-lookup"><span data-stu-id="84613-214">The offer creator will have an option to delete the documents marked as **Not required**.</span></span>

1. <span data-ttu-id="84613-215">لحفظ قالب حزمة العرض لكي يتمكن جميع منشئي العروض من استخدامها، انقر قوق **حفظ ونشر**.</span><span class="sxs-lookup"><span data-stu-id="84613-215">To save the offer package template so that it's usable by all offer creators, click **Save and publish**.</span></span>

   <span data-ttu-id="84613-216">لعرض قوالب حزم العرض في حالة المسودة، انتقل إلى علامة التبويب **مسودات**. إذا تم إجراء تغيير على قالب حزمة العرض، فيجب حفظها وإعادة نشرها.</span><span class="sxs-lookup"><span data-stu-id="84613-216">To view draft offer package templates, go to the **Drafts** tab. If a change is made to the offer package template, it must be  saved and republished.</span></span>

## <a name="configure-an-offer-process"></a><span data-ttu-id="84613-217">تكوين عملية عرض</span><span class="sxs-lookup"><span data-stu-id="84613-217">Configure an offer process</span></span>

<span data-ttu-id="84613-218">تتكون عملية إنشاء العرض من عدة أجزاء يمكن تكوينها بواسطة مسؤول Attract.</span><span class="sxs-lookup"><span data-stu-id="84613-218">There are several parts of the offer creation process that can be configured by an Attract administrator.</span></span>

- <span data-ttu-id="84613-219">**الموافقات على العرض** - تحديد ما إذا كان الموافقات على العرض مطلوبة قبل إرسال العرض إلى المرشح.</span><span class="sxs-lookup"><span data-stu-id="84613-219">**Offer approvals** - Choose whether offer approvals are required before the offer can be sent to the candidate.</span></span> <span data-ttu-id="84613-220">كونك المسؤول، يمكنك أيضًا أن تقرر ما إذا كانت جميع الموافقات على العرض ستحدث بطريقة تسلسلية أو كسير عمل موافقة متوازٍ.</span><span class="sxs-lookup"><span data-stu-id="84613-220">As an administrator, you can also decide whether all offer approvals will happen in a sequential manner or parallel approval workflow.</span></span> <span data-ttu-id="84613-221">يمكن أيضًا تعيين ما إذا كان يجب على الموافقين على العرض إضافة تعليق إلى جانب موافقتهم على العرض.</span><span class="sxs-lookup"><span data-stu-id="84613-221">You can also mandate whether offer approvers must add a comment along with their offer approval.</span></span> <span data-ttu-id="84613-222">تعتبر الموافقات على العروض إلزامية لكافة العروض غير القياسية.</span><span class="sxs-lookup"><span data-stu-id="84613-222">Offer approvals are mandatory for all non-standard offers.</span></span>

- <span data-ttu-id="84613-223">**تجربة العرض لدى المرشح** - كونك المسؤول، يمكنك أن تختار تعيين ما إذا كانت كافة العروض لها تاريخ انتهاء صلاحية، وفي هذه الحالة، تعيين المقابل الافتراضي لتاريخ انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="84613-223">**Candidate’s offer experience** - As administrator, you can choose to set whether all offers have an expiration date, and if so, what the default offset for the expiration date should be.</span></span> <span data-ttu-id="84613-224">يمكنك أيضًا تكوين ما إذا كان باستطاعة المرشحين رفض عرض ما.</span><span class="sxs-lookup"><span data-stu-id="84613-224">You can also configure whether candidates can decline an offer.</span></span>

- <span data-ttu-id="84613-225">**التواقيع الإلكترونية** - كمسؤول، يمكنك أيضًا اختيار الطريقة التي يستطيع المرشحون استخدامها للتوقيع.</span><span class="sxs-lookup"><span data-stu-id="84613-225">**e-Signatures** - As an administrator, you can also choose the method that candidates can use to sign offers.</span></span>
    - <span data-ttu-id="84613-226">Adobe Sign - سيتم إرسال وتوقيع جميع حزم العروض عبر Adobe Sign.</span><span class="sxs-lookup"><span data-stu-id="84613-226">Adobe Sign - All offer packages will be sent and signed via Adobe Sign.</span></span> <span data-ttu-id="84613-227">يحتاج جميع منشئي العروض الذين ينشرون العروض إلى توصيل حساب Adobe Sign بـ Attract.</span><span class="sxs-lookup"><span data-stu-id="84613-227">Each offer creator publishing the offer needs to have their Adobe Sign account connected to Attract.</span></span> <span data-ttu-id="84613-228">للحصول على تراخيص Adobe Sign وإصدار تجريبي منه، يُرجى زيارة هذا [الارتباط](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span><span class="sxs-lookup"><span data-stu-id="84613-228">For Adobe Sign licenses and a free Trial, please visit this [link](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).</span></span>

    - <span data-ttu-id="84613-229">DocuSign - سيتم إرسال وتوقيع جميع حزم العروض عبر DocuSign.</span><span class="sxs-lookup"><span data-stu-id="84613-229">DocuSign - All offer packages will be sent and signed via DocuSign.</span></span> <span data-ttu-id="84613-230">يحتاج جميع منشئي العروض الذين ينشرون العروض إلى توصيل حساب DocuSign بـ Attract.</span><span class="sxs-lookup"><span data-stu-id="84613-230">Each offer creator publishing the offer needs to have their DocuSign account connected to Attract.</span></span> 
    
    - <span data-ttu-id="84613-231">ESign - هذا هو الخيار الافتراضي، وهو جاهز للعمل، حيث يستطيع المستخدم التوقيع على العرض عن طريق كتابة اسمه والأحرف الأولى من اسمه.</span><span class="sxs-lookup"><span data-stu-id="84613-231">ESign - This is the default option, provided out of the box, where the user can sign an offer by typing their name and initials.</span></span>


<span data-ttu-id="84613-232">لمزيد من المعلومات حول عملية إنشاء العرض، راجع [إنشاء العروض والموافقة والتوقيع عليها](./creating-offers.md).</span><span class="sxs-lookup"><span data-stu-id="84613-232">To learn more about the offer creation process, see [Create, approve, and sign offers](./creating-offers.md).</span></span>
