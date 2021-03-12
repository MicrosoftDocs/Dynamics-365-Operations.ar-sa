---
title: إنشاء ملف تعريف وظائف البيع بالتجزئة
description: يوضح هذا الموضوع كيفية إنشاء ملف تعريف وظائف في Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: a53fc77a7d457534428929bd431175be7cf450f7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979637"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="8363e-103">إنشاء ملف تعريف وظائف البيع بالتجزئة</span><span class="sxs-lookup"><span data-stu-id="8363e-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8363e-104">يوضح هذا الموضوع كيفية إنشاء ملف تعريف وظائف في Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8363e-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8363e-105">نظرة عامة</span><span class="sxs-lookup"><span data-stu-id="8363e-105">Overview</span></span>

<span data-ttu-id="8363e-106">يوفر ملف تعريف التجارة الإعدادات المتنوعة المستخدمة للقنوات عبر الإنترنت.</span><span class="sxs-lookup"><span data-stu-id="8363e-106">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="8363e-107">يجب أن تحدد كل قناه ملف تعريف وظائف.</span><span class="sxs-lookup"><span data-stu-id="8363e-107">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="8363e-108">إنشاء ملف تعريف وظائف</span><span class="sxs-lookup"><span data-stu-id="8363e-108">Create a functionality profile</span></span>

<span data-ttu-id="8363e-109">لإنشاء ملف تعريف وظائف اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="8363e-109">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="8363e-110">في جزء التنقل، انتقل إلى **الوحدات \>إعداد القناة \> ملفات تعريف نقطة البيع \> ملفات تعريف الوظائف**.</span><span class="sxs-lookup"><span data-stu-id="8363e-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="8363e-111">في جزء الإجراءات، حدد **جديد**.</span><span class="sxs-lookup"><span data-stu-id="8363e-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="8363e-112">في حقل **ملف التعريف**، ادخل معرفا لملف التعريف ("FN006" في المثال التالي من الصورة أدناه).</span><span class="sxs-lookup"><span data-stu-id="8363e-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="8363e-113">في حقل **الوصف**، ادخل قيمه ("ملف تعريف أعمال المغامرة" في صورة المثال أدناه).</span><span class="sxs-lookup"><span data-stu-id="8363e-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="8363e-114">في قسم **عام**، حدد بلدا للإعدادات المحلية **ISO**.</span><span class="sxs-lookup"><span data-stu-id="8363e-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="8363e-115">في قسم **عام**، قم بتعديل الإعدادات الأخرى حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="8363e-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="8363e-116">في قسم **عام**، حدد **معرف ملف تعريف الاستلام**  لإيصالات استلام البريد الكتروني.</span><span class="sxs-lookup"><span data-stu-id="8363e-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="8363e-117">في قسم **الوظائف**، قم بتعديل الإعدادات حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="8363e-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="8363e-118">في قسم **المبلغ**، قم بتعديل الإعدادات حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="8363e-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="8363e-119">في قسم **أكواد المعلومات**، قم بتعديل الإعدادات حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="8363e-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="8363e-120">في قسم **ترقيم الإيصال**، قم بتعديل الإعدادات حسب الحاجة.</span><span class="sxs-lookup"><span data-stu-id="8363e-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="8363e-121">تعرض الصورة التالية مثالاً لملف تعريف الوظائف.</span><span class="sxs-lookup"><span data-stu-id="8363e-121">The following image shows an example functionality profile.</span></span>
  
![مثال لملف تعريف وظائف](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="8363e-123">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="8363e-123">Additional resources</span></span>

[<span data-ttu-id="8363e-124">أكواد المعلومات ومجموعات أكواد المعلومات</span><span class="sxs-lookup"><span data-stu-id="8363e-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="8363e-125">إنشاء دفتر عناوين جديد</span><span class="sxs-lookup"><span data-stu-id="8363e-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="8363e-126">نظرة عامة على تخطيط الشاشة</span><span class="sxs-lookup"><span data-stu-id="8363e-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="8363e-127">تكوين Retail Hardware Station وتثبيتها</span><span class="sxs-lookup"><span data-stu-id="8363e-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 
