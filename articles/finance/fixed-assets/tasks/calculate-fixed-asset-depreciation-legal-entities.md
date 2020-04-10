---
title: حساب إهلاك الأصول الثابتة عبر الكيانات القانونية
description: يمكن تشغيل إهلاك الأصول الثابتة عبر الكيانات القانونية في خطوة واحدة.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 074a1b80584050302920a95c20fb547523a4866c
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142905"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="8180f-103">حساب إهلاك الأصول الثابتة عبر الكيانات القانونية</span><span class="sxs-lookup"><span data-stu-id="8180f-103">Calculate fixed asset depreciation across legal entities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8180f-104">يمكن تشغيل إهلاك الأصول الثابتة عبر الكيانات القانونية في خطوة واحدة.</span><span class="sxs-lookup"><span data-stu-id="8180f-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="8180f-105">يوضح هذا الإجراء كيفية إعداد العملية للعديد من الكيانات القانونية‬ وكيفية تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="8180f-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="8180f-106">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.</span><span class="sxs-lookup"><span data-stu-id="8180f-106">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="set-up-cross-company-depreciation-run-journals"></a><span data-ttu-id="8180f-107">إعداد دفاتر يومية تشغيل الإهلاك عبر الشركة</span><span class="sxs-lookup"><span data-stu-id="8180f-107">Set up cross company depreciation run journals</span></span>
1. <span data-ttu-id="8180f-108">انتقل إلى الأصول الثابتة > إعداد > معلمات الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="8180f-108">Go to Fixed assets > Setup > Fixed assets parameters.</span></span>
2. <span data-ttu-id="8180f-109">قم بتوسيع قسم عروض الأصول الثابتة‬.</span><span class="sxs-lookup"><span data-stu-id="8180f-109">Expand the Fixed asset proposals section.</span></span>
3. <span data-ttu-id="8180f-110">وانقر فوق إضافة.</span><span class="sxs-lookup"><span data-stu-id="8180f-110">Click Add.</span></span>
4. <span data-ttu-id="8180f-111">في الحقل "طبقة الترحيل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8180f-111">In the Posting layer field, enter or select a value.</span></span>
5. <span data-ttu-id="8180f-112">في الحقل "اسم دفتر اليومية"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8180f-112">In the Journal name field, enter or select a value.</span></span>
    * <span data-ttu-id="8180f-113">قم بتكرار إعداد دفتر اليومية في صفحة معلمات الأصول الثابتة في كل كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="8180f-113">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span>  

## <a name="depreciation-run"></a><span data-ttu-id="8180f-114">تشغيل الإهلاك</span><span class="sxs-lookup"><span data-stu-id="8180f-114">Depreciation run</span></span>
1. <span data-ttu-id="8180f-115">انتقل إلى الأصول الثابتة > إدخالات دفتر اليومية‬ > إنشاء مقترح الإهلاك‬‬.</span><span class="sxs-lookup"><span data-stu-id="8180f-115">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="8180f-116">في الحقل "طبقة الترحيل"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="8180f-116">In the Posting layer field, enter or select a value.</span></span>
    * <span data-ttu-id="8180f-117">سيتم تعيين اسم دفتر اليومية افتراضيًا من معلمات الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="8180f-117">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="8180f-118">ويمكن تغييره من هنا للكيان القانوني الحالي.</span><span class="sxs-lookup"><span data-stu-id="8180f-118">It can be changed here for the current legal entity.</span></span>  
3. <span data-ttu-id="8180f-119">في الحقل "إلى تاريخ"، أدخل تاريخًا.</span><span class="sxs-lookup"><span data-stu-id="8180f-119">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="8180f-120">حدد الكيانات القانونية المقرر تضمينها في تشغيل الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="8180f-120">Select the legal entities to be included in the depreciation run.</span></span>  
    * <span data-ttu-id="8180f-121">لن يظهر في القائمة غير الكيانات القانونية ذات دفاتر اليومية التي تم إعدادها لعروض الأصول الثابتة في صفحة معلمات الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="8180f-121">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span>  
4. <span data-ttu-id="8180f-122">حدد نعم في الحقل ترحيل دفاتر اليومية.</span><span class="sxs-lookup"><span data-stu-id="8180f-122">Select Yes in the Post journals field.</span></span>
    * <span data-ttu-id="8180f-123">تتضمن حقول التصفية جميع الأصول الثابتة والمجموعات والدفاتر الخاصة بالكيانات القانونية المحددة لتشغيل الإهلاك هذا.</span><span class="sxs-lookup"><span data-stu-id="8180f-123">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span>  
    * <span data-ttu-id="8180f-124">يتم تمكين خيار معالجة الدُفعة بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="8180f-124">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="8180f-125">عند تمكين هذا الخيار، سيتم تشغيل إنشاء دفتر يومية الإهلاك وترحيله في الخلفية.</span><span class="sxs-lookup"><span data-stu-id="8180f-125">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span>  
5. <span data-ttu-id="8180f-126">انقر فوق "إنشاء دفتر اليومية".</span><span class="sxs-lookup"><span data-stu-id="8180f-126">Click Create journal.</span></span>
6. <span data-ttu-id="8180f-127">انتقل إلى الأصول الثابتة > إدخالات دفتر اليومية‬ > دفتر يومية الأصول الثابتة‬.</span><span class="sxs-lookup"><span data-stu-id="8180f-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

