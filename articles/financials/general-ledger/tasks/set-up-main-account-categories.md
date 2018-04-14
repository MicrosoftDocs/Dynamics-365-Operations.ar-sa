--- 
title: "إعداد فئات الحساب الرئيسي"
description: "يتم استخدام فئات الحساب الرئيسي للتقارير الافتراضية في الإبلاغ المالي وفي Power BI."
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d67ca0f21388630ca7875b0cb647195a8344b80e
ms.contentlocale: ar-sa
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="a86a3-103">إعداد فئات الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="a86a3-103">Set up main account categories</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a86a3-104">يتم استخدام فئات الحساب الرئيسي للتقارير الافتراضية في الإبلاغ المالي وفي Power BI.</span><span class="sxs-lookup"><span data-stu-id="a86a3-104">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="a86a3-105">يمكن إعادة تسمية فئات الحساب الرئيسي التي تم إنشاؤها بشكل افتراضي ولكن لا يمكن حذفها.</span><span class="sxs-lookup"><span data-stu-id="a86a3-105">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="a86a3-106">يمكن إنشاء فئات حساب إضافية واستخدامها لأغراض إعداد التقارير والتحليل.</span><span class="sxs-lookup"><span data-stu-id="a86a3-106">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="a86a3-107">تستخدم هذه المهمة شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="a86a3-107">This task uses the USMF demo company.</span></span>


## <a name="create-a-main-account-category"></a><span data-ttu-id="a86a3-108">إنشاء فئة حساب رئيسي</span><span class="sxs-lookup"><span data-stu-id="a86a3-108">Create a main account category</span></span>
1. <span data-ttu-id="a86a3-109">انتقل إلى دفتر الأستاذ العام > دليل الحسابات > الحسابات > فئات الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="a86a3-109">Go to General ledger > Chart of accounts > Accounts > Main account categories.</span></span>
2. <span data-ttu-id="a86a3-110">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="a86a3-110">Click New.</span></span>
3. <span data-ttu-id="a86a3-111">في الحقل "فئة الحساب الرئيسي"، أدخل اسمًا فريدًا.</span><span class="sxs-lookup"><span data-stu-id="a86a3-111">In the Main account category field, enter a unique name.</span></span>
4. <span data-ttu-id="a86a3-112">في الحقل "الوصف"، أدخل وصفًا لفئة الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="a86a3-112">In the Description field, enter a description for the main account category.</span></span>
5. <span data-ttu-id="a86a3-113">في الحقل "نوع الحساب الرئيسي"، حدد نوع الحساب الرئيسي الذي سيتم ربطه بالفئة.</span><span class="sxs-lookup"><span data-stu-id="a86a3-113">In the Main account type field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="a86a3-114">ربط الحسابات الرئيسية بفئة حساب</span><span class="sxs-lookup"><span data-stu-id="a86a3-114">Link main accounts to account category</span></span>
1. <span data-ttu-id="a86a3-115">انقر فوق "ربط الحسابات الرئيسية".</span><span class="sxs-lookup"><span data-stu-id="a86a3-115">Click Link main accounts.</span></span>
2. <span data-ttu-id="a86a3-116">في القائمة، حديد الحسابات الأساسية المطلوب ربطها بفئة الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="a86a3-116">In the list, select the main accounts to assign to the main account category.</span></span>
    * <span data-ttu-id="a86a3-117">سيؤدي تعيين الحسابات الرئيسية لفئة حساب رئيسي إلى تجميع أرصدة الحسابات عند استخدام هذه الفئة للتقارير المالية والتحليل المالي.</span><span class="sxs-lookup"><span data-stu-id="a86a3-117">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="a86a3-118">حدد الخيار "مرتبطة" أو امسحه لاختيار الحسابات الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="a86a3-118">Select or clear the Linked option to choose the main accounts.</span></span>
4. <span data-ttu-id="a86a3-119">انقر فوق موافق.</span><span class="sxs-lookup"><span data-stu-id="a86a3-119">Click OK.</span></span>
5. <span data-ttu-id="a86a3-120">انقر فوق نعم.</span><span class="sxs-lookup"><span data-stu-id="a86a3-120">Click Yes.</span></span>


