--- 
title: "إعداد الفصل بين المهام"
description: "يمكنك إعداد قواعد لفصل المهام التي يجب تنفيذها بواسطة مستخدمين مختلفين."
author: maertenm
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 754f28cd2831d8a9a57c408518d240de460b732b
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="a9642-103">إعداد الفصل بين المهام</span><span class="sxs-lookup"><span data-stu-id="a9642-103">Set up segregation of duties</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9642-104">يمكنك إعداد قواعد لفصل المهام التي يجب تنفيذها بواسطة مستخدمين مختلفين.</span><span class="sxs-lookup"><span data-stu-id="a9642-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="a9642-105">يسمى هذا المفهوم الفصل بين المهام.</span><span class="sxs-lookup"><span data-stu-id="a9642-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="a9642-106">على سبيل المثال، قد لا تريد أن يقر نفس الشخص بكل من استلام البضائع ومعالجة الدفع للمورد.</span><span class="sxs-lookup"><span data-stu-id="a9642-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="a9642-107">يساعدك الفصل بين المهام في الحد من مخاطر الغش كما يساعدك أيضًا على اكتشاف الأخطاء أو المخالفات.</span><span class="sxs-lookup"><span data-stu-id="a9642-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="a9642-108">يمكنك أيضا استخدام الفصل بين المهام لفرض سياسات الرقابة الداخلية.</span><span class="sxs-lookup"><span data-stu-id="a9642-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="a9642-109">أكمل الإجراء التالي لإنشاء قاعدة.</span><span class="sxs-lookup"><span data-stu-id="a9642-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="a9642-110">يجب أن تكون مسؤول نظام لإكمال الإجراء.</span><span class="sxs-lookup"><span data-stu-id="a9642-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="a9642-111">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي DAT.</span><span class="sxs-lookup"><span data-stu-id="a9642-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="a9642-112">انتقل إلى إدارة النظام > الأمان > الفصل بين المهام > قواعد الفصل بين المهام.</span><span class="sxs-lookup"><span data-stu-id="a9642-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="a9642-113">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="a9642-113">Click New.</span></span>
3. <span data-ttu-id="a9642-114">في حقل "الاسم"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a9642-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a9642-115">أدخل اسمًا للقاعدة.</span><span class="sxs-lookup"><span data-stu-id="a9642-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="a9642-116">في الحقل "المهمة الأولى"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="a9642-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a9642-117">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="a9642-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a9642-118">حدد المهمة الأولى التي تحكمها القاعدة.</span><span class="sxs-lookup"><span data-stu-id="a9642-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="a9642-119">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="a9642-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="a9642-120">في الحقل "المهمة الثانية"، انقر فوق زر القائمة المنسدلة لفتح البحث.</span><span class="sxs-lookup"><span data-stu-id="a9642-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a9642-121">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="a9642-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a9642-122">حدد المهمة الثانية التي تحكمها القاعدة.</span><span class="sxs-lookup"><span data-stu-id="a9642-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="a9642-123">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="a9642-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="a9642-124">في الحقل "مستوى الشدة"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="a9642-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="a9642-125">حدد شدة المخاطر التي تحدث عندما ينفذ نفس المستخدم أو الدور كلتا المهمتين.</span><span class="sxs-lookup"><span data-stu-id="a9642-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="a9642-126">في الحقل "مخاطر الأمان"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a9642-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="a9642-127">أدخل وصفًا لمخاطر الأمان.</span><span class="sxs-lookup"><span data-stu-id="a9642-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="a9642-128">في الحقل "تقليل المخاطر"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="a9642-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="a9642-129">أدخل وصفاً للإجراءات التي تتخذها لتقليل مخاطر الأمان.</span><span class="sxs-lookup"><span data-stu-id="a9642-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="a9642-130">على سبيل المثال، يمكنك تقليل المخاطر بإجراء عمليات مراجعة أدق للعملية أو بإجراء مراجعة إدارية شهرية أو مشاركة الموارد مع الأقسام الأخرى.</span><span class="sxs-lookup"><span data-stu-id="a9642-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="a9642-131">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="a9642-131">Click Save.</span></span>


