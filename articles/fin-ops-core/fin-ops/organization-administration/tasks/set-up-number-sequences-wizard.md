---
title: إعداد التسلسلات الرقمية باستخدام معالج
description: يوضح هذا الموضوع كيفية إعداد جميع التسلسلات الرقمية المطلوبة في نفس الوقت باستخدام معالج.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76dc32f2254ffd2a2e33eef594d6e602092bcb6f
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140480"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="2c71a-103">إعداد التسلسلات الرقمية باستخدام معالج</span><span class="sxs-lookup"><span data-stu-id="2c71a-103">Set up number sequences using a wizard</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c71a-104">تُستخدم التسلسلات الرقمية لإنشاء معرفات فريدة قابلة للقراءة لسجلات البيانات الرئيسية وسجلات الحركات التي تتطلب وجودها.</span><span class="sxs-lookup"><span data-stu-id="2c71a-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="2c71a-105">ويشار إلى البيانات الرئيسية أو سجل الحركة الذي يتطلب معرفًا بمرجع.</span><span class="sxs-lookup"><span data-stu-id="2c71a-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="2c71a-106">قبل إنشاء سجلات جديدة لأحد المراجع، يجب أن تقوم بإعداد تسلسل رقمي وإقرانه بالمرجع.</span><span class="sxs-lookup"><span data-stu-id="2c71a-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="2c71a-107">يوضح هذا الموضوع كيفية إعداد جميع التسلسلات الرقمية المطلوبة في نفس الوقت باستخدام معالج.</span><span class="sxs-lookup"><span data-stu-id="2c71a-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="2c71a-108">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="2c71a-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="2c71a-109">انتقل إلى **جزء التنقل > الوحدات النمطية > إدارة المؤسسة > التسلسلات الرقمية > التسلسلات الرقمية**.</span><span class="sxs-lookup"><span data-stu-id="2c71a-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="2c71a-110">حدد **إنشاء**.</span><span class="sxs-lookup"><span data-stu-id="2c71a-110">Select **Generate**.</span></span>
3. <span data-ttu-id="2c71a-111">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="2c71a-111">Select **Next**.</span></span>

   - <span data-ttu-id="2c71a-112">يمكنك في هذه الصفحة تعديل كود التعريف وأدنى قيمة وأعلى قيمة.</span><span class="sxs-lookup"><span data-stu-id="2c71a-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="2c71a-113">بالإضافة إلى أنه يمكنك الإشارة إلى ما إذا كان يجب أن يكون التسلسل الرقمي مستمرًا.</span><span class="sxs-lookup"><span data-stu-id="2c71a-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="2c71a-114">لا تحدد الخيار **مستمر** إذا كان يجب عليك تخصيص أرقام التسلسل الرقمي بشكل مسبق.</span><span class="sxs-lookup"><span data-stu-id="2c71a-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="2c71a-115">لإضافة شريحة نطاق إلى تنسيق تسلسل رقمي، حدد التنسيق في القائمة، ثم انقر فوق **تضمين النطاق في التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="2c71a-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="2c71a-116">لإزالة شريحة نطاق من تنسيق تسلسل رقمي، حدد التنسيق في القائمة، ثم انقر فوق **إزالة النطاق من التنسيق**.</span><span class="sxs-lookup"><span data-stu-id="2c71a-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="2c71a-117">لاستبعاد تسلسل رقمي من الإنشاء التلقائي، حدد التسلسل الرقمي في القائمة، ثم حدد **حذف**.</span><span class="sxs-lookup"><span data-stu-id="2c71a-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="2c71a-118">حدد **التالي**.</span><span class="sxs-lookup"><span data-stu-id="2c71a-118">Select **Next**.</span></span>
5. <span data-ttu-id="2c71a-119">حدد **إنهاء**.</span><span class="sxs-lookup"><span data-stu-id="2c71a-119">Select **Finish**.</span></span>

