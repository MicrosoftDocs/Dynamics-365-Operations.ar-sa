---
title: الضمانات على الأصول وأنواع الأصول
description: يشرح هذا الموضوع كيفية إعداد الضمانات على الأصول وأنواع الأصول في إدارة الأصول.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3b13f8aba7e1d2448495f97a4772eb573e08c025
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874591"
---
# <a name="warranty-on-assets-and-asset-types"></a><span data-ttu-id="8ccc8-103">الضمان على الأصول وأنواع الأصول</span><span class="sxs-lookup"><span data-stu-id="8ccc8-103">Warranty on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="8ccc8-104">يشرح هذا الموضوع كيفية إعداد الضمانات على الأصول وأنواع الأصول في إدارة الأصول.</span><span class="sxs-lookup"><span data-stu-id="8ccc8-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="8ccc8-105">إعداد ضمان على نوع أصل</span><span class="sxs-lookup"><span data-stu-id="8ccc8-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="8ccc8-106">حدد **إدارة الأصول** \> **الإعداد** \> **أنواع الأصول** \> **أنواع الأصول**.</span><span class="sxs-lookup"><span data-stu-id="8ccc8-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="8ccc8-107">في الجزء الأيمن، حدد نوع الأصل لإرفاق اتفاقية ضمان المورّد به، ثم حدد **الإعدادات الافتراضية لنوع الأصل**.</span><span class="sxs-lookup"><span data-stu-id="8ccc8-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="8ccc8-108">على علامة التبويب السريعة **عام**، في حقل **ضمان المورّد**، حدد الاتفاقية.</span><span class="sxs-lookup"><span data-stu-id="8ccc8-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="8ccc8-109">إعداد ضمان على أصل</span><span class="sxs-lookup"><span data-stu-id="8ccc8-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="8ccc8-110">حدد **إدارة الأصول** \> **عام** \> **الأصول** \> **كل الأصول‏‎**.</span><span class="sxs-lookup"><span data-stu-id="8ccc8-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="8ccc8-111">حدد الأصل، ثم حدد **تحرير**.</span><span class="sxs-lookup"><span data-stu-id="8ccc8-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="8ccc8-112">على علامة التبويب السريعة **المورّد** في قسم **ضمان المورّد**، في حقل **المورّد**، حدد اتفاقية الضمان.</span><span class="sxs-lookup"><span data-stu-id="8ccc8-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="8ccc8-113">في الحقلين **بدء الضمان** و**انتهاء الضمان**، حدد تاريخي البدء والانتهاء.</span><span class="sxs-lookup"><span data-stu-id="8ccc8-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="8ccc8-114">إذا تم تحديد تاريخ في حقل **بدء الضمان** على أمر عملي، يصبح الضمان صالحًا لأمر العمل في ذلك التاريخ.</span><span class="sxs-lookup"><span data-stu-id="8ccc8-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="8ccc8-115">عند إنشاء أمر عمل، يتم تعيين حقل **بدء الضمان** بشكل تلقائي إلى تاريخ الإنشاء.</span><span class="sxs-lookup"><span data-stu-id="8ccc8-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="8ccc8-116">ومع ذلك، يمكنك تغيير التاريخ بحيث يتوافق مع تاريخ بدء اتفاقية الضمان، على سبيل المثال.</span><span class="sxs-lookup"><span data-stu-id="8ccc8-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![الشكل 1](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="8ccc8-118">إذا أنشأت أمر عمل لأصل يغطيه ضمان المورّد، وفي حال وجود تاريخ بدء متوقع لأمر العمل خلال فترة الضمان، ستتلقى إشعارًا حول اتفاقية الضمان.</span><span class="sxs-lookup"><span data-stu-id="8ccc8-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="8ccc8-119">يمكنك عندئذٍ إلغاء أمر العمل، كما هو مطلوب.</span><span class="sxs-lookup"><span data-stu-id="8ccc8-119">You can then cancel the work order, as you require.</span></span>
