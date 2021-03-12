---
title: إنشاء أصل ثابت
description: يوضح هذا الموضوع كيفية إنشاء سجل أصل ثابت جديد من صفحة قائمة الأصول الثابتة.
author: moaamer
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab330c604b2485687544a7d8b3eef3a652fa2069
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985127"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="5c694-103">إنشاء أصل ثابت</span><span class="sxs-lookup"><span data-stu-id="5c694-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5c694-104">يوضح هذا الموضوع كيفية إنشاء سجل أصل ثابت جديد من صفحة قائمة **الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="5c694-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="5c694-105">يقوم النظام بتعيين رقم الأصل، استنادًا إلى التسلسل الرقمي الذي يتم تعيينه إلى مجموعة الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="5c694-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="5c694-106">إذا كنت تستخدم قالب الأصل الثابت لاستيراد الأصول من خلال وظيفة Microsoft Excel الإضافية، أو إذا كنت تستخدم وظيفة استيراد أخرى، يقوم النظام تلقائيًا بإنشاء سجلات الأصول الثابتة وزيادات رقم الأصل.</span><span class="sxs-lookup"><span data-stu-id="5c694-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="5c694-107">لإنشاء سجل أصل يدويًا، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5c694-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="5c694-108">انتقل إلى **جزء التنقل \> الوحدات النمطية \> الأصول الثابتة \> الأصول الثابتة \> الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="5c694-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="5c694-109">في **جزء الإجراء**، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="5c694-109">On the **Action pane**, select **New**.</span></span>
3. <span data-ttu-id="5c694-110">في حقل **مجموعة الأصول الثابتة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="5c694-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="5c694-111">سيتم تعيين حقل **الرقم** بشكل افتراضي إذا قمت بتمكين الوظيفة **الترقيم التلقائي للأصول الثابتة‬** في **محددات الأصول الثابتة** و **مجموعة الأصول الثابتة**.</span><span class="sxs-lookup"><span data-stu-id="5c694-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="5c694-112">وإلا، فيجب إدخال رقم فريد لتعريف الأصل الثابت.</span><span class="sxs-lookup"><span data-stu-id="5c694-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="5c694-113">في حقل **الاسم**، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="5c694-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="5c694-114">أدخل المعلومات الإضافية التي تحتاج إليها شركتك لهذا الأصل.</span><span class="sxs-lookup"><span data-stu-id="5c694-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="5c694-115">في **جزء الإجراء**، حدد **دفاتر**.</span><span class="sxs-lookup"><span data-stu-id="5c694-115">On the **Action pane**, select **Books**.</span></span>
6. <span data-ttu-id="5c694-116">أدخل تاريخًا في حقل **تاريخ الاستحواذ**.</span><span class="sxs-lookup"><span data-stu-id="5c694-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="5c694-117">أدخل رقمًا في حقل **سعر الاستحواذ**.</span><span class="sxs-lookup"><span data-stu-id="5c694-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="5c694-118">أدخل المعلومات الإضافية التي تحتاج إليها شركتك لهذا الدفتر.</span><span class="sxs-lookup"><span data-stu-id="5c694-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="5c694-119">أدخل المعلومات الإضافية التي تحتاج إليها شركتك للدفاتر المتبقية.</span><span class="sxs-lookup"><span data-stu-id="5c694-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="5c694-120">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="5c694-120">Close the page.</span></span>

<span data-ttu-id="5c694-121">يمكنك أيضًا استيراد الأصول الثابتة باستخدام وظيفة Excel الإضافية أو عن طريق تشغيل وظيفة استيراد من مساحة عمل **إدارة البيانات**.</span><span class="sxs-lookup"><span data-stu-id="5c694-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="5c694-122">قبل أن تقوم بتشغيل الاستيراد، أدخل قيم الحقول المطلوبة في القالب.</span><span class="sxs-lookup"><span data-stu-id="5c694-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="5c694-123">إذا لم تقم بتحديد رقم الأصل الثابت في قالب وظيفة Excel الإضافية، أو في إدارة البيانات، يقوم النظام بإنشاء رقم أصل ثابت لكل أصل تم استيراده ويقوم تلقائيًا بزيادة التسلسل الرقمي لكل منها.</span><span class="sxs-lookup"><span data-stu-id="5c694-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="5c694-124">ومع ذلك، إذا قمت باستيراد الأصول وتحديد أرقام الأصول في القالب، **فلن** يقوم النظام تلقائيًا بزيادة التسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="5c694-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="5c694-125">في هذه الحالة، قد يتوجب على المسؤول تحديث التسلسل الرقمي يدويًا.</span><span class="sxs-lookup"><span data-stu-id="5c694-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="5c694-126">إذا قمت بتحديد رقم الأصل الثابت في قالب وظيفة Excel الإضافية، يستخدم النظام رقم الأصل الثابت المحدد ويقوم بزيادة التسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="5c694-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="5c694-127">بعد ترحيل الإهلاك، فإنه سيتم تأمين الحقلين **نهاية التضمين بالخدمة** و **تاريخ بدء الإهلاك** في الصفحة **الدفتر**.</span><span class="sxs-lookup"><span data-stu-id="5c694-127">After posting the depreciation, the **Placed in service** and **Depreciation run date** fields will be locked on the **Book** page.</span></span> <span data-ttu-id="5c694-128">كذلك، لن يتم تحديث كلا الحقلين من كيان البيانات.</span><span class="sxs-lookup"><span data-stu-id="5c694-128">Also, both neither field will be updated from the data entity.</span></span>

> [!WARNING]
> <span data-ttu-id="5c694-129">لن يتم حذف سجل الأصل الثابت إذا تم ترحيل الحركات إلى الدفتر المقترن، أو إذا تم إدخال الأصل الثابت الذي تم إنشاؤه حديثًا في بند دفتر اليومية ولكن لم يتم ترحيله.</span><span class="sxs-lookup"><span data-stu-id="5c694-129">The fixed asset record won't be deleted if transactions were posted to the associated book, or if the newly created fixed asset is entered on a journal line but not posted.</span></span> 
