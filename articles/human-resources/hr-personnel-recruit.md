---
title: تعيين المرشحين للوظائف
description: يوضح هذا الموضوع كيفية توظيف المرشحين في Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9a35abcb8a2f6aa8031c8d84a44c2a8ad93883ac
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669151"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="e320f-103">تعيين المرشحين للوظائف</span><span class="sxs-lookup"><span data-stu-id="e320f-103">Recruit job candidates</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="e320f-104">يساعدك Dynamics 365 Human Resources في إدارة طلبات التعيين.</span><span class="sxs-lookup"><span data-stu-id="e320f-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="e320f-105">كما أنه يساعدك على تحويل المرشحين للوظائف بسلاسة إلى موظفين.</span><span class="sxs-lookup"><span data-stu-id="e320f-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="e320f-106">إذا كانت مؤسستك تستخدم تطبيق تعيين منفصل، فقد تتضمن عملية التعيين الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="e320f-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="e320f-107">أدخل طلب التعيين الخاص بك في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e320f-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="e320f-108">قم بتلقي إحالات المرشحين في Human Resources من تطبيق التعيين.</span><span class="sxs-lookup"><span data-stu-id="e320f-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="e320f-109">أكمل عملية الموافقة على الترشيح في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e320f-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="e320f-110">إذا كنت لا تستخدم طلب تعيين منفصلاً، يمكنك أيضًا إدارة المرشحين في Human Resources يدويًا.</span><span class="sxs-lookup"><span data-stu-id="e320f-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="e320f-111">إذا كنت مسؤولاً أو مطورًا وترغب في دمج Human Resources مع تطبيق تعيين تابع لجهة خارجية، فراجع [تكوين تكامل Common Data Service](hr-admin-integration-common-data-service.md) و[تكوين الكيانات الظاهرية لـ Common Data Service](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="e320f-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md) and [Configure Common Data Service virtual entities](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="e320f-112">يمكنك أيضًا العثور على تطبيقات تكامل التعيين في [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="e320f-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="e320f-113">لتجربة ميزة المعاينة الخاصة بنا للتكامل مع LinkedIn Talent Hub، راجع [التكامل مع LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="e320f-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="e320f-114">تمكين طلبات التعيين</span><span class="sxs-lookup"><span data-stu-id="e320f-114">Enable recruiting requests</span></span>

<span data-ttu-id="e320f-115">إذا كنت ترغب في إرسال طلبات التعيين في Human Resources، فيجب عليك أولاً تمكين الوظيفة في **معلمات Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="e320f-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources parameters**.</span></span>

1. <span data-ttu-id="e320f-116">في مساحة عمل **إدارة العاملين**، حدد **ارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="e320f-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="e320f-117">ضمن **الإعداد**، حدد **محددات الموارد البشرية**.</span><span class="sxs-lookup"><span data-stu-id="e320f-117">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="e320f-118">في علامة التبويب **عام**، ضمن **التعيين**، قم بتعيين **تمكين طلبات التعيين** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="e320f-118">On the **General** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

   ![تمكين طلبات التعيين](./media/hr-recruit-0-enable-requests.png)

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="e320f-120">إضافة موقع طلب تعيين</span><span class="sxs-lookup"><span data-stu-id="e320f-120">Add a recruiting request location</span></span>

<span data-ttu-id="e320f-121">إذا كان لمؤسستك مواقع متعددة، فيمكنك إضافتها حتى يتمكن مقدمو الطلبات من تحديد موقع يعمل فيه المعين الجديد.</span><span class="sxs-lookup"><span data-stu-id="e320f-121">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="e320f-122">سيتم تضمين الموقع في عملية ترحيل الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="e320f-122">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="e320f-123">في شريط البحث، أدخل **موقع طلب التعيين**.</span><span class="sxs-lookup"><span data-stu-id="e320f-123">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="e320f-124">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e320f-124">Select **New**.</span></span>

3. <span data-ttu-id="e320f-125">في حقل **موقع طلب التعيين**، أدخل اسم الموقع.</span><span class="sxs-lookup"><span data-stu-id="e320f-125">In the **Recruiting request location** field, enter the location name.</span></span>

   ![إضافة موقع طلب تعيين](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="e320f-127">في **الوصف**، أدخل وصفًا للموقع.</span><span class="sxs-lookup"><span data-stu-id="e320f-127">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="e320f-128">ضمن **الموقع**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="e320f-128">Under **Location**, select **Add**.</span></span> <span data-ttu-id="e320f-129">إذا ظهرت النافذة المنبثقة **العنوان الجديد**، فأدخل عنوان الموقع.</span><span class="sxs-lookup"><span data-stu-id="e320f-129">If the **New address** popout appears, enter the address for the location.</span></span>

   ![إدخال العنوان](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="e320f-131">ضمن **معلومات جهة الاتصال**، أدخل المعلومات الخاصة بجهة اتصال الموقع.</span><span class="sxs-lookup"><span data-stu-id="e320f-131">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="e320f-132">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e320f-132">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="e320f-133">إضافة طلب تعيين</span><span class="sxs-lookup"><span data-stu-id="e320f-133">Add a recruiting request</span></span>

<span data-ttu-id="e320f-134">يستطيع المديرون إرسال طلبات التعيين في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e320f-134">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="e320f-135">إذا كنت تستخدم طلب تعيين منفصلاً، فإن إكمال هذه الخطوات سيرسل طلب توظيف ويبدأ عملية التوظيف في هذا التطبيق.</span><span class="sxs-lookup"><span data-stu-id="e320f-135">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="e320f-136">وبخلاف ذلك، أكمل هذا الإجراء لبدء سير العمل لعملية التوظيف الداخلية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="e320f-136">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="e320f-137">حدد **الخدمة الذاتية للموظف**.</span><span class="sxs-lookup"><span data-stu-id="e320f-137">Select **Employee self service**.</span></span>

2. <span data-ttu-id="e320f-138">حدد علامة التبويب **فريقي**.</span><span class="sxs-lookup"><span data-stu-id="e320f-138">Select the **My team** tab.</span></span>

3. <span data-ttu-id="e320f-139">حدد **طلب للتعيين**.</span><span class="sxs-lookup"><span data-stu-id="e320f-139">Select  **Request to recruit**.</span></span>

   ![بدء طلب تعيين](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="e320f-141">أكمل حقل **الوصف**، و **الوظيفة**، و **تاريخ البدء المقدر**.</span><span class="sxs-lookup"><span data-stu-id="e320f-141">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![إكمال طلب التعيين](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="e320f-143">حدد **متابعة**.</span><span class="sxs-lookup"><span data-stu-id="e320f-143">Select **Continue**.</span></span> <span data-ttu-id="e320f-144">يظهر طلب التعيين للمنصب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="e320f-144">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="e320f-145">ضمن **عام**، حدد أحد المسؤولين عن التعيين من القائمة المنسدلة **مسؤول التعيين**، ثم حدد موقعًا من القائمة المنسدلة **موقع طلب التعيين**.</span><span class="sxs-lookup"><span data-stu-id="e320f-145">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="e320f-146">ضمن **الوظيفة**، قم بتغيير أي معلومات حسب الحاجة، ثم حدد **إنشاء تفاصيل من الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="e320f-146">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![إنشاء تفاصيل من الوظيفة](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="e320f-148">ستتم تعبئة بقية طلب التعيين بالمعلومات الافتراضية للوظيفة التي أدخلتها.</span><span class="sxs-lookup"><span data-stu-id="e320f-148">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="e320f-149">ضمن **الوصف الخارجي**، أدخل وصفًا خارجيًا للوظيفة.</span><span class="sxs-lookup"><span data-stu-id="e320f-149">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="e320f-150">ضمن **المناصب**، حدد **إضافة**، ثم حدد منصبًا لطلب التعيين هذا.</span><span class="sxs-lookup"><span data-stu-id="e320f-150">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![إضافة منصب](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="e320f-152">ضمن **المهارات**، حدد **إضافة**، ثم حدد مهارة.</span><span class="sxs-lookup"><span data-stu-id="e320f-152">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="e320f-153">ضمن **المتطلبات التعليمية**، حدد **إضافة**، ثم حدد القيم من القائمتين المنسدلتين **التعليم** و **مستوى التعليم**.</span><span class="sxs-lookup"><span data-stu-id="e320f-153">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![إضافة المتطلبات التعليمية](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="e320f-155">ضمن **التعليق**، أضف التعليقات عند الضرورة.</span><span class="sxs-lookup"><span data-stu-id="e320f-155">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="e320f-156">ضمن **التعويض**، حدد مستوى من القائمة المنسدلة **المستوى**، ثم اضبط **الحد الأدنى** و **نقطة التحكم** و **الحد الأقصى** حسب الضرورة.</span><span class="sxs-lookup"><span data-stu-id="e320f-156">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="e320f-157">عندما يكتمل طلب التعيين وأصبحت مستعدًا لبدء عملية التعيين، حدد **تنشيط** في شريط القوائم.</span><span class="sxs-lookup"><span data-stu-id="e320f-157">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![تنشيط طلب التعيين](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="e320f-159">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e320f-159">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="e320f-160">عرض طلبات التعيين الخاص بك وتحريرها</span><span class="sxs-lookup"><span data-stu-id="e320f-160">View and edit your recruiting requests</span></span>

<span data-ttu-id="e320f-161">إذا كنت مديرًا وترغب في عرض طلباتك الخاصة:</span><span class="sxs-lookup"><span data-stu-id="e320f-161">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="e320f-162">حدد **الخدمة الذاتية للموظف**.</span><span class="sxs-lookup"><span data-stu-id="e320f-162">Select **Employee self service**.</span></span>

2. <span data-ttu-id="e320f-163">حدد علامة التبويب **فريقي**.</span><span class="sxs-lookup"><span data-stu-id="e320f-163">Select the **My team** tab.</span></span>

3. <span data-ttu-id="e320f-164">ضمن **معلومات فريقي**، حدد علامة التبويب **طلبات التعيين**.</span><span class="sxs-lookup"><span data-stu-id="e320f-164">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![علامة التبويب تحديد طلبات التعيين](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="e320f-166">لعرض طلب تعيين أو تحريره، حدده في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e320f-166">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="e320f-167">إذا كنت أخصائي موارد بشرية وترغب في عرض جميع طلبات التعيين:</span><span class="sxs-lookup"><span data-stu-id="e320f-167">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="e320f-168">حدد **إدارة العاملين**.</span><span class="sxs-lookup"><span data-stu-id="e320f-168">Select **Personnel management**.</span></span>

2. <span data-ttu-id="e320f-169">حدد **طلبات التعيين**.</span><span class="sxs-lookup"><span data-stu-id="e320f-169">Select **Recruiting requests**.</span></span>

   ![عرض طلبات التعيين في إدارة العاملين](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="e320f-171">لعرض طلب تعيين أو تحريره، حدده في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="e320f-171">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="e320f-172">إضافة ملف تعريف مرشح أو تحريره</span><span class="sxs-lookup"><span data-stu-id="e320f-172">Add or edit a candidate profile</span></span>

<span data-ttu-id="e320f-173">إذا تم دمج مؤسستك مع تطبيق آخر لإدارة طلبات التعيين، فستتم إعادة توجيه طلبات التعيين إلى هذا التطبيق.</span><span class="sxs-lookup"><span data-stu-id="e320f-173">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="e320f-174">يقوم طلب التعيين بعد ذلك بإرسال معلومات المرشح إلى Human Resources.</span><span class="sxs-lookup"><span data-stu-id="e320f-174">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="e320f-175">وبخلاف ذلك، يمكنك متابعة عمليات التعيين الداخلية الخاصة بك وإدخال معلومات المرشح يدويًا.</span><span class="sxs-lookup"><span data-stu-id="e320f-175">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="e320f-176">حدد **إدارة العاملين**.</span><span class="sxs-lookup"><span data-stu-id="e320f-176">Select **Personnel management**.</span></span>

2. <span data-ttu-id="e320f-177">حدد **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="e320f-177">Select **Links**.</span></span>

3. <span data-ttu-id="e320f-178">ضمن **التعيين**، حدد **المرشحين**.</span><span class="sxs-lookup"><span data-stu-id="e320f-178">Under **Recruiting**, select **Candidates**.</span></span>

   ![عرض المرشحين](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="e320f-180">لإضافة مرشح، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="e320f-180">To add a candidate, select **New**.</span></span> <span data-ttu-id="e320f-181">لتحرير مرشح موجود، حدد المرشح من القائمة ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="e320f-181">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="e320f-182">يظهر ملف تعريف المرشح.</span><span class="sxs-lookup"><span data-stu-id="e320f-182">The candidate profile appears.</span></span>

5. <span data-ttu-id="e320f-183">ضمن **ملخص المرشح**، قم بإدخال أو تحرير معلومات المرشح عند الضرورة.</span><span class="sxs-lookup"><span data-stu-id="e320f-183">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="e320f-184">ضمن **طلب التعيين**، حدد طلب تعيين لربط المرشح به.</span><span class="sxs-lookup"><span data-stu-id="e320f-184">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="e320f-185">أكمل بعد ذلك حقول **تاريخ البدء المقدر** و **مدير التعيين** و **المنصب** و **الوصف** حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="e320f-185">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![الربط بطلب تعيين](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="e320f-187">أكمل جميع المعلومات في المجالات التالية التي تريد تضمينها في سجل المرشح:</span><span class="sxs-lookup"><span data-stu-id="e320f-187">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="e320f-188">**التعليقات**</span><span class="sxs-lookup"><span data-stu-id="e320f-188">**Comments**</span></span>
   - <span data-ttu-id="e320f-189">**الخبرة المهنية**</span><span class="sxs-lookup"><span data-stu-id="e320f-189">**Professional experience**</span></span>
   - <span data-ttu-id="e320f-190">**معلومات جهة الاتصال**</span><span class="sxs-lookup"><span data-stu-id="e320f-190">**Contact information**</span></span>
   - <span data-ttu-id="e320f-191">**التعليم**</span><span class="sxs-lookup"><span data-stu-id="e320f-191">**Education**</span></span>
   - <span data-ttu-id="e320f-192">**المهارات**</span><span class="sxs-lookup"><span data-stu-id="e320f-192">**Skills**</span></span>
   - <span data-ttu-id="e320f-193">**الشهادات**</span><span class="sxs-lookup"><span data-stu-id="e320f-193">**Certificates**</span></span>
   - <span data-ttu-id="e320f-194">**عمليات مراقبة**</span><span class="sxs-lookup"><span data-stu-id="e320f-194">**Screenings**</span></span>

8. <span data-ttu-id="e320f-195">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="e320f-195">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="e320f-196">تعيين مرشح</span><span class="sxs-lookup"><span data-stu-id="e320f-196">Hire a candidate</span></span>

<span data-ttu-id="e320f-197">عندما تكون مستعدًا لتعيين مرشح، اتبع هذا الإجراء لتحويل المرشح إلى موظف.</span><span class="sxs-lookup"><span data-stu-id="e320f-197">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="e320f-198">في نموذج المرشح، حدد **تعيين**.</span><span class="sxs-lookup"><span data-stu-id="e320f-198">On the candidate form, select **Hire**.</span></span>

   ![تعيين مرشح](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="e320f-200">في نموذج **تعيين عامل جديد**، ضمن **التفاصيل**، أكمل جميع الحقول.</span><span class="sxs-lookup"><span data-stu-id="e320f-200">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![إدخال تفاصيل التعيين الجديد](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="e320f-202">ضمن **تفاصيل المنصب**، تحقق من المعلومات وقم بتغييرها إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="e320f-202">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="e320f-203">ضمن **قوائم اختيار الإعداد**، حدد قوائم اختيار الإعداد ذات الصلة لهذا الموظف.</span><span class="sxs-lookup"><span data-stu-id="e320f-203">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="e320f-204">حدد **متابعة** لإنشاء سجل الموظف.</span><span class="sxs-lookup"><span data-stu-id="e320f-204">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="e320f-205">وفقًا لمهام سير العمل في مؤسستك، قد يمر سجل المرشح بخطوات موافقة إضافية قبل أن يصبح سجل موظف.</span><span class="sxs-lookup"><span data-stu-id="e320f-205">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="e320f-206">اتخاذ قرار بعدم تعيين مرشح</span><span class="sxs-lookup"><span data-stu-id="e320f-206">Decide not to hire a candidate</span></span>

<span data-ttu-id="e320f-207">إذا قررت عدم تعيين مرشح، فاتبع هذا الإجراء لإزالته من عملية التدقيق.</span><span class="sxs-lookup"><span data-stu-id="e320f-207">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="e320f-208">في نموذج المرشح، حدد **عدم التعيين**.</span><span class="sxs-lookup"><span data-stu-id="e320f-208">On the candidate form, select **Do not hire**.</span></span>

   ![عدم تعيين المرشح](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="e320f-210">حدد **كود السبب** وقم بتضمين أي تعليقات.</span><span class="sxs-lookup"><span data-stu-id="e320f-210">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="e320f-211">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="e320f-211">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="e320f-212">استبعاد مرشح</span><span class="sxs-lookup"><span data-stu-id="e320f-212">Dismiss a candidate</span></span>

<span data-ttu-id="e320f-213">إذا لزم الأمر، يمكنك استبعاد المرشح بعد تعيينه.</span><span class="sxs-lookup"><span data-stu-id="e320f-213">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="e320f-214">على سبيل المثال، قد يرفض المرشح عرضك أو لا يظهر في يومه الأول.</span><span class="sxs-lookup"><span data-stu-id="e320f-214">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="e320f-215">في نموذج المرشح، حدد **استبعاد مرشح**.</span><span class="sxs-lookup"><span data-stu-id="e320f-215">On the candidate form, select **Dismiss candidate**.</span></span>

  ![استبعاد المرشح](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="e320f-217">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="e320f-217">See also</span></span>

[<span data-ttu-id="e320f-218">تكوين كيانات Common Data Service الظاهرية</span><span class="sxs-lookup"><span data-stu-id="e320f-218">Configure Common Data Service virtual entities</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="e320f-219">تنظيم القوى العاملة</span><span class="sxs-lookup"><span data-stu-id="e320f-219">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="e320f-220">إعداد مكونات وظيفة</span><span class="sxs-lookup"><span data-stu-id="e320f-220">Set up the components of a job</span></span>](hr-personnel-jobs.md)