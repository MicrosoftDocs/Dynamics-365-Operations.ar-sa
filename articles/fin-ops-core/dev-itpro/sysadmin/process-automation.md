---
title: أتمتة العملية
description: يوفر هذا الموضوع تفاصيل حول كيفية سماح التنفيذ التلقائي للعمليات بالجدولة البسيطة للعمليات التي سيتم تشغيلها بواسطة خادم الدفعة.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 08/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 320e18f7fc61300ed2966afef530907fc9fc5ca5
ms.sourcegitcommit: e2a47d31175bbd60acfd7a23ffea70c669358572
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2020
ms.locfileid: "3690036"
---
# <a name="process-automation"></a><span data-ttu-id="39ee4-103">أتمتة العملية</span><span class="sxs-lookup"><span data-stu-id="39ee4-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="39ee4-104">تسمح أتمتة العملية بالجدولة البسيطة للعمليات التي سيتم تشغيلها بواسطة خادم الدفعة.</span><span class="sxs-lookup"><span data-stu-id="39ee4-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="39ee4-105">يسمح عرض التقويم المحدث للعمل المجدول للمستخدمين بعرض وتنفيذ الإجراء المجدول والعمل المنجز.</span><span class="sxs-lookup"><span data-stu-id="39ee4-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="39ee4-106">الإدارة</span><span class="sxs-lookup"><span data-stu-id="39ee4-106">Administration</span></span>

<span data-ttu-id="39ee4-107">توجد صفحة الإدارة المركزية الخاصة بكافة أتمتة العمليات في الوحدة النمطية لإدارة النظام ضمن قائمة **الإعداد**.</span><span class="sxs-lookup"><span data-stu-id="39ee4-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="39ee4-108">تسرد هذه الصفحة كافة العمليات المؤتمتة (المسلسلة) التي تم إعدادها في النظام.</span><span class="sxs-lookup"><span data-stu-id="39ee4-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="39ee4-109">كما سيسمح لك أيضًا بإضافة أتمتة عمليات جديدة مباشرة من هذه الصفحة.</span><span class="sxs-lookup"><span data-stu-id="39ee4-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="39ee4-110">بعد إعداد السلسلة، يمكنك إدارة كل سلسلة من هذه القائمة.</span><span class="sxs-lookup"><span data-stu-id="39ee4-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="39ee4-111">يمكنك اختيار تحرير السلسلة بأكملها أو حذفها أو عرض كافة التواجدات في طريقة عرض قائمة أو تعطيل السلسلة إذا كنت ترغب في إيقاف العمل المجدول مؤقتًا لفترة من الوقت.</span><span class="sxs-lookup"><span data-stu-id="39ee4-111">You can chose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a period of time.</span></span> 

<span data-ttu-id="39ee4-112">لن تظهر أي عمليات معطلة في إدارة الميزات عند تعطيل الميزة.</span><span class="sxs-lookup"><span data-stu-id="39ee4-112">Any processes that are disabled in feature management will not show when the feature is disabled.</span></span> <span data-ttu-id="39ee4-113">علاوةً على ذلك، لن يجدول محرك جدولة أتمتة العملية أي حدوث أو عملية خلفية لميزة معطلة.</span><span class="sxs-lookup"><span data-stu-id="39ee4-113">Additionally, the Process automation scheduling engine will not schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="39ee4-114">ستؤدي إعادة تمكين الميزة إلى تشغيل فوري لأي مرات حدوث مجدولة أو عمليات خلفية في الماضي.</span><span class="sxs-lookup"><span data-stu-id="39ee4-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span>

## <a name="calendar-view"></a><span data-ttu-id="39ee4-115">طريقة عرض التقويم</span><span class="sxs-lookup"><span data-stu-id="39ee4-115">Calendar view</span></span> 
<span data-ttu-id="39ee4-116">أحد الفوائد الرئيسية لتنفيذ لأتمتة العملية هي القدرة على رؤية العمل المجدول في طريقة عرض تقويم بسيطة.</span><span class="sxs-lookup"><span data-stu-id="39ee4-116">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="39ee4-117">تسمح لك طريقة العرض رؤية العمل لمدة أسبوع في المرة الواحدة.</span><span class="sxs-lookup"><span data-stu-id="39ee4-117">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="39ee4-118">ستشاهد هذا العرض على الجانب الأيمن من صفحة **أتمتة العملية**.</span><span class="sxs-lookup"><span data-stu-id="39ee4-118">You will see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="39ee4-119">سيتم ملؤها بالعمل المجدول للسلسلة المحددة.</span><span class="sxs-lookup"><span data-stu-id="39ee4-119">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="39ee4-120">[![تقويم أتمتة العملية](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="39ee4-120">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="39ee4-121">تغييرات التكرار</span><span class="sxs-lookup"><span data-stu-id="39ee4-121">Occurrence changes</span></span>
<span data-ttu-id="39ee4-122">يمكن تعديل كل تكرار دون التأثير على التكرارات الأخرى التي تم تعريفها بواسطة السلسلة التي أنشأتها.</span><span class="sxs-lookup"><span data-stu-id="39ee4-122">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="39ee4-123">يمكن تحرير تكرارات العمل المجدول من طريقة عرض التقويم عن طريق تحديد زر **عرض/تحرير** وتحديد **التكرار**.</span><span class="sxs-lookup"><span data-stu-id="39ee4-123">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="39ee4-124">وهذا يسمح لك بالوصول إلى كافة الإعدادات المعروضة في الأصل في معالج إعداد السلسلة ويوفر القدرة على إجراء تغيير واحد للتكرار المحدد.</span><span class="sxs-lookup"><span data-stu-id="39ee4-124">This allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="39ee4-125">يمكن أيضا إيقاف تشغيل تكرار العمل المجدول بتحديد زر **تعطيل** من طريقة العرض التقويم.</span><span class="sxs-lookup"><span data-stu-id="39ee4-125">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span> 

## <a name="developer-documentation"></a><span data-ttu-id="39ee4-126">وثائق المطور</span><span class="sxs-lookup"><span data-stu-id="39ee4-126">Developer documentation</span></span> 
<span data-ttu-id="39ee4-127">يجري حاليً تأليف وثائق المطور للسماح للمطورين بتوسيع إطار عمل أتمتة العملية.</span><span class="sxs-lookup"><span data-stu-id="39ee4-127">Developer documentation is currently being written to allow developers to extend the process automation framework.</span></span> <span data-ttu-id="39ee4-128">سوف توفر هذه الوثائق معلومات حول كيفية إنشاء عمليات مخصصة تتطلب تشغيلها بواسطة خادم الدفعة المجدولة باستخدام معالج أتمتة العملية وتظهر في طريقة عرض التقويم تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="39ee4-128">This documentation will provide information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>
