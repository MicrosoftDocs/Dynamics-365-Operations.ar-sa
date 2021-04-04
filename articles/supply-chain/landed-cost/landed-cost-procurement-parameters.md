---
title: معلمات الشراء وتحديد الموارد للتكلفة المستلمة
description: يوضح هذا الموضوع كيفيه إعداد معلمات الشراء والتوريد ذات الصلة عند استخدام وحدة التكلفة المستلمة.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 49e046a1437917cfa866f690511789496fac2c53
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500732"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="f8ae3-103">معلمات الشراء وتحديد الموارد للتكلفة المستلمة</span><span class="sxs-lookup"><span data-stu-id="f8ae3-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f8ae3-104">تحتوي صفحة **معلمات الشراء وتحديد الموارد** على إعدادات قليلة ذات صلة خاصة عند استخدامك وحدة **التكلفة المستلمة**.</span><span class="sxs-lookup"><span data-stu-id="f8ae3-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="f8ae3-105">استخدم مربع الحوار **تحديث بنود الأمر** الذي يتم فتحه من صفحة **معلمات الشراء وتحديد الموارد** لتحديد ما إذا كان يجب تحديث بنود أمر الشراء تلقائيًا عند إجراء تغييرات على رأس أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="f8ae3-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="f8ae3-106">لإكمال هذا الإعداد، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="f8ae3-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="f8ae3-107">انتقل إلى **التدبير والتوريد‬ \> الإعداد \> معلمات التدبير والتوريد**.</span><span class="sxs-lookup"><span data-stu-id="f8ae3-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="f8ae3-108">في علامة التبويب **عام**، حدد الارتباط **تحديث بنود الأمر**.</span><span class="sxs-lookup"><span data-stu-id="f8ae3-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="f8ae3-109">يسرد مربع الحوار **تحديث بنود الأمر** الحقول في البيانات الرئيسية للأمر والتي يمكنها أيضا تطبيق تحديثات تلقائية علي الحقول المرتبطة في بنود الأمر.</span><span class="sxs-lookup"><span data-stu-id="f8ae3-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="f8ae3-110">قم بتعيين كل حقل في القائمة إلى إحدى القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="f8ae3-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="f8ae3-111">**دائمًا** – يجب تحديث بنود الأوامر تلقائياً عند تحديث البيانات الرئيسية للأمر.</span><span class="sxs-lookup"><span data-stu-id="f8ae3-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="f8ae3-112">**أبدًا** – يجب ألا يتم تحديث بنود الأوامر عند تحديث البيانات الرئيسية للأمر.</span><span class="sxs-lookup"><span data-stu-id="f8ae3-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="f8ae3-113">**المطالبة** – ستتم مطالبة المستخدم بتحديد ما إذا كان يجب تحديث بنود الأمر أو لا.</span><span class="sxs-lookup"><span data-stu-id="f8ae3-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
