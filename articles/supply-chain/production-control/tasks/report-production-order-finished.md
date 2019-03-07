---
title: الإبلاغ عن انتهاء أمر إنتاج
description: يوضح هذا الإجراء كيفية الإبلاغ عن أمر إنتاج كمنتهٍ.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 97e67ff51e4bc4533aeb2485c34cd5ec8a882bb6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "320479"
---
# <a name="report-a-production-order-as-finished"></a><span data-ttu-id="8d6f8-103">الإبلاغ عن انتهاء أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="8d6f8-103">Report a production order as finished</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8d6f8-104">يوضح هذا الإجراء كيفية الإبلاغ عن أمر إنتاج كمنتهٍ.</span><span class="sxs-lookup"><span data-stu-id="8d6f8-104">This procedure shows how to report a production order as finished.</span></span> <span data-ttu-id="8d6f8-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="8d6f8-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8d6f8-106">هذا هو الإجراء السادس من أصل سبعة إجراءات الذي يشرح دورة حياة أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="8d6f8-106">This is the sixth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="report-a-production-order-as-finished"></a><span data-ttu-id="8d6f8-107">الإبلاغ عن انتهاء أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="8d6f8-107">Report a production order as finished</span></span>
1. <span data-ttu-id="8d6f8-108">انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="8d6f8-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="8d6f8-109">حدد أمر إنتاج يكون في الحالة "تم بدءه".</span><span class="sxs-lookup"><span data-stu-id="8d6f8-109">Select a production order that has the Started status.</span></span>  
2. <span data-ttu-id="8d6f8-110">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="8d6f8-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="8d6f8-111">انقر فوق تقرير كمنتهِ.</span><span class="sxs-lookup"><span data-stu-id="8d6f8-111">Click Report as finished.</span></span>
    * <span data-ttu-id="8d6f8-112">في هذه الصفحة، يمكنك تأكيد كمية المنتج المنتهي للإبلاغ عنها كمنتهية.</span><span class="sxs-lookup"><span data-stu-id="8d6f8-112">On this page, you can confirm the quantity of the finished product to be reported as finished.</span></span>  
4. <span data-ttu-id="8d6f8-113">انقر فوق علامة التبويب "عام".</span><span class="sxs-lookup"><span data-stu-id="8d6f8-113">Click the General tab.</span></span>
5. <span data-ttu-id="8d6f8-114">عيّن "كمية البضائع" على "18".</span><span class="sxs-lookup"><span data-stu-id="8d6f8-114">Set Good quantity to '18'.</span></span>
6. <span data-ttu-id="8d6f8-115">عيّن "كمية الأخطاء" على "2".</span><span class="sxs-lookup"><span data-stu-id="8d6f8-115">Set Error quantity to '2'.</span></span>
7. <span data-ttu-id="8d6f8-116">في الحقل "سبب الخطأ"، حدد "المادة".</span><span class="sxs-lookup"><span data-stu-id="8d6f8-116">In the Error cause field, select 'Material'.</span></span>
8. <span data-ttu-id="8d6f8-117">حدد خانات الاختيار "إنهاء الوظيفة" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="8d6f8-117">Select or clear the End job check box.</span></span>
9. <span data-ttu-id="8d6f8-118">حدد خانة الاختيار "قبول الخطأ" أو قم بإلغاء تحديدها.</span><span class="sxs-lookup"><span data-stu-id="8d6f8-118">Select or clear the Accept error check box.</span></span>
10. <span data-ttu-id="8d6f8-119">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="8d6f8-119">Click OK.</span></span>

## <a name="verify-the-report-as-finished-journal"></a><span data-ttu-id="8d6f8-120">التحقق من دفتر يومية "الإبلاغ عنه كمنتهٍ".</span><span class="sxs-lookup"><span data-stu-id="8d6f8-120">Verify the Report as finished journal</span></span>
1. <span data-ttu-id="8d6f8-121">في جزء "الإجراءات"، انقر فوق "عرض".</span><span class="sxs-lookup"><span data-stu-id="8d6f8-121">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="8d6f8-122">انقر فوق "تم الإبلاغ عنه كمنتهٍ".</span><span class="sxs-lookup"><span data-stu-id="8d6f8-122">Click Reported as finished.</span></span>
3. <span data-ttu-id="8d6f8-123">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8d6f8-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="8d6f8-124">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="8d6f8-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8d6f8-125">تم ترحيل دفتر يومية التقرير كمنتهٍ.</span><span class="sxs-lookup"><span data-stu-id="8d6f8-125">The Report as finished journal is posted.</span></span> <span data-ttu-id="8d6f8-126">إذا أردت إجراء تعديلات على دفتر اليومية، يمكنك إنشاء دفتر يومية جديد يدويًا حيث يمكنك إجراء تغييرات.</span><span class="sxs-lookup"><span data-stu-id="8d6f8-126">If you want to make adjustments to the journal, you can manually create  a new journal where you can make changes.</span></span>  

