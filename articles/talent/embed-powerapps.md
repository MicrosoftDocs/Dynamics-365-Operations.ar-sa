---
title: تضمين تطبيقات PowerApps في Dynamics 365‏ - Core HR
description: يشرح هذا المقال كيفية حل هذه المشكلة التي يختفي فيها عنصر قائمة PowerApps من الوحدة النمطية "إدارة النظام".
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b510c10ebfcf4939eb2e1297972d27aa1812ae5a
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550993"
---
# <a name="embed-powerapps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="71574-103">تضمين تطبيقات PowerApps في Dynamics 365‏ - Core HR</span><span class="sxs-lookup"><span data-stu-id="71574-103">Embed PowerApps apps in Dynamics 365 - Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="71574-104">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="71574-104">**Issue**</span></span>

<span data-ttu-id="71574-105">اختفى عنصر قائمة **PowerApps** من الوحدة النمطية **إدارة النظام**.</span><span class="sxs-lookup"><span data-stu-id="71574-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="71574-106">**السبب**</span><span class="sxs-lookup"><span data-stu-id="71574-106">**Cause**</span></span>

<span data-ttu-id="71574-107">تم تغيير تصميم واجهة المستخدم، وتم الآن تضمين Microsoft PowerApps في نموذج التخصيص القياسي.</span><span class="sxs-lookup"><span data-stu-id="71574-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="71574-108">**الدقة**</span><span class="sxs-lookup"><span data-stu-id="71574-108">**Resolution**</span></span>

<span data-ttu-id="71574-109">تم تغيير الطريقة التي يتم من خلالها تضمين تطبيقات PowerApps.</span><span class="sxs-lookup"><span data-stu-id="71574-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="71574-110">تمت الآن إضافة تطبيقات PowerApps من خلال نموذج التخصيص.</span><span class="sxs-lookup"><span data-stu-id="71574-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="71574-111">يمكنك إضافة تطبيقات PowerApps إلى معظم الصفحات تقريبًا في Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="71574-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="71574-112">للحصول على معلومات تفصيلية حول كيفية تضمين تطبيقات PowerApps في Talent، راجع [تضمين تطبيقات PowerApps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="71574-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="71574-113">يجب أن تتم ترقية أي عميل PowerApps قام بتضمين التطبيقات قبل التغيير إلى النموذج الجديد.</span><span class="sxs-lookup"><span data-stu-id="71574-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="71574-114">يقع زر **PowerApps** في الزاوية اليسرى العليا في كل صفحة من صفحات Talent تقريبًا.</span><span class="sxs-lookup"><span data-stu-id="71574-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="71574-115">يمكنك استخدام هذا الزر لإدراج تطبيق PowerApps.</span><span class="sxs-lookup"><span data-stu-id="71574-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="71574-116">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="71574-116">Here is an example.</span></span>

1. <span data-ttu-id="71574-117">انتقل إلى **إدارة العاملين \> الارتباطات \> العاملون \> الموظفون**.</span><span class="sxs-lookup"><span data-stu-id="71574-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="71574-118">حدد زر **PowerApps**، ثم حدد **إدراج PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="71574-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![زر PowerApps](media/png.png)

3. <span data-ttu-id="71574-120">أكمل الحقول في مربع حوار **إدراج PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="71574-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![إدراج مربع حوار PowerApp](media/insert-powerapp.png)

<span data-ttu-id="71574-122">بدلًا من ذلك، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="71574-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="71574-123">في صفحة جزء الإجراءات، في علامة التبويب **خيارات**، في مجموعة **تخصيص**، حدد **تخصيص هذا النموذج**</span><span class="sxs-lookup"><span data-stu-id="71574-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![تخصيص مجموعة في علامة التبويب خيارات](media/options.png)

    <span data-ttu-id="71574-125">يظهر شريط أدوات التخصيص.</span><span class="sxs-lookup"><span data-stu-id="71574-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="71574-126">على شريط الأدوات، حدد **إدراج \> PowerApp**.</span><span class="sxs-lookup"><span data-stu-id="71574-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![إدراج تطبيق PowerApps باستخدام شريط أدوات التخصيص](media/powerapp-bar.png)
