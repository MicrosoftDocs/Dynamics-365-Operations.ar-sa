--- 
title: "إعداد التسلسلات الرقمية باستخدام معالج"
description: "تُستخدم التسلسلات الرقمية لإنشاء معرفات فريدة قابلة للقراءة لسجلات البيانات الرئيسية وسجلات الحركات التي تتطلب وجودها."
author: sericks007
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e7d988cd1261c00925ad7ae612a947a0083028ee
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-number-sequences-by-using-a-wizard"></a><span data-ttu-id="84eb4-103">إعداد التسلسلات الرقمية باستخدام معالج</span><span class="sxs-lookup"><span data-stu-id="84eb4-103">Set up number sequences by using a wizard</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="84eb4-104">تُستخدم التسلسلات الرقمية لإنشاء معرفات فريدة قابلة للقراءة لسجلات البيانات الرئيسية وسجلات الحركات التي تتطلب وجودها.</span><span class="sxs-lookup"><span data-stu-id="84eb4-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="84eb4-105">ويشار إلى البيانات الرئيسية أو سجل الحركة الذي يتطلب معرفًا بمرجع.</span><span class="sxs-lookup"><span data-stu-id="84eb4-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="84eb4-106">قبل إنشاء سجلات جديدة لأحد المراجع، يجب أن تقوم بإعداد تسلسل رقمي وإقرانه بالمرجع.</span><span class="sxs-lookup"><span data-stu-id="84eb4-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="84eb4-107">يوضح هذا الإجراء كيفية إعداد جميع التسلسلات الرقمية المطلوبة في نفس الوقت باستخدام معالج.</span><span class="sxs-lookup"><span data-stu-id="84eb4-107">This procedure explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="84eb4-108">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="84eb4-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="84eb4-109">انتقل إلى إدارة المؤسسة > التسلسلات الرقمية > التسلسلات الرقمية.</span><span class="sxs-lookup"><span data-stu-id="84eb4-109">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="84eb4-110">انقر فوق "إنشاء".</span><span class="sxs-lookup"><span data-stu-id="84eb4-110">Click Generate.</span></span>
3. <span data-ttu-id="84eb4-111">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="84eb4-111">Click Next.</span></span>
    * <span data-ttu-id="84eb4-112">يمكنك في هذه الصفحة تعديل كود التعريف وأدنى قيمة وأعلى قيمة.</span><span class="sxs-lookup"><span data-stu-id="84eb4-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="84eb4-113">بالإضافة إلى أنه يمكنك الإشارة إلى ما إذا كان يجب أن يكون التسلسل الرقمي مستمرًا.</span><span class="sxs-lookup"><span data-stu-id="84eb4-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
    * <span data-ttu-id="84eb4-114">لا تحدد الخيار "مستمر" إذا كان يجب عليك التخصيص المسبق للتسلسل الرقمي.</span><span class="sxs-lookup"><span data-stu-id="84eb4-114">Do not select the Continuous option if you must preallocate numbers for the number sequence.</span></span>     <span data-ttu-id="84eb4-115">لإضافة مقطع نطاق إلى تنسيق تسلسل رقمي، حدد التنسيق في القائمة، ثم انقر فوق "تضمين النطاق في التنسيق".</span><span class="sxs-lookup"><span data-stu-id="84eb4-115">To add a scope segment to the format of a number sequence, select the format in the list, and then click Include scope in format.</span></span>     <span data-ttu-id="84eb4-116">لإزالة مقطع نطاق من تنسيق تسلسل رقمي، حدد التنسيق في القائمة، ثم انقر فوق "إزالة النطاق من التنسيق".</span><span class="sxs-lookup"><span data-stu-id="84eb4-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then click Remove scope from format.</span></span>     <span data-ttu-id="84eb4-117">لاستبعاد تسلسل رقمي من الإنشاء التلقائي، حدد التسلسل الرقمي في القائمة، ثم انقر فوق "حذف".</span><span class="sxs-lookup"><span data-stu-id="84eb4-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then click Delete.</span></span>  
4. <span data-ttu-id="84eb4-118">انقر فوق التالي.</span><span class="sxs-lookup"><span data-stu-id="84eb4-118">Click Next.</span></span>
5. <span data-ttu-id="84eb4-119">انقر فوق إنهاء.</span><span class="sxs-lookup"><span data-stu-id="84eb4-119">Click Finish.</span></span>


