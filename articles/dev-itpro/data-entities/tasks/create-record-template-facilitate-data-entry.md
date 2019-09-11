---
title: إنشاء قالب سجل لتسهيل إدخال البيانات
description: يوضح هذا الموضوع كيفية إنشاء قالب سجل بحيث تنتفي الحاجة إلى عملية إدخال واضحة لقيم الحقول التي يتم استخدامها في أغلب الأحيان لكل سجل جديد.
author: margoc
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08ee7d0f0ce7e92eaa85137dcd2761bfd702eb8c
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/08/2019
ms.locfileid: "1866918"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="dc09a-103">إنشاء قالب سجل لتسهيل إدخال البيانات</span><span class="sxs-lookup"><span data-stu-id="dc09a-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc09a-104">يوضح هذا الموضوع كيفية إنشاء قالب سجل بحيث تنتفي الحاجة إلى عملية إدخال واضحة لقيم الحقول التي يتم استخدامها في أغلب الأحيان لكل سجل جديد.</span><span class="sxs-lookup"><span data-stu-id="dc09a-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="dc09a-105">في هذا الإجراء، ستقوم بإنشاء سجل جديد لأجهزة الكمبيوتر المحمولة الجديدة التي يجب أن تُضاف إلى الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="dc09a-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="dc09a-106">يستخدم هذا الإجراء الشركة النموذجية USMF.</span><span class="sxs-lookup"><span data-stu-id="dc09a-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="dc09a-107">في جزء التنقل، انتقل إلى **الوحدات النمطية > الأصول الثابتة > الأصول الثابتة > الأصول الثابتة‬**.</span><span class="sxs-lookup"><span data-stu-id="dc09a-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="dc09a-108">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="dc09a-108">Select **New**.</span></span>
3. <span data-ttu-id="dc09a-109">في حقل **مجموعة الأصول الثابتة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="dc09a-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="dc09a-110">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="dc09a-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="dc09a-111">على سبيل المثال، أدخل **كمبيوتر محمول لمسؤول في الشركة**.</span><span class="sxs-lookup"><span data-stu-id="dc09a-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="dc09a-112">في الحقل **اسم البحث‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="dc09a-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="dc09a-113">على سبيل المثال، أدخل **كمبيوتر محمول**.</span><span class="sxs-lookup"><span data-stu-id="dc09a-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="dc09a-114">قم بتوسيع قسم **المعلومات التقنية**.</span><span class="sxs-lookup"><span data-stu-id="dc09a-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="dc09a-115">في الحقول **النوع‬** و**الطراز** و**سنة الطراز‬**، اكتب قيمًا.</span><span class="sxs-lookup"><span data-stu-id="dc09a-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="dc09a-116">في جزء الإجراءات، حدد **خيارات**.</span><span class="sxs-lookup"><span data-stu-id="dc09a-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="dc09a-117">حدد **معلومات السجل‬**.</span><span class="sxs-lookup"><span data-stu-id="dc09a-117">Select **Record info**.</span></span>
10. <span data-ttu-id="dc09a-118">حدد **قالب المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="dc09a-118">Select **User template**.</span></span>
11. <span data-ttu-id="dc09a-119">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="dc09a-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="dc09a-120">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="dc09a-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="dc09a-121">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="dc09a-121">Select **OK**.</span></span>
14. <span data-ttu-id="dc09a-122">حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="dc09a-122">Select **Close**.</span></span>

