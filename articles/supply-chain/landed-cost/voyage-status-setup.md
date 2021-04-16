---
title: إعداد حالة الرحلة
description: يصف هذا الموضوع كيفية إنشاء قيم الحالة التي يمكن للمستخدمين تعيينها إلى الرحلات.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 80433c17ed9d790d88b20ecc253c8e4459ffea10
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829778"
---
# <a name="voyage-status-setup"></a><span data-ttu-id="61364-103">إعداد حالة الرحلة البحرية‬</span><span class="sxs-lookup"><span data-stu-id="61364-103">Voyage status setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="61364-104">في صفحة **حالات الرحلات**، أنشئ مجموعة القيم الحالة التي يمكن أن يقوم المستخدمون بتعيينها للرحلات.</span><span class="sxs-lookup"><span data-stu-id="61364-104">On the **Voyage statuses** page, you establish the set of status values that users can assign to voyages.</span></span> <span data-ttu-id="61364-105">يمكن للمستخدمين تعيين قيم حالة الرحلة لجميع مستويات الرحلة: الرحلة، وحاوية الشحن، والسجل، وأمر الشراء، والبند (بنود الشراء وبنود أوامر التحويل).</span><span class="sxs-lookup"><span data-stu-id="61364-105">Users can assign voyage status values to all levels of a voyage: voyage, shipping container, folio, purchase order, and item (purchase lines and transfer order lines).</span></span> <span data-ttu-id="61364-106">يتم استخدامها لغرضين:</span><span class="sxs-lookup"><span data-stu-id="61364-106">They are used for two purposes:</span></span>

- <span data-ttu-id="61364-107">أبلغ المستخدم بحالة الرحلة أو حاوية الشحن أو السجل أو أمر الشراء أو العنصر (سطور الشراء وبنود أمر التحويل).</span><span class="sxs-lookup"><span data-stu-id="61364-107">Inform the user about the status of the voyage, shipping container, folio, purchase order, or item (purchase lines and transfer order lines).</span></span>
- <span data-ttu-id="61364-108">حدد استخدام منطقه التكلفة من خلال منع التعديل أو الحذف.</span><span class="sxs-lookup"><span data-stu-id="61364-108">Limit the use of the cost area by preventing modification or deletion.</span></span>

<span data-ttu-id="61364-109">لإعداد حالات الرحلات الخاصة بك، انتقل إلى **التكلفة المستلمة \>الإعداد \> حالات الرحلات**.</span><span class="sxs-lookup"><span data-stu-id="61364-109">To set up your voyage statuses, go to **Landed cost \> Setup \> Voyage statuses**.</span></span> <span data-ttu-id="61364-110">هناك، يمكنك إضافة الحالات وإزالتها وتحريرها باستخدام الأزرار الموجودة في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="61364-110">There, you can add, remove, and edit statuses by using the buttons on the Action Pane.</span></span>

<span data-ttu-id="61364-111">لكل منطقة تكلفة مجموعتها الخاصة والتسلسل الهرمي لحالات الرحلة.</span><span class="sxs-lookup"><span data-stu-id="61364-111">Each cost area has its own set and hierarchy of voyage statuses.</span></span> <span data-ttu-id="61364-112">وبالتالي، في صفحة **حالات الرحلات**، في حقل **منطقة التكلفة**، يجب عليك أولاً تحديد منطقة التكلفة التي تريد عرض أو إنشاء حالات الرحلة لها.</span><span class="sxs-lookup"><span data-stu-id="61364-112">Therefore, on the **Voyage statuses** page, in the **Cost area** field, you must first select the cost area that you want to view or create voyage statuses for.</span></span> <span data-ttu-id="61364-113">وبعد ذلك، لكل حاله رحله، قم بتعيين الحقول الموضحة في الجدول التالي حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="61364-113">Then, for each voyage status, set the fields that are described in the following table, as required.</span></span> <span data-ttu-id="61364-114">لاحظ أنه يمكن أيضًا تغيير حالة الرحلة تلقائيًا عن طريق أحداث النظام، مثل القواعد التي تم وضعها باستخدام مركز التحكم في التعقب.</span><span class="sxs-lookup"><span data-stu-id="61364-114">Note that the status of a voyage can also be automatically changed by system events, such as rules that have been established by using the tracking control center.</span></span>

| <span data-ttu-id="61364-115">الحقل</span><span class="sxs-lookup"><span data-stu-id="61364-115">Field</span></span> | <span data-ttu-id="61364-116">الوصف</span><span class="sxs-lookup"><span data-stu-id="61364-116">Description</span></span> |
|---|---|
| <span data-ttu-id="61364-117">حالة الرحلة البحرية</span><span class="sxs-lookup"><span data-stu-id="61364-117">Voyage status</span></span> | <span data-ttu-id="61364-118">أدخل اسم حالة الرحلة.</span><span class="sxs-lookup"><span data-stu-id="61364-118">Enter the name of the voyage status.</span></span> |
| <span data-ttu-id="61364-119">الوصف</span><span class="sxs-lookup"><span data-stu-id="61364-119">Description</span></span> | <span data-ttu-id="61364-120">أدخل وصفًا لحالة الرحلة.</span><span class="sxs-lookup"><span data-stu-id="61364-120">Enter a description of the voyage status.</span></span> |
| <span data-ttu-id="61364-121">تعديل</span><span class="sxs-lookup"><span data-stu-id="61364-121">Modify</span></span> | <span data-ttu-id="61364-122">حدد مربع الاختيار هذا إذا كان يُسمح للمستخدمين بتعديل الرحلات التي لها هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="61364-122">Select this check box if users are allowed to modify voyages that have this status.</span></span> |
| <span data-ttu-id="61364-123">Delete</span><span class="sxs-lookup"><span data-stu-id="61364-123">Delete</span></span> | <span data-ttu-id="61364-124">حدد مربع الاختيار هذا إذا كان يُسمح للمستخدمين بحذف الرحلات التي لها هذه الحالة.</span><span class="sxs-lookup"><span data-stu-id="61364-124">Select this check box if users are allowed to delete voyages that have this status.</span></span> |
| <span data-ttu-id="61364-125">إلزامي</span><span class="sxs-lookup"><span data-stu-id="61364-125">Mandatory</span></span> | <span data-ttu-id="61364-126">حدد مربع الاختيار هذا لجعل حالة الرحلة إلزامية، بحيث لا يمكن تخطيها.</span><span class="sxs-lookup"><span data-stu-id="61364-126">Select this check box to make the voyage status mandatory, so that it can't be skipped.</span></span> |
| <span data-ttu-id="61364-127">الأصل</span><span class="sxs-lookup"><span data-stu-id="61364-127">Parent</span></span> | <span data-ttu-id="61364-128">استخدم هذا الحقل لإنشاء تسلسل هرمي بين قيم الحالة.</span><span class="sxs-lookup"><span data-stu-id="61364-128">Use this field to establish a hierarchy among the status values.</span></span> <span data-ttu-id="61364-129">يمكن تغيير حالات الرحلات (إما يدويًا أو تلقائيًا) إلى الأسفل فقط في التسلسل الهرمي، من الحالة الرئيسية إلى إحدى حالاتها الفرعية.</span><span class="sxs-lookup"><span data-stu-id="61364-129">Voyage statuses can be changed (either manually or automatically) only downward in the hierarchy, from a parent status to one of its child statuses.</span></span>

> [!NOTE]
> <span data-ttu-id="61364-130">يجب عليك فقط إعداد حالات الرحلة المحددة التي تستخدمها مؤسستك.</span><span class="sxs-lookup"><span data-stu-id="61364-130">You have to set up only the specific voyage statuses that your organization uses.</span></span> <span data-ttu-id="61364-131">تشمل حالات الرحلات النموذجية *مؤكدة*، و *البضائع أثناء النقل*، و *تم الاستلام*، و *جاهز للتكاليف*، و *التكاليف*.</span><span class="sxs-lookup"><span data-stu-id="61364-131">Typical voyage statuses include *Confirmed*, *Goods in transit*, *Received*, *Ready for costing*, and *Costed*.</span></span> <span data-ttu-id="61364-132">ومع ذلك، قد تكون الحالات الأخرى موجودة.</span><span class="sxs-lookup"><span data-stu-id="61364-132">However, other statuses might be present.</span></span>
