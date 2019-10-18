---
title: إنشاء موفري التكوين ووضع علامة نشط عليهم
description: يشرح هذا الموضوع كيف يمكن لمستخدم تم تعيينه إلى دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء موفر تكوين لإنشاء التقارير الإلكترونية.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2c092414f058a27cde963b1e8befd41ab3d1e3c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249194"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="b4356-103">إنشاء موفري التكوين ووضع علامة نشط عليهم</span><span class="sxs-lookup"><span data-stu-id="b4356-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b4356-104">يشرح هذا الموضوع كيف يمكن لمستخدم تم تعيينه إلى دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء موفر تكوين لإنشاء التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="b4356-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="b4356-105">ستشير كل تكوينات التقارير الإلكترونية إلى الموفر على أنه مالك التكوين.</span><span class="sxs-lookup"><span data-stu-id="b4356-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="b4356-106">في هذا المثال، ستقوم بإنشاء موفر تكوين لشركة عينة، .Litware, Inc ويمكن تنفيذ هذه الخطوات في أي شركة كموفري تكوينات ER المشتركة بين جميع الشركات.</span><span class="sxs-lookup"><span data-stu-id="b4356-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="b4356-107">إنشاء موفر</span><span class="sxs-lookup"><span data-stu-id="b4356-107">Create a provider</span></span>
1. <span data-ttu-id="b4356-108">انتقل إلى **جزء التنقل** في الزاوية العلوية اليسرى وحدد **إدارة المؤسسة**.</span><span class="sxs-lookup"><span data-stu-id="b4356-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="b4356-109">انتقل إلى **مساحات العمل > إعداد التقارير الإلكترونية**.</span><span class="sxs-lookup"><span data-stu-id="b4356-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="b4356-110">انتقل إلى **الارتباطات ذات الصلة > موفري التكوين**.</span><span class="sxs-lookup"><span data-stu-id="b4356-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="b4356-111">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="b4356-111">Select **New**.</span></span>
    - <span data-ttu-id="b4356-112">يكون سجل الموفر فريدًا من حيث الاسم وعنوان URL.</span><span class="sxs-lookup"><span data-stu-id="b4356-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="b4356-113">راجع محتويات هذه الصفحة وتجاوز هذا الإجراء في حال وجود سجل خاص بشركة Litware, Inc. (https://www.litware.com) الموجود بالفعل.</span><span class="sxs-lookup"><span data-stu-id="b4356-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="b4356-114">في حقل الاسم، اكتب`Litware, Inc.`.</span><span class="sxs-lookup"><span data-stu-id="b4356-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="b4356-115">في حقل عنوان الإنترنت، اكتب `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="b4356-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="b4356-116">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="b4356-116">Select **Save**.</span></span>
8. <span data-ttu-id="b4356-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="b4356-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="b4356-118">تحديد الموفر كموفر نشط</span><span class="sxs-lookup"><span data-stu-id="b4356-118">Select as an active provider</span></span>
1. <span data-ttu-id="b4356-119">حدد الموفر Litware, Inc. .</span><span class="sxs-lookup"><span data-stu-id="b4356-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="b4356-120">حدد **تعيين كنشط**.</span><span class="sxs-lookup"><span data-stu-id="b4356-120">Select **Set active**.</span></span>

![صفحة مساحة عمل إعداد التقارير الإلكترونية](../media/GER-Task-ActiveProvider-1.png)
