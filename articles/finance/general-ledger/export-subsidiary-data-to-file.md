---
title: تصدير بيانات الشركة الفرعية إلى ملفات
description: يشرح هذا الموضوع كيفية التحضير لتصدير البيانات من Microsoft Dynamics 365 Finance ثم استيرادها إلى كيان قانوني موحد.
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 179a401178935b8a76d6718a7fb1f63e08344f50
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968669"
---
# <a name="export-subsidiary-data-to-files"></a><span data-ttu-id="fd46f-103">تصدير بيانات الشركة الفرعية إلى ملفات</span><span class="sxs-lookup"><span data-stu-id="fd46f-103">Export subsidiary data to files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd46f-104">يمكنك استخدام صفحة **التصدير** (**إدارة النظام \> مساحات العمل \> الاستيراد/التصدير**) للتحضير لتصدير بيانات الشركة التابعة إلى ملفات يمكن استيرادها بعد ذلك إلى كيان قانوني موحد.</span><span class="sxs-lookup"><span data-stu-id="fd46f-104">You use the **Export** page (**System administration \> Workspaces \> Import/Export**) to prepare to export subsidiary data to files that can then be imported into a consolidated legal entity.</span></span> <span data-ttu-id="fd46f-105">لمزيد من المعلومات حول عمليات الاستيراد والتصدير راجع [نظرة عامة حول وظائف استيراد البيانات وتصديرها](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="fd46f-105">For more information about the import and export processes, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

1. <span data-ttu-id="fd46f-106">إنشاء كيان قانوني لعملية التوحيد.</span><span class="sxs-lookup"><span data-stu-id="fd46f-106">Create a legal entity for the consolidation process.</span></span> <span data-ttu-id="fd46f-107">للحصول على معلومات حول كيفية إنشاء كيان قانوني، راجع [إنشاء كيان قانوني](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span><span class="sxs-lookup"><span data-stu-id="fd46f-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="fd46f-108">لمزيد من المعلومات، راجع [إعداد كيان قانوني لاستخدامه في عملية التوحيد](prepare-company-for-consolidation.md)و[إعداد أحد الكيانات القانونية التابعة لإجراء التوحيد](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="fd46f-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span> 

2. <span data-ttu-id="fd46f-109">انتقل إلى **عمليات التوحيدات \> تصدير أرصدة الشركة**.</span><span class="sxs-lookup"><span data-stu-id="fd46f-109">Go to **Consolidations \> Export company balances**.</span></span> <span data-ttu-id="fd46f-110">في صفحة **تصدير أرصدة الشركة**، من علامة التبويب **المعايير**، حدد تفاصيل التوحيد عن طريق إعداد الحقول التالية.</span><span class="sxs-lookup"><span data-stu-id="fd46f-110">On the **Export company balances** page, on the **Criteria** tab, specify the details of the consolidation by setting the following fields.</span></span>

    | <span data-ttu-id="fd46f-111">الحقل</span><span class="sxs-lookup"><span data-stu-id="fd46f-111">Field</span></span>                             | <span data-ttu-id="fd46f-112">الوصف</span><span class="sxs-lookup"><span data-stu-id="fd46f-112">Description</span></span> |
    |-----------------------------------|-------|
    | <span data-ttu-id="fd46f-113">الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="fd46f-113">Main account</span></span>                      | <span data-ttu-id="fd46f-114">حدد الحسابات المراد دمجها.</span><span class="sxs-lookup"><span data-stu-id="fd46f-114">Specify the accounts to consolidate.</span></span> <span data-ttu-id="fd46f-115">لتضمين كافة الحسابات، اترك هذا الحقل فارغًا.</span><span class="sxs-lookup"><span data-stu-id="fd46f-115">To include all accounts, leave this field blank.</span></span> |
    | <span data-ttu-id="fd46f-116">استخدام حساب التوحيد</span><span class="sxs-lookup"><span data-stu-id="fd46f-116">Use consolidation account</span></span>         | <span data-ttu-id="fd46f-117">إذا كنت قد حددت حسابات التوحيد، فقم بتعيين هذا الخيار على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="fd46f-117">If you've specified consolidation accounts, set this option to **Yes**.</span></span> |
    | <span data-ttu-id="fd46f-118">تحديد حساب الدمج من</span><span class="sxs-lookup"><span data-stu-id="fd46f-118">Select consolidation account from</span></span> | <span data-ttu-id="fd46f-119">حدد إما **حسابًا رئيسيًا** أو **مجموعة حسابات توحيد**.</span><span class="sxs-lookup"><span data-stu-id="fd46f-119">Select either **Main account** or **Consolidation account group**.</span></span> |
    | <span data-ttu-id="fd46f-120">مجموعة حسابات الدمج</span><span class="sxs-lookup"><span data-stu-id="fd46f-120">Consolidation account group</span></span>       | <span data-ttu-id="fd46f-121">حدد مجموعة حسابات التوحيد لحساب التوحيد الذي حددته.</span><span class="sxs-lookup"><span data-stu-id="fd46f-121">Select a consolidation account group for the consolidation account that you selected.</span></span> |
    | <span data-ttu-id="fd46f-122">فترة التوحيد</span><span class="sxs-lookup"><span data-stu-id="fd46f-122">Consolidation period</span></span>              | <span data-ttu-id="fd46f-123">حدد تواريخ "من" و "إلى" للتوحيد.</span><span class="sxs-lookup"><span data-stu-id="fd46f-123">Specify "from" and "to" dates for the consolidation.</span></span> |
    | <span data-ttu-id="fd46f-124">تضمين المبالغ الفعلية</span><span class="sxs-lookup"><span data-stu-id="fd46f-124">Include actual amounts</span></span>            | <span data-ttu-id="fd46f-125">قم بتعيين هذا الخيار إلى **نعم** لتضمين المبالغ الفعلية.</span><span class="sxs-lookup"><span data-stu-id="fd46f-125">Set this option to **Yes** to include actual amounts.</span></span> |
    | <span data-ttu-id="fd46f-126">تضمين مبالغ الموازنات</span><span class="sxs-lookup"><span data-stu-id="fd46f-126">Include budget amounts</span></span>            | <span data-ttu-id="fd46f-127">قم بتعيين هذا الخيار إلى **نعم** لتضمين مبالغ الموازنة في عمليات التوحيد.</span><span class="sxs-lookup"><span data-stu-id="fd46f-127">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="fd46f-128">نماذج الموازنة</span><span class="sxs-lookup"><span data-stu-id="fd46f-128">Budget models</span></span>                     | <span data-ttu-id="fd46f-129">حدد نموذج الموازنة المطلوب تضمينه.</span><span class="sxs-lookup"><span data-stu-id="fd46f-129">Specify the budget model to include.</span></span> |

3. <span data-ttu-id="fd46f-130">في علامة التبويب **الأبعاد المالية**، حدد تفاصيل للتوحيد:</span><span class="sxs-lookup"><span data-stu-id="fd46f-130">On the **Financial dimensions** tab, specify the details of the consolidation:</span></span>

    - <span data-ttu-id="fd46f-131">حدد معلومات البعد المالي الذي يجب نقله من الحركات في حسابات الشركة التابعة إلى الحركات في الكيان القانوني الموحد.</span><span class="sxs-lookup"><span data-stu-id="fd46f-131">Specify the financial dimension information that should be transferred from the transactions in the subsidiary accounts to the transactions in the consolidated legal entity.</span></span>
    - <span data-ttu-id="fd46f-132">حدد الأبعاد المالية في القائمة.</span><span class="sxs-lookup"><span data-stu-id="fd46f-132">Select financial dimensions in the list.</span></span>
    - <span data-ttu-id="fd46f-133">حدد المواصفات الصحيحة لكل بعد مالي تم توحيده.</span><span class="sxs-lookup"><span data-stu-id="fd46f-133">Identify the correct specification for each financial dimension that is consolidated.</span></span> <span data-ttu-id="fd46f-134">تشتمل الخيارات المتاحة **البُعد** و **بُعد المجموعة** و **حسابات الشركة** و **الحساب**.</span><span class="sxs-lookup"><span data-stu-id="fd46f-134">The available options include **Dimension**, **Group dimension**, **Company accounts**, and **Account**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="fd46f-135">يتيح لك خيار **بُعد المجموعة** تحديد قيمة البُعد التي يتم استخدامها بواسطة مجموعة الشركات الجاري توحيدها.</span><span class="sxs-lookup"><span data-stu-id="fd46f-135">The **Group dimension** option lets you define the dimension value that is used by the group of companies that is being consolidated.</span></span>

    - <span data-ttu-id="fd46f-136">حدد ترتيب الشريحة الذي سيتم التوحيد من خلاله.</span><span class="sxs-lookup"><span data-stu-id="fd46f-136">Specify the segment order to consolidate in.</span></span>

4. <span data-ttu-id="fd46f-137">في علامة تبويب **الكيانات القانونية**، اتبع الخطوات التالية لتحديد الكيان القانوني الذي تقوم بتصديره:</span><span class="sxs-lookup"><span data-stu-id="fd46f-137">On the **Legal entities** tab, follow these steps to specify the legal entity that you're exporting:</span></span>

    1. <span data-ttu-id="fd46f-138">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="fd46f-138">Select **New**.</span></span>
    2. <span data-ttu-id="fd46f-139">في حقل **الكيان القانوني المصدر**، أدخل الكيان القانوني.</span><span class="sxs-lookup"><span data-stu-id="fd46f-139">In the **Source legal entity** field, enter the legal entity.</span></span>

        <span data-ttu-id="fd46f-140">إذا كانت نفس المعايير تنطبق على العديد من الشركات التابعة الموجودة في نفس قاعدة البيانات، فيمكنك نقل البيانات من تلك الشركات التابعة إلى ملفات تصدير منفصلة عبر عملية واحدة.</span><span class="sxs-lookup"><span data-stu-id="fd46f-140">If the same criteria apply to several subsidiaries that are in the same database, you can transfer data from those subsidiaries to separate export files in a single operation:</span></span>

        1. <span data-ttu-id="fd46f-141">قم بإنشاء سطر لكل كيان قانوني تابع يتم تصدير حساباته إلى ملفات.</span><span class="sxs-lookup"><span data-stu-id="fd46f-141">Create a line for each subsidiary legal entity for which accounts should be exported to files.</span></span> <span data-ttu-id="fd46f-142">وسوف يتم استيراد هذه الملفات إلى الكيان القانوني الموحد فيما بعد.</span><span class="sxs-lookup"><span data-stu-id="fd46f-142">These files will be imported into the consolidated legal entity later.</span></span>
        2. <span data-ttu-id="fd46f-143">مع كل شركة تابعة، قم بإدخال اسم الشركة التابعة واسم ملف التصدير الذي سيتم إنشاؤه خلال مهمة التصدير.</span><span class="sxs-lookup"><span data-stu-id="fd46f-143">For each subsidiary, enter the subsidiary name and the name of the export file that will be created during the export job.</span></span>

    3. <span data-ttu-id="fd46f-144">في حقل **نوع الحساب لاختلافات التحويل**، حدد **الأرباح والخسائر** أو **الميزانية العمومية**.</span><span class="sxs-lookup"><span data-stu-id="fd46f-144">In **Account type of conversion differences** field, Select **Profit and loss** or **Balance sheet**.</span></span>
    4. <span data-ttu-id="fd46f-145">أدخل اسم ملف لملف التصدير الذي سيتم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="fd46f-145">Enter a file name for the export file that will be created.</span></span>

5. <span data-ttu-id="fd46f-146">حدد **موافق** لتشغيل التصدير.</span><span class="sxs-lookup"><span data-stu-id="fd46f-146">Select **OK** to run the export.</span></span>

<span data-ttu-id="fd46f-147">وعند اكتمال التصدير، ستستلم رسالة تُظهر أرقام السجلات التي تم حفظها في كل ملف.</span><span class="sxs-lookup"><span data-stu-id="fd46f-147">When the export is completed, you receive a message that shows the number of records that were saved in each file.</span></span> <span data-ttu-id="fd46f-148">ويمكن بعد ذلك استيراد الملفات إلى الكيان القانوني الموحد.</span><span class="sxs-lookup"><span data-stu-id="fd46f-148">You can then import the files into the consolidated legal entity.</span></span>
