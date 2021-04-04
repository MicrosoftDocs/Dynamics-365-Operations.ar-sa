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
ms.openlocfilehash: 6aca285133495dfe023dfd18bdeb050aabcafee6
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478274"
---
# <a name="recruit-job-candidates"></a><span data-ttu-id="1fbb7-103">تعيين المرشحين للوظائف</span><span class="sxs-lookup"><span data-stu-id="1fbb7-103">Recruit job candidates</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="1fbb7-104">يساعدك Dynamics 365 Human Resources في إدارة طلبات التعيين.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-104">Dynamics 365 Human Resources helps you to manage recruiting requests.</span></span> <span data-ttu-id="1fbb7-105">كما أنه يساعدك على تحويل المرشحين للوظائف بسلاسة إلى موظفين.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-105">It also helps you seamlessly transition job candidates to employees.</span></span> <span data-ttu-id="1fbb7-106">إذا كانت مؤسستك تستخدم تطبيق تعيين منفصل، فقد تتضمن عملية التعيين الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="1fbb7-106">If your organization uses a separate recruiting application, your recruiting process might include the following steps:</span></span>

- <span data-ttu-id="1fbb7-107">أدخل طلب التعيين الخاص بك في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-107">Enter your recruiting request in Human Resources.</span></span>
- <span data-ttu-id="1fbb7-108">قم بتلقي إحالات المرشحين في Human Resources من تطبيق التعيين.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-108">Receive candidate referrals in Human Resources from the recruiting application.</span></span>
- <span data-ttu-id="1fbb7-109">أكمل عملية الموافقة على الترشيح في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-109">Complete the candidate approval process in Human Resources.</span></span>

<span data-ttu-id="1fbb7-110">إذا كنت لا تستخدم طلب تعيين منفصلاً، يمكنك أيضًا إدارة المرشحين في Human Resources يدويًا.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-110">If you aren't using a separate recruiting application, you can also manually manage candidates in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="1fbb7-111">إذا كنت مسؤولاً أو مطورًا وترغب في دمج Human Resources مع تطبيق تعيين تابع لجهة خارجية، فراجع [تكوين تكامل Dataverse](hr-admin-integration-common-data-service.md) و[تكوين الجداول الظاهرية لـ Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)</span><span class="sxs-lookup"><span data-stu-id="1fbb7-111">If you're an admin or developer and want to integrate Human Resources with a third-party recruiting application, see [Configure Dataverse integration](hr-admin-integration-common-data-service.md) and [Configure Dataverse virtual tables](hr-admin-integration-common-data-service-virtual-entities.md)</span></span>
>
> <span data-ttu-id="1fbb7-112">يمكنك أيضًا العثور على تطبيقات تكامل التعيين في [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span><span class="sxs-lookup"><span data-stu-id="1fbb7-112">You can also find recruiting integration apps on [AppSource](https://appsource.microsoft.com/marketplace/apps?search=recruiting%20dynamics).</span></span>
>
> <span data-ttu-id="1fbb7-113">لتجربة ميزة المعاينة الخاصة بنا للتكامل مع LinkedIn Talent Hub، راجع [التكامل مع LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span><span class="sxs-lookup"><span data-stu-id="1fbb7-113">To try out our preview feature for integrating with LinkedIn Talent Hub, see [Integrate with LinkedIn Talent Hub](hr-admin-integration-linkedin.md).</span></span>

## <a name="enable-recruiting-requests"></a><span data-ttu-id="1fbb7-114">تمكين طلبات التعيين</span><span class="sxs-lookup"><span data-stu-id="1fbb7-114">Enable recruiting requests</span></span>

<span data-ttu-id="1fbb7-115">إذا كنت ترغب في إرسال طلبات التعيين في Human Resources، فيجب عليك أولاً تمكين الوظيفة في **معلمات Human Resources المشتركة**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-115">If you want to submit recruiting requests in Human Resources, you must first enable the functionality in **Human resources shared parameters**.</span></span>

1. <span data-ttu-id="1fbb7-116">في مساحة عمل **إدارة العاملين**، حدد **ارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-116">In the **Personnel management** workspace, select **Links**.</span></span>

2. <span data-ttu-id="1fbb7-117">ضمن **الإعداد**، حدد **معلمات Human Resources المشتركة**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-117">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="1fbb7-118">في علامة التبويب **التوظيف**، ضمن **التعيين**، قم بتعيين **تمكين طلبات التعيين** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-118">On the **Recruitment** tab, under **RECRUITING**, set **Enable recruiting requests** to **Yes**.</span></span>

## <a name="add-a-recruiting-request-location"></a><span data-ttu-id="1fbb7-119">إضافة موقع طلب تعيين</span><span class="sxs-lookup"><span data-stu-id="1fbb7-119">Add a recruiting request location</span></span>

<span data-ttu-id="1fbb7-120">إذا كان لمؤسستك مواقع متعددة، فيمكنك إضافتها حتى يتمكن مقدمو الطلبات من تحديد موقع يعمل فيه المعين الجديد.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-120">If your organization has multiple locations, you can add them so requestors can select a location where the new recruit will be working.</span></span> <span data-ttu-id="1fbb7-121">سيتم تضمين الموقع في عملية ترحيل الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-121">The location will be included in the job posting.</span></span>

1. <span data-ttu-id="1fbb7-122">في شريط البحث، أدخل **موقع طلب التعيين**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-122">In the search bar, enter **recruiting request location**.</span></span>

2. <span data-ttu-id="1fbb7-123">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-123">Select **New**.</span></span>

3. <span data-ttu-id="1fbb7-124">في حقل **موقع طلب التعيين**، أدخل اسم الموقع.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-124">In the **Recruiting request location** field, enter the location name.</span></span>

   ![إضافة موقع طلب تعيين](./media/hr-recruit-0a-add-location.png)

4. <span data-ttu-id="1fbb7-126">في **الوصف**، أدخل وصفًا للموقع.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-126">In the **Description**, enter a description for the location.</span></span>

5. <span data-ttu-id="1fbb7-127">ضمن **الموقع**، حدد **إضافة**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-127">Under **Location**, select **Add**.</span></span> <span data-ttu-id="1fbb7-128">إذا ظهرت النافذة المنبثقة **العنوان الجديد**، فأدخل عنوان الموقع.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-128">If the **New address** popout appears, enter the address for the location.</span></span>

   ![إدخال العنوان](./media/hr-recruit-0b-address.png)

6. <span data-ttu-id="1fbb7-130">ضمن **معلومات جهة الاتصال**، أدخل المعلومات الخاصة بجهة اتصال الموقع.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-130">Under **Contact information**, enter the information for the location's contact.</span></span>

7. <span data-ttu-id="1fbb7-131">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-131">Select **Save**.</span></span>

## <a name="add-a-recruiting-request"></a><span data-ttu-id="1fbb7-132">إضافة طلب تعيين</span><span class="sxs-lookup"><span data-stu-id="1fbb7-132">Add a recruiting request</span></span>

<span data-ttu-id="1fbb7-133">يستطيع المديرون إرسال طلبات التعيين في Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-133">Managers can submit recruiting requests in Human Resources.</span></span> <span data-ttu-id="1fbb7-134">إذا كنت تستخدم طلب تعيين منفصلاً، فإن إكمال هذه الخطوات سيرسل طلب توظيف ويبدأ عملية التوظيف في هذا التطبيق.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-134">If you use a separate recruiting application, completing these steps will send a recruiting request and start the recruiting process in that application.</span></span> <span data-ttu-id="1fbb7-135">وبخلاف ذلك، أكمل هذا الإجراء لبدء سير العمل لعملية التوظيف الداخلية الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-135">Otherwise, complete this procedure to begin the workflow for your own internal recruiting process.</span></span>

1. <span data-ttu-id="1fbb7-136">حدد **الخدمة الذاتية للموظف**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-136">Select **Employee self service**.</span></span>

2. <span data-ttu-id="1fbb7-137">حدد علامة التبويب **فريقي**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-137">Select the **My team** tab.</span></span>

3. <span data-ttu-id="1fbb7-138">حدد **طلب للتعيين**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-138">Select  **Request to recruit**.</span></span>

   ![بدء طلب تعيين](./media/hr-recruit-1-request-to-recruit.png)

4. <span data-ttu-id="1fbb7-140">أكمل حقل **الوصف**، و **الوظيفة**، و **تاريخ البدء المقدر**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-140">Complete the **Description**, **Job**, and **Estimated start date** fields.</span></span>

   ![إكمال طلب التعيين](./media/hr-recruit-2-request-to-recruit.png)

5. <span data-ttu-id="1fbb7-142">حدد **متابعة**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-142">Select **Continue**.</span></span> <span data-ttu-id="1fbb7-143">يظهر طلب التعيين للمنصب الخاص بك.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-143">The recruiting request for your position appears.</span></span>

6. <span data-ttu-id="1fbb7-144">ضمن **عام**، حدد أحد المسؤولين عن التعيين من القائمة المنسدلة **مسؤول التعيين**، ثم حدد موقعًا من القائمة المنسدلة **موقع طلب التعيين**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-144">Under **General**, select a recruiter from the **Recruiter** dropdown, and then select a location from the **Recruiting request location** dropdown.</span></span>

7. <span data-ttu-id="1fbb7-145">ضمن **الوظيفة**، قم بتغيير أي معلومات حسب الحاجة، ثم حدد **إنشاء تفاصيل من الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-145">Under **Job**, change any information as needed, and then select **Create details from job**.</span></span>

   ![إنشاء تفاصيل من الوظيفة](./media/hr-recruit-3-create-details-from-job.png)

   <span data-ttu-id="1fbb7-147">ستتم تعبئة بقية طلب التعيين بالمعلومات الافتراضية للوظيفة التي أدخلتها.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-147">The rest of the recruiting request will populate with the default information for the job you entered.</span></span>

8. <span data-ttu-id="1fbb7-148">ضمن **الوصف الخارجي**، أدخل وصفًا خارجيًا للوظيفة.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-148">Under **External description**, enter an external-facing job description.</span></span>

9. <span data-ttu-id="1fbb7-149">ضمن **المناصب**، حدد **إضافة**، ثم حدد منصبًا لطلب التعيين هذا.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-149">Under **Positions**, select **Add**, and then select a position for this recruiting request.</span></span>

   ![إضافة منصب](./media/hr-recruit-4-select-position.png)

10. <span data-ttu-id="1fbb7-151">ضمن **المهارات**، حدد **إضافة**، ثم حدد مهارة.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-151">Under **Skills**, select **Add**, and then select a skill.</span></span>

11. <span data-ttu-id="1fbb7-152">ضمن **المتطلبات التعليمية**، حدد **إضافة**، ثم حدد القيم من القائمتين المنسدلتين **التعليم** و **مستوى التعليم**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-152">Under **Educational requirements**, select **Add**, and then select values from the **Education** and **Level of education** dropdowns.</span></span>

   ![إضافة المتطلبات التعليمية](./media/hr-recruit-5-select-educational-requirements.png)

12. <span data-ttu-id="1fbb7-154">ضمن **التعليق**، أضف التعليقات عند الضرورة.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-154">Under **Comment**, add comments as necessary.</span></span>

13. <span data-ttu-id="1fbb7-155">ضمن **التعويض**، حدد مستوى من القائمة المنسدلة **المستوى**، ثم اضبط **الحد الأدنى** و **نقطة التحكم** و **الحد الأقصى** حسب الضرورة.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-155">Under **Compensation**, select a level from the **Level** dropdown, and then adjust **Low threshold**, **Control point**, and **High threshold** as necessary.</span></span>

14. <span data-ttu-id="1fbb7-156">عندما يكتمل طلب التعيين وأصبحت مستعدًا لبدء عملية التعيين، حدد **تنشيط** في شريط القوائم.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-156">When your recruiting request is complete and you're ready to start the recruiting process, select **Activate** in the menu bar.</span></span>

   ![تنشيط طلب التعيين](./media/hr-recruit-6-activate-recruit-request.png)

15. <span data-ttu-id="1fbb7-158">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-158">Select **Save**.</span></span>

## <a name="view-and-edit-your-recruiting-requests"></a><span data-ttu-id="1fbb7-159">عرض طلبات التعيين الخاص بك وتحريرها</span><span class="sxs-lookup"><span data-stu-id="1fbb7-159">View and edit your recruiting requests</span></span>

<span data-ttu-id="1fbb7-160">إذا كنت مديرًا وترغب في عرض طلباتك الخاصة:</span><span class="sxs-lookup"><span data-stu-id="1fbb7-160">If you're a manager and want to view your own requests:</span></span>

1. <span data-ttu-id="1fbb7-161">حدد **الخدمة الذاتية للموظف**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-161">Select **Employee self service**.</span></span>

2. <span data-ttu-id="1fbb7-162">حدد علامة التبويب **فريقي**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-162">Select the **My team** tab.</span></span>

3. <span data-ttu-id="1fbb7-163">ضمن **معلومات فريقي**، حدد علامة التبويب **طلبات التعيين**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-163">Under **My team information**, select the **Recruiting requests** tab.</span></span>

   ![علامة التبويب تحديد طلبات التعيين](./media/hr-recruit-7-recruiting-requests.png)

4. <span data-ttu-id="1fbb7-165">لعرض طلب تعيين أو تحريره، حدده في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-165">To view or edit a recruiting request, select it in the grid.</span></span>

<span data-ttu-id="1fbb7-166">إذا كنت أخصائي موارد بشرية وترغب في عرض جميع طلبات التعيين:</span><span class="sxs-lookup"><span data-stu-id="1fbb7-166">If you're an HR pro and want to view all recruiting requests:</span></span>

1. <span data-ttu-id="1fbb7-167">حدد **إدارة العاملين**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-167">Select **Personnel management**.</span></span>

2. <span data-ttu-id="1fbb7-168">حدد **طلبات التعيين**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-168">Select **Recruiting requests**.</span></span>

   ![عرض طلبات التعيين في إدارة العاملين](./media/hr-recruit-8-recruiting-requests-personnel-management.png)

3. <span data-ttu-id="1fbb7-170">لعرض طلب تعيين أو تحريره، حدده في الشبكة.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-170">To view or edit a recruiting request, select it in the grid.</span></span>

## <a name="add-or-edit-a-candidate-profile"></a><span data-ttu-id="1fbb7-171">إضافة ملف تعريف مرشح أو تحريره</span><span class="sxs-lookup"><span data-stu-id="1fbb7-171">Add or edit a candidate profile</span></span>

<span data-ttu-id="1fbb7-172">إذا تم دمج مؤسستك مع تطبيق آخر لإدارة طلبات التعيين، فستتم إعادة توجيه طلبات التعيين إلى هذا التطبيق.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-172">If your organization has integrated with another application to manage recruiting requests, recruiting requests are forwarded to that application.</span></span> <span data-ttu-id="1fbb7-173">يقوم طلب التعيين بعد ذلك بإرسال معلومات المرشح إلى Human Resources.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-173">The recruiting application then sends candidate information back to Human Resources.</span></span> <span data-ttu-id="1fbb7-174">وبخلاف ذلك، يمكنك متابعة عمليات التعيين الداخلية الخاصة بك وإدخال معلومات المرشح يدويًا.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-174">Otherwise, you can follow your own internal recruiting processes and enter candidate information manually.</span></span>

1. <span data-ttu-id="1fbb7-175">حدد **إدارة العاملين**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-175">Select **Personnel management**.</span></span>

2. <span data-ttu-id="1fbb7-176">حدد **الارتباطات**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-176">Select **Links**.</span></span>

3. <span data-ttu-id="1fbb7-177">ضمن **التعيين**، حدد **المرشحين**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-177">Under **Recruiting**, select **Candidates**.</span></span>

   ![عرض المرشحين](./media/hr-recruit-9-candidates.png)

4. <span data-ttu-id="1fbb7-179">لإضافة مرشح، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-179">To add a candidate, select **New**.</span></span> <span data-ttu-id="1fbb7-180">لتحرير مرشح موجود، حدد المرشح من القائمة ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-180">To edit an existing candidate, select the candidate from the list and then select **Edit**.</span></span> <span data-ttu-id="1fbb7-181">يظهر ملف تعريف المرشح.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-181">The candidate profile appears.</span></span>

5. <span data-ttu-id="1fbb7-182">ضمن **ملخص المرشح**، قم بإدخال أو تحرير معلومات المرشح عند الضرورة.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-182">Under **Candidate summary**, enter or edit the candidate information as necessary.</span></span>

6. <span data-ttu-id="1fbb7-183">ضمن **طلب التعيين**، حدد طلب تعيين لربط المرشح به.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-183">Under **Recruiting request**, select a recruiting request to link the candidate to.</span></span> <span data-ttu-id="1fbb7-184">أكمل بعد ذلك حقول **تاريخ البدء المقدر** و **مدير التعيين** و **المنصب** و **الوصف** حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-184">Then complete the **Estimated start date**, **Hiring manager**, **Position**, and **Description fields** as appropriate.</span></span>

   ![الربط بطلب تعيين](./media/hr-recruit-10-link-to-recruiting-request.png)

7. <span data-ttu-id="1fbb7-186">أكمل جميع المعلومات في المجالات التالية التي تريد تضمينها في سجل المرشح:</span><span class="sxs-lookup"><span data-stu-id="1fbb7-186">Complete all the information in the following areas that you want to include in the candidate's record:</span></span>
   - <span data-ttu-id="1fbb7-187">**التعليقات**</span><span class="sxs-lookup"><span data-stu-id="1fbb7-187">**Comments**</span></span>
   - <span data-ttu-id="1fbb7-188">**الخبرة المهنية**</span><span class="sxs-lookup"><span data-stu-id="1fbb7-188">**Professional experience**</span></span>
   - <span data-ttu-id="1fbb7-189">**معلومات جهة الاتصال**</span><span class="sxs-lookup"><span data-stu-id="1fbb7-189">**Contact information**</span></span>
   - <span data-ttu-id="1fbb7-190">**التعليم**</span><span class="sxs-lookup"><span data-stu-id="1fbb7-190">**Education**</span></span>
   - <span data-ttu-id="1fbb7-191">**المهارات**</span><span class="sxs-lookup"><span data-stu-id="1fbb7-191">**Skills**</span></span>
   - <span data-ttu-id="1fbb7-192">**الشهادات**</span><span class="sxs-lookup"><span data-stu-id="1fbb7-192">**Certificates**</span></span>
   - <span data-ttu-id="1fbb7-193">**عمليات مراقبة**</span><span class="sxs-lookup"><span data-stu-id="1fbb7-193">**Screenings**</span></span>

8. <span data-ttu-id="1fbb7-194">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-194">Select **Save**.</span></span>

## <a name="hire-a-candidate"></a><span data-ttu-id="1fbb7-195">تعيين مرشح</span><span class="sxs-lookup"><span data-stu-id="1fbb7-195">Hire a candidate</span></span>

<span data-ttu-id="1fbb7-196">عندما تكون مستعدًا لتعيين مرشح، اتبع هذا الإجراء لتحويل المرشح إلى موظف.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-196">When you're ready to hire a candidate, follow this procedure to transition the candidate to an employee.</span></span>

1. <span data-ttu-id="1fbb7-197">في نموذج المرشح، حدد **تعيين**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-197">On the candidate form, select **Hire**.</span></span>

   ![تعيين مرشح](./media/hr-recruit-11-hire.png)

2. <span data-ttu-id="1fbb7-199">في نموذج **تعيين عامل جديد**، ضمن **التفاصيل**، أكمل جميع الحقول.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-199">On the **Hire new worker** form, under **Details**, complete all the fields.</span></span>

   ![إدخال تفاصيل التعيين الجديد](./media/hr-recruit-12-hire-new-worker.png)

3. <span data-ttu-id="1fbb7-201">ضمن **تفاصيل المنصب**، تحقق من المعلومات وقم بتغييرها إذا لزم الأمر.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-201">Under **Position details**, verify and change information as necessary.</span></span>

4. <span data-ttu-id="1fbb7-202">ضمن **قوائم اختيار الإعداد**، حدد قوائم اختيار الإعداد ذات الصلة لهذا الموظف.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-202">Under **Onboarding checklists**, select the relevant onboarding checklists for this employee.</span></span>

5. <span data-ttu-id="1fbb7-203">حدد **متابعة** لإنشاء سجل الموظف.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-203">Select **Continue** to create the employee record.</span></span>

   >[!NOTE]
   ><span data-ttu-id="1fbb7-204">وفقًا لمهام سير العمل في مؤسستك، قد يمر سجل المرشح بخطوات موافقة إضافية قبل أن يصبح سجل موظف.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-204">Depending on your organization's workflows, the candidate record may go through additional approval steps before becoming an employee record.</span></span>

## <a name="decide-not-to-hire-a-candidate"></a><span data-ttu-id="1fbb7-205">اتخاذ قرار بعدم تعيين مرشح</span><span class="sxs-lookup"><span data-stu-id="1fbb7-205">Decide not to hire a candidate</span></span>

<span data-ttu-id="1fbb7-206">إذا قررت عدم تعيين مرشح، فاتبع هذا الإجراء لإزالته من عملية التدقيق.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-206">If you decide not to hire a candidate, follow this procedure to remove them from the vetting process.</span></span> 

1. <span data-ttu-id="1fbb7-207">في نموذج المرشح، حدد **عدم التعيين**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-207">On the candidate form, select **Do not hire**.</span></span>

   ![عدم تعيين المرشح](./media/hr-recruit-13-do-not-hire.png)

2. <span data-ttu-id="1fbb7-209">حدد **كود السبب** وقم بتضمين أي تعليقات.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-209">Select a **Reason code** and include any comments.</span></span>

3. <span data-ttu-id="1fbb7-210">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-210">Select **OK**.</span></span>

## <a name="dismiss-a-candidate"></a><span data-ttu-id="1fbb7-211">استبعاد مرشح</span><span class="sxs-lookup"><span data-stu-id="1fbb7-211">Dismiss a candidate</span></span>

<span data-ttu-id="1fbb7-212">إذا لزم الأمر، يمكنك استبعاد المرشح بعد تعيينه.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-212">If needed, you can dismiss a candidate after hiring them.</span></span> <span data-ttu-id="1fbb7-213">على سبيل المثال، قد يرفض المرشح عرضك أو لا يظهر في يومه الأول.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-213">For example, a candidate might reject your offer or not show up on their first day.</span></span>

- <span data-ttu-id="1fbb7-214">في نموذج المرشح، حدد **استبعاد مرشح**.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-214">On the candidate form, select **Dismiss candidate**.</span></span>

  ![استبعاد المرشح](./media/hr-recruit-14-dismiss-candidate.png)

## <a name="see-also"></a><span data-ttu-id="1fbb7-216">راجع أيضًا</span><span class="sxs-lookup"><span data-stu-id="1fbb7-216">See also</span></span>

[<span data-ttu-id="1fbb7-217">تكوين جداول Dataverse الظاهرية</span><span class="sxs-lookup"><span data-stu-id="1fbb7-217">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="1fbb7-218">تنظيم القوى العاملة</span><span class="sxs-lookup"><span data-stu-id="1fbb7-218">Organize your workforce</span></span>](hr-personnel-departments-jobs-positions.md)<br>
[<span data-ttu-id="1fbb7-219">إعداد مكونات وظيفة</span><span class="sxs-lookup"><span data-stu-id="1fbb7-219">Set up the components of a job</span></span>](hr-personnel-jobs.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
