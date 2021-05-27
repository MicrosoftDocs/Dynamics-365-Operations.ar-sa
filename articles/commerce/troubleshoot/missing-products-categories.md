---
title: المنتجات والفئات مفقودة بعد نسخ البيئة
description: يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم العثور على المنتجات والفئات بعد نسخ الموقع بين البيئات أو داخل نفس البيئة.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 4964b9623a91286d4f8260bcae7941feb48f8962
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022388"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="5ed46-103">المنتجات والفئات مفقودة بعد نسخ البيئة</span><span class="sxs-lookup"><span data-stu-id="5ed46-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5ed46-104">يوفر هذا الموضوع إرشادات استكشاف الأخطاء وإصلاحها والتي يمكن أن تساعد في حالة عدم العثور على المنتجات والفئات بعد نسخ الموقع بين البيئات أو داخل نفس البيئة.</span><span class="sxs-lookup"><span data-stu-id="5ed46-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="5ed46-105">الوصف</span><span class="sxs-lookup"><span data-stu-id="5ed46-105">Description</span></span>

<span data-ttu-id="5ed46-106">بعد نسخ الموقع من بيئة إلى أخرى، أو في نفس البيئة، يتم فقدان المنتجات والفئات من الموقع.</span><span class="sxs-lookup"><span data-stu-id="5ed46-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="5ed46-107">تكون المنتجات والفئات مفقودة من واجهة متجر التجارة الإلكترونية ومن علامة تبويب **المنتجات** في منشئ موقع Commerce.</span><span class="sxs-lookup"><span data-stu-id="5ed46-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="5ed46-108">الدقة</span><span class="sxs-lookup"><span data-stu-id="5ed46-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="5ed46-109">تعيين رقم وحدة تشغيل القناة إلى موقع تم نسخه حديثًا في منشئ موقع Commerce</span><span class="sxs-lookup"><span data-stu-id="5ed46-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="5ed46-110">لتعيين رقم وحدة التشغيل (OUN) للقناة إلى موقع تم نسخه حديثًا في منشئ موقع Commerce، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="5ed46-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5ed46-111">حدد الموقع المنسوخ حديثًا.</span><span class="sxs-lookup"><span data-stu-id="5ed46-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="5ed46-112">ضمن **إعدادات الموقع**، حدد **القنوات**.</span><span class="sxs-lookup"><span data-stu-id="5ed46-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="5ed46-113">بجوار اسم القناة، حدد علامة القطع (**...**)، ثم حدد **تغيير قناة المتجر على الإنترنت**.</span><span class="sxs-lookup"><span data-stu-id="5ed46-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="5ed46-114">في مربع الحوار **تغيير قناة المتجر على الإنترنت**، حدد القناة التي تريد تعيينها للموقع المنسوخ حديثًا، ثم حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="5ed46-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="5ed46-115">حدد **حفظ ونشر**.</span><span class="sxs-lookup"><span data-stu-id="5ed46-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5ed46-116">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="5ed46-116">Additional resources</span></span>

[<span data-ttu-id="5ed46-117">إقران موقع Dynamics 365 Commerce بقناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="5ed46-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)
