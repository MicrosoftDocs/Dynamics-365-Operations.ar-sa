--- 
title: "إنشاء موفري التكوين ووضع علامة عليهم على أنهم نشطاء"
description: "تشرح الخطوات التالية كيف يمكن لمستخدم تم تعيينه إلى دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء موفر تكوين لإنشاء التقارير الإلكترونية."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 37957f224cb57fd9f6c5014740bcea124a99a03a
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="a0936-103">إنشاء موفري التكوين ووضع علامة عليهم على أنهم نشطاء</span><span class="sxs-lookup"><span data-stu-id="a0936-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a0936-104">تشرح الخطوات التالية كيف يمكن لمستخدم تم تعيينه إلى دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء موفر تكوين لإنشاء التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="a0936-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="a0936-105">ستشير كل تكوينات التقارير الإلكترونية إلى الموفر على أنه مالك التكوين.</span><span class="sxs-lookup"><span data-stu-id="a0936-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="a0936-106">في هذا المثال، ستقوم بإنشاء موفر تكوين لشركة عينة، .Litware, Inc ويمكن تنفيذ هذه الخطوات في أي شركة كموفري تكوينات ER المشتركة بين جميع الشركات.</span><span class="sxs-lookup"><span data-stu-id="a0936-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="a0936-107">إنشاء موفر</span><span class="sxs-lookup"><span data-stu-id="a0936-107">Create a provider</span></span>
1. <span data-ttu-id="a0936-108">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="a0936-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a0936-109">انقر فوق "موفرو التكوين".</span><span class="sxs-lookup"><span data-stu-id="a0936-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="a0936-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="a0936-110">Click New.</span></span>
    * <span data-ttu-id="a0936-111">يكون سجل الموفر فريدًا من حيث الاسم وعنوان URL.</span><span class="sxs-lookup"><span data-stu-id="a0936-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="a0936-112">راجع محتويات هذه الصفحة وتجاوز هذا الإجراء في حال وجود سجل خاص بشركة Litware, Inc. (`http://www.litware.com`) already exists.</span><span class="sxs-lookup"><span data-stu-id="a0936-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (`http://www.litware.com`) already exists.</span></span>  
4. <span data-ttu-id="a0936-113">في الحقل "الاسم"، اكتب "Litware, Inc.".</span><span class="sxs-lookup"><span data-stu-id="a0936-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="a0936-114">.Litware, Inc</span><span class="sxs-lookup"><span data-stu-id="a0936-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="a0936-115">في حقل "عنوان الإنترنت"، اكتب `http://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="a0936-115">In the Internet address field, type `http://www.litware.com`.</span></span>
6. <span data-ttu-id="a0936-116">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="a0936-116">Click Save.</span></span>
7. <span data-ttu-id="a0936-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="a0936-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="a0936-118">تحديد الموفر كموفر نشط</span><span class="sxs-lookup"><span data-stu-id="a0936-118">Select as an active provider</span></span>
1. <span data-ttu-id="a0936-119">حدد الموفر Litware, Inc. .</span><span class="sxs-lookup"><span data-stu-id="a0936-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="a0936-120">انقر فوق "تعيين كنشط".</span><span class="sxs-lookup"><span data-stu-id="a0936-120">Click Set active.</span></span>


