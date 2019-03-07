---
title: إنشاء حقول مخصصة والعمل باستخدامها
description: يوضح هذا الموضوع كيف يسمح Microsoft Dynamics 365 for Finance and Operations لبعض المستخدمين بإنشاء حقول مخصصة لتخصيص التطبيق لملاءمة أعمالهم.
author: jasongre
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 18402579789c17de7b46dd7a013b3b6327ea5d4f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "348010"
---
# <a name="create-and-work-with-custom-fields"></a><span data-ttu-id="3ee0b-103">إنشاء حقول مخصصة والعمل باستخدامها</span><span class="sxs-lookup"><span data-stu-id="3ee0b-103">Create and work with custom fields</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ee0b-104">بينما يوفر Microsoft Dynamics 365 for Finance and Operations مجموعة شاملة من الحقول الجاهزة لإدارة مجموعة كبيرة من عمليات الأعمال، قد تحتاج الشركات في بعض الأحيان إلى تعقب معلومات إضافية في النظام.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-104">While Microsoft Dynamics 365 for Finance and Operations provides an extensive set of fields out-of-the-box for managing a broad range of business processes, sometimes there is a need for a company to track additional information in the system.</span></span> <span data-ttu-id="3ee0b-105">لتلبية هذه الحاجة، يتيح لك Finance and Operations إمكانية إنشاء حقول مخصصة لتكييف التطبيق ليناسب عملك، بشرط أن يكون لديك أذونات لهذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-105">To accommodate this need, Finance and Operations allows you to create custom fields to tailor the application to fit your business, provided you have permissions to the feature.</span></span>

<span data-ttu-id="3ee0b-106">تتوفر القدرة على إضافة حقول مخصصة في تحديث النظام الأساسي 13 والإصدارات الأحدث.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-106">The ability to add custom fields is available in platform update 13 and later.</span></span>

<span data-ttu-id="3ee0b-107">يوضح هذا الفيديو مدى سهولة إضافة حقل مخصص إلى صفحة: [إضافة حقول مخصصة في Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span><span class="sxs-lookup"><span data-stu-id="3ee0b-107">This video shows how easy it is to add a custom field to a page: [Adding custom fields in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=gWSGZI9Vtnc).</span></span>

## <a name="creating-custom-fields"></a><span data-ttu-id="3ee0b-108">إنشاء الحقول المخصصة</span><span class="sxs-lookup"><span data-stu-id="3ee0b-108">Creating custom fields</span></span>

<span data-ttu-id="3ee0b-109">بعد قيامك بتحديد المعلومات الإضافية التي تريد أن تتعقبها في التطبيق، يمكنك إنشاء الحقل في الجدول المناسب وعرض هذا الحقل الجديد على صفحة.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-109">After you've identified additional information that you would like to track in the application, you can create the custom field on the appropriate table and expose that new field on a page.</span></span>

<span data-ttu-id="3ee0b-110">توضح الخطوات التالية عملية إنشاء حقل مخصص ووضع هذا الحقل في نموذج.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-110">The following steps describe the process for creating a custom field and placing that field on a form.</span></span>

1. <span data-ttu-id="3ee0b-111">انتقل إلى النموذج الذي تظهر فيه الحاجة إلى الحقل الجديد.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-111">Navigate to the form where the new field is needed.</span></span>
2. <span data-ttu-id="3ee0b-112">نظرًا لأن الهدف النهائي هو عرض الحقل المخصص في نموذج، توجد نقطة الإدخال لإنشاء الحقول المخصصة داخل تجربة التخصيص.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-112">Because the end goal is to expose the custom field on a form, the entry point for creating custom fields exists inside the personalization experience.</span></span> <span data-ttu-id="3ee0b-113">افتح شريط أدوات التخصيص عن طريق تحديد **خيارات**، ثم **تخصيص النموذج**.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-113">Open the personalization toolbar by selecting **Options**, and then **Personalize this form**.</span></span>
3. <span data-ttu-id="3ee0b-114">انقر فوق **إدراج** ثم **الحقل**.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-114">Click **Insert** and then **Field**.</span></span>
4. <span data-ttu-id="3ee0b-115">حدد منطقة النموذج الذي تريد فيه عرض الحقل الجديد.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-115">Select the region of the form where you want to expose the new field.</span></span> <span data-ttu-id="3ee0b-116">بعد التحديد، سيعرض مربع حوار **إدراج الحقول** قائمة بالحقول الموجودة التي يمكن إدراجها في المنطقة المحددة للنموذج.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-116">After selection, the **Insert fields** dialog box will display a list of existing fields that can be inserted into the selected region of the form.</span></span>
5. <span data-ttu-id="3ee0b-117">تأكد من أن الحقل الذي يهمك غير موجود بالفعل في القائمة.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-117">Ensure that the field you are interested in does not already exist in the list.</span></span> <span data-ttu-id="3ee0b-118">إذا كان الأمر كذلك، فيمكنك ببساطة تحديد هذا الحقل في القائمة وانقر فوق **إدراج**.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-118">If it does, you can simply select that field in the list and click **Insert**.</span></span>
6. <span data-ttu-id="3ee0b-119">انقر فوق الزر **إنشاء حقل جديد** أعلى القائمة لبدء عملية إنشاء حقل مخصص.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-119">Click the **Create new field** button above the list to initiate the process of creating a custom field.</span></span> <span data-ttu-id="3ee0b-120">سيؤدي هذا إلى فتح مربع الحوار **إنشاء حقل جديد**.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-120">This will open the **Create new field** dialog box.</span></span>

    <span data-ttu-id="3ee0b-121">إذا لم تشاهد الزر **إنشاء حقل جديد**، فإنه ليس لديك الأذونات اللازمة لاستخدام هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-121">If you do not see the **Create new field** button, you do not have the necessary permissions to use this feature.</span></span>

7. <span data-ttu-id="3ee0b-122">في مربع الحوار **إنشاء حقل جديد**، أدخل المعلومات التالية.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-122">In the **Create new field** dialog box, enter the following information.</span></span>

    1. <span data-ttu-id="3ee0b-123">حدد جدول قاعدة البيانات التي يجب إضافة هذا الحقل إليها.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-123">Select the database table where this field should be added.</span></span> <span data-ttu-id="3ee0b-124">لاحظ أن الجداول التي تدعم الحقول المخصصة فقط ستظهر في القائمة المنسدلة.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-124">Note that only tables that support custom fields will appear in the drop-down list.</span></span> <span data-ttu-id="3ee0b-125">راجع القسم التالي للحصول على التفاصيل الفنية في الجداول المدعومة.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-125">See the section below for technical details on supported tables.</span></span>
    2. <span data-ttu-id="3ee0b-126">حدد نوع بيانات الحقل الجديد.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-126">Select the data type for the new field.</span></span> <span data-ttu-id="3ee0b-127">أنواع البيانات المتوفرة هي خانة الاختيار، والتاريخ، والوقت والتاريخ، والعشرية، والرقم، وقائمة الاختيار، والنص.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-127">The available data types are checkbox, date, date time, decimal, number, picklist, and text.</span></span>

        - <span data-ttu-id="3ee0b-128">إذا اخترت نوع بيانات النص، يمكنك أيضًا تحديد الحد الأقصى لطول النص الذي يمكن إدخاله في هذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-128">If you choose the text data type, you can also specify the maximum length of the text that can be entered in this field.</span></span>
        - <span data-ttu-id="3ee0b-129">إذا اخترت نوع بيانات قائمة الخيارات، يمكنك أيضًا تحديد مجموعة القيم الصالحة لهذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-129">If you choose the picklist data type, you can also select the set of valid values for the field.</span></span>

    3. <span data-ttu-id="3ee0b-130">قم بتوفير اسم وعنوان ونص تعليمات للحقل.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-130">Provide a name, label, and help text for the field.</span></span> <span data-ttu-id="3ee0b-131">يتطابق الاسم مع اسم الحقل الفعلي في قاعدة البيانات، حيث تكون التسمية ونص التعليمات هي النص المستخدم لتمثيل هذا الحقل في واجهة المستخدم.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-131">The name corresponds to the physical field name in the database, whereas the label and help text are the text used to represent this field in the user interface.</span></span>

8. <span data-ttu-id="3ee0b-132">إذا كان هذا هو الحقل الوحيد الذي تحتاج إلى إنشائه لهذا النموذج، فانقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-132">If this is the only field that you need to create for this form, click **Save**.</span></span> <span data-ttu-id="3ee0b-133">إذا كنت تحتاج إلى إنشاء حقول إضافية، فانقر فوق **حفظ وجديد** ثم أرجع إلى الخطوة 7.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-133">If you need to create additional fields, click **Save and new** and go back to step 7.</span></span> <span data-ttu-id="3ee0b-134">لاحظ أنه يوجد حاليًا حد أقصى قدره **20 حقلاً مخصصًا لكل جدول**.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-134">Note that there is currently a limit of **20 custom fields per table**.</span></span>
9. <span data-ttu-id="3ee0b-135">ستعيدك مغادرة مربع الحوار **إنشاء حقل جديد** إلى مربع الحوار **إدراج حقول**.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-135">Leaving the **Create new field** dialog box will return you to the **Insert fields** dialog box.</span></span> <span data-ttu-id="3ee0b-136">سيتم تمييز أي حقول مخصصة تمت إضافتها للتو تلقائيًا في قائمة الحقول المُراد إدراجها في النموذج.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-136">Any custom fields that were just added will be automatically marked in the field list to be inserted into the form.</span></span>
10. <span data-ttu-id="3ee0b-137">انقر فوق **إدراج** لإدراج الحقول المميزة في المنطقة المحددة للنموذج.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-137">Click **Insert** to insert the marked fields into the selected region of the form.</span></span>
11. <span data-ttu-id="3ee0b-138">**اختياري:** قم بتمكين وضع **النقل** من شريط أدوات التخصيص لنقل الحقول الجديدة إلى موقعها المطلوب في المنطقة المحددة.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-138">**Optional:** Enable **Move** mode from the personalization toolbar to move the new fields to their desired location in the selected region.</span></span> <span data-ttu-id="3ee0b-139">راجع [تخصيص تجربة المستخدم](personalize-user-experience.md) للحصول على مزيد من المعلومات حول كيفية استخدام إمكانيات التخصيص المختلفة لتحسين نموذج لاستخدامك الشخصي.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-139">See [Personalize the user experience](personalize-user-experience.md) for more information about how to use the various personalization capabilities to optimize a form for your personal usage.</span></span>

## <a name="sharing-custom-fields-with-other-users"></a><span data-ttu-id="3ee0b-140">مشاركة الحقول المخصصة مع مستخدمين آخرين</span><span class="sxs-lookup"><span data-stu-id="3ee0b-140">Sharing custom fields with other users</span></span>

<span data-ttu-id="3ee0b-141">بعد أن تقوم بإنشاء حقل مخصص وعرضه في نموذج، فقد تحتاج إلى تقديم طريقة عرض الصفحة المحدثة هذه التي تتضمن الحقل الجديد للمستخدمين الآخرين في النظام.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-141">After you have created a custom field and exposed it on a form, you might want to provide this updated page view that includes the new field to other users in the system.</span></span> <span data-ttu-id="3ee0b-142">يمكن أن يتم ذلك بطريقتين مختلفتين باستخدام إمكانات تخصيص المنتج:</span><span class="sxs-lookup"><span data-stu-id="3ee0b-142">This can be accomplished in two different ways using the personalization capabilities of the product:</span></span>

- <span data-ttu-id="3ee0b-143">يتم التوجيه الموصى به من خلال مسؤول النظام، الذي يمكنه تقديم تخصيص لجميع المستخدمين أو مجموعة فرعية من المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-143">The recommended route is through the system administrator, who can push a personalization to all users or a subset of users.</span></span> <span data-ttu-id="3ee0b-144">راجع [تخصيص تجربة المستخدم](personalize-user-experience.md) لمزيد من التفاصيل.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-144">See [Personalize the user experience](personalize-user-experience.md) for more details.</span></span>
- <span data-ttu-id="3ee0b-145">وبدلاً من ذلك، يمكنك تصدير التغييرات الخاصة بك (تسمى *عمليات التخصيص*) وإرسالها إلى مستخدم واحد أو أكثر وجعل كل واحد من هؤلاء المستخدمين يستورد التغييرات الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-145">Alternatively, you can export your changes (called *personalizations*), send them to one or more users, and have each of those users import your changes.</span></span> <span data-ttu-id="3ee0b-146">يتيح لك الخيار **إدارة** في شريط أدوات التخصيص إمكانية تصدير واستيراد التخصيصات.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-146">The **Manage** option on the personalization toolbar enables you to export and import personalizations.</span></span>

## <a name="managing-custom-fields"></a><span data-ttu-id="3ee0b-147">إدارة الحقول المخصصة</span><span class="sxs-lookup"><span data-stu-id="3ee0b-147">Managing custom fields</span></span>

<span data-ttu-id="3ee0b-148">يمكن إنجاز إدارة جميع الحقول المخصصة في النظام من خلال صفحة **الحقول المخصصة** في وحدة إدارة النظام.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-148">Management of all the custom fields in the system can be accomplished through the **Custom fields** page in the System administration module.</span></span> <span data-ttu-id="3ee0b-149">تتيح هذه الصفحة للمستخدمين حق الوصول إلى العديد من الإمكانات، بما في ذلك:</span><span class="sxs-lookup"><span data-stu-id="3ee0b-149">This page allows users access to many capabilities, including:</span></span>

- <span data-ttu-id="3ee0b-150">عرض قائمة بجميع الحقول المخصصة في النظام.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-150">Viewing a list of all custom fields in the system.</span></span>
- <span data-ttu-id="3ee0b-151">تحرير محدود للحقول المخصصة الموجودة.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-151">Limited editing of existing custom fields.</span></span>
- <span data-ttu-id="3ee0b-152">حذف الحقول المخصصة.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-152">Deleting custom fields.</span></span>
- <span data-ttu-id="3ee0b-153">عرض الحقول المخصصة في كيانات البيانات.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-153">Exposing custom fields on data entities.</span></span>
- <span data-ttu-id="3ee0b-154">تقديم ترجمات تسميات الحقول المخصصة ونص التعليمات.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-154">Providing translations of custom field labels and help text.</span></span>

### <a name="viewing-all-custom-fields"></a><span data-ttu-id="3ee0b-155">عرض جميع الحقول المخصصة</span><span class="sxs-lookup"><span data-stu-id="3ee0b-155">Viewing all custom fields</span></span>

<span data-ttu-id="3ee0b-156">توفر صفحة **الحقول المخصصة** الرؤية لجميع الحقول المخصصة التي تم تحديدها في النظام.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-156">The **Custom fields** page provides visibility to all the custom fields that have been defined in the system.</span></span> <span data-ttu-id="3ee0b-157">حدد ببساطة الجدول الذي تهتم به، وسيتم تحديث الصفحة لعرض قائمة الحقول المخصصة المقترنة بهذا الجدول.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-157">Simply select the table that you are interested in, and the page will update to show a list of the custom fields associated with that table.</span></span> <span data-ttu-id="3ee0b-158">سيتيح لك اختيار حقل مخصص من القائمة إمكانية عرض جميع تفاصيل هذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-158">Choosing a custom field from the list will allow you to view all the details about the field.</span></span>

### <a name="editing-custom-fields"></a><span data-ttu-id="3ee0b-159">تحرير الحقول المخصصة</span><span class="sxs-lookup"><span data-stu-id="3ee0b-159">Editing custom fields</span></span>

<span data-ttu-id="3ee0b-160">بعد إنشاء حقل مخصص، يمكن تعديل أجزاء معينة فقط من المعلومات حول الحقل المخصص في صفحة **الحقول المخصصة**.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-160">After a custom field has been created, only certain pieces of information about the custom field can be modified on the **Custom fields** page.</span></span>

<span data-ttu-id="3ee0b-161">*يمكنك* تعديل هذه السمات:</span><span class="sxs-lookup"><span data-stu-id="3ee0b-161">You *can* modify these attributes:</span></span>

- <span data-ttu-id="3ee0b-162">التسمية</span><span class="sxs-lookup"><span data-stu-id="3ee0b-162">Label</span></span>
- <span data-ttu-id="3ee0b-163">نص تعليمات</span><span class="sxs-lookup"><span data-stu-id="3ee0b-163">Help text</span></span>
- <span data-ttu-id="3ee0b-164">الطول، للحقول النصية</span><span class="sxs-lookup"><span data-stu-id="3ee0b-164">Length, for Text fields</span></span>

<span data-ttu-id="3ee0b-165">*لا يمكنك* تحرير السمات التالية:</span><span class="sxs-lookup"><span data-stu-id="3ee0b-165">You *cannot* edit the following attributes:</span></span>

- <span data-ttu-id="3ee0b-166">اسم الحقل</span><span class="sxs-lookup"><span data-stu-id="3ee0b-166">Field name</span></span>
- <span data-ttu-id="3ee0b-167">نوع البيانات</span><span class="sxs-lookup"><span data-stu-id="3ee0b-167">Data type</span></span>

<span data-ttu-id="3ee0b-168">بالإضافة إلى ذلك، بالنسبة لحقول قائمة الاختيار، يمكن إعادة ترتيب مجموعة القيم الصالحة للحقل المخصص، ويمكن إضافة القيم الجديدة; ومع ذلك، لا يمكن إزالة القيمة الموجودة لحقل قائمة الاختيار.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-168">Additionally, for picklist fields, the set of valid values for the custom field can be reordered, and new values can be added; however, existing values for the picklist field cannot be removed.</span></span> <span data-ttu-id="3ee0b-169">تذكر أن تنقر فوق **تطبيق التغييرات** عندما تنتهي من تحرير الحقول لجدول محدد حتى يتم حفظ التغييرات.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-169">Remember to click **Apply changes** when you are done editing fields for a particular table so the changes are saved.</span></span>

### <a name="exposing-custom-fields-on-data-entities"></a><span data-ttu-id="3ee0b-170">عرض الحقول المخصصة في كيانات البيانات</span><span class="sxs-lookup"><span data-stu-id="3ee0b-170">Exposing custom fields on data entities</span></span>

<span data-ttu-id="3ee0b-171">كما قد يكون من المهم السماح بظهور الحقول المخصصة في كيانات البيانات.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-171">It may also be important to allow custom fields to be visible on data entities.</span></span> <span data-ttu-id="3ee0b-172">يتم استخدام كيانات البيانات في الميزة [فتح في Office](../../dev-itpro/office-integration/office-integration.md)، فضلاً عن سيناريوهات استيراد/تصدير البيانات.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-172">Data entities are utilized in the [Open in Office](../../dev-itpro/office-integration/office-integration.md) feature, as well as for data import/export scenarios.</span></span>

<span data-ttu-id="3ee0b-173">اتبع هذه الخطوات لعرض حقل مخصص في كيان بيانات:</span><span class="sxs-lookup"><span data-stu-id="3ee0b-173">Follow these steps to expose a custom field on a data entity:</span></span>

1. <span data-ttu-id="3ee0b-174">حدد الحقل المخصص في نموذج **الحقول المخصصة**.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-174">Select the custom field on the **Custom fields** form.</span></span>
2. <span data-ttu-id="3ee0b-175">قم بتوسيع قسم **الكيانات** لعرض مجموعة الكيانات ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-175">Expand the **Entities** section to view the set of relevant entities.</span></span>
3. <span data-ttu-id="3ee0b-176">انقر فوق الزر **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-176">Click the **Edit** button.</span></span>
4. <span data-ttu-id="3ee0b-177">قم بتعديل الحقل **ممكّن** المراد تحديده لكل كيان يجب أن يعرض هذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-177">Modify the **Enabled** field to be selected for each entity that should expose this field.</span></span>
5. <span data-ttu-id="3ee0b-178">انقر فوق **تطبيق التغييرات** لحفظ التحديدات.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-178">Click **Apply changes** to save your selections.</span></span>

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a><span data-ttu-id="3ee0b-179">السماح بعرض الحقول المخصصة بلغات أخرى</span><span class="sxs-lookup"><span data-stu-id="3ee0b-179">Allowing custom fields to be displayed in other languages</span></span>

<span data-ttu-id="3ee0b-180">نظرًا لأنه قد تظهر الحاجة إلى وصول المستخدمين إلى الحقول المخصصة بلغات مختلفة، توفر صفحة **الحقول المخصصة** آلية للسماح بترجمة نص التعليمات والتسمية لحقل مخصص بلغات أخرى.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-180">Because custom fields may need to be accessed by users in a variety of languages, the **Custom fields** page provides a mechanism to allow the label and help text for a custom field to be translated into other languages.</span></span>

<span data-ttu-id="3ee0b-181">توضح الخطوات التالية عملية ترجمة الحقول المخصصة بلغات أخرى:</span><span class="sxs-lookup"><span data-stu-id="3ee0b-181">The following steps describe the process for translating custom fields in other languages:</span></span>

1. <span data-ttu-id="3ee0b-182">حدد الحقل المخصص في صفحة **الحقول المخصصة**.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-182">Select the custom field on the **Custom fields** page.</span></span>
2. <span data-ttu-id="3ee0b-183">حدد الزر **ترجمات** في "جزء الإجراءات".</span><span class="sxs-lookup"><span data-stu-id="3ee0b-183">Select the **Translations** button in the Action Pane.</span></span> <span data-ttu-id="3ee0b-184">سيؤدي هذا إلى فتح قائمة منسدلة بالترجمات الموجودة لهذا الحقل.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-184">This will open a drop-down menu with existing translations for this field.</span></span>
3. <span data-ttu-id="3ee0b-185">تعرض القائمة المنسدلة **لغة** مجموعة اللغات التي توفير الترجمات لها بالفعل.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-185">The **Language** drop-down menu shows the set of languages for which translations have already been provided.</span></span>

    <span data-ttu-id="3ee0b-186">إذا كنت ترغب في تحرير ترجمة موجودة، فحدد اللغة المطلوبة من القائمة وقم بتعديل القيم للتسمية ونص التعليمات.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-186">If you want to edit an existing translation, select the desired language from the menu and modify the values for the label and help text.</span></span>

    <span data-ttu-id="3ee0b-187">وإلا، انقر فوق الزر **إضافة لغة**، وحدد اللغة المطلوبة من القائمة، ثم قم بتوفير القيم المترجمة لنص التعليمات والتسمية.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-187">Otherwise, click the **Add language** button, select the desired language from the menu, and then provide translated values for the label and help text.</span></span>

4. <span data-ttu-id="3ee0b-188">انقر فوق **موافق** عند الانتهاء.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-188">Click **OK** when you are finished.</span></span>

### <a name="deleting-custom-fields"></a><span data-ttu-id="3ee0b-189">حذف الحقول المخصصة</span><span class="sxs-lookup"><span data-stu-id="3ee0b-189">Deleting custom fields</span></span>

<span data-ttu-id="3ee0b-190">في بعض الحالات النادرة، قد تقرر أن حقل مخصص لم يعد مطلوبًا.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-190">In some rare cases, you may decide that a custom field is no longer needed.</span></span> <span data-ttu-id="3ee0b-191">عند حدوث ذلك، يستطيع مسؤول نظام اختيار حذف الحقل من صفحة **الحقول المخصصة**.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-191">When this occurs, a system administrator can choose to delete the field from the **Custom fields** page.</span></span> <span data-ttu-id="3ee0b-192">للقيام بذلك، تأكد من تحديد الحقل الصحيح، وانقر فوق **حذف**، ثم انقر فوق **نعم** لتأكيد الحذف، وأخيرًا انقر فوق **تطبيق التغييرات**.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-192">To do this, ensure the correct field is selected, click **Delete**, click **Yes** to confirm the deletion, and finally click **Apply changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="3ee0b-193">لا يمكن التراجع عن هذا الإجراء، وسيؤدي ذلك إلى حذف البيانات المقترنة بهذا الحقل نهائيًا من قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-193">This action cannot be undone, and will result in the data associated with the field being permanently deleted from the database.</span></span>

## <a name="appendix"></a><span data-ttu-id="3ee0b-194">الملحق</span><span class="sxs-lookup"><span data-stu-id="3ee0b-194">Appendix</span></span>

### <a name="who-can-create-custom-fields"></a><span data-ttu-id="3ee0b-195">مَن الذي يمكنه إنشاء الحقول المخصصة؟</span><span class="sxs-lookup"><span data-stu-id="3ee0b-195">Who can create custom fields?</span></span>

<span data-ttu-id="3ee0b-196">كحماية للنظام، يستطيع مسؤولو النظام فقط إنشاء حقول مخصصة بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-196">As a safeguard to the system, only system administrators are able to create custom fields by default.</span></span> <span data-ttu-id="3ee0b-197">ومع ذلك، يمكن منح هؤلاء المستخدمين المحترفين الذين تعتبرهم المؤسسة ضروريين حقوق إنشاء حقول مخصصة من قِبل مسؤول نظام باستخدام دور الأمان **المستخدم المحترف للتخصيص في وقت التشغيل**.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-197">However, those power users whom the organization deems necessary can be given rights to create custom fields by a system administrator using the **Runtime customization power user** security role.</span></span> <span data-ttu-id="3ee0b-198">لن يتمكن المستخدمون الذين ليس لديهم دور الأمان هذا من إنشاء الحقول المخصصة، ولكن سيظل بإمكانهم رؤية والتفاعل مع الحقول المخصصة التي تمت إضافتها بواسطة مستخدمين آخرين في النظام.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-198">Users without this security role will not be able to create custom fields, but will still be able to see and interact with custom fields added by other users in the system.</span></span>

### <a name="what-tables-support-custom-fields"></a><span data-ttu-id="3ee0b-199">ما الجداول التي تدعم الحقول المخصصة؟</span><span class="sxs-lookup"><span data-stu-id="3ee0b-199">What tables support custom fields?</span></span>

<span data-ttu-id="3ee0b-200">بالنسبة للأداء والأسباب الفنية، تتيح الجداول التي تفي بالشروط التالية حاليًا إمكانية إضافة الحقول المخصصة.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-200">For performance and technical reasons, only tables that meet the following conditions currently allow custom fields to be added.</span></span>

- <span data-ttu-id="3ee0b-201">يجب أن يتم تمييز الجدول كإحدى هذه المجموعات:</span><span class="sxs-lookup"><span data-stu-id="3ee0b-201">The table must be tagged as one of these groups:</span></span>

    - <span data-ttu-id="3ee0b-202">مجموعة</span><span class="sxs-lookup"><span data-stu-id="3ee0b-202">Group</span></span>
    - <span data-ttu-id="3ee0b-203">WorksheetHeader</span><span class="sxs-lookup"><span data-stu-id="3ee0b-203">WorksheetHeader</span></span>
    - <span data-ttu-id="3ee0b-204">الرئيسي</span><span class="sxs-lookup"><span data-stu-id="3ee0b-204">Main</span></span>
    - <span data-ttu-id="3ee0b-205">متنوع</span><span class="sxs-lookup"><span data-stu-id="3ee0b-205">Miscellaneous</span></span>
    - <span data-ttu-id="3ee0b-206">المحددة</span><span class="sxs-lookup"><span data-stu-id="3ee0b-206">Parameter</span></span>
    - <span data-ttu-id="3ee0b-207">المرجع</span><span class="sxs-lookup"><span data-stu-id="3ee0b-207">Reference</span></span>
    - <span data-ttu-id="3ee0b-208">TransactionHeader</span><span class="sxs-lookup"><span data-stu-id="3ee0b-208">TransactionHeader</span></span>

- <span data-ttu-id="3ee0b-209">لا يمكن للجدول توسيع جدول آخر.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-209">The table cannot extend another table.</span></span>
- <span data-ttu-id="3ee0b-210">لا يمكن تمييز الجدول كجدول نظام.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-210">The table cannot be marked as a system table.</span></span>
- <span data-ttu-id="3ee0b-211">لا يمكن أن يكون الجدول جدولاً مؤقتًا.</span><span class="sxs-lookup"><span data-stu-id="3ee0b-211">The table cannot be a temporary table.</span></span>
