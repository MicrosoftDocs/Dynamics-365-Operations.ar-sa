--- 
title: "إنشاء موفر تكوين وتمييزه كنشط لإعداد التقارير الإلكتروني (ER)"
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9ed6f62318cd6806de1b4c9d6aa314c5f0a25500
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-configuration-provider-and-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="1c157-103">إنشاء موفر تكوين وتمييزه كنشط لإعداد التقارير الإلكتروني (ER)</span><span class="sxs-lookup"><span data-stu-id="1c157-103">Create a configuration provider and mark it as active for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1c157-104">تشرح الخطوات التالية كيف يمكن لمستخدم تم تعيينه إلى دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء موفر تكوين لإنشاء التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="1c157-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="1c157-105">ستشير كل تكوينات التقارير الإلكترونية إلى الموفر على أنه مالك التكوين.</span><span class="sxs-lookup"><span data-stu-id="1c157-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="1c157-106">في هذا المثال، ستقوم بإنشاء موفر تكوين لشركة عينة، .Litware, Inc ويمكن تنفيذ هذه الخطوات في أي شركة كموفري تكوينات ER المشتركة بين جميع الشركات.</span><span class="sxs-lookup"><span data-stu-id="1c157-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="1c157-107">إنشاء موفر</span><span class="sxs-lookup"><span data-stu-id="1c157-107">Create a provider</span></span>
1. <span data-ttu-id="1c157-108">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="1c157-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="1c157-109">انقر فوق "موفرو التكوين".</span><span class="sxs-lookup"><span data-stu-id="1c157-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="1c157-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="1c157-110">Click New.</span></span>
    * <span data-ttu-id="1c157-111">يكون سجل الموفر فريدًا من حيث الاسم وعنوان URL.</span><span class="sxs-lookup"><span data-stu-id="1c157-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="1c157-112">راجع محتويات هذه الصفحة وتجاوز هذا الإجراء في حال وجود سجل خاص بشركة Litware, Inc. (`http://www.litware.com`) already exists.</span><span class="sxs-lookup"><span data-stu-id="1c157-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (`http://www.litware.com`) already exists.</span></span>  
4. <span data-ttu-id="1c157-113">في الحقل "الاسم"، اكتب "Litware, Inc.".</span><span class="sxs-lookup"><span data-stu-id="1c157-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="1c157-114">.Litware, Inc</span><span class="sxs-lookup"><span data-stu-id="1c157-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="1c157-115">في حقل "عنوان الإنترنت"، اكتب `http://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="1c157-115">In the Internet address field, type `http://www.litware.com`.</span></span>
6. <span data-ttu-id="1c157-116">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="1c157-116">Click Save.</span></span>
7. <span data-ttu-id="1c157-117">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="1c157-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="1c157-118">تحديد الموفر كموفر نشط</span><span class="sxs-lookup"><span data-stu-id="1c157-118">Select as an active provider</span></span>
1. <span data-ttu-id="1c157-119">حدد الموفر Litware, Inc. .</span><span class="sxs-lookup"><span data-stu-id="1c157-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="1c157-120">انقر فوق "تعيين كنشط".</span><span class="sxs-lookup"><span data-stu-id="1c157-120">Click Set active.</span></span>


