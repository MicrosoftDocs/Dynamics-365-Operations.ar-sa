---
title: إعداد الفصل بين المهام
description: يمكنك إعداد قواعد لفصل المهام التي يجب تنفيذها بواسطة مستخدمين مختلفين.
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1c1521d6bbbe12964fef0942fcc4943f12a4360a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562487"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="d84c9-103">إعداد الفصل بين المهام</span><span class="sxs-lookup"><span data-stu-id="d84c9-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d84c9-104">يمكنك إعداد قواعد لفصل المهام التي يجب تنفيذها بواسطة مستخدمين مختلفين.</span><span class="sxs-lookup"><span data-stu-id="d84c9-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="d84c9-105">يسمى هذا المفهوم الفصل بين المهام.</span><span class="sxs-lookup"><span data-stu-id="d84c9-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="d84c9-106">على سبيل المثال، قد لا تريد أن يقر نفس الشخص بكل من استلام البضائع ومعالجة الدفع للمورد.</span><span class="sxs-lookup"><span data-stu-id="d84c9-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="d84c9-107">يساعدك الفصل بين المهام في الحد من مخاطر الغش كما يساعدك أيضًا على اكتشاف الأخطاء أو المخالفات.</span><span class="sxs-lookup"><span data-stu-id="d84c9-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="d84c9-108">يمكنك أيضا استخدام الفصل بين المهام لفرض سياسات الرقابة الداخلية.</span><span class="sxs-lookup"><span data-stu-id="d84c9-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="d84c9-109">أكمل الإجراء التالي لإنشاء قاعدة.</span><span class="sxs-lookup"><span data-stu-id="d84c9-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="d84c9-110">يجب أن تكون مسؤول نظام لإكمال الإجراء.</span><span class="sxs-lookup"><span data-stu-id="d84c9-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="d84c9-111">انتقل إلى **إدارة النظام**  > **الأمان** > **الفصل بين المهام** > **قواعد الفصل بين المهام**.</span><span class="sxs-lookup"><span data-stu-id="d84c9-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="d84c9-112">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="d84c9-112">Click **New**.</span></span>
3. <span data-ttu-id="d84c9-113">في الحقل **الاسم**، اكتب قيمة للقاعدة.</span><span class="sxs-lookup"><span data-stu-id="d84c9-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="d84c9-114">في الحقل **المهمة الأولى**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d84c9-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d84c9-115">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d84c9-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="d84c9-116">حدد المهمة الأولى التي تحكمها القاعدة.</span><span class="sxs-lookup"><span data-stu-id="d84c9-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="d84c9-117">في الحقل **المهمة الثانية**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="d84c9-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="d84c9-118">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="d84c9-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="d84c9-119">حدد المهمة الثانية التي تحكمها القاعدة.</span><span class="sxs-lookup"><span data-stu-id="d84c9-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="d84c9-120">في الحقل **مستوى الشدة**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="d84c9-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="d84c9-121">حدد شدة المخاطر التي تحدث عندما ينفذ نفس المستخدم أو الدور كلتا المهمتين.</span><span class="sxs-lookup"><span data-stu-id="d84c9-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="d84c9-122">في الحقل **مخاطر الأمان**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d84c9-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="d84c9-123">أدخل وصفًا لمخاطر الأمان.</span><span class="sxs-lookup"><span data-stu-id="d84c9-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="d84c9-124">في الحقل **تقليل المخاطر**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="d84c9-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="d84c9-125">أدخل وصفاً للإجراءات التي تتخذها لتقليل مخاطر الأمان.</span><span class="sxs-lookup"><span data-stu-id="d84c9-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="d84c9-126">على سبيل المثال، يمكنك تقليل المخاطر بإجراء عمليات مراجعة أدق للعملية أو بإجراء مراجعة إدارية شهرية أو مشاركة الموارد مع الأقسام الأخرى.</span><span class="sxs-lookup"><span data-stu-id="d84c9-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="d84c9-127">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="d84c9-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="d84c9-128">لم يتم التحقق من التوافق مع قواعد الفصل بين المهام عند إنشاء قاعده.</span><span class="sxs-lookup"><span data-stu-id="d84c9-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="d84c9-129">يمكنك إنشاء قاعده لإنشاء تعارض للأدوار الموجودة.</span><span class="sxs-lookup"><span data-stu-id="d84c9-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="d84c9-130">كما يمكن أيضا ان تكون تعيينات ادوار المستخدمين الموجودة متعارضة مع القاعدة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="d84c9-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="d84c9-131">يجب التحقق من صحة التوافق بعد إنشاء أحدي القواعد أو تعديلها.</span><span class="sxs-lookup"><span data-stu-id="d84c9-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="d84c9-132">لمزيد من المعلومات، راجع [تحديد وحل التعارضات في الفصل بين المهام](identify-resolve-conflicts-segregation-duties.md)</span><span class="sxs-lookup"><span data-stu-id="d84c9-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]