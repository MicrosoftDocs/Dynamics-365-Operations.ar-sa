---
title: المنتجات والفئات مفقودة بعد نسخ البيئة
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم العثور على المنتجات والفئات بعد نسخ الموقع بين البيئات أو داخل نفس البيئة.
author: Reza-Assadi
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
ms.openlocfilehash: 527fd0fa62775f65f61b538474b1d45d1a0155ed
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801713"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="868ec-103">المنتجات والفئات مفقودة بعد نسخ البيئة</span><span class="sxs-lookup"><span data-stu-id="868ec-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="868ec-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم العثور على المنتجات والفئات بعد نسخ الموقع بين البيئات أو داخل نفس البيئة.</span><span class="sxs-lookup"><span data-stu-id="868ec-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="868ec-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="868ec-105">Description</span></span>

<span data-ttu-id="868ec-106">بعد نسخ الموقع من بيئة إلى أخرى، أو في نفس البيئة، يتم فقدان المنتجات والفئات من الموقع.</span><span class="sxs-lookup"><span data-stu-id="868ec-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="868ec-107">تكون المنتجات والفئات مفقودة من واجهة متجر التجارة الإلكترونية ومن علامة تبويب **المنتجات** في منشئ موقع Commerce.</span><span class="sxs-lookup"><span data-stu-id="868ec-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="868ec-108">الدقة</span><span class="sxs-lookup"><span data-stu-id="868ec-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="868ec-109">تعيين رقم وحدة تشغيل القناة إلى موقع تم نسخه حديثًا في منشئ موقع Commerce</span><span class="sxs-lookup"><span data-stu-id="868ec-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="868ec-110">لتعيين رقم وحدة التشغيل (OUN) للقناة إلى موقع تم نسخه حديثًا في منشئ موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="868ec-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="868ec-111">حدد الموقع المنسوخ حديثًا.</span><span class="sxs-lookup"><span data-stu-id="868ec-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="868ec-112">ضمن **إعدادات الموقع**، حدد **القنوات**.</span><span class="sxs-lookup"><span data-stu-id="868ec-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="868ec-113">بجوار اسم القناة، حدد علامة القطع (**...**)، ثم حدد **تغيير قناة المتجر على الإنترنت**.</span><span class="sxs-lookup"><span data-stu-id="868ec-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="868ec-114">في مربع الحوار **تغيير قناة المتجر على الإنترنت**، حدد القناة التي تريد تعيينها للموقع المنسوخ حديثًا، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="868ec-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="868ec-115">حدد **حفظ ونشر**.</span><span class="sxs-lookup"><span data-stu-id="868ec-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="868ec-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="868ec-116">Additional resources</span></span>

[<span data-ttu-id="868ec-117">إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="868ec-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)
