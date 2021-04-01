---
title: تحديد الأبعاد المالية
description: يوضح دليل المهام هذا إضافة البعد المالي المدعوم من الكيان والبعد المالي المخصص.
author: aprilolson
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionDetails,  DimensionAttributeTableExtensionActivate, DimensionValueDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf0136f216e5aa04cfae35afdb02d79893a6d39c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240728"
---
# <a name="define-financial-dimensions"></a><span data-ttu-id="25e0d-103">تحديد الأبعاد المالية</span><span class="sxs-lookup"><span data-stu-id="25e0d-103">Define financial dimensions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25e0d-104">يوضح دليل المهام هذا إضافة البعد المالي المدعوم من الكيان والبعد المالي المخصص.</span><span class="sxs-lookup"><span data-stu-id="25e0d-104">This task guide demonstrates adding an entity backed financial dimension and a custom financial dimension.</span></span>  <span data-ttu-id="25e0d-105">يستخدم هذا الدليل شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="25e0d-105">The guide uses the USMF demo company.</span></span>


## <a name="create-an-entity-backed-financial-dimension"></a><span data-ttu-id="25e0d-106">إنشاء بُعد مالي مدعوم من الكيان</span><span class="sxs-lookup"><span data-stu-id="25e0d-106">Create an entity backed financial dimension</span></span>
1. <span data-ttu-id="25e0d-107">انتقل إلى **جزء التنقل > الوحدات النمطية > دفتر الأستاذ العام > دليل الحسابات > الأبعاد > الأبعاد المالية**.</span><span class="sxs-lookup"><span data-stu-id="25e0d-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Dimensions > Financial dimensions**.</span></span>
2. <span data-ttu-id="25e0d-108">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="25e0d-108">Click **New**.</span></span>
3. <span data-ttu-id="25e0d-109">في الحقل **نموذج قيم المستخدمين**، حدد كيانًا محددًا بواسطة النظام ليعتمد البُعد المالي عليه.</span><span class="sxs-lookup"><span data-stu-id="25e0d-109">In the **User values form** field, select a system-defined entity to base the financial dimension on.</span></span> 
4. <span data-ttu-id="25e0d-110">في الحقل **اسم البُعد**، اكتب قيمة لوصف البُعد المالي.</span><span class="sxs-lookup"><span data-stu-id="25e0d-110">In the **Dimension name** field, type a value to describe the financial dimension.</span></span> <span data-ttu-id="25e0d-111">قد يكون الاسم مختلفًا عن الكيان المحدد بواسطة النظام، ولكن لا يمكن أن يحتوي على مسافات أو أحرف خاصة.</span><span class="sxs-lookup"><span data-stu-id="25e0d-111">The name can be different than the system-defined entity but cannot contain spaces or special characters.</span></span>
5. <span data-ttu-id="25e0d-112">انقر فوق **تنشيط**.</span><span class="sxs-lookup"><span data-stu-id="25e0d-112">Click **Activate**.</span></span> <span data-ttu-id="25e0d-113">يؤدي تنشيط البُعد المالي إلى تحديث الجدول باسم البُعد المالي وإزالة الأبعاد المحذوفة.</span><span class="sxs-lookup"><span data-stu-id="25e0d-113">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="25e0d-114">يمكنك إدخال قيم الأبعاد قبل تنشيط بُعد مالي، ولكن لا يمكن استخدام بُعد مالي حتى يتم تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="25e0d-114">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>  
6. <span data-ttu-id="25e0d-115">انقر فوق **إغلاق** على رسالة التنشيط.</span><span class="sxs-lookup"><span data-stu-id="25e0d-115">Click **Close** on the activation message.</span></span>
7. <span data-ttu-id="25e0d-116">انقر فوق **تنشيط**.</span><span class="sxs-lookup"><span data-stu-id="25e0d-116">Click **Activate**.</span></span> <span data-ttu-id="25e0d-117">يمكن جدولة تنشيط البُعد لتشغيله على أساس الدفعة في وقت وتاريخ معينين.</span><span class="sxs-lookup"><span data-stu-id="25e0d-117">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>  
8. <span data-ttu-id="25e0d-118">في **جزء الإجراءات**، انقر فوق **قيم الأبعاد**.</span><span class="sxs-lookup"><span data-stu-id="25e0d-118">On **Action pane**, click **Dimension values**.</span></span> <span data-ttu-id="25e0d-119">تكون بعض قيم الأبعاد خاصة بشركة معينة.</span><span class="sxs-lookup"><span data-stu-id="25e0d-119">Some dimension values are company specific.</span></span> <span data-ttu-id="25e0d-120">يمكنك التحقق مما إذا كان قيم الأبعاد خاصة بشركة معينة إذا ظهر اسم الشركة في قائمة قيم الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="25e0d-120">You can verify if they are company specific by if the company name is showing in the dimension values list.</span></span>  

## <a name="create-a-custom-financial-dimension"></a><span data-ttu-id="25e0d-121">إنشاء بُعد مالي مخصص</span><span class="sxs-lookup"><span data-stu-id="25e0d-121">Create a custom financial dimension</span></span>
1. <span data-ttu-id="25e0d-122">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="25e0d-122">Close the page.</span></span>
2. <span data-ttu-id="25e0d-123">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="25e0d-123">Click **New**.</span></span>
3. <span data-ttu-id="25e0d-124">في حقل **استخدام القيم من**، حدد **البُعد المخصص**.</span><span class="sxs-lookup"><span data-stu-id="25e0d-124">In the **Use values from** field, select **Custom dimension**.</span></span>
4. <span data-ttu-id="25e0d-125">في الحقل **اسم البُعد**، اكتب قيمة لوصف البُعد المالي.</span><span class="sxs-lookup"><span data-stu-id="25e0d-125">In the **Dimension name** field, type a value to describe the financial dimension.</span></span>
    - <span data-ttu-id="25e0d-126">لا يمكن أن يحتوي الاسم على مسافات أو أحرف خاصة.</span><span class="sxs-lookup"><span data-stu-id="25e0d-126">The name cannot contain spaces or special characters.</span></span>  
    - <span data-ttu-id="25e0d-127">يمكنك أيضًا تعيين قناع تنسيق لتقييد كمية ونوع المعلومات التي تستطيع إدخالها لقيم الأبعاد.</span><span class="sxs-lookup"><span data-stu-id="25e0d-127">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span>   
    - <span data-ttu-id="25e0d-128">تستطيع إدخال الحروف التي تظل كما هي لكل قيمة بعد مثل الأحرف أو واصلة.</span><span class="sxs-lookup"><span data-stu-id="25e0d-128">You can enter characters that remain the same for each dimension value, such as letters or a hyphen.</span></span> <span data-ttu-id="25e0d-129">كما تستطيع إدخال علامات الأرقام (#) وعلامات العطف (&) كعناصر نائبة للأحرف والأرقام التي ستتغير كل مرة يتم إنشاء قيمة بعد.</span><span class="sxs-lookup"><span data-stu-id="25e0d-129">You can also enter number signs (#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="25e0d-130">استخدم علامة الأرقام (#) كعنصر نائب لرقم وعلامة العطف (&) كعنصر نائب عن حرف.</span><span class="sxs-lookup"><span data-stu-id="25e0d-130">Use a number sign (#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span>  <span data-ttu-id="25e0d-131">مثال: لتقييد قيمة البُعد على الحرفين CC وثلاثة أرقام، أدخل CC-### كقناع تنسيق.</span><span class="sxs-lookup"><span data-stu-id="25e0d-131">Example: To limit the dimension value to the letters CC and three numbers, you enter CC-### as the format mask.</span></span>  
5. <span data-ttu-id="25e0d-132">انقر فوق **تنشيط**.</span><span class="sxs-lookup"><span data-stu-id="25e0d-132">Click **Activate**.</span></span> <span data-ttu-id="25e0d-133">يؤدي تنشيط البُعد المالي إلى تحديث الجدول باسم البُعد المالي وإزالة الأبعاد المحذوفة.</span><span class="sxs-lookup"><span data-stu-id="25e0d-133">Activating the financial dimension updates the table with the financial dimension name and removes deleted dimensions.</span></span> <span data-ttu-id="25e0d-134">يمكنك إدخال قيم الأبعاد قبل تنشيط بُعد مالي، ولكن لا يمكن استخدام بُعد مالي حتى يتم تنشيطه.</span><span class="sxs-lookup"><span data-stu-id="25e0d-134">You can enter dimension values before you activate a financial dimension, but a financial dimension cannot be used until it is activated.</span></span>     
6. <span data-ttu-id="25e0d-135">انقر فوق **تنشيط**.</span><span class="sxs-lookup"><span data-stu-id="25e0d-135">Click **Activate**.</span></span> <span data-ttu-id="25e0d-136">يمكن جدولة تنشيط البُعد لتشغيله على أساس الدفعة في وقت وتاريخ معينين.</span><span class="sxs-lookup"><span data-stu-id="25e0d-136">Dimension activation can be scheduled to run by batch at a specific date and time.</span></span>      
7. <span data-ttu-id="25e0d-137">في **جزء الإجراءات**، انقر فوق **قيم الأبعاد**.</span><span class="sxs-lookup"><span data-stu-id="25e0d-137">On **Action pane**, click **Dimension values**.</span></span>
8. <span data-ttu-id="25e0d-138">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="25e0d-138">Click **New**.</span></span>
9. <span data-ttu-id="25e0d-139">في الحقل **قيمة البُعد**، اكتب اسمًا لوصف قيمة البعد المالي.</span><span class="sxs-lookup"><span data-stu-id="25e0d-139">In the **Dimension value** field, type a name to describe your financial dimension value.</span></span>
10. <span data-ttu-id="25e0d-140">في الحقل **الوصف**، اكتب وصفًا يصف قيمة البُعد المالي.</span><span class="sxs-lookup"><span data-stu-id="25e0d-140">In the **Description** field, type a description that describes your financial dimension value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]