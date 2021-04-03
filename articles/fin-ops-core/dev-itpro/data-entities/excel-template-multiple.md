---
title: قوالب بيانات مع أوراق عمل متعددة
description: يصف هذا الموضوع كيفية استيراد البيانات باستخدام قوالب كيانات البيانات من Excel إلى Finance and Operations.
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 64515ff74c0ca2b01bb9dac06331ba0424811411
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565561"
---
# <a name="data-templates-with-multiple-worksheets"></a><span data-ttu-id="7cd34-103">قوالب بيانات مع أوراق عمل متعددة</span><span class="sxs-lookup"><span data-stu-id="7cd34-103">Data templates with multiple worksheets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cd34-104">تدعم إدارة البيانات في التطبيق القوالب التي تستند إلى Microsoft Excel لكيانات البيانات.</span><span class="sxs-lookup"><span data-stu-id="7cd34-104">Data management in the application supports Microsoft Excel-based templates for data entities.</span></span> <span data-ttu-id="7cd34-105">يمكن أن تحتوي هذه القوالب على ورقة عمل واحدة أو أكثر.</span><span class="sxs-lookup"><span data-stu-id="7cd34-105">These templates can contain one or more worksheets.</span></span> <span data-ttu-id="7cd34-106">تستخدم عادة قوالب أوراق العمل المتعددة عندما يكون ذلك مناسبًا لإدارة البيانات في ملف واحد واستيرادها في كيانات بيانات متعددة.</span><span class="sxs-lookup"><span data-stu-id="7cd34-106">Templates with multiple worksheets are often used when it is convenient to manage data in a single file and import it to multiple data entities.</span></span> <span data-ttu-id="7cd34-107">على سبيل المثال ستكون المواقع والمستودعات.</span><span class="sxs-lookup"><span data-stu-id="7cd34-107">An example would be sites and warehouses.</span></span>

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a><span data-ttu-id="7cd34-108">تحميل ملف في المرة الواحدة وتعيينه إلى كافة الكيانات</span><span class="sxs-lookup"><span data-stu-id="7cd34-108">Upload a file once and map it to all entities</span></span>
<span data-ttu-id="7cd34-109">لنأخذ مثالاً حيث يتضمن ملف Excel ورقتي عمل باسم **المواقع‏‎** و **المستودعات**.</span><span class="sxs-lookup"><span data-stu-id="7cd34-109">Let's take an example where there is one Excel file with worksheets called **Sites** and **Warehouses**.</span></span> <span data-ttu-id="7cd34-110">لإعداد مشروع استيراد البيانات، يجب عليك إضافة كيان البيانات الأول، **المواقع** ثم تحميل الملف.</span><span class="sxs-lookup"><span data-stu-id="7cd34-110">To set up the data import project, you would add the first data entity, **Sites** and then upload the file.</span></span> <span data-ttu-id="7cd34-111">ستكون قادراً على تحديد **المواقع** كورقة عمل يتم استخدامها لهذا الكيان.</span><span class="sxs-lookup"><span data-stu-id="7cd34-111">You will be able to select **Sites** as the worksheet to be used for this entity.</span></span>

<span data-ttu-id="7cd34-112">إذا قمت بإضافة الكيان الثاني **المستودعات** دون مغادرة نموذج **إضافة ملف**، فسوف تسمح لك عمليات البحث في أوراق العمل بتحديد ورقة عمل **المستودعات** دون الحاجة إلى تحميل الملف مرة أخرى.</span><span class="sxs-lookup"><span data-stu-id="7cd34-112">If you add the second entity **Warehouses** without leaving the **Add file** form, the worksheet lookup will let you select the **Warehouses** worksheet without having to upload the file again.</span></span> <span data-ttu-id="7cd34-113">قد يكون السبب الوحيد لتحميل ملف جديد إذا كانت بيانات **المستودعات** في ملف مختلف.</span><span class="sxs-lookup"><span data-stu-id="7cd34-113">The only reason to upload a new file would be if the **Warehouses** data was in a different file.</span></span>

![أوراق عمل متعددة](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a><span data-ttu-id="7cd34-115">إصلاح ورقة العمل إلى تعيين كيان</span><span class="sxs-lookup"><span data-stu-id="7cd34-115">Fix worksheet to entity mapping</span></span>

<span data-ttu-id="7cd34-116">يمكن تثبيت تعيين ورقة العمل لكيان البيانات في وظيفة الاستيراد من الشبكة.</span><span class="sxs-lookup"><span data-stu-id="7cd34-116">The mapping of the worksheet to a data entity in the import job can be fixed from the grid.</span></span> <span data-ttu-id="7cd34-117">يوضح عمود **ورقة عمل** في الشبكة أوراق العمل من الملف الذي تم تعيينه.</span><span class="sxs-lookup"><span data-stu-id="7cd34-117">The **Worksheet** column in the grid shows the worksheets from the file that was mapped.</span></span> <span data-ttu-id="7cd34-118">يمكنك اختيار ورقة عمل مختلف من القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="7cd34-118">You can choose a different worksheet from the drop-down menu.</span></span> <span data-ttu-id="7cd34-119">إذا كانت ورقة العمل المُحددة تم تعيينها بالفعل إلى أحد الكيانات في مشروع البيانات، فسوف يطلب منك النظام تأكيد التغيير.</span><span class="sxs-lookup"><span data-stu-id="7cd34-119">If the chosen worksheet is already mapped to an entity in the data project, the system asks you to confirm the change.</span></span> <span data-ttu-id="7cd34-120">ننصح بتثبيت جميع التعيينات في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="7cd34-120">We recommend that you fix all mappings in the grid.</span></span>

![تحديث تعيين ورقة العمل](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a><span data-ttu-id="7cd34-122">إعادة تعيين إلى ملف جديد</span><span class="sxs-lookup"><span data-stu-id="7cd34-122">Re-map to a new file</span></span>

<span data-ttu-id="7cd34-123">في الحالات التي يجب فيها تحميل إصدار جديد من نفس الملف أو ملف جديد بالكامل بالنسبة للكيانات الموجودة في مشروع البيانات، يجب عليك استخدام تجربة **إضافة ملف**، وإضافة الكيانات مرة أخرى كما لو كانت تتم إضافتها لأول مرة.</span><span class="sxs-lookup"><span data-stu-id="7cd34-123">In cases where a new version of the same file or a completely new file must be uploaded for existing entities in a data project, you must use the **Add file** experience, and add the entities again as if they were being added for the first time.</span></span> <span data-ttu-id="7cd34-124">سوف تظهر لك رسالة تأكيد من النظام بأنك تريد الكتابة فوق الكيانات الموجودة في مشروع البيانات قبل المتابعة.</span><span class="sxs-lookup"><span data-stu-id="7cd34-124">The system will confirm that you want to overwrite the existing entities in the data project before proceeding.</span></span> <span data-ttu-id="7cd34-125">سوف تستمر الكيانات التي لم تُضاف مرة أخرى (أو تمت الكتابة فوقها) في الاحتفاظ بالتعيينات السابقة من الملف السابق.</span><span class="sxs-lookup"><span data-stu-id="7cd34-125">Entities that are not added again (or overwritten) will continue to hold the previous mappings from the previous file.</span></span>

## <a name="upload-a-file-using-run-project"></a><span data-ttu-id="7cd34-126">تحميل ملف باستخدام مشروع التشغيل</span><span class="sxs-lookup"><span data-stu-id="7cd34-126">Upload a file using Run project</span></span>

<span data-ttu-id="7cd34-127">يمكنك تحميل ملف Excel أثناء استخدام خيار **تشغيل المشروع** لتنفيذ استيراد مشروع.</span><span class="sxs-lookup"><span data-stu-id="7cd34-127">You can upload an Excel file while using the **Run project** option to execute an import project.</span></span> <span data-ttu-id="7cd34-128">يجب أن تكون حذرًا لتحميل الملفات التي لها نفس أوراق العمل فقط كالتعيينات الموجودة في وحدات البيانات في مشروع البيانات.</span><span class="sxs-lookup"><span data-stu-id="7cd34-128">You must be careful to upload only files that have the same worksheets as the existing mappings on the data entities in the data project.</span></span> <span data-ttu-id="7cd34-129">إذا لم يتم العثور على ورقة عمل في الملف الذي تم تحميله مؤخرا، يعرض النظام رسالة خطأ وستتوقف عملية الاستيراد.</span><span class="sxs-lookup"><span data-stu-id="7cd34-129">If a worksheet is not found in the newly uploaded file, the system displays an error and will stop the import.</span></span> <span data-ttu-id="7cd34-130">إذا كان يجب تغيير التعيين إلى ورقة العمل لأحد الكيانات، فيجب أولًا تحديث التعيينات في مشروع البيانات من ضمن مشروع البيانات قبل استخدام الملف في تجربة **تشغيل المشروع**.</span><span class="sxs-lookup"><span data-stu-id="7cd34-130">If the mapping to the worksheet must be changed for an entity, then the mappings in the data project must be first updated from within the data project before using the file in the **Run project** experience.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]