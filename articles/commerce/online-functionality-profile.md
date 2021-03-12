---
title: إنشاء ملف تعريف الوظائف عبر الإنترنت
description: يوضح هذا الموضوع كيفية إنشاء ملف تعريف وظائف على الإنترنت في Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1b0afeabfecb60672156692f3cd809445624020c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969966"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="7e562-103">إنشاء ملف تعريف الوظائف عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="7e562-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7e562-104">يقدم هذا الموضوع نظره عامه حول اعداد ملف تعريف الوظائف عبر الإنترنت لـ Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7e562-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7e562-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="7e562-105">Overview</span></span>

<span data-ttu-id="7e562-106">يوفر ملف تعريف الوظائف عبر الإنترنت الإعدادات المتنوعة المستخدمة للقنوات عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="7e562-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="7e562-107">يجب ان تحدد كل قناه عبر الإنترنت ملف تعريف وظائف عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="7e562-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="7e562-108">إنشاء ملف تعريف الوظائف عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="7e562-108">Create an online functionality profile</span></span>

<span data-ttu-id="7e562-109">يوضح الاجراء التالي كيفيه إنشاء ملف تعريف وظائف عبر الإنترنت من داخل تطبيق Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="7e562-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="7e562-110">في جزء التنقل، انتقل إلى **الوحدات \>إعداد القناة \> إعداد متجر على الإنترنت \> ملفات تعريف الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="7e562-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="7e562-111">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="7e562-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="7e562-112">في **ملف التعريف**، أدخل معرفًا لملف التعريف.</span><span class="sxs-lookup"><span data-stu-id="7e562-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="7e562-113">في حقل **الوصف**، ادخل قيمه ("ملف تعريف أعمال المغامرة" في صورة المثال أدناه).</span><span class="sxs-lookup"><span data-stu-id="7e562-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="7e562-114">في قسم **الوظائف**، قم بتعديل إعدادات **السلة** أو **عملاء RETAIL** أو **السحب**، حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="7e562-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="7e562-115">في جزء الإجراءات، حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="7e562-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="7e562-116">تعرض الصورة التالية مثالاً لملف تعريف الوظائف على الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="7e562-116">The following image shows an example online functionality profile.</span></span>
  
![مثال لملف تعريف الوظائف على الإنترنت](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="7e562-118">الوظائف</span><span class="sxs-lookup"><span data-stu-id="7e562-118">Functions</span></span>

- <span data-ttu-id="7e562-119">**تجميع المنتجات**: عند التمكين ، تسمح هذه الوظيفة لسله التسوق بتحديث الكمية التي تتم فيها أضافه نفس الصنف عده مرات.</span><span class="sxs-lookup"><span data-stu-id="7e562-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="7e562-120">**السماح بالسحب بدون مدفوعات**: عند التمكين ، تعالج هذه الدالة السيناريو عندما تكون الأصناف المضافة إلى السلة ذات سعر 0.00 دولار.</span><span class="sxs-lookup"><span data-stu-id="7e562-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="7e562-121">**إنشاء عميل في الوضع الغير متزامن**: يعد هذا اعداد قديم ينطبق علي قنوات التجارة الكترونيه للجهة الخارجية ولا يمكن تطبيقه علي موقع التجارة الكترونيه لـ Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7e562-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7e562-122">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="7e562-122">Additional resources</span></span>

[<span data-ttu-id="7e562-123">نظرة عامة على القنوات</span><span class="sxs-lookup"><span data-stu-id="7e562-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7e562-124">المتطلبات الأساسية‬ لإعداد قناة</span><span class="sxs-lookup"><span data-stu-id="7e562-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="7e562-125">إعداد قناة عبر الإنترنت</span><span class="sxs-lookup"><span data-stu-id="7e562-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="7e562-126">إعداد قناة بيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="7e562-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="7e562-127">إعداد قناة مركز اتصال</span><span class="sxs-lookup"><span data-stu-id="7e562-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)
