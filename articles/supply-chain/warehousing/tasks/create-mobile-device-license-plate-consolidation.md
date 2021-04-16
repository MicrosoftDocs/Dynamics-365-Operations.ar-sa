---
title: إنشاء عنصر في قائمة الجهاز المحمول لدمج لوحة الترخيص
description: يوضح هذا الإجراء كيفية إنشاء عنصر قائمة جهاز محمول لعمل خاص بدمج لوحة الترخيص.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1dfb0bb2db5690a966d70f96a3bba2d60833abd4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830992"
---
# <a name="create-a-mobile-device-menu-item-for-license-plate-consolidation"></a><span data-ttu-id="65960-103">إنشاء عنصر في قائمة الجهاز المحمول لدمج لوحة الترخيص</span><span class="sxs-lookup"><span data-stu-id="65960-103">Create a mobile device menu item for license plate consolidation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="65960-104">يوضح هذا الإجراء كيفية إنشاء عنصر قائمة جهاز محمول لعمل خاص بدمج لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="65960-104">This procedure shows you how to create a mobile device menu item for license plate consolidation work.</span></span> <span data-ttu-id="65960-105">يتيح ذلك للعاملين في المستودع دمج الأصناف في لوحة ترخيص واحدة مع الأصناف الموجودة على لوحة ترخيص أخرى داخل الموقع نفسه.</span><span class="sxs-lookup"><span data-stu-id="65960-105">This enables warehouse workers to consolidate items on one license plate with items on another license place within the same location.</span></span> <span data-ttu-id="65960-106">على سبيل المثال، باستطاعة العاملين استخدام هذا الإجراء إذا كانت الخطوات المرحلية اللاحقة هي نفسها على أمري العمل، بحيث يجب تنفيذ العمل مرة واحدة فقط للعناصر المدمجة.</span><span class="sxs-lookup"><span data-stu-id="65960-106">For example, they might use this if subsequent staging steps were the same on both work orders, so that the work only needs to be performed once for the merged items.</span></span> <span data-ttu-id="65960-107">يمكنك تنفيذ هذا الإجراء في شركة بيانات العرض التوضيحي USMF.</span><span class="sxs-lookup"><span data-stu-id="65960-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="65960-108">وعادة ما تُنفذ هذه المهمة عن طريق مدير مستودع.</span><span class="sxs-lookup"><span data-stu-id="65960-108">The task would typically be carried out by a warehouse manager.</span></span> <span data-ttu-id="65960-109">يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.</span><span class="sxs-lookup"><span data-stu-id="65960-109">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

1. <span data-ttu-id="65960-110">انتقل إلى إدارة المستودعات > إعداد > الجهاز المحمول > عناصر قائمة الجهاز المحمول.</span><span class="sxs-lookup"><span data-stu-id="65960-110">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="65960-111">انقر فوق "جديد".</span><span class="sxs-lookup"><span data-stu-id="65960-111">Click New.</span></span>
3. <span data-ttu-id="65960-112">في الحقل "اسم عنصر القائمة‬"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="65960-112">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="65960-113">في الحقل "المسمى الوظيفي"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="65960-113">In the Title field, type a value.</span></span>
5. <span data-ttu-id="65960-114">في الحقل "الوضع"، حدد "غير مباشر".</span><span class="sxs-lookup"><span data-stu-id="65960-114">In the Mode field, select 'Indirect'.</span></span>
6. <span data-ttu-id="65960-115">في حقل "كود النشاط"، حدد "دمج لوحات الترخيص".</span><span class="sxs-lookup"><span data-stu-id="65960-115">In the Activity code field, select 'Consolidate license plates'.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]