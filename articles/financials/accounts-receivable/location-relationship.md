---
title: "إضافة موقع وأنواع علاقات الأطراف"
description: "يشرح هذا الموضوع كيفية إضافة موقع جديد وعلاقة طرف."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: 543784e8072f88c10f63e1b44921b9f2d37308c3
ms.contentlocale: ar-sa
ms.lasthandoff: 09/17/2018

---

# <a name="add-location-roles-and-party-relationship-types"></a><span data-ttu-id="34295-103">إضافة أدوار مواقع وأنواع علاقات الأطراف</span><span class="sxs-lookup"><span data-stu-id="34295-103">Add location roles and party relationship types</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a><span data-ttu-id="34295-104">إضافة أدوار المواقع</span><span class="sxs-lookup"><span data-stu-id="34295-104">Add location roles</span></span>

<span data-ttu-id="34295-105">توجد طريقتان لإضافة أدوار مواقع جديدة للعنوان ومعلومات جهة الاتصال:</span><span class="sxs-lookup"><span data-stu-id="34295-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="34295-106">أضفها إلى صفحة **‏‫الغرض من معلومات العنوان وجهة الاتصال‬**.</span><span class="sxs-lookup"><span data-stu-id="34295-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="34295-107">سيتم حفظ الدور الجديد في الجدول **LogisticsLocationRole** بنوع = 0، الذي يشير إلى أن الدور ليس دور نظام محدد في تعداد **LogisticsLocationRoleType** وملحقاته.</span><span class="sxs-lookup"><span data-stu-id="34295-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="34295-108">سيكون المستخدم قادراً على استخدام هذا الدور عند إنشاء عنوان أو معلومات جهة الاتصال.</span><span class="sxs-lookup"><span data-stu-id="34295-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![الغرض من معلومات المحتوى وجهة الاتصال](media/Address-Contact.PNG)

-  <span data-ttu-id="34295-110">أضفها إلى ملحق تعداد **LogisticsLocationRoleType**، وانشرها خلال عملية مزامنة قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="34295-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="34295-111">قم بإنشاء ملحق لتعداد **LogisticsLocationRoleType** وأضف الدور الجديد في الامتداد.</span><span class="sxs-lookup"><span data-stu-id="34295-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. <span data-ttu-id="34295-113">قم بإنشاء ملف مورد للدور الجديد، ثم قم بتعيين قيمة للخصائص.</span><span class="sxs-lookup"><span data-stu-id="34295-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![ملف مورد جديد](media/Resource.PNG)
        
    3.  <span data-ttu-id="34295-115">قم بإنشاء فئة لنشر البيانات واستخدم طريقة المعالج لنشر الدور الجديد.</span><span class="sxs-lookup"><span data-stu-id="34295-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![نشر البيانات](media/Dirdata.PNG)

    4.  <span data-ttu-id="34295-117">لاختبار نشر دور الموقع الجديد، فإنه يمكنك إنشاء فئة قابلة للتشغيل، واطلب DirDataPopulation::insertLogisticsLocationRoles() في Main().</span><span class="sxs-lookup"><span data-stu-id="34295-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="34295-118">بعد إكمال هذه العملية، فإنه ينبغي عليك رؤية الدور الجديد المنشور في الجدول **LogisticsLocationRole** من نوع \> 0.</span><span class="sxs-lookup"><span data-stu-id="34295-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="34295-119">سيتم عرض الدور الجديد على **‏‫الغرض من معلومات العنوان وجهة الاتصال‬**.</span><span class="sxs-lookup"><span data-stu-id="34295-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![إدراج موقع جديد](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a><span data-ttu-id="34295-121">إضافة أنواع علاقات الأطراف</span><span class="sxs-lookup"><span data-stu-id="34295-121">Add party relationship types</span></span> 

<span data-ttu-id="34295-122">هناك طريقتان لإضافة نوع علاقة جديد:</span><span class="sxs-lookup"><span data-stu-id="34295-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="34295-123">إضافتها خلال الصفحة **أنواع العلاقات**.</span><span class="sxs-lookup"><span data-stu-id="34295-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="34295-124">سيتم حفظ العلاقة الجديدة على **DirRelationshipTypeTable** باستخدام systemtype = 0.</span><span class="sxs-lookup"><span data-stu-id="34295-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![أنواع العلاقات](media/Relationship.PNG)

-  <span data-ttu-id="34295-126">إضافتها في ملحق تعداد **DirSystemRelationshipType**، ونشرها خلال عملية مزامنة قاعدة البيانات.</span><span class="sxs-lookup"><span data-stu-id="34295-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="34295-127">قم بإنشاء التعداد **DirSystemRelationship** وأضف نوع العلاقة الجديد.</span><span class="sxs-lookup"><span data-stu-id="34295-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="34295-128">قم بإنشاء مهيئ لهذا النوع الجديد.</span><span class="sxs-lookup"><span data-stu-id="34295-128">Create an initializer for this new type.</span></span> <span data-ttu-id="34295-129">يمكنك العثور على أمثلة متعددة في الكود الأساسي، أحدها هو **DirRelationshipTypeChildInitialize**.</span><span class="sxs-lookup"><span data-stu-id="34295-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="34295-130">إنها فئة مهيئ لنوع علاقة طرف "تابع".</span><span class="sxs-lookup"><span data-stu-id="34295-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="34295-131">يمكنك البدء بالمهيئ الخاص بك عن طريق نسخ ولصق هذا الكود ثم قم بتحديث المناطق المميزة.</span><span class="sxs-lookup"><span data-stu-id="34295-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  <span data-ttu-id="34295-133">لاختبار نشر نوع العلاقة الجديد، فإنه يمكنك إنشاء فئة قابلة للتشغيل، واطلب DirDataPopulation::insertDirRelationshipTypes() في Main().</span><span class="sxs-lookup"><span data-stu-id="34295-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="34295-134">ينبغي عليك رؤية نوع العلاقة الجديد في **DirRelationshipTypeTable**، ثم سيتوافر نوع العلاقة الجديد على صفحة **أنواع العلاقات**.</span><span class="sxs-lookup"><span data-stu-id="34295-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![فئة قابلة للتشغيل](media/Runnable.PNG)

