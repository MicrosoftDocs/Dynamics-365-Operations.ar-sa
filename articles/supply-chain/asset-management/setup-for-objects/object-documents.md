---
title: مستندات الأصول
description: يشرح هذا الموضوع مستندات الأصول في إدارة الأصول.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8458c302b506f9f048b7886f55a392d9afceb446
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808366"
---
# <a name="asset-documents"></a><span data-ttu-id="e83cb-103">مستندات الأصول</span><span class="sxs-lookup"><span data-stu-id="e83cb-103">Asset documents</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e83cb-104">يشرح هذا الموضوع مستندات الأصول في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="e83cb-104">This topic explains asset documents in Asset Management.</span></span>

<span data-ttu-id="e83cb-105">في إدارة الأصول، يمكنك إعداد المستندات بحيث تكون مرتبطة تلقائيًا بأنواع الوظائف أو الشركات المصنعة للأصول أو أنواع الأصول أو الأصول، على سبيل المثال.</span><span class="sxs-lookup"><span data-stu-id="e83cb-105">In Asset Management, you can set up documents so that they are automatically related to job types, asset manufacturers, asset types, or assets, for example.</span></span> <span data-ttu-id="e83cb-106">تكون هذه الوظيفة مفيدة عند إصدار نسخ مستندات محدثة.</span><span class="sxs-lookup"><span data-stu-id="e83cb-106">This functionality is useful when updated document versions are released.</span></span> <span data-ttu-id="e83cb-107">وفي هذه الحالة، يجب عليك فقط وضع المستند المحدّث في الموقع القياسي الذي تستخدمه لمستندات Supply chain Management، وإرفاق المستند بسجل مستند الأصل الذي قمت بإنشائه.</span><span class="sxs-lookup"><span data-stu-id="e83cb-107">In that case, you just have to put the updated document in the standard location that you use for your Supply Chain Management documents, and attach the document to the asset document record that you've created.</span></span> <span data-ttu-id="e83cb-108">بعد ذلك، يمكن الوصول إلى المستند المحدث من بنود قائمة **كل الأصول** و **الأصول‏‎ النشطة** و **أصولي النشطة** و **جميع أوامر العمل** و **وظائف أوامر العمل النشطة**.</span><span class="sxs-lookup"><span data-stu-id="e83cb-108">The updated document can then be accessed from the **All assets**, **Active assets**, **My active assets**, **All work orders**, and **Active work order jobs** menu items.</span></span> <span data-ttu-id="e83cb-109">تستخدم عملية إرفاق المستندات بسجل مستندات الأصول النظام القياسي للتعامل مع المستندات.</span><span class="sxs-lookup"><span data-stu-id="e83cb-109">The process for attaching documents to an asset document record uses the standard document handling system.</span></span>

<span data-ttu-id="e83cb-110">**مثال 1:** قد يصف مستند يرتبط بنوع وظيفة إجراءً لنوع الوظيفة هذا.</span><span class="sxs-lookup"><span data-stu-id="e83cb-110">**Example 1:** A document that is related to a job type might describe a procedure for that job type.</span></span>

<span data-ttu-id="e83cb-111">**مثال 2:** قد يكون مستند يرتبط بمجموعة من نوع أصل وشركة مصنعة ونموذج الدليل القياسي لنموذج الشركة المصنعة للأصل المحدد.</span><span class="sxs-lookup"><span data-stu-id="e83cb-111">**Example 2:** A document that is related to a combination of an asset type, manufacturer, and model might be the standard manual for the selected asset manufacturer model.</span></span>

## <a name="create-asset-document-relation"></a><span data-ttu-id="e83cb-112">إنشاء علاقة مستندات الأصول</span><span class="sxs-lookup"><span data-stu-id="e83cb-112">Create asset document relation</span></span>

1. <span data-ttu-id="e83cb-113">حدد **إدارة الأصول** \> **إعداد** \> **مستندات الأصول**.</span><span class="sxs-lookup"><span data-stu-id="e83cb-113">Select **Asset management** \> **Setup** \> **Asset documents**.</span></span>
2. <span data-ttu-id="e83cb-114">حدد **جديد** لإنشاء سجل مستند الأصل.</span><span class="sxs-lookup"><span data-stu-id="e83cb-114">Select **New** to create an asset document record.</span></span>
3. <span data-ttu-id="e83cb-115">وفقًا لمستوى التحديد المطلوب لعلاقة المستند، قم بإجراء تحديدات ذات صلة في حقل أو أكثر من الحقول التالية: **نوع الأصل** و **الشركة المصنعة** و **النموذج‏‎** و **الأصل‏‎** و **فئة نوع المهمة** و **نوع المهمة** و **متغير نوع المهمة** و **متطلبات المهمة‬**.</span><span class="sxs-lookup"><span data-stu-id="e83cb-115">Depending on how specific you want the document relation to be, make relevant selections in one or more of the following fields: **Asset type**, **Manufacturer**, **Model**, **Asset**, **Job type category**, **Job type**, **Job type variant**, and **Job requirement**.</span></span> <span data-ttu-id="e83cb-116">تعتمد الخيارات المتوفرة في الحقلين **متغير نوع المهمة** و **متطلبات المهمة** على تحديدك في حقل **نوع المهمة**.</span><span class="sxs-lookup"><span data-stu-id="e83cb-116">The options that are available in the **Job type variant** and **Job requirement** fields depend on your selection in the **Job type** field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e83cb-117">عندما يبحث النظام عن مستندات يجب أن تكون ذات صلة بأصل أو أمر عمل، تقوم "إدارة الأصول" بمراجعة كافة سجلات مستندات الأصول للتحقق من وجود تطابق محتمل.</span><span class="sxs-lookup"><span data-stu-id="e83cb-117">When the system searches for documents that should be related to an asset or a work order, Asset Management goes through all asset document records to check for a possible match.</span></span> <span data-ttu-id="e83cb-118">وهي تتحقق دائمًا من المجموعة الأكثر تحديدًا أولاً.</span><span class="sxs-lookup"><span data-stu-id="e83cb-118">It always checks the most specific combination first.</span></span> <span data-ttu-id="e83cb-119">وبعبارة أخرى، تقوم إدارة الأصول أولاً بالتحقق من تطابق في حقل **متطلبات المهمة** .</span><span class="sxs-lookup"><span data-stu-id="e83cb-119">In other words, Asset Management first checks for a match for the **Job requirement** field.</span></span> <span data-ttu-id="e83cb-120">إذا لم يتم العثور على تطابق، فهي تتحقق من وجود تطابق لحقل **متغير نوع المهمة**.</span><span class="sxs-lookup"><span data-stu-id="e83cb-120">If no match is found, it checks for a match for the **Job type variant** field.</span></span> <span data-ttu-id="e83cb-121">إذا لم يتم العثور على تطابق، فهي تتحقق من وجود تطابق لحقل **نوع المهمة**.</span><span class="sxs-lookup"><span data-stu-id="e83cb-121">If no match is found, it checks for a match for the **Job type** field, and so on.</span></span> <span data-ttu-id="e83cb-122">كما ترى في تخطيط الصفحة **مستندات الأصول**، يعني هذا السلوك أنه، للعثور على المجموعة الأكثر تحديدًا، تقوم إدارة الأصول بالتحقق من كل سجل من اليسار إلى اليمين للحصول على تطابق.</span><span class="sxs-lookup"><span data-stu-id="e83cb-122">As you can see in the layout of the **Asset documents** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="e83cb-123">قد تكون عدة مستندات ذات صلة بأصل أو أمر عمل.</span><span class="sxs-lookup"><span data-stu-id="e83cb-123">Several documents might be related to an asset or a work order.</span></span> <span data-ttu-id="e83cb-124">يمكنك تحرير مستوى الخدمة على طلب صيانة أو أمر عمل كما تحتاج.</span><span class="sxs-lookup"><span data-stu-id="e83cb-124">You can edit the service level on a maintenance request or a work order as you require.</span></span>

4. <span data-ttu-id="e83cb-125">حدد **المرفقات**.</span><span class="sxs-lookup"><span data-stu-id="e83cb-125">Select **Attachments**.</span></span> <span data-ttu-id="e83cb-126">تظهر صفحة **مُعالجة المستندات** القياسية.</span><span class="sxs-lookup"><span data-stu-id="e83cb-126">The standard **Document handling** page appears.</span></span>
5. <span data-ttu-id="e83cb-127">قم بإعداد المستندات أو الملاحظات التي يجب إرفاقها بسجل مستند الأصل.</span><span class="sxs-lookup"><span data-stu-id="e83cb-127">Set up the documents or notes that should be attached to the asset document record.</span></span> <span data-ttu-id="e83cb-128">بعد إرفاق المستندات، يعرض حقل **المرفقات** عدد المستندات المرتبطة بالسجل.</span><span class="sxs-lookup"><span data-stu-id="e83cb-128">After you attach documents, the **Attachments** field shows the number of documents that are related to the record.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]