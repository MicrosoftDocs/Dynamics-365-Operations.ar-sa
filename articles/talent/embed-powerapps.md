---
title: تضمين تطبيقات Power Apps في Dynamics 365 Human Resources
description: يشرح هذا المقال كيفية حل هذه المشكلة التي يختفي فيها عنصر قائمة Microsoft Power Apps من الوحدة النمطية "إدارة النظام".
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
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017863"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a><span data-ttu-id="932cc-103">تضمين تطبيقات Power Apps في Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="932cc-103">Embed Power Apps apps in Dynamics 365 Human Resources</span></span>

<span data-ttu-id="932cc-104">**إصدار**</span><span class="sxs-lookup"><span data-stu-id="932cc-104">**Issue**</span></span>

<span data-ttu-id="932cc-105">اختفى عنصر قائمة **Power Apps** من الوحدة النمطية **إدارة النظام**.</span><span class="sxs-lookup"><span data-stu-id="932cc-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="932cc-106">**السبب**</span><span class="sxs-lookup"><span data-stu-id="932cc-106">**Cause**</span></span>

<span data-ttu-id="932cc-107">تم تغيير تصميم واجهة المستخدم، وتم الآن تضمين Microsoft Power Apps في نموذج التخصيص القياسي.</span><span class="sxs-lookup"><span data-stu-id="932cc-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="932cc-108">**الدقة**</span><span class="sxs-lookup"><span data-stu-id="932cc-108">**Resolution**</span></span>

<span data-ttu-id="932cc-109">تم تغيير الطريقة التي يتم من خلالها تضمين Power Apps.</span><span class="sxs-lookup"><span data-stu-id="932cc-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="932cc-110">تمت الآن إضافة Power Apps من خلال نموذج التخصيص.</span><span class="sxs-lookup"><span data-stu-id="932cc-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="932cc-111">يمكنك إضافة Power Apps إلى معظم الصفحات تقريبًا في Microsoft Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="932cc-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="932cc-112">للحصول على معلومات تفصيلية حول كيفية تضمين Power Apps في Talent، راجع [تضمين Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="932cc-112">For information about how to embed Power Apps in Talent, see [Embed Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="932cc-113">يجب أن تتم ترقية أي عميل Power Apps قام بتضمين التطبيقات قبل التغيير إلى النموذج الجديد.</span><span class="sxs-lookup"><span data-stu-id="932cc-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="932cc-114">يقع زر **Power Apps** في الزاوية اليسرى العليا في كل صفحة من صفحات Talent تقريبًا.</span><span class="sxs-lookup"><span data-stu-id="932cc-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="932cc-115">يمكنك استخدام هذا الزر لإدراج تطبيقات.</span><span class="sxs-lookup"><span data-stu-id="932cc-115">You can use this button to insert apps.</span></span>

<span data-ttu-id="932cc-116">فيما يلي مثال على ذلك.</span><span class="sxs-lookup"><span data-stu-id="932cc-116">Here is an example.</span></span>

1. <span data-ttu-id="932cc-117">انتقل إلى **إدارة العاملين \> الارتباطات \> العاملون \> الموظفون**.</span><span class="sxs-lookup"><span data-stu-id="932cc-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="932cc-118">حدد الزر **Power Apps**، ثم حدد **إضافة تطبيق من Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="932cc-118">Select the **Power Apps** button, and then select **Add an app from Power Apps**.</span></span>

    ![زر Power Apps](media/png.png)

3. <span data-ttu-id="932cc-120">أكمل الحقول في مربع الحوار **إضافة تطبيق من Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="932cc-120">Complete the fields in the **Add an app from Power Apps** dialog box.</span></span>

    ![مربع الحوار إضافة تطبيق من Power Apps](media/insert-powerapp.png)

<span data-ttu-id="932cc-122">بدلًا من ذلك، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="932cc-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="932cc-123">في جزء الإجراءات بالصفحة، في علامة التبويب **الخيارات**، في مجموعة **تخصيص**، حدد **تخصيص هذه الصفحة**</span><span class="sxs-lookup"><span data-stu-id="932cc-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this page**.</span></span>

    ![تخصيص مجموعة في علامة التبويب خيارات](media/options.png)

    <span data-ttu-id="932cc-125">يظهر شريط أدوات التخصيص.</span><span class="sxs-lookup"><span data-stu-id="932cc-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="932cc-126">في شريط الأدوات، حدد **إضافة تطبيق من Power Apps**.</span><span class="sxs-lookup"><span data-stu-id="932cc-126">On the toolbar, select **Add an app from Power Apps**.</span></span>

    ![إضافة تطبيق من Power Apps باستخدام شريط أدوات التخصيص](media/powerapp-bar.png)
