---
title: إصدار أمر إنتاج
description: يوضح هذا الإجراء كيفية تحرير أمر إنتاج.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmRelease, SrsReportViewerForm, ProdSetupRelease
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4aeede64a9976adc7208be552e8445ba1a514204
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204534"
---
# <a name="release-a-production-order"></a><span data-ttu-id="c3a5e-103">إصدار أمر إنتاج</span><span class="sxs-lookup"><span data-stu-id="c3a5e-103">Release a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c3a5e-104">يوضح هذا الإجراء كيفية تحرير أمر إنتاج.</span><span class="sxs-lookup"><span data-stu-id="c3a5e-104">This procedure shows how to release a production order.</span></span> <span data-ttu-id="c3a5e-105">شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي USMF.</span><span class="sxs-lookup"><span data-stu-id="c3a5e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c3a5e-106">هذا هو الإجراء الرابع من أصل سبعة إجراءات الذي يشرح دورة حياة أمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="c3a5e-106">This is the fourth procedure out of seven which explains the production order lifecycle.</span></span>

1. <span data-ttu-id="c3a5e-107">انتقل إلى التحكم بالإنتاج‬ > أوامر الإنتاج > كافة أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="c3a5e-107">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="c3a5e-108">في الشبكة، حدد أمر إنتاج يكون في الحالة "مجدول‬".</span><span class="sxs-lookup"><span data-stu-id="c3a5e-108">In the grid, select a production order that has the Scheduled status.</span></span>  
2. <span data-ttu-id="c3a5e-109">في جزء "الإجراءات"، انقر فوق "أمر إنتاج".</span><span class="sxs-lookup"><span data-stu-id="c3a5e-109">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="c3a5e-110">انقر فوق "إصدار".</span><span class="sxs-lookup"><span data-stu-id="c3a5e-110">Click Release.</span></span>
    * <span data-ttu-id="c3a5e-111">في هذه الصفحة، يمكنك التأكد من تحرير المجموعة المحددة من أوامر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="c3a5e-111">On this page, you can confirm the release of the selected range of production orders.</span></span> <span data-ttu-id="c3a5e-112">انقر فوق "تحديد" إذا كنت تريد إضافة أوامر.</span><span class="sxs-lookup"><span data-stu-id="c3a5e-112">Click Select if you want to add orders.</span></span>  
    * <span data-ttu-id="c3a5e-113">تشير خطوة التحرير إلى الوقت الذي سيتم فيه تحرير أمر الإنتاج في صالة الإنتاج بحيث يتمكن العاملون في صالة الإنتاج من التبليغ عن التقدم المحرز في وظائف الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="c3a5e-113">The Release step indicates when the production order is released to the production shop floor so that the shop floor operators can report progress on the production jobs.</span></span> <span data-ttu-id="c3a5e-114">ويمكن إصدار أوراق خاصة بالإنتاج تحتوي على معلومات ذات الصلة حول معالجة الوظائف.</span><span class="sxs-lookup"><span data-stu-id="c3a5e-114">Production papers that contain relevant information about processing the jobs can be issued.</span></span> <span data-ttu-id="c3a5e-115">يتم إنشاء عمل المستودع لانتقاء المواد الخام للأصناف التي يتم إعدادها لعملية المستودع.</span><span class="sxs-lookup"><span data-stu-id="c3a5e-115">The warehouse work for raw material picking is generated for the items that are set up for the warehouse process.</span></span>  
4. <span data-ttu-id="c3a5e-116">انقر فوق علامة التبويب "عام".</span><span class="sxs-lookup"><span data-stu-id="c3a5e-116">Click the General tab.</span></span>
    * <span data-ttu-id="c3a5e-117">حدد تقارير الإنتاج التي يجب طباعتها.</span><span class="sxs-lookup"><span data-stu-id="c3a5e-117">Select which production reports should be printed.</span></span> <span data-ttu-id="c3a5e-118">يطبع "تقرير بطاقة الوظيفة‬" صفحة لكل مهمة مجدولة ويتطلب جدولة أمر الإنتاج على مستوى الوظيفة‬.</span><span class="sxs-lookup"><span data-stu-id="c3a5e-118">The Job card report prints a page for each scheduled job and requires the production order to be scheduled at the job level.</span></span> <span data-ttu-id="c3a5e-119">يحتوي التقرير على معلومات حول وقت البدء والانتهاء المجدولين والكمية التي يجب إنتاجها والمورد الذي يعالج الوظيفة.</span><span class="sxs-lookup"><span data-stu-id="c3a5e-119">The report contains information about the scheduled start and end time, the quantity to produce, and which resource processes the job.</span></span> <span data-ttu-id="c3a5e-120">يجمع "تقرير وظيفة المسار" المعلومات نفسها على نفس الصفحة، ولكنه لا يطبع صفحة لكل وظيفة.</span><span class="sxs-lookup"><span data-stu-id="c3a5e-120">The Route job report collects the same information on the same page, but does not print a page for each job.</span></span> <span data-ttu-id="c3a5e-121">يعرض "تقرير وظيفة المسار" العمليات فقط وليس الوظائف.</span><span class="sxs-lookup"><span data-stu-id="c3a5e-121">The Route card report only shows the operations but not the jobs.</span></span> <span data-ttu-id="c3a5e-122">لذلك، هذا التقرير لا يتطلب جدولة الوظائف، ولكن يمكن استخدامه عندما تتم جدولة أوامر الإنتاج على مستوى العملية.</span><span class="sxs-lookup"><span data-stu-id="c3a5e-122">Therefore, this report does not require job scheduling, but can be used when production orders are scheduled at the operation level.</span></span>  
5. <span data-ttu-id="c3a5e-123">انقر فوق خانة الاختيار "طباعة بطاقة المسار".</span><span class="sxs-lookup"><span data-stu-id="c3a5e-123">Click the Print route card checkbox.</span></span>
6. <span data-ttu-id="c3a5e-124">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="c3a5e-124">Click OK.</span></span>
7. <span data-ttu-id="c3a5e-125">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="c3a5e-125">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]