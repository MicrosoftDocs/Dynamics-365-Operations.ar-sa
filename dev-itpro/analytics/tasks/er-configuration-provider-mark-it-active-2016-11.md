--- 
title: "إنشاء موفر تكوين وتمييزه كنشط للتقارير الإلكترونية (ER)"
description: "تشرح الخطوات التالية كيف يمكن لمستخدم تم تعيينه إلى دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء موفر تكوين لإنشاء التقارير الإلكترونية."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: bdb3a3857a7293828a7766b6988c123a43e0673c
ms.contentlocale: ar-sa
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-configuration-providand-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="4abe6-103">إنشاء موفر تكوين وتمييزه كنشط للتقارير الإلكترونية (ER)</span><span class="sxs-lookup"><span data-stu-id="4abe6-103">Create a configuration providand mark it as active for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4abe6-104">تشرح الخطوات التالية كيف يمكن لمستخدم تم تعيينه إلى دور مسؤول النظام أو مطور التقارير الإلكترونية إنشاء موفر تكوين لإنشاء التقارير الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="4abe6-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="4abe6-105">ستشير كل تكوينات التقارير الإلكترونية إلى الموفر على أنه مالك التكوين.</span><span class="sxs-lookup"><span data-stu-id="4abe6-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="4abe6-106">في هذا المثال، ستقوم بإنشاء موفر تكوين لشركة عينة، .Litware, Inc ويمكن تنفيذ هذه الخطوات في أي شركة كموفري تكوينات ER المشتركة بين جميع الشركات.</span><span class="sxs-lookup"><span data-stu-id="4abe6-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="4abe6-107">إنشاء موفر</span><span class="sxs-lookup"><span data-stu-id="4abe6-107">Create a provider</span></span>
1. <span data-ttu-id="4abe6-108">انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.</span><span class="sxs-lookup"><span data-stu-id="4abe6-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="4abe6-109">انقر فوق "موفرو التكوين".</span><span class="sxs-lookup"><span data-stu-id="4abe6-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="4abe6-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="4abe6-110">Click New.</span></span>
    * <span data-ttu-id="4abe6-111">يكون سجل الموفر فريدًا من حيث الاسم وعنوان URL.</span><span class="sxs-lookup"><span data-stu-id="4abe6-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="4abe6-112">راجع محتويات هذه الصفحة وتجاوز هذا الإجراء في حال وجود سجل خاص بشركة .Litware, Inc ‏(http://www.litware.com) بالفعل.</span><span class="sxs-lookup"><span data-stu-id="4abe6-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="4abe6-113">في الحقل "الاسم"، اكتب "Litware, Inc.".</span><span class="sxs-lookup"><span data-stu-id="4abe6-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="4abe6-114">.Litware, Inc</span><span class="sxs-lookup"><span data-stu-id="4abe6-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="4abe6-115">في الحقل "عنوان الإنترنت‬"، اكتب "http://www.litware.com".</span><span class="sxs-lookup"><span data-stu-id="4abe6-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * <span data-ttu-id="4abe6-116">http://www.litware.com</span><span class="sxs-lookup"><span data-stu-id="4abe6-116">http://www.litware.com</span></span>  
6. <span data-ttu-id="4abe6-117">انقر فوق "حفظ".</span><span class="sxs-lookup"><span data-stu-id="4abe6-117">Click Save.</span></span>
7. <span data-ttu-id="4abe6-118">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="4abe6-118">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="4abe6-119">تحديد الموفر كموفر نشط</span><span class="sxs-lookup"><span data-stu-id="4abe6-119">Select as an active provider</span></span>
1. <span data-ttu-id="4abe6-120">حدد الموفر Litware, Inc. .</span><span class="sxs-lookup"><span data-stu-id="4abe6-120">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="4abe6-121">انقر فوق "تعيين كنشط".</span><span class="sxs-lookup"><span data-stu-id="4abe6-121">Click Set active.</span></span>


