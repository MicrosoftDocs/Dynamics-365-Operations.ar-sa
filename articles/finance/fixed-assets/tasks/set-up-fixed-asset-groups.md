---
title: إعداد مجموعات الأصول الثابتة
description: يوضح هذا الموضوع كيفية إنشاء مجموعة أصول ثابتة جديدة.
author: saraschi2
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee3cec5c6abf08c88a61af2ec4bde6a863de2f95
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224635"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="64b6d-103">إعداد مجموعات الأصول الثابتة</span><span class="sxs-lookup"><span data-stu-id="64b6d-103">Set up fixed asset groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="64b6d-104">يوضح هذا الموضوع كيفية إنشاء مجموعة أصول ثابتة جديدة.</span><span class="sxs-lookup"><span data-stu-id="64b6d-104">This topic explains how to create a new fixed asset group.</span></span> <span data-ttu-id="64b6d-105">إنه يستخدم دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.</span><span class="sxs-lookup"><span data-stu-id="64b6d-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="64b6d-106">في جزء التنقل، انتقل إلى **الوحدات النمطية > الأصول الثابتة > الإعداد > مجموعات الأصول الثابتة‬**.</span><span class="sxs-lookup"><span data-stu-id="64b6d-106">In the navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset groups**.</span></span>
2. <span data-ttu-id="64b6d-107">حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="64b6d-107">Select **New**.</span></span>
3. <span data-ttu-id="64b6d-108">في حقل **مجموعة الأصول الثابتة**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="64b6d-108">In the **Fixed asset group** field, type a value.</span></span>
4. <span data-ttu-id="64b6d-109">في الحقل **الاسم**، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="64b6d-109">In the **Name** field, type a value.</span></span> <span data-ttu-id="64b6d-110">ستبطل إعدادات "الترقيم التلقائي للأصول الثابتة" و"كود التسلسل الرقمي"‬ على مجموعة **الأصول الثابتة** إعدادات محددات الأصول الثابتة.</span><span class="sxs-lookup"><span data-stu-id="64b6d-110">Autonumber fixed assets and Number sequence code on the **Fixed asset** group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="64b6d-111">يمكنك تغييرها هنا إذا كانت الأصول في مجموعة الأصول الثابتة هذه بترقيم مختلف من مجموعات أخرى.</span><span class="sxs-lookup"><span data-stu-id="64b6d-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="64b6d-112">حدد **الدفاتر**.</span><span class="sxs-lookup"><span data-stu-id="64b6d-112">Select **Books**.</span></span>
6. <span data-ttu-id="64b6d-113">في الحقل **الدفتر**، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="64b6d-113">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="64b6d-114">تم تعيين الحقل **حساب الإهلاك‬** إلى **نعم**، وبالتالي سيتم تضمين دفتر الأصول في مقترحات الإهلاك.</span><span class="sxs-lookup"><span data-stu-id="64b6d-114">The **Calculate depreciation** field is set to **Yes**, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="64b6d-115">إذا تم تعيين **حساب الإهلاك** إلى **لا**، فلن يتم إهلاك الأصل بشكل تلقائي.</span><span class="sxs-lookup"><span data-stu-id="64b6d-115">If **Calculate depreciation** is set to **No**, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="64b6d-116">عيّن مدة خدمة الأصل بالسنوات.</span><span class="sxs-lookup"><span data-stu-id="64b6d-116">Set the Service life of the asset, in years.</span></span> <span data-ttu-id="64b6d-117">لاحظ أن حساب قيمة الحقل **فترات الإهلاك** يتم بعد تعيين مدة الخدمة.</span><span class="sxs-lookup"><span data-stu-id="64b6d-117">Note that the **Depreciation periods** field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="64b6d-118">في الحقل **قواعد الإهلاك‬‬**، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="64b6d-118">In the **Depreciation convention** field, select an option.</span></span>
9. <span data-ttu-id="64b6d-119">قم بإغلاق الصفحة.</span><span class="sxs-lookup"><span data-stu-id="64b6d-119">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]