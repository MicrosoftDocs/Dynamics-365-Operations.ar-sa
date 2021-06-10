---
title: تغيير عملة المحاسبة أو التقارير
description: يشرح هذا الموضوع كيفية تغيير عملة المحاسبة أو التقارير، أو إضافة عملة التقارير إلى إعداد دفتر الأستاذ.
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0435deb009173684c7faaf5340e8095c019ec71c
ms.sourcegitcommit: 2cd82983357b32f70f4e4a0c15d4d1f69e08bd54
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/20/2021
ms.locfileid: "6085464"
---
# <a name="change-the-accounting-or-reporting-currency"></a><span data-ttu-id="3f022-103">تغيير عملة المحاسبة أو التقارير</span><span class="sxs-lookup"><span data-stu-id="3f022-103">Change the accounting or reporting currency</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f022-104">يشرح هذا الموضوع كيفية تغيير عملة المحاسبة أو التقارير، أو إضافة عملة التقارير إلى إعداد دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="3f022-104">This topic explains how to change the accounting or reporting currency, or add a reporting currency to the setup of a ledger.</span></span>

## <a name="symptom"></a><span data-ttu-id="3f022-105">العَرَضْ</span><span class="sxs-lookup"><span data-stu-id="3f022-105">Symptom</span></span>

<span data-ttu-id="3f022-106">تريد تغيير عملة المحاسبة أو التقارير، أو إضافة عملة تقارير إلى إعداد دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="3f022-106">You want to change the accounting or reporting currency, or add a reporting currency to the ledger setup.</span></span> <span data-ttu-id="3f022-107">يحدث هذا عادةً في السيناريوهات التالية:</span><span class="sxs-lookup"><span data-stu-id="3f022-107">This typically occurs in the following scenarios:</span></span>

- <span data-ttu-id="3f022-108">تم تحديد العملة الخاطئة للمحاسبة أو التقارير عند إعداد كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="3f022-108">The wrong accounting or reporting currency was specified when a legal entity was set up.</span></span> <span data-ttu-id="3f022-109">أنت الآن تريد تغيير تلك العملة.</span><span class="sxs-lookup"><span data-stu-id="3f022-109">You now want to change that currency.</span></span>
- <span data-ttu-id="3f022-110">تم تحديد عملة التقارير عند إعداد كيان قانوني، لكن المؤسسة تريد الآن إزالة عملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="3f022-110">A reporting currency was specified when a legal entity was set up, but the organization now wants to remove the reporting currency.</span></span>
- <span data-ttu-id="3f022-111">تقوم المؤسسة بالترقية أو الترحيل إلى Microsoft Dynamics 365 Finance، وتريد تغيير عملة المحاسبة أو التقارير.</span><span class="sxs-lookup"><span data-stu-id="3f022-111">The organization is upgrading or migrating to Microsoft Dynamics 365 Finance, and wants to change the accounting or reporting currency.</span></span>

<span data-ttu-id="3f022-112">تريد المؤسسة التي لم تستخدم سابقًا إمكانية العملة المزدوجة أن تبدأ في استخدامها.</span><span class="sxs-lookup"><span data-stu-id="3f022-112">An organization that didn't previously use the Dual currency capability wants to start to use it.</span></span> <span data-ttu-id="3f022-113">تحدث هذه المشكلة عادةً في السيناريوهات التالية.</span><span class="sxs-lookup"><span data-stu-id="3f022-113">This issue typically occurs in the following scenarios.</span></span>

- <span data-ttu-id="3f022-114">لم يتم تحديد عملة التقارير عند إنشاء كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="3f022-114">No reporting currency was specified when a legal entity was set up.</span></span> <span data-ttu-id="3f022-115">(عملة التقارير اختيارية). أنت تريد الآن إضافة عملة التقارير.</span><span class="sxs-lookup"><span data-stu-id="3f022-115">(A reporting currency is optional.) You now want to add a reporting currency.</span></span>

## <a name="resolution"></a><span data-ttu-id="3f022-116">الحل</span><span class="sxs-lookup"><span data-stu-id="3f022-116">Resolution</span></span>

<span data-ttu-id="3f022-117">يتمثل الاعتبار الأكثر أهميةً في ما إذا كان قد تم ترحيل أي حركات (فعلية أو موازنة) في الكيان القانوني لإعداد دفتر الأستاذ.</span><span class="sxs-lookup"><span data-stu-id="3f022-117">The most important consideration is whether any transactions (actual or budget) have been posted in the legal entity for the ledger setup.</span></span> <span data-ttu-id="3f022-118">**لا يمكنك تغيير عملة المحاسبة أو التقارير، أو إضافة عملة التقارير، إذا تم ترحيل أي حركات (فعلية أو موازنة) في الكيان القانوني.**</span><span class="sxs-lookup"><span data-stu-id="3f022-118">**You can't change the accounting or reporting currency, or add a reporting currency, if any transactions (actual or budget) have been posted in the legal entity.**</span></span> <span data-ttu-id="3f022-119">اتبع الخطوات الواردة في أحد الأقسام التالية، بناءً على ما إذا كان قد تم ترحيل الحركات أو لا.</span><span class="sxs-lookup"><span data-stu-id="3f022-119">Follow the steps in one of the following sections, depending on whether transactions have been posted.</span></span>

### <a name="no-transactions-have-been-posted"></a><span data-ttu-id="3f022-120">لم يتم ترحيل أي حركات</span><span class="sxs-lookup"><span data-stu-id="3f022-120">No transactions have been posted</span></span>

1. <span data-ttu-id="3f022-121">في الكيان القانوني الذي تقوم بتحديث العملات له، انتقل إلى **دفتر الأستاذ العام \> إعداد دفتر الأستاذ \> دفتر الأستاذ**.</span><span class="sxs-lookup"><span data-stu-id="3f022-121">In the legal entity that you're updating currencies for, go to **General ledger \> Ledger setup \> Ledger**.</span></span>
2. <span data-ttu-id="3f022-122">في صفحة **دفتر الأستاذ**، حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="3f022-122">On the **Ledger** page, select **Edit**.</span></span>
3. <span data-ttu-id="3f022-123">في علامة التبويب السريعة **العملة**، حدد عملة المحاسبة وعملة التقارير لاستخدامهما للكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="3f022-123">On the **Currency** FastTab, select the accounting currency and reporting currency to use for the legal entity.</span></span>
4. <span data-ttu-id="3f022-124">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="3f022-124">Select **Save**.</span></span>

<span data-ttu-id="3f022-125">إذا كانت الحقول الخاصة بعملة المحاسبة وعملة التقارير غير متوفرة في صفحة **دفتر الأستاذ**، تم ترحيل حركة واحدة أو أكثر (فعلية أو موازنة) في الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="3f022-125">If the fields for the accounting currency and the reporting currency aren't available on the **Ledger** page, one or more transactions (actual or budget) have been posted in the legal entity.</span></span> <span data-ttu-id="3f022-126">وبالتالي، لا يمكن تغيير العملات.</span><span class="sxs-lookup"><span data-stu-id="3f022-126">Therefore, the currencies can't be changed.</span></span> <span data-ttu-id="3f022-127">في هذه الحالة، اتبع الخطوات الموجودة في القسم التالي.</span><span class="sxs-lookup"><span data-stu-id="3f022-127">In this case, follow the steps in the next section.</span></span>

### <a name="transactions-have-been-posted"></a><span data-ttu-id="3f022-128">تم ترحيل الحركات</span><span class="sxs-lookup"><span data-stu-id="3f022-128">Transactions have been posted</span></span>

<span data-ttu-id="3f022-129">**إذا تم ترحيل الحركات في الكيان القانوني، فإن الطريقة الوحيدة لتغيير أو إضافة عملات المحاسبة والتقارير هي إنشاء كيان قانوني جديد لديه العملات الصحيحة.**</span><span class="sxs-lookup"><span data-stu-id="3f022-129">**If transactions have been posted in the legal entity, the only way to change or add accounting and reporting currencies is to create a new legal entity that has the correct currencies.**</span></span> <span data-ttu-id="3f022-130">للمساعدة في تسهيل هذه العملية، تتيح لك إدارة البيانات في النظام إمكانية نسخ سجلات الإعداد والسجلات الرئيسية من الكيان القانوني الحالي إلى كيان قانوني جديد.</span><span class="sxs-lookup"><span data-stu-id="3f022-130">To help make this process easier, Data management in the system lets you copy setup records and master records from the current legal entity to a new legal entity.</span></span>

<span data-ttu-id="3f022-131">التغييرات في المحاسبة وعملات التقارير منتشرة.</span><span class="sxs-lookup"><span data-stu-id="3f022-131">Changes to the accounting and reporting currencies are pervasive.</span></span> <span data-ttu-id="3f022-132">إنها لا تؤثر على دفتر الأستاذ العام فقط ولكن أيضًا على كل دفتر أستاذ فرعي (الحسابات المدينة، والحسابات الدائنة، والمخزون، والمشروع، وما إلى ذلك)، وكل حلول موردي البرامج المستقلين (ISV)، وأي ملحق وفرته ويخزن المبالغ.</span><span class="sxs-lookup"><span data-stu-id="3f022-132">They affect not only General ledger but also every subledger (Accounts receivable, Accounts payable, Inventory, Project, and so on), every independent software vendor (ISV) solutions, and any extension that you've made that stores amounts.</span></span>

<span data-ttu-id="3f022-133">إن عملية البحث عن وترجمة كل مبلغ إلى عملة مختلفة عرضة للخطأ.</span><span class="sxs-lookup"><span data-stu-id="3f022-133">The process of finding and translating each amount to a different currency is subject to error.</span></span> <span data-ttu-id="3f022-134">ولذلك، لن يوافق الفريق الهندسي على برنامج نصي يغير أو يضيف عملات المحاسبة والتقارير.</span><span class="sxs-lookup"><span data-stu-id="3f022-134">Therefore, the engineering team won't approve a script that changes or adds accounting and reporting currencies.</span></span> <span data-ttu-id="3f022-135">بالإضافة إلى ذلك، على الرغم من أن الأداة التي كانت متاحة في السابق لـ Microsoft Dynamics AX ‏2012 تتيح لك تغيير أو إضافة عملات المحاسبة والتقارير، فقد تم إهمال هذه الأداة لكلٍّ من AX ‏2012 R3 وFinance.</span><span class="sxs-lookup"><span data-stu-id="3f022-135">Additionally, although a tool that used to be available for Microsoft Dynamics AX 2012 let you change or add accounting and reporting currencies, that tool was deprecated for both AX 2012 R3 and Finance.</span></span>

<span data-ttu-id="3f022-136">اتبع هذه الخطوات لنسخ الإعداد والبيانات الرئيسية من الكيان القانوني الحالي إلى كيان قانوني جديد.</span><span class="sxs-lookup"><span data-stu-id="3f022-136">Follow these steps to copy the setup and master data from the current legal entity to a new legal entity.</span></span>

1. <span data-ttu-id="3f022-137">انتقل إلى **مساحات العمل \> إدارة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="3f022-137">Go to **Workspaces \> Data management**.</span></span>
2. <span data-ttu-id="3f022-138">حدد **القوالب** ضمن مجموعة **الاستيراد/التصدير**.</span><span class="sxs-lookup"><span data-stu-id="3f022-138">Select **Templates** under the **Import/Export** group.</span></span>
3. <span data-ttu-id="3f022-139">تأكد من توفر القوالب.</span><span class="sxs-lookup"><span data-stu-id="3f022-139">Make sure that templates are available.</span></span> <span data-ttu-id="3f022-140">إذا لم تتوفر أي قوالب، فحدد **تحميل القوالب الافتراضية**، وانتظر حتى يتم إنشاء القوالب.</span><span class="sxs-lookup"><span data-stu-id="3f022-140">If no templates are available, select **Load default templates**, and wait for the templates to be generated.</span></span>
4. <span data-ttu-id="3f022-141">عُد إلى مساحة عمل **إدارة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="3f022-141">Return to the **Data management** workspace.</span></span>
5. <span data-ttu-id="3f022-142">حدد **نسخ إلى كيان قانوني**.</span><span class="sxs-lookup"><span data-stu-id="3f022-142">Select **Copy into legal entity**.</span></span>
6. <span data-ttu-id="3f022-143">أدخل اسم مجموعة ووصفًا.</span><span class="sxs-lookup"><span data-stu-id="3f022-143">Enter a group name and description.</span></span>
7. <span data-ttu-id="3f022-144">في حقل **الكيان القانوني المصدر**، حدد الكيان القانوني ليتم نسخ البيانات منه.</span><span class="sxs-lookup"><span data-stu-id="3f022-144">In the **Source legal entity** field, select the legal entity to copy data from.</span></span>
8. <span data-ttu-id="3f022-145">في علامة التبويب السريعة **الكيانات القانونية للوجهة**، حدد **إنشاء الكيانات القانونية** لإنشاء كيان قانوني جديد يمكنك نسخ بيانات الكيان القانوني المصدر إليه.</span><span class="sxs-lookup"><span data-stu-id="3f022-145">In the **Destination legal entities** FastTab, select **Create legal entities** to create a new legal entity that you can copy the source legal entity data to.</span></span> <span data-ttu-id="3f022-146">حدد **تحديد الموجود** لنسخ البيانات إلى كيان قانوني موجود.</span><span class="sxs-lookup"><span data-stu-id="3f022-146">Select **Select existing** to copy data to an existing legal entity.</span></span>
9. <span data-ttu-id="3f022-147">اختياري: قم بتعيين حقل **نسخ التسلسلات الرقمية** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="3f022-147">Optional: Set the **Copy number sequences** field to **Yes**.</span></span> <span data-ttu-id="3f022-148">(يُنصح بهذه الخطوة عند نسخ البيانات.)</span><span class="sxs-lookup"><span data-stu-id="3f022-148">(This step is recommended when you copy data.)</span></span>
10. <span data-ttu-id="3f022-149">في منطقة **الكيانات المحددة**، حدد **إضافة قالب**.</span><span class="sxs-lookup"><span data-stu-id="3f022-149">In the **Selected entities** area, select **Add template**.</span></span>
11. <span data-ttu-id="3f022-150">حدد القوالب المُراد استخدامها.</span><span class="sxs-lookup"><span data-stu-id="3f022-150">Select the templates to use.</span></span> <span data-ttu-id="3f022-151">تتضمن القوالب المقترحة لكيان قانوني جديد **025 - دفتر الأستاذ العام** و **الماليات**.</span><span class="sxs-lookup"><span data-stu-id="3f022-151">Suggested templates for a new legal entity include **025 - General Ledger** and **Financials**.</span></span> <span data-ttu-id="3f022-152">نوصي بمراجعة جميع القوالب الأخرى المتوفرة لتحديد ما إذا كان أي منها ينطبق على متطلباتك.</span><span class="sxs-lookup"><span data-stu-id="3f022-152">We recommend that you review all the other available templates to determine whether any of them apply to your requirements.</span></span>
12. <span data-ttu-id="3f022-153">حدد **نسخ إلى كيان قانوني** لبدء معالجة دُفعة من شأنها إنشاء الكيانات المحددة ونسخها في الكيان القانوني الوجهة.</span><span class="sxs-lookup"><span data-stu-id="3f022-153">Select **Copy into legal entity** to start a batch process that will create the selected entities and copy them into the destination legal entity.</span></span>
13. <span data-ttu-id="3f022-154">بعد اكتمال العملية، ولكن قبل ترحيل أي حركة، انتقل إلى دفتر الأستاذ، وقم بتحديث عملات المحاسبة والتقارير كما هو موضح سابقًا في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="3f022-154">After the process is completed, but before any transaction are posted, go to the ledger, and update the accounting and reporting currencies as described earlier in this topic.</span></span>

<span data-ttu-id="3f022-155">إذا قمت بإنشاء كيان قانوني جديد بحيث يمكنك تغيير عملة المحاسبة أو التقارير، فتحقق من تحويل الأرصدة الافتتاحية من عملات الكيان القانوني القديم إلى العملات الجديدة.</span><span class="sxs-lookup"><span data-stu-id="3f022-155">If you created a new legal entity so that you can change the accounting or reporting currency, verify that the beginning balances are translated from the currencies of the old legal entity to the new currencies.</span></span>

<span data-ttu-id="3f022-156">بالنسبة للفيديو الذي يعرض الخطوات السابقة، راجع [النسخ إلى الكيان القانوني](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).</span><span class="sxs-lookup"><span data-stu-id="3f022-156">For a video that shows the preceding steps, see [Copy Into Legal Entity](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).</span></span>
