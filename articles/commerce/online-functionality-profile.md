---
title: إنشاء ملف تعريف الوظائف عبر الإنترنت
description: يوضح هذا الموضوع كيفية إنشاء ملف تعريف وظائف على الإنترنت في Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: be78b92858979b8bb009a4699eff96379ef7cef3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791092"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="759b3-103">إنشاء ملف تعريف وظائف على الإنترنت</span><span class="sxs-lookup"><span data-stu-id="759b3-103">Create an online functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="759b3-104">يقدم هذا الموضوع نظرة عامة حول اعداد ملف تعريف الوظائف عبر الإنترنت لـ Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="759b3-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="759b3-105">يوفر ملف تعريف الوظائف عبر الإنترنت الإعدادات المتنوعة المستخدمة للقنوات عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="759b3-105">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="759b3-106">يجب ان تحدد كل قناه عبر الإنترنت ملف تعريف وظائف عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="759b3-106">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="759b3-107">إنشاء ملف تعريف الوظائف عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="759b3-107">Create an online functionality profile</span></span>

<span data-ttu-id="759b3-108">يوضح الاجراء التالي كيفيه إنشاء ملف تعريف وظائف عبر الإنترنت من داخل تطبيق Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="759b3-108">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="759b3-109">في جزء التنقل، انتقل إلى **الوحدات \>إعداد القناة \> إعداد متجر على الإنترنت \> ملفات تعريف الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="759b3-109">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="759b3-110">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="759b3-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="759b3-111">في **ملف التعريف**، أدخل معرفًا لملف التعريف.</span><span class="sxs-lookup"><span data-stu-id="759b3-111">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="759b3-112">في حقل **الوصف**، ادخل قيمه ("ملف تعريف أعمال المغامرة" في صورة المثال أدناه).</span><span class="sxs-lookup"><span data-stu-id="759b3-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="759b3-113">في قسم **الوظائف**، قم بتعديل إعدادات **السلة** أو **عملاء RETAIL** أو **السحب**، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="759b3-113">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="759b3-114">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="759b3-114">On the action pane, select **Save**.</span></span>

<span data-ttu-id="759b3-115">تعرض الصورة التالية مثالاً لملف تعريف الوظائف على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="759b3-115">The following image shows an example online functionality profile.</span></span>
  
![مثال لملف تعريف الوظائف على الإنترنت](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="759b3-117">الوظائف</span><span class="sxs-lookup"><span data-stu-id="759b3-117">Functions</span></span>

- <span data-ttu-id="759b3-118">**تجميع المنتجات**: عند التمكين ، تسمح هذه الوظيفة لسله التسوق بتحديث الكمية التي تتم فيها أضافه نفس الصنف عده مرات.</span><span class="sxs-lookup"><span data-stu-id="759b3-118">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="759b3-119">**السماح بالسحب بدون مدفوعات**: عند التمكين ، تعالج هذه الدالة السيناريو عندما تكون الأصناف المضافة إلى السلة ذات سعر 0.00 دولار.</span><span class="sxs-lookup"><span data-stu-id="759b3-119">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="759b3-120">**إنشاء عميل في الوضع الغير متزامن**: يعد هذا اعداد قديم ينطبق علي قنوات التجارة الكترونيه للجهة الخارجية ولا يمكن تطبيقه علي موقع التجارة الكترونيه لـ Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="759b3-120">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="759b3-121">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="759b3-121">Additional resources</span></span>

[<span data-ttu-id="759b3-122">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="759b3-122">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="759b3-123">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="759b3-123">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="759b3-124">إعداد قناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="759b3-124">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="759b3-125">إعداد قناة بيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="759b3-125">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="759b3-126">إعداد قناة مركز اتصال</span><span class="sxs-lookup"><span data-stu-id="759b3-126">Set up a call center channel</span></span>](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
