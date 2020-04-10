---
title: إعداد الفصل بين المهام
description: يمكنك إعداد قواعد لفصل المهام التي يجب تنفيذها بواسطة مستخدمين مختلفين.
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 712cc90bef4f3ad56291e99edd9f963ae88add48
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143502"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="9965f-103">إعداد الفصل بين المهام</span><span class="sxs-lookup"><span data-stu-id="9965f-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9965f-104">يمكنك إعداد قواعد لفصل المهام التي يجب تنفيذها بواسطة مستخدمين مختلفين.</span><span class="sxs-lookup"><span data-stu-id="9965f-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="9965f-105">يسمى هذا المفهوم الفصل بين المهام.</span><span class="sxs-lookup"><span data-stu-id="9965f-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="9965f-106">على سبيل المثال، قد لا تريد أن يقر نفس الشخص بكل من استلام البضائع ومعالجة الدفع للمورد.</span><span class="sxs-lookup"><span data-stu-id="9965f-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="9965f-107">يساعدك الفصل بين المهام في الحد من مخاطر الغش كما يساعدك أيضًا على اكتشاف الأخطاء أو المخالفات.</span><span class="sxs-lookup"><span data-stu-id="9965f-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="9965f-108">يمكنك أيضا استخدام الفصل بين المهام لفرض سياسات الرقابة الداخلية.</span><span class="sxs-lookup"><span data-stu-id="9965f-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="9965f-109">أكمل الإجراء التالي لإنشاء قاعدة.</span><span class="sxs-lookup"><span data-stu-id="9965f-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="9965f-110">يجب أن تكون مسؤول نظام لإكمال الإجراء.</span><span class="sxs-lookup"><span data-stu-id="9965f-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="9965f-111">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي DAT.</span><span class="sxs-lookup"><span data-stu-id="9965f-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="9965f-112">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة النظام > الأمان > الفصل بين المهام > قواعد الفصل بين المهام‬**.</span><span class="sxs-lookup"><span data-stu-id="9965f-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="9965f-113">انقر فوق **جديد**.</span><span class="sxs-lookup"><span data-stu-id="9965f-113">Click **New**.</span></span>
3. <span data-ttu-id="9965f-114">في الحقل **الاسم**، اكتب قيمة للقاعدة.</span><span class="sxs-lookup"><span data-stu-id="9965f-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="9965f-115">في الحقل **المهمة الأولى**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="9965f-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="9965f-116">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="9965f-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="9965f-117">حدد المهمة الأولى التي تحكمها القاعدة.</span><span class="sxs-lookup"><span data-stu-id="9965f-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="9965f-118">في الحقل **المهمة الثانية**، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="9965f-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="9965f-119">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="9965f-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="9965f-120">حدد المهمة الثانية التي تحكمها القاعدة.</span><span class="sxs-lookup"><span data-stu-id="9965f-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="9965f-121">في الحقل **مستوى الشدة**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="9965f-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="9965f-122">حدد شدة المخاطر التي تحدث عندما ينفذ نفس المستخدم أو الدور كلتا المهمتين.</span><span class="sxs-lookup"><span data-stu-id="9965f-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="9965f-123">في الحقل **مخاطر الأمان**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9965f-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="9965f-124">أدخل وصفًا لمخاطر الأمان.</span><span class="sxs-lookup"><span data-stu-id="9965f-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="9965f-125">في الحقل **تقليل المخاطر**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="9965f-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="9965f-126">أدخل وصفاً للإجراءات التي تتخذها لتقليل مخاطر الأمان.</span><span class="sxs-lookup"><span data-stu-id="9965f-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="9965f-127">على سبيل المثال، يمكنك تقليل المخاطر بإجراء عمليات مراجعة أدق للعملية أو بإجراء مراجعة إدارية شهرية أو مشاركة الموارد مع الأقسام الأخرى.</span><span class="sxs-lookup"><span data-stu-id="9965f-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="9965f-128">انقر فوق **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="9965f-128">Click **Save**.</span></span>

