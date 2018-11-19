---
title: "ما الجديد أو المتغير في Dynamics 365 for Talent Core HR (31 أكتوبر 2018)"
description: "يصف هذا الموضوع الميزات الجديدة أو المعدَّلة في Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c5acd09e25ecd5fefa637342f83d0ee0f1891402
ms.contentlocale: ar-sa
ms.lasthandoff: 11/01/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a><span data-ttu-id="42c07-103">ما الجديد أو المتغير في Dynamics 365 for Talent Core HR ‏(31 أكتوبر 2018)</span><span class="sxs-lookup"><span data-stu-id="42c07-103">What's new or changed in Dynamics 365 for Talent Core HR (October 31, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="42c07-104">**الإصدار 8.1.2031**</span><span class="sxs-lookup"><span data-stu-id="42c07-104">**Build 8.1.2031**</span></span>

<span data-ttu-id="42c07-105">يصف هذا الموضوع الميزات الجديدة أو المعدَّلة في Core HR.</span><span class="sxs-lookup"><span data-stu-id="42c07-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="create-links-from-talent-to-finance-and-operations"></a><span data-ttu-id="42c07-106">إنشاء ارتباطات من Talent إلى Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="42c07-106">Create links from Talent to Finance and Operations</span></span>
<span data-ttu-id="42c07-107">تسمح لك وظيفة التنقل الجديدة هذه بإنشاء ارتباطات من Talent إلى Finance and Operations، مما يوفر لك التنقل المباشر إلى صفحات Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="42c07-107">This new navigation functionality allows you to link from Talent to Finance and Operations, giving you direct navigation into Finance and Operations pages.</span></span> <span data-ttu-id="42c07-108">عندما يتم تكوين الارتباطات، يمكنك تحديد اسم ومجموعة الارتباط، والمكان حيث يجب أن يظهر الارتباط في Talent، والصفحة الهدف التي يجب فتحها في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="42c07-108">When links are configured, you can specify the name and group of the link, where the link should surface in Talent, and the target page to be opened within Finance and Operations.</span></span>

#### <a name="coming-soon"></a><span data-ttu-id="42c07-109">قريبًا</span><span class="sxs-lookup"><span data-stu-id="42c07-109">Coming soon</span></span>
<span data-ttu-id="42c07-110">ستتم إضافة سياق الحقل في المستقبل للسماح بالتنقل المباشر إلى السجلات المناظرة في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="42c07-110">Field context will be added in the future to allow for direct navigation to corresponding records in Finance and Operations.</span></span> <span data-ttu-id="42c07-111">على سبيل المثال، يمكنك استخدام **ارتباط للحقل‬** لتوفير السياق للانتقال مباشرة إلى موظف أو منصب معين في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="42c07-111">For example, you can use **Link to field** to provide the context to navigate directly to a specific employee or position in Finance and Operations.</span></span>

### <a name="configure-target-systems"></a><span data-ttu-id="42c07-112">تكوين الأنظمة الهدف</span><span class="sxs-lookup"><span data-stu-id="42c07-112">Configure target systems</span></span>

<span data-ttu-id="42c07-113">في Talent، يستطيع مسؤولو النظام تعريف الارتباطات التي ستظهر من خلال مساحة عمل "إدارة النظام"</span><span class="sxs-lookup"><span data-stu-id="42c07-113">In Talent, system administrators can define links that will be surfaced through the System Administration workspace.</span></span> <span data-ttu-id="42c07-114">تشكّل بيئات Finance and Operations التي تريد الانتقال إليها على أنها "هدف" الارتباط جزءًا من هذا التكوين.</span><span class="sxs-lookup"><span data-stu-id="42c07-114">Part of the configuration is the Finance and Operations environments that you would like to navigate to as the "target" of the link.</span></span> <span data-ttu-id="42c07-115">يمكنك القيام بذلك عن طريق إعطاء اسم للنظام الهدف وتوفير عنوان URL لبيئة Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="42c07-115">You do this by giving the target system a name and providing the URL of the Finance and Operations environment.</span></span> <span data-ttu-id="42c07-116">فيما يلي مثال عن عنوان Finance and Operations URL الذي قد تقدمه: https://devax00124aos.cloud.test.dynamics.com/.</span><span class="sxs-lookup"><span data-stu-id="42c07-116">Here is an example of a Finance and Operations URL that you would provide: https://devax00124aos.cloud.test.dynamics.com/.</span></span> <span data-ttu-id="42c07-117">بعد تكوين الأنظمة الهدف، يمكنك تعريف الارتباطات.</span><span class="sxs-lookup"><span data-stu-id="42c07-117">After you have configured your target systems,  you can define your links.</span></span>

### <a name="configure-links"></a><span data-ttu-id="42c07-118">تكوين الارتباطات</span><span class="sxs-lookup"><span data-stu-id="42c07-118">Configure links</span></span>

<span data-ttu-id="42c07-119">سيتم تعريف المعلومات التالية لكل ارتباط يتم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="42c07-119">Each link that is created will have the following information defined.</span></span>

- <span data-ttu-id="42c07-120">ارتباط - اسم الارتباط، المستخدم للتعريف فقط.</span><span class="sxs-lookup"><span data-stu-id="42c07-120">Link - Name of the link, used for identification only.</span></span>

- <span data-ttu-id="42c07-121">تمكين هذا الارتباط - عيّن هذا الخيار إلى **نعم** إذا أردت عرض الارتباط لمستخدمي Talent.</span><span class="sxs-lookup"><span data-stu-id="42c07-121">Enable this Link - Set to **Yes** if you want to display the link to users of Talent.</span></span>

- <span data-ttu-id="42c07-122">الاسم المعروض - تحديد الاسم الذي يظهر كارتباط إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="42c07-122">Display name - Define the name that will appear as a link to Finance and Operations.</span></span> <span data-ttu-id="42c07-123">البيانات غير مترجمة في الوقت الحالي.</span><span class="sxs-lookup"><span data-stu-id="42c07-123">This data is currently is not translated.</span></span>

- <span data-ttu-id="42c07-124">ارتباط الواجهة على النموذج‬ - اختر الصفحة التي تريد عرض الارتباط عليها.</span><span class="sxs-lookup"><span data-stu-id="42c07-124">Surface link on form - Choose which page you would like to display the link on.</span></span>

- <span data-ttu-id="42c07-125">مجموعة - المجموعات غير مطلوبة، ولكن إذا كنت ترغب في تنظيم الارتباطات باستخدام المجموعات، فحدد مجموعة موجودة أو أنشئ مجموعة جديدة باستخدام الحقل **مجموعة**.</span><span class="sxs-lookup"><span data-stu-id="42c07-125">Group - Groups are not required, but if you want to organize your links using groups, select an existing group or create a new one using the **Group** field.</span></span>

- <span data-ttu-id="42c07-126">النظام الهدف - حدد النظام الهدف الذي تم إنشاؤه باستخدام الخيار **تكوين النظام الهدف**.</span><span class="sxs-lookup"><span data-stu-id="42c07-126">Target system - Select the target system that was created using the **Configure target system** option.</span></span> <span data-ttu-id="42c07-127">سيكون هذا بيئة Finance and Operations التي سيتم استخدامها عند التنقل باستخدام الارتباط.</span><span class="sxs-lookup"><span data-stu-id="42c07-127">This will be the Finance and Operations environment that will be used when navigating by using the link.</span></span>

- <span data-ttu-id="42c07-128">استخدام الشركة الحالية للمستخدم‬ - حدد **نعم** إذا كنت تريد استخدام سياق الشركة الحالية للمستخدم‬ عند الانتقال إلى Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="42c07-128">Use user's current Company - Select **Yes** if you would like to use the User's current company context when navigating to Finance and Operations.</span></span> <span data-ttu-id="42c07-129">إذا تم تحديد **لا**، فيمكنك تحديد الشركة التي يجب استخدامها.</span><span class="sxs-lookup"><span data-stu-id="42c07-129">If **No** is selected, then you can select the company that should be used.</span></span>

- <span data-ttu-id="42c07-130">عنصر قائمة الهدف‬ - أدخل عنصر القائمة من Finance and Operation الذي يجب أن يستخدمه الارتباط عند التنقل.</span><span class="sxs-lookup"><span data-stu-id="42c07-130">Target menu item - Enter the menu item from Finance and Operation that the link should use when navigating.</span></span> <span data-ttu-id="42c07-131">تتوفر عناصر القائمة التي يمكنك الانتقال إليها مباشرة.</span><span class="sxs-lookup"><span data-stu-id="42c07-131">Menu items that you can directly navigate to are available.</span></span> <span data-ttu-id="42c07-132">للعثور على عنصر القائمة المطلوب، افتح Finance and Operations وافتح الصفحة التي تعتبر هدف التنقل.</span><span class="sxs-lookup"><span data-stu-id="42c07-132">To find the menu item required, open Finance and Operations and open the page that is the target of the navigation.</span></span> <span data-ttu-id="42c07-133">انسخ عنصر القائمة من عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="42c07-133">Copy the menu item from the URL.</span></span> <span data-ttu-id="42c07-134">على سبيل المثال، إذا أردت أن ينقلك الارتباط إلى قائمة الموظفين في Finance and Operations، فأدخل القيمة التي تظهر بعد "&mi" في عنوان URL.</span><span class="sxs-lookup"><span data-stu-id="42c07-134">For example, if you want the link to take you to the employee list in Finance and Operations, enter the value that appears after the "&mi" in the URL.</span></span> <span data-ttu-id="42c07-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="42c07-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span></span> <span data-ttu-id="42c07-136">عنصر القائمة للانتقال إليه في صفحة قائمة الموظفين في هذا المثال هو: HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="42c07-136">The menu item to navigate to the employee list page in this example is: HcmWorkerListPage_Employees.</span></span>

- <span data-ttu-id="42c07-137">ارتباط بمصدر البيانات - حدد مصدر البيانات الذي يشير إليه الارتباط.</span><span class="sxs-lookup"><span data-stu-id="42c07-137">Link to data source - Select the source of data that the link is referencing.</span></span> <span data-ttu-id="42c07-138">تتوفر المصادر الأكثر شيوعًا مثل **العامل** و**المنصب**.</span><span class="sxs-lookup"><span data-stu-id="42c07-138">The most common sources like **Worker** and **Position** are available.</span></span>

- <span data-ttu-id="42c07-139">ارتباط للحقل‬ - (قريبًا) يسمح تحديد هذا الحقل بالتنقل المباشر من سجل فردي في Talent إلى سجل فردي في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="42c07-139">Link to field - (Coming soon) This field selection will allow for direct navigation from a single record in Talent to a single record in Finance and Operations.</span></span>

### <a name="access-to-links"></a><span data-ttu-id="42c07-140">الوصول إلى الارتباطات</span><span class="sxs-lookup"><span data-stu-id="42c07-140">Access to links</span></span>

<span data-ttu-id="42c07-141">سوف يرى مسؤولو النظام الارتباطات التي تم إنشاؤها حديثًا على الصفحات المحددة حتى لو تم تعيين الخيار **تمكين هذا الارتباط** إلى **لا**.</span><span class="sxs-lookup"><span data-stu-id="42c07-141">System administrators will see the newly created links on the defined pages even if the **Enable this link** option is set to **No**.</span></span> <span data-ttu-id="42c07-142">يمكن استخدام هذا لاختبار الارتباطات قبل إظهارها للموظفين الآخرين.</span><span class="sxs-lookup"><span data-stu-id="42c07-142">This can be used for testing links prior to surfacing them to other employees.</span></span> <span data-ttu-id="42c07-143">ستتمكن كافة الأدوار الأخرى من رؤية الارتباطات الأخرى فقط بعد تعيين الخيار **تمكين هذا الارتباط** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="42c07-143">All other roles will only see the configured links after the **Enable this link** option is set to **Yes**.</span></span> <span data-ttu-id="42c07-144">سيتمكن الموظفون الذين يمكنهم الوصول إلى الصفحات التي تظهر فيها الارتباطات من الوصول إلى الارتباطات.</span><span class="sxs-lookup"><span data-stu-id="42c07-144">Employees who have access to the pages in which the links are surfaced will have access to the links.</span></span>

<span data-ttu-id="42c07-145">ستتوفر أيضًا للموظفين حقوق أمان معرّفة ضمن Finance and Operations لتمكين وصولهم إلى الصفحات في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="42c07-145">Users can also have security rights within Finance and Operations defined to access the pages in Finance and Operations.</span></span> <span data-ttu-id="42c07-146">إذا لم تتوفر لديهم مثل هذه الحقوق، فسيظهر مربع حوار أمان عند استخدام الارتباط.</span><span class="sxs-lookup"><span data-stu-id="42c07-146">If they don't, a security dialog box will be displayed when using the link.</span></span>


## <a name="other-changesfixes"></a><span data-ttu-id="42c07-147">التغييرات/الإصلاحات الأخرى</span><span class="sxs-lookup"><span data-stu-id="42c07-147">Other changes/fixes</span></span>

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a><span data-ttu-id="42c07-148">لا يمكن تعيين مناصب لها تاريخ بدء مستقبلي إلى موظف جديد</span><span class="sxs-lookup"><span data-stu-id="42c07-148">Positions with a future start date cannot be assigned to a new employee</span></span>

<span data-ttu-id="42c07-149">تم إدخال تغييرات للسماح بتعيينات الموظفين إلى مناصب يقع تاريخها في المستقبل.</span><span class="sxs-lookup"><span data-stu-id="42c07-149">Changes have been made to allow employee assignments to future-dated positions.</span></span> <span data-ttu-id="42c07-150">يمكن تحديد مناصب لديها تواريخ مستقبلي، وسيتم تعيين الموظف عند حفظ أو إكمال سير العمل (إذا تم تمكين سير العمل).</span><span class="sxs-lookup"><span data-stu-id="42c07-150">Positions that have start dates in the future can be selected and the employee assignment will be made upon save or completion of the workflow (if the workflow is enabled).</span></span>

### <a name="new-employee-cannot-be-assigned-existing-position"></a><span data-ttu-id="42c07-151">لا يمكن تعيين منصب موجود إلى موظف جديد.</span><span class="sxs-lookup"><span data-stu-id="42c07-151">New employee cannot be assigned existing position</span></span>

<span data-ttu-id="42c07-152">تم إدخال تغييرات بحيث يمكن تعيين موظف جديد إلى مناصب موجودة.</span><span class="sxs-lookup"><span data-stu-id="42c07-152">Changes have been made so new employee assignment can now be assigned to existing positions.</span></span>

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a><span data-ttu-id="42c07-153">يختفي تاريخ الرتبة/موقع المكتب عندما يكون تاريخ بدء التوظيف في الماضي ويتم حفظ السجل</span><span class="sxs-lookup"><span data-stu-id="42c07-153">Seniority date/Office location disappears when the employment start date is in the past and the record is saved</span></span>

<span data-ttu-id="42c07-154">تم إجراء تغييرات لتصحيح رؤية **تاريخ الرتبة** و**موقع المكتب** عند حفظ التغييرات على موظفين سابقين.</span><span class="sxs-lookup"><span data-stu-id="42c07-154">Changes have been made to correct the visibilty of the **Senority date** and **Office location** when saving changes for past employees.</span></span>

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a><span data-ttu-id="42c07-155">لا يمكن إدخال البيانات لعمليات التوظيف ذات تاريخ مستقبلي على صفحة العامل</span><span class="sxs-lookup"><span data-stu-id="42c07-155">Can't enter data for future-dated employments on the worker page</span></span>

<span data-ttu-id="42c07-156">تم تعطيل بيانات التوظيف لعمليات التوظيف ذات التاريخ المستقبلي على صفحة العامل الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="42c07-156">Employment data for future-dated employments has been disabled on the main worker page.</span></span> <span data-ttu-id="42c07-157">يمكن إدخال بيانات التوظيف من صفحات **مدير التاريخ‬**.</span><span class="sxs-lookup"><span data-stu-id="42c07-157">Employment data can be entered through the **Date Manager** pages.</span></span> <span data-ttu-id="42c07-158">سيتم إدخال المزيد من التغييرات في الإصدارات المستقبلية لتمكين إدخال بيانات التوظيف مباشرة أثناء عملية سير العمل.</span><span class="sxs-lookup"><span data-stu-id="42c07-158">Additional changes will be made in future releases to enable entering employment data directly during the workflow process.</span></span>

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a><span data-ttu-id="42c07-159">إضافة ValidFrom وValidTo إلى HcmPersonalContactPersonEntity</span><span class="sxs-lookup"><span data-stu-id="42c07-159">Add ValidFrom and ValidTo to HcmPersonalContactPersonEntity</span></span>

<span data-ttu-id="42c07-160">تم تحديث الكيان HcmPersonalContactPersonEntity لإطار عمل Data Management Framework (DMF) بحيث يتضمن التاريخين "صالح من" و"صالح إلى" لتمين بعض سيناريوهات دمج المزايا.</span><span class="sxs-lookup"><span data-stu-id="42c07-160">The Data Management Framework (DMF) entity HcmPersonalContactPersonEntity has been updated to include "valid from" and "valid to" dates to enable certain benefit integration scenarios.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="42c07-161">مشكلات معروفة​</span><span class="sxs-lookup"><span data-stu-id="42c07-161">Known issue</span></span>
- <span data-ttu-id="42c07-162">**المشكلة**: عند إضافة مرفق جديد إلى عامل، يظهر الزران **جديد** و**تحرير** بلون رمادي.</span><span class="sxs-lookup"><span data-stu-id="42c07-162">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="42c07-163">**الحل البديل:** قبل فتح صفحة المرفق، تأكد من أن مربعات الحقائق في صفحة **العامل** مغلقة.</span><span class="sxs-lookup"><span data-stu-id="42c07-163">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="42c07-164">إذا كانت مربعات الحقائق مغلقة عند تحميل صفحة **العامل**، سيتم تمكين زر المرفقات</span><span class="sxs-lookup"><span data-stu-id="42c07-164">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="42c07-165">(سوف يتم إصلاح هذه المشكلة في التحديث التالي للنظام الأساسي.)</span><span class="sxs-lookup"><span data-stu-id="42c07-165">(This issue will be fixed in the next platform update.)</span></span>

