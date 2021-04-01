---
title: إعداد فئات الحساب الرئيسي
description: يشرح هذا الموضوع كيفية إعداد ‏‫فئات الحساب الرئيسية في Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 957fdc184410dc85f54cd3163799a9003f0727bb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222205"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="28099-103">إعداد فئات الحساب الرئيسي</span><span class="sxs-lookup"><span data-stu-id="28099-103">Set up main account categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="28099-104">يشرح هذا الموضوع كيفية إعداد ‏‫فئات الحساب الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="28099-104">This topic explains how to set up main account categories.</span></span> <span data-ttu-id="28099-105">يتم استخدام فئات الحساب الرئيسي للتقارير الافتراضية في الإبلاغ المالي وفي Power BI.</span><span class="sxs-lookup"><span data-stu-id="28099-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="28099-106">يمكن إعادة تسمية فئات الحساب الرئيسي التي تم إنشاؤها بشكل افتراضي ولكن لا يمكن حذفها.</span><span class="sxs-lookup"><span data-stu-id="28099-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="28099-107">يمكن إنشاء فئات حساب إضافية واستخدامها لأغراض إعداد التقارير والتحليل.</span><span class="sxs-lookup"><span data-stu-id="28099-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="28099-108">يستخدم هذا الموضوع شركة العرض التجريبي "USMF".</span><span class="sxs-lookup"><span data-stu-id="28099-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="28099-109">إنشاء فئة حساب رئيسي</span><span class="sxs-lookup"><span data-stu-id="28099-109">Create a main account category</span></span>
1. <span data-ttu-id="28099-110">في جزء التنقل، انتقل إلى **الوحدات النمطية > دفتر الأستاذ العام > دليل الحسابات > الحسابات > فئات الحساب الرئيسية‬**.</span><span class="sxs-lookup"><span data-stu-id="28099-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="28099-111">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="28099-111">Select **New**.</span></span>
3. <span data-ttu-id="28099-112">أدخل اسمًا فريدًا في حقل **فئة الحساب الرئيسي** .</span><span class="sxs-lookup"><span data-stu-id="28099-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="28099-113">في الحقل **الوصف**، أدخل وصفًا لفئة الحساب الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="28099-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="28099-114">في الحقل **نوع الحساب الرئيسي**، حدد نوع الحساب الرئيسي الذي سيتم ربطه بالفئة.</span><span class="sxs-lookup"><span data-stu-id="28099-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="28099-115">ربط الحسابات الرئيسية بفئة حساب</span><span class="sxs-lookup"><span data-stu-id="28099-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="28099-116">انقر فوق **ربط الحسابات الرئيسية**.</span><span class="sxs-lookup"><span data-stu-id="28099-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="28099-117">في القائمة، حدد الحسابات الرئيسية لتعيينها إلى فئة الحساب الرئيسي عن طريق تحديد خانات الاختيار في العمود **مرتبط**.</span><span class="sxs-lookup"><span data-stu-id="28099-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="28099-118">سيؤدي تعيين الحسابات الرئيسية لفئة حساب رئيسي إلى تجميع أرصدة الحسابات عند استخدام هذه الفئة للتقارير المالية والتحليل المالي.</span><span class="sxs-lookup"><span data-stu-id="28099-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="28099-119">حدد الخيار **مرتبط** أو قم بإلغاء تحديده لاختيار الحسابات الرئيسية.</span><span class="sxs-lookup"><span data-stu-id="28099-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="28099-120">حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="28099-120">Select **OK**.</span></span>
5. <span data-ttu-id="28099-121">حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="28099-121">Select **Yes**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]