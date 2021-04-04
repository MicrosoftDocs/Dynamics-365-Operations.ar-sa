---
title: لا يظهر متجر البيع بالتجزئة في قائمة المتاجر المطلوب الانتهاء منها
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور متجر البيع بالتجزئة في قائمة المتاجر التي يمكن انتقاء الأصناف منها.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 652f5f1a779a412c21c18814071ba0fb7dd2e155
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585184"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a><span data-ttu-id="efdc8-103">لا يظهر متجر البيع بالتجزئة في قائمة المتاجر المطلوب الانتهاء منها</span><span class="sxs-lookup"><span data-stu-id="efdc8-103">Retail store doesn't appear in the list of stores to pick up from</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="efdc8-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم ظهور متجر البيع بالتجزئة في قائمة المتاجر التي يمكن انتقاء الأصناف منها.</span><span class="sxs-lookup"><span data-stu-id="efdc8-104">This topic provides troubleshooting guidance that can help when a retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="description"></a><span data-ttu-id="efdc8-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="efdc8-105">Description</span></span>

<span data-ttu-id="efdc8-106">لا يظهر متجر البيع بالتجزئة في قائمة المتاجر التي يمكن انتقاء الأصناف منها.</span><span class="sxs-lookup"><span data-stu-id="efdc8-106">A retail store doesn't appear in the list of stores where items can be picked up.</span></span>

## <a name="resolution"></a><span data-ttu-id="efdc8-107">الدقة</span><span class="sxs-lookup"><span data-stu-id="efdc8-107">Resolution</span></span>

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a><span data-ttu-id="efdc8-108">تكوين خط الطول وخط العرض لعنوان المتجر في المركز الرئيسي لـ Commerce</span><span class="sxs-lookup"><span data-stu-id="efdc8-108">Configure the longitude and latitude for the store address in Commerce headquarters</span></span>

<span data-ttu-id="efdc8-109">لتكوين خط الطول وخط العرض لعنوان المتجر في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="efdc8-109">To configure the longitude and latitude for the store address in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="efdc8-110">انتقل إلى **Retail وCommerce \> القنوات \> المتاجر \> جميع المتاجر**.</span><span class="sxs-lookup"><span data-stu-id="efdc8-110">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="efdc8-111">ابحث عن المتجر الذي ترغب في ظهوره بين خيارات الانتقاء في موقع التجارة الإلكترونية.</span><span class="sxs-lookup"><span data-stu-id="efdc8-111">Find the store that you want to appear among the pickup options on the e-commerce site.</span></span> <span data-ttu-id="efdc8-112">قم بتدوين قيمة **رقم وحدة التشغيل** الخاصة به.</span><span class="sxs-lookup"><span data-stu-id="efdc8-112">Make a note of its **Operating unit number** value.</span></span>
1. <span data-ttu-id="efdc8-113">انتقل إلى **إدارة المؤسسة \> المؤسسات \> وحدات التشغيل**.</span><span class="sxs-lookup"><span data-stu-id="efdc8-113">Go to **Organization administration \> Organizations \> Operating units**.</span></span>
1. <span data-ttu-id="efdc8-114">ابحث عن رقم وحدة التشغيل الذي قمت بالإشارة إليه سابقًا، ثم حدد وحدة التشغيل في نتائج البحث.</span><span class="sxs-lookup"><span data-stu-id="efdc8-114">Search for the operating unit number that you noted earlier, and then select the operating unit in the search results.</span></span>
1. <span data-ttu-id="efdc8-115">في علامة التبويب السريعة **العناوين**، حدد **المزيد من الخيارات**، ثم حدد **متقدم**.</span><span class="sxs-lookup"><span data-stu-id="efdc8-115">On the **Addresses** FastTab, select **More options**, and then select **Advanced**.</span></span>
1. <span data-ttu-id="efdc8-116">في علامة التبويب السريعة **عام**، تأكد من أن حقلي **خط الطول** و **خط العرض** تعيينهما بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="efdc8-116">On the **General** FastTab, make sure that the **Longitude** and **Latitude** fields are correctly set.</span></span> <span data-ttu-id="efdc8-117">كجزء من هذه الخطوة، تأكد من تحديد القيم بشكل صحيح كأرقام موجبة أو سالبة.</span><span class="sxs-lookup"><span data-stu-id="efdc8-117">As part of this step, make sure that the values are correctly specified as positive or negative numbers.</span></span>

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a><span data-ttu-id="efdc8-118">تكوين مجموعات الاستيفاء في المركز الرئيسي لـ Commerce</span><span class="sxs-lookup"><span data-stu-id="efdc8-118">Configure fulfillment groups in Commerce headquarters</span></span>

<span data-ttu-id="efdc8-119">لتكوين مجموعات الاستيفاء في المركز الرئيسي لـ Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="efdc8-119">To configure fulfillment groups in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="efdc8-120">انتقل إلى **Retail وCommerce \> القنوات \> المتاجر على الإنترنت**.</span><span class="sxs-lookup"><span data-stu-id="efdc8-120">Go to **Retail and Commerce \> Channels \> Online stores**.</span></span>
1. <span data-ttu-id="efdc8-121">حدد المتجر على الإنترنت المراد تكوينه.</span><span class="sxs-lookup"><span data-stu-id="efdc8-121">Select the online store to configure.</span></span>
1. <span data-ttu-id="efdc8-122">في جزء الإجراءات، حدد علامة التبويب **الإعداد**، ثم حدد **تعيين مجموعة الاستيفاء**.</span><span class="sxs-lookup"><span data-stu-id="efdc8-122">On the Action Pane, select **Set up**, and then select **Fulfillment group assignment**.</span></span>
1. <span data-ttu-id="efdc8-123">في صفحة **تعيين مجموعة الاستيفاء**، حدد مجموعة الاستيفاء الخاصة بالمتجر على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="efdc8-123">On the **Fulfillment group assignment** page, select the fulfillment group for the online store.</span></span>
1. <span data-ttu-id="efdc8-124">تحت **الإعداد**، تأكد من تكوين مخزن البيع بالتجزئة بشكل صحيح لمجموعة الاستيفاء.</span><span class="sxs-lookup"><span data-stu-id="efdc8-124">Under **Setup**, make sure that the retail store is correctly configured for the fulfillment group.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="efdc8-125">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="efdc8-125">Additional resources</span></span> 

[<span data-ttu-id="efdc8-126">إنشاء وحدة تشغيل</span><span class="sxs-lookup"><span data-stu-id="efdc8-126">Create an operating unit</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit)

[<span data-ttu-id="efdc8-127">إعداد قناة على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="efdc8-127">Set up an online channel</span></span>](../channel-setup-online.md)
