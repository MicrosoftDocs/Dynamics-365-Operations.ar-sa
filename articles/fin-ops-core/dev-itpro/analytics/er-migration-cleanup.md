---
title: مسح ترحيل ER
description: يشرح هذا الموضوع كيفيه استخدام وظيفة مسح ترحيل ER لحل المشكلات المتعلقة بقوالب ER.
author: NickSelin
manager: AnnBe
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: b09afc30c401e2dccfc4114261dc5e713c8c470c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565505"
---
# <a name="er-migration-cleanup"></a><span data-ttu-id="6029e-103">مسح ترحيل ER</span><span class="sxs-lookup"><span data-stu-id="6029e-103">ER migration cleanup</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6029e-104">عند إدارة مثيلات Finance قد تقرر ترحيل المثيل الحالي إلى موقع آخر.</span><span class="sxs-lookup"><span data-stu-id="6029e-104">When you manage your Finance instances, you might decide to migrate your current instance to another location.</span></span> <span data-ttu-id="6029e-105">على سبيل المثال، يمكنك ترحيل مثيل الإنتاج إلى بيئة اختبار معزولة جديدة.</span><span class="sxs-lookup"><span data-stu-id="6029e-105">For example, you might migrate your production instance to a new sandbox environment.</span></span> <span data-ttu-id="6029e-106">إذا قمت بتكوين إطار عمل التقارير الإلكترونية (ER) لتخزين القوالب في مخزن البيانات الثنائية كبيرة الحجم لـ Microsoft Azure يشير الجدول **DocuValue** في بيئة الاختبار المعزولة الجديدة إلى مثيل مخزن البيانات الثنائية كبيرة الحجم في بيئة الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="6029e-106">If you configured the Electronic reporting (ER) framework to store templates in Microsoft Azure Blob storage, the **DocuValue** table in the new sandbox environment refers to the instance of Blob storage in the production environment.</span></span> <span data-ttu-id="6029e-107">ومع ذلك، لا يمكن الوصول إلى هذا المثيل من بيئة الاختبار المعزولة، لأن عملية الترحيل لا تدعم ترحيل البيانات الاصطناعية في مخزن البيانات الثنائية كبيرة الحجم.</span><span class="sxs-lookup"><span data-stu-id="6029e-107">However, this instance can't be accessed from the sandbox environment because the migration process doesn't support the migration of artifacts in Blob storage.</span></span> <span data-ttu-id="6029e-108">وبدلا من ذلك، فانه من المتوقع أنه في بيئة وضع الحماية الجديدة، تشير إلى مثيل لمخزن البيانات الثنائية كبيرة الحجم في بيئة وضع الحماية‬ التي لا تحصل بعد على قوالب ER.</span><span class="sxs-lookup"><span data-stu-id="6029e-108">Rather, it's expected that in the new sandbox environment, you refer to the instance of Blob storage in the sandbox environment that does not yet obtain the ER templates.</span></span>

<span data-ttu-id="6029e-109">إذا حاولت تشغيل تنسيق تقارير إلكترونية يستخدم قالبًا لإنشاء مستندات الأعمال، يحدث استثناء، ويتم اعلامك بالقالب المفقود.</span><span class="sxs-lookup"><span data-stu-id="6029e-109">If you try to run an ER format that uses a template to generate business documents, an exception occurs, and you're notified about the missing template.</span></span> <span data-ttu-id="6029e-110">ويتم أيضًا إرشادك لاستخدام خيار مسح ترحيل التقارير الإلكترونية (ER) لحذف تكوين تنسيق التقارير الذي يحتوي على القالب ثم إعادة استيراده.</span><span class="sxs-lookup"><span data-stu-id="6029e-110">You're also guided to use the ER migration cleanup option to delete and then re-import the ER format configuration that contains the template.</span></span>

<span data-ttu-id="6029e-111">[![تشغيل تنسيق ER](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)</span><span class="sxs-lookup"><span data-stu-id="6029e-111">[![Running an ER format](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)</span></span>

<span data-ttu-id="6029e-112">ستتلقى خطأً مشابهاً إذا انتقلت إلى صفحة **التكوينات** (**إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**) وفي شجره التكوينات، حاول حذف تكوين التنسيق الخاص بـ ER الذي يستخدم القالب.</span><span class="sxs-lookup"><span data-stu-id="6029e-112">You will receive a similar error if you navigate to the **Configurations** page (**Organization administration** \> **Electronic reporting** \> **Configurations**) and in the configurations tree, try to delete an ER format configuration that uses a template.</span></span>

<span data-ttu-id="6029e-113">[![حذف تنسيق ER](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)</span><span class="sxs-lookup"><span data-stu-id="6029e-113">[![Deletion an ER format](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)</span></span>

<span data-ttu-id="6029e-114">أكمل الخطوات التالية لحل المشكلات مع قوالب ER التي لا يمكنك الوصول إليها.</span><span class="sxs-lookup"><span data-stu-id="6029e-114">Complete the following steps to resolve issues with ER templates that you are unable to access.</span></span>

1.  <span data-ttu-id="6029e-115">انتقل إلى **إدارة المؤسسة** \> **دوري** \> صفحة **مسح الترحيل**.</span><span class="sxs-lookup"><span data-stu-id="6029e-115">Go to **Organization administration** \> **Periodic** \> **Migration cleanup** page.</span></span>
2.  <span data-ttu-id="6029e-116">حدد تكوين تنسيق ER الذي لا يمكن تنفيذه أو حذفه.</span><span class="sxs-lookup"><span data-stu-id="6029e-116">Select an ER format configuration that can’t be executed or deleted.</span></span>
3.  <span data-ttu-id="6029e-117">حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="6029e-117">Select **Delete**.</span></span>
4.  <span data-ttu-id="6029e-118">قم بتأكيد حذف تكوين التنسيق المحدد لـ ER.</span><span class="sxs-lookup"><span data-stu-id="6029e-118">Confirm the deletion of the selected ER format configuration.</span></span>
5.  <span data-ttu-id="6029e-119">[قم باستيراد](download-electronic-reporting-configuration-lcs.md) تكوين تنسيق ER المحذوف إلى مثيل Finance الحالي.</span><span class="sxs-lookup"><span data-stu-id="6029e-119">[Import](download-electronic-reporting-configuration-lcs.md) the deleted ER format configuration to the current Finance instance.</span></span>

## <a name="applicability"></a><span data-ttu-id="6029e-120">إمكانية التطبيق</span><span class="sxs-lookup"><span data-stu-id="6029e-120">Applicability</span></span>

> <span data-ttu-id="6029e-121">[مهم] يتم استهداف خيار **مسح الترحيل** فقط لتكوينات تنسيق ER التي تحتوي علي قوالب ER غير قابله للوصول.</span><span class="sxs-lookup"><span data-stu-id="6029e-121">[Important] The **Migration cleanup** option is targeted only for ER format configurations that contain non-accessible ER templates.</span></span> <span data-ttu-id="6029e-122">عند حذف تكوين التنسيق الخاص بـ ER باستخدام خيار **مسح الترحيل** يحذف ER القوالب المرتبطة بنتائج التكوينات في قاعده بيانات التطبيق الوحيدة.</span><span class="sxs-lookup"><span data-stu-id="6029e-122">When you delete an ER format configuration by using the **Migration cleanup** option, ER deletes the templates that are related to the configuration artifacts in the only application database.</span></span> <span data-ttu-id="6029e-123">لم يتم التحقق من وجود الملفات الفعلية المناسبة في مخزن البيانات الثنائية كبيرة الحجم.</span><span class="sxs-lookup"><span data-stu-id="6029e-123">The existence of the appropriate physical files in Blob storage are not validated.</span></span> <span data-ttu-id="6029e-124">بدلا من ذلك، من المفترض عدم وجود أي منها.</span><span class="sxs-lookup"><span data-stu-id="6029e-124">Instead, it is assumed that there are none.</span></span> <span data-ttu-id="6029e-125">لذلك، لا تستخدم خيار **مسح الترحيل** كبديل لخيار حذف تكوين ER في صفحة **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="6029e-125">Therefore, do not use the **Migration cleanup** option as an alternative to the ER configuration deletion option on the **Configurations** page.</span></span> <span data-ttu-id="6029e-126">استخدم خيار **مسح الترحيل** فقط عند فشل خيار حذف تكوين ER في صفحة **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="6029e-126">Use the **Migration cleanup** option only when the ER configuration deletion option on the **Configurations** page failed.</span></span>
>
> <span data-ttu-id="6029e-127">إذا استخدمت خيار **مسح الترحيل** لحذف تكوين تنسيق ER عند توفر القالب المُشار إليه في مخزن البيانات الثنائية كبيرة الحجم، فإنه يمكنك فقط حذف نتائج التكوين ذات الصلة في قاعدة بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="6029e-127">If you use the **Migration cleanup** option to delete an ER format configuration when the referred template is available in the Blob storage, you only delete related configuration artifacts in the application database.</span></span> <span data-ttu-id="6029e-128">يظل الملف الفعلي للقالب في مخزن البيانات الثنائية كبيرة الحجم.</span><span class="sxs-lookup"><span data-stu-id="6029e-128">The physical file of the template in the Blob storage remains.</span></span> <span data-ttu-id="6029e-129">لم تعد الكتابة فوق مخزن البيانات الثنائية كبيرة الحجم مسموحًا بها.</span><span class="sxs-lookup"><span data-stu-id="6029e-129">File overwriting in Blob storage is no longer allowed.</span></span> <span data-ttu-id="6029e-130">لمزيد من المعلومات، راجع [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217).</span><span class="sxs-lookup"><span data-stu-id="6029e-130">For more information, see [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217).</span></span> <span data-ttu-id="6029e-131">بالإضافة إلى ذلك، لن تتمكن بعد ذلك من إعادة استيراد التكوينات التي تم حذفها باستخدام مسح الترحيل في هذه البيئة.</span><span class="sxs-lookup"><span data-stu-id="6029e-131">Additionally, you will no longer be able to re-import the configurations deleted by using the Migration cleanup in this environment.</span></span> <span data-ttu-id="6029e-132">لحل هذه المشكلة، يجب العثور علي الملف المقابل في مخزن البيانات الثنائية كبيرة الحجم وحذفه يدويا.</span><span class="sxs-lookup"><span data-stu-id="6029e-132">To resolve this issue, you need to find the corresponding file in Blob storage and manually delete it.</span></span>

<span data-ttu-id="6029e-133">[![استيراد تنسيق ER](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)</span><span class="sxs-lookup"><span data-stu-id="6029e-133">[![Importing an ER format](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)</span></span>

<span data-ttu-id="6029e-134">قد تحدث مشكله مشابهه إذا قمت بترحيل مثيل التطبيق الخاص بك إلى موقع آخر تم استخدامه كهدف ترحيل أكثر من مره ولمخزن البيانات الثنائية كبيرة الحجم التي تحتوي بالفعل على ملفات قالب ER.</span><span class="sxs-lookup"><span data-stu-id="6029e-134">A similar issue may occur if you migrate your application instance to another location that has been used as a migration target more than once and for which the Blob storage already contains ER template files.</span></span>

<span data-ttu-id="6029e-135">بسبب وجود تكوينات متعددة لتنسيق التقارير الإلكترونية، قد تستغرق هذه العملية وقتًا طويلاً.</span><span class="sxs-lookup"><span data-stu-id="6029e-135">Because you can have several ER format configurations, this process can be time consuming.</span></span> <span data-ttu-id="6029e-136">لذلك باستخدام ميزة [‏‫مساحة تخزين النسخ الاحتياطية لقوالب التقارير الإلكترونية‬](er-backup-storage-templates.md) " لاسترداد القوالب باستخدام المراجع المقطوعة تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="6029e-136">Therefore, using the [Backup storage of ER templates](er-backup-storage-templates.md) feature to automatically recover templates with broken references is preferred.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]