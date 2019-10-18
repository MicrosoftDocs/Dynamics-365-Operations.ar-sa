---
title: إدخال بيانات مقدم الطلب والطلب يدوياً
description: يوضح هذا الإجراء كيفية الاحتفاظ بمعلومات عن مقدمي الطلبات واستمارات تقديم طلباتهم.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea61e3c1d76ade6e0d694b4b521e4be76fc8799d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176329"
---
# <a name="enter-applicant-and-application-data-manually"></a><span data-ttu-id="e179a-103">إدخال بيانات مقدم الطلب والطلب يدوياً</span><span class="sxs-lookup"><span data-stu-id="e179a-103">Enter applicant and application data manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e179a-104">يوضح هذا الإجراء كيفية الاحتفاظ بمعلومات عن مقدمي الطلبات واستمارات تقديم طلباتهم.</span><span class="sxs-lookup"><span data-stu-id="e179a-104">This procedure shows how to manually maintain information about applicants and their application.</span></span>   <span data-ttu-id="e179a-105">يمكنك إدخال المعلومات الشخصية وتواريخ وأوقات إجراء المقابلات والمراجع والاختصاصات وطلبات الإقامة لمقدمي الطلبات، كما يمكنك المحافظة على كل هذه المعطيات.</span><span class="sxs-lookup"><span data-stu-id="e179a-105">You can enter and maintain personal information, interview dates and times, references, competencies, and accommodation requests for applicants.</span></span> <span data-ttu-id="e179a-106">ويمكنك أيضًا تحديث حالة استمارة تقديم طلبات التوظيف لمقدمي الطلبات وإنشاء رسائل خطية أو رسائل بريد إلكتروني للتواصل مع مقدمي الطلبات.</span><span class="sxs-lookup"><span data-stu-id="e179a-106">You can also update the status of applicants’ applications for employment and create letters or email messages to communicate with applicants.</span></span> <span data-ttu-id="e179a-107">عند إنشاء سجل لمقدم طلب، يتم إنشاء سجل شخص لمقدم الطلب هذا في دفتر العناوين العمومي.</span><span class="sxs-lookup"><span data-stu-id="e179a-107">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span>       <span data-ttu-id="e179a-108">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="e179a-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-new-applicant-record"></a><span data-ttu-id="e179a-109">إنشاء سجل مقدم طلب جديد</span><span class="sxs-lookup"><span data-stu-id="e179a-109">Create a new applicant record</span></span>
1. <span data-ttu-id="e179a-110">انتقل إلى الموارد البشرية > التوظيف ‬> مقدمو الطلبات‬ > مقدمو الطلبات‬‬.</span><span class="sxs-lookup"><span data-stu-id="e179a-110">Go to Human resources > Recruitment > Applicants > Applicants.</span></span>
2. <span data-ttu-id="e179a-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e179a-111">Click New.</span></span>
3. <span data-ttu-id="e179a-112">في الحقل "الاسم الأول"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e179a-112">In the First name field, type a value.</span></span>
4. <span data-ttu-id="e179a-113">في الحقل "اسم العائلة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e179a-113">In the Last name field, type a value.</span></span>
    * <span data-ttu-id="e179a-114">يمكنك إدخال معلومات إضافية حول مقدم الطلب، إذا كانت متوفرة.</span><span class="sxs-lookup"><span data-stu-id="e179a-114">You can enter additional applicant information if it's available.</span></span> <span data-ttu-id="e179a-115">على سبيل المثال، يمكن تضمين معلومات مثل أعلى درجة حصل عليها مقدم الطلب أو المسمى الوظيفي الحالي أو صاحب العمل السابق.</span><span class="sxs-lookup"><span data-stu-id="e179a-115">For example, information can include the applicant's highest degree, current job title, or previous employer.</span></span>  
5. <span data-ttu-id="e179a-116">بدّل توسيع المقطع "معلومات الاتصال‬‬".</span><span class="sxs-lookup"><span data-stu-id="e179a-116">Toggle the expansion of the Contact information section.</span></span>
6. <span data-ttu-id="e179a-117">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="e179a-117">Click Add.</span></span>
7. <span data-ttu-id="e179a-118">في حقل "الوصف"، اكتب "بريد إلكتروني للمراسلات".</span><span class="sxs-lookup"><span data-stu-id="e179a-118">In the Description field, type 'Communications email'.</span></span>
8. <span data-ttu-id="e179a-119">في الحقل "النوع"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="e179a-119">In the Type field, select an option.</span></span>
9. <span data-ttu-id="e179a-120">في الحقل "‏‫رقم/عنوان جهة الاتصال‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e179a-120">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="e179a-121">سيتم استخدام عنوان البريد الإلكتروني هذا لإنشاء اتصالات البريد الإلكتروني مع مقدم الطلب.</span><span class="sxs-lookup"><span data-stu-id="e179a-121">This email address will be used to generate email communication with the applicant.</span></span>  
10. <span data-ttu-id="e179a-122">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="e179a-122">Click Add.</span></span>
11. <span data-ttu-id="e179a-123">في وصف الحقل، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e179a-123">In the Description field, type a value.</span></span>
12. <span data-ttu-id="e179a-124">في الحقل "‏‫رقم/عنوان جهة الاتصال‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="e179a-124">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="e179a-125">حرر المعلومات الشخصية لمقدم الطلب.</span><span class="sxs-lookup"><span data-stu-id="e179a-125">Applicant personal information.</span></span>  
    * <span data-ttu-id="e179a-126">يمكنك إدخال معلومات إضافية شخصية لمقدم الطلب، إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="e179a-126">You can enter additional personal information for the applicant, if needed.</span></span> <span data-ttu-id="e179a-127">على سبيل المثال، قد تتضمن هذه المعلومات تاريخ الميلاد أو الأصل العرقي أو نوع الجنس أو الحالة الاجتماعية.</span><span class="sxs-lookup"><span data-stu-id="e179a-127">For example, this can include birth date, ethnic origin, gender, or marital status.</span></span>  
13. <span data-ttu-id="e179a-128">في جزء الإجراءات، انقر فوق "الاختصاصات‬".</span><span class="sxs-lookup"><span data-stu-id="e179a-128">On the Action Pane, click Competencies.</span></span>
    * <span data-ttu-id="e179a-129">يمكنك إدخال ملف تعريف اختصاصات مقدم الطلب، بما في ذلك المهارات أو الخبرات المهنية أو التعليم أو الاختبارات أو الشهادات.</span><span class="sxs-lookup"><span data-stu-id="e179a-129">You can enter the applicant's competency profile, including their skills, professional experiences, education, tests, or certificates.</span></span>  
    * <span data-ttu-id="e179a-130">يمكن استخدام هذه المعلومات لتعيين مهارات مقدم الطلب إلى المهارات المرتبطة بالوظائف المحددة في البيانات الخاصة بشركتك.</span><span class="sxs-lookup"><span data-stu-id="e179a-130">This information can be used to map the applicant's skills to the skills associated with the jobs defined in your company's data.</span></span>   

## <a name="create-an-application-for-the-applicant"></a><span data-ttu-id="e179a-131">إنشاء استمارة تقديم لمقدم الطلب</span><span class="sxs-lookup"><span data-stu-id="e179a-131">Create an application for the applicant</span></span>
1. <span data-ttu-id="e179a-132">انقر فوق "استمارات التقديم".</span><span class="sxs-lookup"><span data-stu-id="e179a-132">Click Applications.</span></span>
2. <span data-ttu-id="e179a-133">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="e179a-133">Click New.</span></span>
3. <span data-ttu-id="e179a-134">في الحقل "مشروع التعيين"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="e179a-134">In the Recruitment project field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e179a-135">عن طريق تحديد مشروع تعيين، سيتم ربط مقدم الطلب بفرصة عمل محددة مضمنة في مشروع التعيين هذا.</span><span class="sxs-lookup"><span data-stu-id="e179a-135">By selecting a recruitment project, the applicant will be associated with a specific opening included in that recruitment project.</span></span>  
4. <span data-ttu-id="e179a-136">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="e179a-136">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e179a-137">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="e179a-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e179a-138">بشكل افتراضي، تستند الوظيفة والقسم إلى مشروع التعيين المحدد.</span><span class="sxs-lookup"><span data-stu-id="e179a-138">By default, the job and department are based on the selected recruitment project.</span></span>  
6. <span data-ttu-id="e179a-139">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="e179a-139">Click Save.</span></span>
    * <span data-ttu-id="e179a-140">بعد حفظ استمارة التقديم، يمكنك إرفاق مستندات بها، بما في ذلك خبرة مقدم الطلب والمكافآت التي حصل عليها ورسالة غلاف.</span><span class="sxs-lookup"><span data-stu-id="e179a-140">After saving the application, you can attach documents to it, including the applicant's experience, awards, and cover letter.</span></span>  

