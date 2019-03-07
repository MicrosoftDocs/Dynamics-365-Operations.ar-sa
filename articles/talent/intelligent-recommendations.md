---
title: التوصيات الذكية
description: يشرح هذا الموضوع كيف يمكن استخدام التعلم الآلي‬ لتوفير توصيات تتعلق بالوظائف والمرشحين لها.
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: c6225a311f5ba0b65b45092a1f626b9d6aff3f5e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "303111"
---
# <a name="intelligent-recommendations"></a><span data-ttu-id="19599-103">التوصيات الذكية</span><span class="sxs-lookup"><span data-stu-id="19599-103">Intelligent recommendations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="19599-104">بإمكان التعلم الآلي أن يساعد مسؤولي التعيين ومدراء التوظيف على التعرف بسرعة على أفضل المرشحين لأحد المناصب.</span><span class="sxs-lookup"><span data-stu-id="19599-104">Machine learning can help recruiters and hiring managers quickly identify top candidates for a position.</span></span> <span data-ttu-id="19599-105">وبإمكانه أيضًا أن يساعد الموظفين المحتملين في العثور على المنصب الأكثر ملاءمة لملف تعريفهم واهتماماتهم.</span><span class="sxs-lookup"><span data-stu-id="19599-105">It can also help prospects find the position that best suits their profile and interests.</span></span> <span data-ttu-id="19599-106">ومع استخدام هذه الميزات وتوفير الملاحظات، ستتحسن التوصيات.</span><span class="sxs-lookup"><span data-stu-id="19599-106">As these features are used, and feedback is provided, recommendations will improve.</span></span>

> [!NOTE] 
> - <span data-ttu-id="19599-107">تتوفر ميزة التوصيات الذكية فقط مع المكون الإضافي Comprehensive Hiring.</span><span class="sxs-lookup"><span data-stu-id="19599-107">The intelligent recommendation features are available only with the Comprehensive hiring add-on.</span></span>
> - <span data-ttu-id="19599-108">لتمكين ميزات توصيات المرشحين والوظائف، يجب على المسؤول تشغيل خيارات المعاينة لها.</span><span class="sxs-lookup"><span data-stu-id="19599-108">To enable the candidate and job recommendation features, an admin must turn on the preview options for them.</span></span> <span data-ttu-id="19599-109">في مركز الإدارة، على علامة التبويب **إدارة الميزات**، تأكد من تعيين الخيار **ميزات المعاينة** إلى **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="19599-109">In the Admin center, on the **Feature management** tab, make sure that the **Preview features** option is set to **On**.</span></span> <span data-ttu-id="19599-110">ثم تأكد من تعيين الخيارين **توصيات المرشحين** و **توصيات الوظائف** إلى **تشغيل**.</span><span class="sxs-lookup"><span data-stu-id="19599-110">Then make sure that the individual **Candidate recommendation** and **Job recommendation** options are set to **On**.</span></span>

## <a name="candidate-recommendations"></a><span data-ttu-id="19599-111">توصيات المرشحين</span><span class="sxs-lookup"><span data-stu-id="19599-111">Candidate recommendations</span></span>

<span data-ttu-id="19599-112">بما أن إعلانات الوظائف قد تجذب عددًا كبيرًا من مقدمي الطلبات، قد يكون من الصعب على مسؤولي التعيين ومدراء التوظيف العثور على المرشحين من ذوي المهارات والخلفيات الأكثر ملاءمة للمنصب الشاغر.</span><span class="sxs-lookup"><span data-stu-id="19599-112">Because job postings might attract hundreds of applicants, it can be difficult for recruiters and hiring managers to find the candidates whose skills and background best match the position.</span></span> <span data-ttu-id="19599-113">من خلال تحليل الرابط بين وصف الوظيفة ومتطلباتها من جهة والبيانات من السير الذاتية وملفات تعريف المرشحين من جهة أخرى، يمكن استخدام التعلم الآلي‬ لإنتاج توصيات المرشحين.</span><span class="sxs-lookup"><span data-stu-id="19599-113">By analyzing the correlation between the job description and requirements, and data from the candidates' resumes and profiles, machine learning can be used to produce candidate recommendations.</span></span> <span data-ttu-id="19599-114">بإمكان توصيات المرشحين أن تساعد مسؤولي التعيين ومدراء التوظيف على التعرف على أفضل الواهب ونقلها إلى مرحلة المقابلة بشكل أسرع.</span><span class="sxs-lookup"><span data-stu-id="19599-114">Candidate recommendations can help recruiters and hiring managers identify the top talent and move them to the interview stage faster.</span></span> <span data-ttu-id="19599-115">بالنسبة إلى أي وظيفة، في حال وجود أكثر من عشرة مرشحين أو موظفين محتملين لديهم سير ذاتية أو ملفات تعريف مكتملة، تظهر أسماء المرشحين أو الموظفين المحتملين الأقرب إلى استيفاء متطلبات الوظيفة في القسم **مقدمو طلبات يجب أخذهم في الاعتبار** في صفحة **الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="19599-115">For any job, if there are more than ten candidates or prospects who have resumes or complete profiles, the candidates or prospects who most closely meet the job's requirements appear in the **Applicants to consider** section on the **Job** page.</span></span>

<span data-ttu-id="19599-116">بالنسبة إلى أي مرشح موصى به، يمكنك تحديد **عرض المرشح** على بطاقة المرشح لمراجعة ملف تعريفه واتخاذ الإجراء الملائم على استمارة التقديم.</span><span class="sxs-lookup"><span data-stu-id="19599-116">For any recommended candidate, you can select **View candidate** on the candidate card to review the candidate's profile and take action on his or her application.</span></span> <span data-ttu-id="19599-117">يمكنك استخدام زر علامة القطع (**...**) لفتح ملف تعريف المرشح على علامة تبويب جديدة. ويمكنك أيضًا استخدام زر علامة القطع لتوفير الملاحظات حول هذه التوصية.</span><span class="sxs-lookup"><span data-stu-id="19599-117">You can use the ellipsis button (**...**) to open the candidate's profile on a new tab. You can also use the ellipsis button to provide feedback about the recommendation.</span></span> <span data-ttu-id="19599-118">بهذه الطريقة، يمكنك المساعدة في تحسين أداء محرك التوصيات وتحسين التوصيات المستقبلية.</span><span class="sxs-lookup"><span data-stu-id="19599-118">In this way, you help fine-tune the recommendation engine and improve future recommendations.</span></span> <span data-ttu-id="19599-119">تتم إزالة أي توصيات لم تعجبك من القسم **مقدمو طلبات يجب أخذهم في الاعتبار** عند تحديث صفحة **الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="19599-119">Any recommendations that you don't like are removed from the **Applicants to consider** section when you refresh the **Job** page.</span></span> <span data-ttu-id="19599-120">يمكنك استخدام بطاقة الملاحظات للإشارة إلى السبب الذي جعلك تعتقد بأن التوصية غير مفيدة.</span><span class="sxs-lookup"><span data-stu-id="19599-120">You can use the feedback card to indicate why you didn't find the recommendation useful.</span></span>

## <a name="job-recommendations"></a><span data-ttu-id="19599-121">توصيات الوظائف</span><span class="sxs-lookup"><span data-stu-id="19599-121">Job recommendations</span></span> 

<span data-ttu-id="19599-122">عندما يستخدم موظف محتمل موقع الوظائف لتقديم طلب الحصول على وظيفة، تتم التوصية بالمناصب الأخرى المفتوحة في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="19599-122">When a prospective employee uses the career site to apply to a job, other open positions at the organization are recommended.</span></span> <span data-ttu-id="19599-123">وتستند هذه التوصيات إلى استمارات التقديم السابقة للموظف المحتمل، وإلى سيرته الذاتية أو ملف تعريف المرشح.</span><span class="sxs-lookup"><span data-stu-id="19599-123">These recommendations are based on the prospect's past applications, and on his or her resume or candidate profile.</span></span> <span data-ttu-id="19599-124">وبالتالي، بإمكان التوصيات أن تساعد الموظفين المحتملين على التعرّف بسرعة على الوظائف الأكثر ملاءمة لهم.</span><span class="sxs-lookup"><span data-stu-id="19599-124">Therefore, job recommendations help prospects quickly identify the jobs that are the best fit for them.</span></span> <span data-ttu-id="19599-125">يتم تقديم توصيات الوظائف للموظفين المتوقعين إذا تم نشر أكثر من عشر وظائف في موقع الوظائف.</span><span class="sxs-lookup"><span data-stu-id="19599-125">Job recommendations are provided to prospects if more than ten jobs are posted on the career site.</span></span> <span data-ttu-id="19599-126">بإمكان الموظفين المحتملين فتح تفاصيل إعلان الوظيفة من بطاقة التوصية.</span><span class="sxs-lookup"><span data-stu-id="19599-126">Prospects can open the details of a job posting from the recommendation card.</span></span> <span data-ttu-id="19599-127">ويمكنهم أيضًا توفير ملاحظات حول التوصية للمساعدة في تحسين التوصيات المستقبلية.</span><span class="sxs-lookup"><span data-stu-id="19599-127">They can also provide feedback about a recommendation to help improve future recommendations.</span></span>
