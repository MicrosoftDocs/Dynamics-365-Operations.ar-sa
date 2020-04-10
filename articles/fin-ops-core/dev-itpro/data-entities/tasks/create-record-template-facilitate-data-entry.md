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
ms.openlocfilehash: ec21415158ad611d0ad55778e76aa128f53561bd
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143374"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="1c662-103">إنشاء قالب سجل لتسهيل إدخال البيانات</span><span class="sxs-lookup"><span data-stu-id="1c662-103">Create a record template to facilitate data entry</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1c662-104">يوضح هذا الموضوع كيفية إنشاء قالب سجل بحيث تنتفي الحاجة إلى عملية إدخال واضحة لقيم الحقول التي يتم استخدامها في أغلب الأحيان لكل سجل جديد.</span><span class="sxs-lookup"><span data-stu-id="1c662-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="1c662-105">في هذا الإجراء، ستقوم بإنشاء سجل جديد لأجهزة الكمبيوتر المحمولة الجديدة التي يجب أن تُضاف إلى الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="1c662-105">In this procedure, you'll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="1c662-106">يستخدم هذا الإجراء الشركة النموذجية USMF.</span><span class="sxs-lookup"><span data-stu-id="1c662-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="1c662-107">في جزء التنقل، انتقل إلى **الوحدات النمطية > الأصول الثابتة > الأصول الثابتة > الأصول الثابتة‬**.</span><span class="sxs-lookup"><span data-stu-id="1c662-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="1c662-108">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="1c662-108">Select **New**.</span></span>
3. <span data-ttu-id="1c662-109">في حقل **مجموعة الأصول الثابتة**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="1c662-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="1c662-110">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1c662-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="1c662-111">على سبيل المثال، أدخل **كمبيوتر محمول لمسؤول في الشركة**.</span><span class="sxs-lookup"><span data-stu-id="1c662-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="1c662-112">في الحقل **اسم البحث‬**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1c662-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="1c662-113">على سبيل المثال، أدخل **كمبيوتر محمول**.</span><span class="sxs-lookup"><span data-stu-id="1c662-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="1c662-114">قم بتوسيع قسم **المعلومات التقنية**.</span><span class="sxs-lookup"><span data-stu-id="1c662-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="1c662-115">في الحقول **النوع‬** و**الطراز** و**سنة الطراز‬**، اكتب قيمًا.</span><span class="sxs-lookup"><span data-stu-id="1c662-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="1c662-116">في جزء الإجراءات، حدد **خيارات**.</span><span class="sxs-lookup"><span data-stu-id="1c662-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="1c662-117">حدد **معلومات السجل‬**.</span><span class="sxs-lookup"><span data-stu-id="1c662-117">Select **Record info**.</span></span>
10. <span data-ttu-id="1c662-118">حدد **قالب المستخدم**.</span><span class="sxs-lookup"><span data-stu-id="1c662-118">Select **User template**.</span></span>
11. <span data-ttu-id="1c662-119">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1c662-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="1c662-120">في حقل **الوصف**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="1c662-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="1c662-121">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="1c662-121">Select **OK**.</span></span>
14. <span data-ttu-id="1c662-122">حدد **إغلاق**.</span><span class="sxs-lookup"><span data-stu-id="1c662-122">Select **Close**.</span></span>

