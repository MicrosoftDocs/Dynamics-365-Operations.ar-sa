---
title: تنفيذ الحقول المخصصة لتطبيق Microsoft Dynamics 365 Project Timesheet للأجهزة المحمولة على iOS وAndroid
description: يوفر هذا الموضوع أنماطًا شائعة لاستخدام الامتدادات لتنفيذ الحقول المخصصة.
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 4343c875da05641c57b7784bf52f1c814dd26d20
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174737"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="eac54-103">تنفيذ الحقول المخصصة لتطبيق Microsoft Dynamics 365 Project Timesheet للأجهزة المحمولة على iOS وAndroid</span><span class="sxs-lookup"><span data-stu-id="eac54-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eac54-104">يوفر هذا الموضوع أنماطًا شائعة لاستخدام الامتدادات لتنفيذ الحقول المخصصة.</span><span class="sxs-lookup"><span data-stu-id="eac54-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="eac54-105">يتم تناول الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="eac54-105">The following topics are covered:</span></span>

- <span data-ttu-id="eac54-106">أنواع البيانات المختلفة التي يدعمها إطار الحقل المخصص</span><span class="sxs-lookup"><span data-stu-id="eac54-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="eac54-107">كيفية إظهار الحقول القابلة للقراءة فقط أو القابلة للتحرير على إدخالات الجدول الزمني ، وحفظ القيم التي يوفرها المستخدم مرة أخرى إلى قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="eac54-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="eac54-108">كيفية إظهار الحقول للقراءة فقط في رأس الجدول الزمني</span><span class="sxs-lookup"><span data-stu-id="eac54-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="eac54-109">كيفية دمج منطق عمل مخصص آخر لإدخال القيم الافتراضية في الحقول والقيام بالتحقق من الصحة الإضافي</span><span class="sxs-lookup"><span data-stu-id="eac54-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="eac54-110">الجمهور</span><span class="sxs-lookup"><span data-stu-id="eac54-110">Audience</span></span>

<span data-ttu-id="eac54-111">تم إعداد هذا الموضوع للمطورين الذين يقومون بدمج الحقول المخصصة في تطبيق Microsoft Dynamics 365 Project Timesheet للأجهزة المحمولة المتوفر لـ Apple iOS وAndroid Google.</span><span class="sxs-lookup"><span data-stu-id="eac54-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="eac54-112">الافتراض هو أن القراء على دراية بتطوير X ++ ووظائف الجدول الزمني للمشروع.</span><span class="sxs-lookup"><span data-stu-id="eac54-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="eac54-113">عقد البيانات – فئة TSTimesheetCustomField X++</span><span class="sxs-lookup"><span data-stu-id="eac54-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="eac54-114">إن فئة **TSTimesheetCustomField** هي فئة عقد بيانات X ++ التي تمثل معلومات حول حقل مخصص لوظيفة الجدول الزمني.</span><span class="sxs-lookup"><span data-stu-id="eac54-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="eac54-115">يتم تمرير قوائم كائنات الحقل المخصص في كلٍّ من عقد بيانات TSTimesheetDetails وعقد بيانات TSTimesheetEntry لإظهار الحقول المخصصة في تطبيق الأجهزة المحمولة.</span><span class="sxs-lookup"><span data-stu-id="eac54-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="eac54-116">**TSTimesheetDetails** - عقد رأس الجدول الزمني.</span><span class="sxs-lookup"><span data-stu-id="eac54-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="eac54-117">**TSTimesheetEntry** - عقد حركة الجدول الزمني.</span><span class="sxs-lookup"><span data-stu-id="eac54-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="eac54-118">تشكل مجموعات من هذه الكائنات التي لها نفس معلومات المشروع وقيمة **timesheetLineRecId** بندًا.</span><span class="sxs-lookup"><span data-stu-id="eac54-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="eac54-119">fieldBaseType (الأنواع)</span><span class="sxs-lookup"><span data-stu-id="eac54-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="eac54-120">تحدد خاصية **FieldBaseType** في كائن **TsTimesheetCustom** نوع الحقل الذي يظهر في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="eac54-121">قيم **الأنواع** التالية التي يتم دعمها.</span><span class="sxs-lookup"><span data-stu-id="eac54-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="eac54-122">قيمة الأنواع</span><span class="sxs-lookup"><span data-stu-id="eac54-122">Types value</span></span> | <span data-ttu-id="eac54-123">‏‏النوع</span><span class="sxs-lookup"><span data-stu-id="eac54-123">Type</span></span>              | <span data-ttu-id="eac54-124">ملاحظات</span><span class="sxs-lookup"><span data-stu-id="eac54-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="eac54-125">0</span><span class="sxs-lookup"><span data-stu-id="eac54-125">0</span></span>           | <span data-ttu-id="eac54-126">السلسلة (والتعداد)</span><span class="sxs-lookup"><span data-stu-id="eac54-126">String (and Enum)</span></span> | <span data-ttu-id="eac54-127">يظهر الحقل كحقل نص.</span><span class="sxs-lookup"><span data-stu-id="eac54-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="eac54-128">1</span><span class="sxs-lookup"><span data-stu-id="eac54-128">1</span></span>           | <span data-ttu-id="eac54-129">عدد صحيح</span><span class="sxs-lookup"><span data-stu-id="eac54-129">Integer</span></span>           | <span data-ttu-id="eac54-130">تظهر القيمة كرقم بدون المنازل العشرية.</span><span class="sxs-lookup"><span data-stu-id="eac54-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="eac54-131">2</span><span class="sxs-lookup"><span data-stu-id="eac54-131">2</span></span>           | <span data-ttu-id="eac54-132">حقيقي</span><span class="sxs-lookup"><span data-stu-id="eac54-132">Real</span></span>              | <span data-ttu-id="eac54-133">تظهر القيمة كرقم يشتمل على المنازل العشرية.</span><span class="sxs-lookup"><span data-stu-id="eac54-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="eac54-134">لإظهار القيمة الفعلية كعملة في التطبيق، استخدم خاصية **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="eac54-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="eac54-135">يمكنك استخدام خاصية **numberOfDecimals** لتعيين رقم المنازل العشرية المبين.</span><span class="sxs-lookup"><span data-stu-id="eac54-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="eac54-136">3</span><span class="sxs-lookup"><span data-stu-id="eac54-136">3</span></span>           | <span data-ttu-id="eac54-137">التاريخ</span><span class="sxs-lookup"><span data-stu-id="eac54-137">Date</span></span>              | <span data-ttu-id="eac54-138">يتم تحديد تنسيقات التاريخ حسب إعداد **التاريخ، والأوقات، وتنسيق الأرقام** الخاص بالمستخدم والمحدد ضمن **تفضيلات البلد/المنطقة واللغة‬** في **خيارات المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="eac54-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="eac54-139">4</span><span class="sxs-lookup"><span data-stu-id="eac54-139">4</span></span>           | <span data-ttu-id="eac54-140">منطقي</span><span class="sxs-lookup"><span data-stu-id="eac54-140">Boolean</span></span>           | |
| <span data-ttu-id="eac54-141">15</span><span class="sxs-lookup"><span data-stu-id="eac54-141">15</span></span>          | <span data-ttu-id="eac54-142">GUID</span><span class="sxs-lookup"><span data-stu-id="eac54-142">GUID</span></span>              | |
| <span data-ttu-id="eac54-143">16</span><span class="sxs-lookup"><span data-stu-id="eac54-143">16</span></span>          | <span data-ttu-id="eac54-144">Int64</span><span class="sxs-lookup"><span data-stu-id="eac54-144">Int64</span></span>             | |

- <span data-ttu-id="eac54-145">إذا لم يتم توفير خاصية **stringOptions** في كائن **TSTimesheetCustomField**، يتم توفير حقل نص فارغ للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="eac54-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="eac54-146">يمكن استخدام خاصية **stringLength** لتعيين الحد الأقصى لطول السلسلة التي يمكن للمستخدمين إدخالها.</span><span class="sxs-lookup"><span data-stu-id="eac54-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="eac54-147">إذا تم توفير خاصية **stringOptions** في كائن **TSTimesheetCustomField**، تكون عناصر القائمة هذه هي القيم الوحيدة التي يمكن للمستخدمين تحديدها باستخدام أزرار الخيارات (أزرار الاختيار).</span><span class="sxs-lookup"><span data-stu-id="eac54-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="eac54-148">في هذه الحالة ، يمكن أن يعمل حقل السلسلة كقيمة تعداد لغرض إدخال المستخدم.</span><span class="sxs-lookup"><span data-stu-id="eac54-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="eac54-149">لحفظ القيمة في قاعدة البيانات كتعداد، قم يدويًا بتعيين قيمة السلسلة مرة أخرى إلى قيمة التعداد قبل حفظها في قاعدة البيانات باستخدام سلسلة الأوامر (راجع قسم "استخدام سلسلة الأوامر في فئة TSTimesheetEntryService لحفظ إدخال جدول زمني من التطبيق مرة أخرى إلى قسم قاعدة البيانات" في وقت لاحق في هذا الموضوع للحصول على مثال).</span><span class="sxs-lookup"><span data-stu-id="eac54-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="eac54-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="eac54-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="eac54-151">يمكنك استخدام هذه الخاصية لتنسيق القيم الحقيقية كعملة.</span><span class="sxs-lookup"><span data-stu-id="eac54-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="eac54-152">يكون هذا النهج قابلاً للتطبيق فقط عندما تكون قيمة **fieldBaseType** هي **حقيقية**.</span><span class="sxs-lookup"><span data-stu-id="eac54-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="eac54-153">**TSCustomFieldExtendedType:None** – لا يتم استخدام أي تنسيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="eac54-154">**TSCustomFieldExtendedType::Currency** – تنسيق القيمة كعملة.</span><span class="sxs-lookup"><span data-stu-id="eac54-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="eac54-155">عندما يكون تنسيق العملة نشطًا يمكن استخدام حقل **stringValue** لتمرير كود العملة الذي يجب أن يظهر في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="eac54-156">القيمة هي قيمة للقراءة فقط.</span><span class="sxs-lookup"><span data-stu-id="eac54-156">The value is a read-only value.</span></span>

    <span data-ttu-id="eac54-157">يحتوي حقل **realValue** على المبلغ النقدي الذي يجب حفظه إلى قاعده البيانات.</span><span class="sxs-lookup"><span data-stu-id="eac54-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="eac54-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="eac54-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="eac54-159">يمكنك استخدام هذه الخاصية لتحديد المكان الذي يجب أن يظهر فيه الحقل المخصص في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="eac54-160">**TSCustomFieldSection::Header** – سيظهر هذا الحقل في قسم **عرض مزيد من التفاصيل** في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="eac54-161">هذه الحقول هي دائما للقراءة فقط.</span><span class="sxs-lookup"><span data-stu-id="eac54-161">These fields are always read-only.</span></span>
- <span data-ttu-id="eac54-162">سطر **TSCustomFieldSection::** – سيظهر الحقل بعد كل حقول الأسطر الخارجية في إدخالات الجدول الزمني.</span><span class="sxs-lookup"><span data-stu-id="eac54-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="eac54-163">يمكن أن تكون هذه الحقول قابلة للتحرير أو للقراءة فقط.</span><span class="sxs-lookup"><span data-stu-id="eac54-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="eac54-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="eac54-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="eac54-165">تحدد هذه الخاصية الحقل عندما يتم حفظ القيم التي يوفرها التطبيق مرة أخرى إلى قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="eac54-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="eac54-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="eac54-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="eac54-167">تحدد هذه الخاصية الحقل عندما يتم حفظ القيم التي يوفرها التطبيق مرة أخرى إلى قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="eac54-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="eac54-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="eac54-168">isEditable (NoYes)</span></span>

<span data-ttu-id="eac54-169">قم بتعيين هذه الخاصية إلى **نعم** لتحديد أن الحقل الموجود في قسم إدخال الجدول الزمني يجب أن يكون قابلاً للتحرير من قِبل المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="eac54-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="eac54-170">قم بتعيين الخاصية إلى **لا** لجعل الحقل للقراءة فقط.</span><span class="sxs-lookup"><span data-stu-id="eac54-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="eac54-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="eac54-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="eac54-172">قم بتعيين هذه الخاصية إلى **نعم** لتحديد أن الحقل الموجود في قسم إدخال الجدول الزمني يجب أن يكون إلزاميًا.</span><span class="sxs-lookup"><span data-stu-id="eac54-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="eac54-173">التسمية (السلسلة)</span><span class="sxs-lookup"><span data-stu-id="eac54-173">label (str)</span></span>

<span data-ttu-id="eac54-174">تحدد هذه الخاصية التسمية التي تظهر بجانب الحقل في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="eac54-175">stringOptions (قائمة السلاسل)</span><span class="sxs-lookup"><span data-stu-id="eac54-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="eac54-176">لا تنطبق هذه الخاصية إلا في حالة تعيين **fieldBaseType** إلى **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="eac54-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="eac54-177">في حالة تعيين **stringOptions**، يتم تحديد قيم السلسلة المتاحة للتحديد عبر أزرار الخيارات (أزرار الاختيار) بواسطة السلاسل الموجودة في القائمة.</span><span class="sxs-lookup"><span data-stu-id="eac54-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="eac54-178">إذا لم يتم توفير سلاسل ، يُسمح بإدخال نص حر في حقل السلسلة (راجع قسم "استخدام سلسلة الأوامر في فئة TSTimesheetEntryService لحفظ إدخال الجدول الزمني من التطبيق مرة أخرى إلى قاعدة البيانات" لاحقًا في هذا الموضوع للحصول على مثال).</span><span class="sxs-lookup"><span data-stu-id="eac54-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="eac54-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="eac54-179">stringLength (int)</span></span>

<span data-ttu-id="eac54-180">تحدد هذه الخاصية الحد الأقصى لطول حقل السلسلة.</span><span class="sxs-lookup"><span data-stu-id="eac54-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="eac54-181">لا تنطبق هذه الخاصية إلا في حالة تعيين **fieldBaseType** إلى **سلسلة**.</span><span class="sxs-lookup"><span data-stu-id="eac54-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="eac54-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="eac54-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="eac54-183">تحدد هذه الخاصية عدد المنازل العشرية التي يتم عرضها لحقل حقيقي.</span><span class="sxs-lookup"><span data-stu-id="eac54-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="eac54-184">لا تنطبق هذه الخاصية إلا في حالة تعيين **fieldBaseType** إلى **حقيقية**.</span><span class="sxs-lookup"><span data-stu-id="eac54-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="eac54-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="eac54-185">orderSequence (int)</span></span>

<span data-ttu-id="eac54-186">تتحكم هذه الخاصية في الترتيب الذي تظهر به الحقول المخصصة في التطبيق عند تحديد أكثر من حقل مخصص.</span><span class="sxs-lookup"><span data-stu-id="eac54-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="eac54-187">يتم عرض الحقول التي تحتوي على أرقام أقل أولاً.</span><span class="sxs-lookup"><span data-stu-id="eac54-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="eac54-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="eac54-188">booleanValue (boolean)</span></span>

<span data-ttu-id="eac54-189">بالنسبة للحقول من نوع **Boolean**، تتجاوز هذه الخاصية القيمة المنطقية للحقل بين الخادم والتطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="eac54-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="eac54-190">guidValue (guid)</span></span>

<span data-ttu-id="eac54-191">بالنسبة للحقول من نوع **GUID**، تتجاوز هذه الخاصية قيمة المعرف الفريد العالمي (GUID) للحقل بين الخادم والتطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="eac54-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="eac54-192">int64Value (int64)</span></span>

<span data-ttu-id="eac54-193">بالنسبة للحقول من نوع **Int64**، تتجاوز هذه الخاصية قيمة Int64 للحقل بين الخادم والتطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="eac54-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="eac54-194">intValue (int)</span></span>

<span data-ttu-id="eac54-195">بالنسبة للحقول من نوع **Int**، تتجاوز هذه الخاصية قيمة Int للحقل بين الخادم والتطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="eac54-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="eac54-196">realValue (real)</span></span>

<span data-ttu-id="eac54-197">بالنسبة للحقول من نوع **Real**، تتجاوز هذه الخاصية القيمة الحقيقية للحقل بين الخادم والتطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="eac54-198">stringValue (السلسلة)</span><span class="sxs-lookup"><span data-stu-id="eac54-198">stringValue (str)</span></span>

<span data-ttu-id="eac54-199">بالنسبة للحقول من نوع **String**، تتجاوز هذه الخاصية قيمة السلسلة للحقل بين الخادم والتطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="eac54-200">وتُستخدم أيضًا في الحقول من نوع **Real** والتي تم تنسيقها كعملة.</span><span class="sxs-lookup"><span data-stu-id="eac54-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="eac54-201">بالنسبة لتلك الحقول، يتم استخدام الخاصية لتمرير رمز العملة إلى التطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="eac54-202">dateValue (التاريخ)</span><span class="sxs-lookup"><span data-stu-id="eac54-202">dateValue (date)</span></span>

<span data-ttu-id="eac54-203">بالنسبة للحقول من نوع **Date**، تمرر هذه الخاصية قيمة التاريخ للحقل بين الخادم والتطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="eac54-204">إظهار وحفظ حقل مخصص في قسم إدخال الجدول الزمني</span><span class="sxs-lookup"><span data-stu-id="eac54-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="eac54-205">يوجد أدناه لقطة شاشة من تطبيق الجوال لإنشاء إدخال الجدول الزمني.</span><span class="sxs-lookup"><span data-stu-id="eac54-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="eac54-206">إنها تعرض الحقول الخارجية والحقل المخصص في قسم "إدخال الوقت" المسمى "سلسلة الاختبار" مع تعيين قيمة التعداد لـ "الخيار الثاني" بالفعل.</span><span class="sxs-lookup"><span data-stu-id="eac54-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![اختبار حقل السلسلة المخصص في التطبيق](media/timesheet-entry.jpg)



<span data-ttu-id="eac54-208">يوجد أدناه لقطة شاشة من تطبيق الجوال للمستخدم يختار أحد خيارات التعداد المتاحة للحقل المخصص "سلسلة الاختبار".</span><span class="sxs-lookup"><span data-stu-id="eac54-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="eac54-209">الخياران هما "الخيار الأول" و"الخيار الثاني" ويظهران كأزرار اختيار.</span><span class="sxs-lookup"><span data-stu-id="eac54-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="eac54-210">الخيار الثاني محدد حاليًا.</span><span class="sxs-lookup"><span data-stu-id="eac54-210">The second option is currently selected.</span></span>

![أزرار الخيارات (أزرار الاختيار) للحقل المخصص لسلسلة الاختبار](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="eac54-212">توسيع جدول TSTimesheetLine بحيث يحتوي على حقل مخصص</span><span class="sxs-lookup"><span data-stu-id="eac54-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="eac54-213">في السيناريوهات النموذجية ، من المحتمل أن يتم حفظ البيانات الخاصة بحقل مخصص في قسم إدخال الجدول الزمني في جدول TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="eac54-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="eac54-214">ومع ذلك، يمكن استخدام الجداول الأخرى إذا كان يمكن استرداد البيانات بناءً على سجل TSTimesheetTrans الذي يتم توفيره، أو إذا لم يكن لديه سياق سجل محدد (على سبيل المثال، إذا تم تعيين الحقل للقراءة فقط في معلمات المشروع) .</span><span class="sxs-lookup"><span data-stu-id="eac54-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="eac54-215">لاحظ أن الحقول المخصصة لا يجب أن يكون لها أي سجلات قاعدة بيانات احتياطية.</span><span class="sxs-lookup"><span data-stu-id="eac54-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="eac54-216">يمكن إنشاؤها ديناميكيًا استنادًا إلى منطق X ++.</span><span class="sxs-lookup"><span data-stu-id="eac54-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="eac54-217">يمكن أن يكون هذا النهج مفيدًا في سيناريوهات القراءة فقط (راجع قسم "استخدام سلسلة الأوامر في فئة TSTimesheetDetails، أسلوب buildCustomFieldListForHeader لملء تفاصيل الجدول الزمني" للحصول على مثال لقيم الحقل المخصص التي تم إنشاؤها ديناميكيًا.)</span><span class="sxs-lookup"><span data-stu-id="eac54-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="eac54-218">فيما يلي لقطة شاشة من Visual Studio لشجرة مكونات البرنامج.</span><span class="sxs-lookup"><span data-stu-id="eac54-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="eac54-219">يعرض امتدادًا لجدول TSTimesheetLine مع إضافة حقل TestLineString كحقل مخصص.</span><span class="sxs-lookup"><span data-stu-id="eac54-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![سلسلة السطر](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="eac54-221">استخدم سلسلة الأوامر في أسلوب buildCustomFieldList للفئة TSTimesheetSettings لإظهار حقل في قسم إدخال الجدول الزمني</span><span class="sxs-lookup"><span data-stu-id="eac54-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="eac54-222">يتحكم هذا الكود في إعدادات العرض للحقل في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="eac54-223">على سبيل المثال ، يتحكم في نوع الحقل والتسمية وما إذا كان الحقل إلزاميًا وفي القسم الذي يظهر فيه الحقل.</span><span class="sxs-lookup"><span data-stu-id="eac54-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="eac54-224">يوضح المثال التالي حقل سلسلة في إدخالات الوقت.</span><span class="sxs-lookup"><span data-stu-id="eac54-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="eac54-225">يحتوي هذا الحقل على خيارين، **الخيار الأول** و**الخيار الثاني**، المتوفرين من خلال أزرار الخيار (أزرار الاختيار).</span><span class="sxs-lookup"><span data-stu-id="eac54-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="eac54-226">والجقل الموجود في التطبيق مرتبط بحقل **TestLineString** الذي تمت إضافته إلى جدول TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="eac54-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="eac54-227">تجدر الإشارة إلى استخدام طريقة **TSTimesheetCustomField::newFromMetatdata()** لتبسيط تهيئة خصائص الحقول المخصصة: **fieldBaseType**، و**tableName**، و**fieldname**، و**label**، و**isEditable**، و**isMandatory**، و**stringLength**، و**numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="eac54-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="eac54-228">يمكنك أيضًا ضبط هذه المعلمات يدويًا ، حسب رغبتك.</span><span class="sxs-lookup"><span data-stu-id="eac54-228">You can also set these parameters manually, as you prefer.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="eac54-229">استخدم سلسلة الأوامر في طريقة buildCustomFieldListForEntry للفئة TSTimesheetEntry لإدخال القيم في إدخال الجدول الزمني</span><span class="sxs-lookup"><span data-stu-id="eac54-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="eac54-230">يتم استخدام أسلوب **buildCustomFieldListForEntry** لإدخال القيم في أسطر الجداول الزمنية المحفوظة في تطبيق الأجهزه المحمولة.</span><span class="sxs-lookup"><span data-stu-id="eac54-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="eac54-231">يأخذ سجل TSTimesheetTrans كمعلمة.</span><span class="sxs-lookup"><span data-stu-id="eac54-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="eac54-232">يمكن استخدام الحقول من هذا السجل لملء قيمة الحقل المخصص في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="eac54-233">استخدم سلسلة الأوامر في فئة TSTimesheetEntryService لحفظ إدخال الجدول الزمني من التطبيق مرة أخرى إلى قاعدة البيانات</span><span class="sxs-lookup"><span data-stu-id="eac54-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="eac54-234">لحفظ حقل مخصص مرة أخرى إلى قاعدة البيانات في استخدام نموذجي ، يجب توسيع طرق متعددة:</span><span class="sxs-lookup"><span data-stu-id="eac54-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="eac54-235">يتم استخدام أسلوب **timesheetLineNeedsUpdating** لتحديد ما إذا كان قد تم تغيير سجل السطر من قِبل المستخدم في التطبيق ويجب حفظه في قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="eac54-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="eac54-236">إذا لم يكن الأداء مصدر قلق ، فيمكن تبسيط هذه الطريقة بحيث تعرض دائمًا **true**.</span><span class="sxs-lookup"><span data-stu-id="eac54-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="eac54-237">يمكن توسيع الأسلوبين **populateTimesheetLineFromEntryDuringCreate** و**populateTimesheetLineFromEntryDuringUpdate** بحيث يقومان بإدخال قيم في سجل قاعدة بيانات TSTimesheetLine من سجل عقد بيانات TSTimesheetEntry الذي يتم توفيره.</span><span class="sxs-lookup"><span data-stu-id="eac54-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="eac54-238">في المثال التالي ، لاحظ كيفية إجراء التعيين بين حقل قاعدة البيانات وحقل الإدخال يدويًا عبر رمز X ++.</span><span class="sxs-lookup"><span data-stu-id="eac54-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="eac54-239">يمكن أيضًا توسيع أسلوب **populateTimesheetWeekFromEntry** إذا كان الحقل المخصص الذي تم تعيينه إلى كائن **TSTimesheetEntry** يجب إعادة كتابته لجدول قاعدة البيانات TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="eac54-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="eac54-240">يقوم المثال التالي بحفظ قيمة **firstOption** أو **secondOption** الذي يقوم المستخدم بتحديده لقاعدة البيانات كقيمة سلسلة بسيطة.</span><span class="sxs-lookup"><span data-stu-id="eac54-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="eac54-241">إذا كان حقل قاعدة البيانات هو حقل من نوع **التعداد**، فإنه يمكن تعيين هذه القيم يدويًا إلى قيمه تعداد ثم حفظها إلى حقل تعداد في جدول قاعده البيانات.</span><span class="sxs-lookup"><span data-stu-id="eac54-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="eac54-242">إظهار وحفظ حقل مخصص في قسم رأس الجدول الزمني</span><span class="sxs-lookup"><span data-stu-id="eac54-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="eac54-243">يوجد أدناه لقطة شاشة من تطبيق الجوال لمستخدم يشاهد جدولًا زمنيًا.</span><span class="sxs-lookup"><span data-stu-id="eac54-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="eac54-244">تم تحديد زر "مزيد من المعلومات" في الزاوية العلوية اليمنى لإظهار خيار "عرض مزيد من التفاصيل".</span><span class="sxs-lookup"><span data-stu-id="eac54-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![أمر عرض المزيد من التفاصيل](media/show-more.png)



<span data-ttu-id="eac54-246">يوجد أدناه لقطة شاشة من تطبيق الجوال تعرض قسم "المزيد" في جدول زمني.</span><span class="sxs-lookup"><span data-stu-id="eac54-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="eac54-247">تمت إضافة حقل مخصص يسمى "معدل استخدام الجدول الزمني هذا (حقل مخصص محسوب)" إلى قسم رأس الجدول الزمني.</span><span class="sxs-lookup"><span data-stu-id="eac54-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="eac54-248">يتم تعيين قيمة للقراءة فقط "0.667" في الحقل المخصص.</span><span class="sxs-lookup"><span data-stu-id="eac54-248">A read-only value of "0.667" is set on the custom field.</span></span>

![قسم المزيد](media/more-section.jpg)



### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="eac54-250">توسيع جدول TSTimesheetTable بحيث يحتوي على حقل مخصص</span><span class="sxs-lookup"><span data-stu-id="eac54-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="eac54-251">في السيناريوهات النموذجية ، من المحتمل أن يتم سحب البيانات الخاصة بحقل مخصص في قسم الرأس من جدول TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="eac54-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="eac54-252">ومع ذلك ، يمكن استخدام الجداول الأخرى إذا كان يمكن استرداد البيانات استنادًا إلى سجل TSTimesheetTable الذي تم توفيره ، أو إذا لم يكن لديه سياق سجل محدد (على سبيل المثال ، إذا تم تعيين الحقل للقراءة فقط في معلمات المشروع).</span><span class="sxs-lookup"><span data-stu-id="eac54-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="eac54-253">لاحظ أن الحقول المخصصة لا يجب أن يكون لها أي سجلات قاعدة بيانات احتياطية.</span><span class="sxs-lookup"><span data-stu-id="eac54-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="eac54-254">يمكن إنشاؤها ديناميكيًا استنادًا إلى منطق X ++.</span><span class="sxs-lookup"><span data-stu-id="eac54-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="eac54-255">يوضح المثال التالي هذا النهج.</span><span class="sxs-lookup"><span data-stu-id="eac54-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="eac54-256">تكون الحقول الموجودة في قسم الرأس دائمًا للقراءة فقط في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="eac54-257">استخدم سلسلة الأوامر في أسلوب buildCustomFieldList للفئة TSTimesheetSettings لإظهار حقل في قسم الرأس</span><span class="sxs-lookup"><span data-stu-id="eac54-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="eac54-258">يتحكم هذا الكود في إعدادات العرض للحقل في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="eac54-259">على سبيل المثال ، يتحكم في نوع الحقل والتسمية وما إذا كان الحقل إلزاميًا وفي القسم الذي يظهر فيه الحقل.</span><span class="sxs-lookup"><span data-stu-id="eac54-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="eac54-260">يوضح المثال التالي قيمة محسوبة في قسم الرأس في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-260">The following example shows a computed value in the header section in the app.</span></span>

```
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="eac54-261">استخدم سلسلة الأوامر في أسلوب buildCustomFieldListForHeader للفئة TSTimesheetDetails لملء تفاصيل الجدول الزمني</span><span class="sxs-lookup"><span data-stu-id="eac54-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="eac54-262">يتم استخدام أسلوب **buildCustomFieldListForHeader** لملء تفاصيل رأس الجدول الزمني في تطبيق الجوال.</span><span class="sxs-lookup"><span data-stu-id="eac54-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="eac54-263">يأخذ سجل TSTimesheetTable كمعلمة.</span><span class="sxs-lookup"><span data-stu-id="eac54-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="eac54-264">يمكن استخدام الحقول من هذا السجل لملء قيمة الحقل المخصص في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="eac54-265">المثال التالي لا يقرأ أي قيم من قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="eac54-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="eac54-266">بدلاً من ذلك، يستخدم منطق X ++ لإنشاء قيمة محسوبة تظهر في التطبيق.</span><span class="sxs-lookup"><span data-stu-id="eac54-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="eac54-267">فرص إمكانية التكوين/إمكانية التوسيع الأخرى</span><span class="sxs-lookup"><span data-stu-id="eac54-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="eac54-268">إضافة تحقق إضافي للتطبيق</span><span class="sxs-lookup"><span data-stu-id="eac54-268">Adding additional validation for the app</span></span>

<span data-ttu-id="eac54-269">المنطق الحالي لوظيفة الجدول الزمني على مستوى قاعدة البيانات سيظل يعمل كما هو متوقع.</span><span class="sxs-lookup"><span data-stu-id="eac54-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="eac54-270">لمقاطعة إتمام حفظ أو إرسال العمليات وإظهار رسالة خطأ محددة، يمكنك إضافة **طرح خطأ ("رسالة إلى المستخدم")** إلى الكود عبر سلسلة من تمديد الأوامر.</span><span class="sxs-lookup"><span data-stu-id="eac54-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="eac54-271">فيما يلي ثلاثة أمثلة للطرق القابلة للتوسعة المفيدة:</span><span class="sxs-lookup"><span data-stu-id="eac54-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="eac54-272">إذا قام **validateWrite** في جدول TSTimesheetLine بإرجاع **false** أثناء عمليه حفظ لسطر جدول زمني، تظهر رسالة خطأ في تطبيق الأجهزه المحمولة.</span><span class="sxs-lookup"><span data-stu-id="eac54-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="eac54-273">إذا قام **validateSubmit** في جدول TSTimesheetTable بإرجاع **false** أثناء إرسال الجدول الزمني في التطبيق، يتم عرض رسالة خطأ للمستخدم.</span><span class="sxs-lookup"><span data-stu-id="eac54-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="eac54-274">المنطق الذي يعبئ الحقول (على سبيل المثال **خاصية السطر**) أثناء **إدخال** الأسلوب في جدول TSTimesheetLine سيظل يعمل.</span><span class="sxs-lookup"><span data-stu-id="eac54-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="eac54-275">إخفاء الحقول الخارجية ووضع علامة عليها للقراءة فقط عبر التكوين</span><span class="sxs-lookup"><span data-stu-id="eac54-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="eac54-276">من معلمات المشروع ، يمكنك جعل الحقول الجاهزة للقراءة فقط أو مخفية في تطبيق الجوال.</span><span class="sxs-lookup"><span data-stu-id="eac54-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="eac54-277">قم بتعيين الخيارات في قسم **الجداول الزمنية للأجهزة المحمولة** في علامة التبويب **الجدول الزمني** في صفحة **محددات إدارة المشاريع ومحاسبتها‬**.</span><span class="sxs-lookup"><span data-stu-id="eac54-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![محددات المشروع](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="eac54-279">تغيير الأنشطة المتاحة للاختيار عبر التوسيعات</span><span class="sxs-lookup"><span data-stu-id="eac54-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="eac54-280">يتم ملء الأنشطة المتاحة للتحديد الخاص بأحد المشاريع من خلال أساليب **getActivitiesForProject()** and **getActivityQuery()** في فئة **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="eac54-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="eac54-281">يمكنك استخدام سلسلة الأوامر لتغيير هذا السلوك لمطابقة سيناريو عملك للأنشطة المتاحة للاختيار لمشروع معين.</span><span class="sxs-lookup"><span data-stu-id="eac54-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="eac54-282">إدخال فئة المشروع الافتراضية في إدخالات الجدول الزمني</span><span class="sxs-lookup"><span data-stu-id="eac54-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="eac54-283">يحدث إدخال فئة المشروع الافتراضية في إدخالات الجدول الزمني على ثلاثة مستويات.</span><span class="sxs-lookup"><span data-stu-id="eac54-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="eac54-284">يمكنك استخدام سلسلة الأوامر لتوسيع السلوك في أي من هذه المستويات أو كلها لتحقيق السلوك المطلوب.</span><span class="sxs-lookup"><span data-stu-id="eac54-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="eac54-285">يتم استخدام التدرج الهرمي التالي:</span><span class="sxs-lookup"><span data-stu-id="eac54-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="eac54-286">يحاول التطبيق وضع الفئة الافتراضية من مورد المشروع.</span><span class="sxs-lookup"><span data-stu-id="eac54-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="eac54-287">يتم تعيين هذه الفئة الافتراضية في أسلوبي **getCurrentUserResource** و**getDelegatedResourcesForCurrentUser** في فئة **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="eac54-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="eac54-288">إذا لم يتم توفير الفئة الافتراضية على مستوى مورد المشروع، فسيحاول التطبيق سحبها من نشاط المشروع.</span><span class="sxs-lookup"><span data-stu-id="eac54-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="eac54-289">يتم تعيين هذه الفئة الافتراضية في أسلوب **getActivitiesForProject** في فئة **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="eac54-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="eac54-290">إذا لم يتم توفير الفئة الافتراضية على مستوى نشاط المشروع، فستكون الفئة الافتراضية مأخوذة من معلمات المشروع.</span><span class="sxs-lookup"><span data-stu-id="eac54-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="eac54-291">يتم تعيين هذه الفئة الافتراضية في أسلوب **getProjectDetailsbyRule** في فئة **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="eac54-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>
