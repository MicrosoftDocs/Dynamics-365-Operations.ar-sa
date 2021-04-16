---
title: معلمات الشراء وتحديد الموارد للتكلفة المستلمة
description: يوضح هذا الموضوع كيفيه إعداد معلمات الشراء والتوريد ذات الصلة عند استخدام وحدة التكلفة المستلمة.
author: sherry-zheng
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
ms.openlocfilehash: df91fcb97794be32924707fcecf2b5fb34844596
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833919"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="95b62-103">معلمات الشراء وتحديد الموارد للتكلفة المستلمة</span><span class="sxs-lookup"><span data-stu-id="95b62-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="95b62-104">تحتوي صفحة **معلمات الشراء وتحديد الموارد** على إعدادات قليلة ذات صلة خاصة عند استخدامك وحدة **التكلفة المستلمة**.</span><span class="sxs-lookup"><span data-stu-id="95b62-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="95b62-105">استخدم مربع الحوار **تحديث بنود الأمر** الذي يتم فتحه من صفحة **معلمات الشراء وتحديد الموارد** لتحديد ما إذا كان يجب تحديث بنود أمر الشراء تلقائيًا عند إجراء تغييرات على رأس أمر الشراء.</span><span class="sxs-lookup"><span data-stu-id="95b62-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="95b62-106">لإكمال هذا الإعداد، اتبع الخطوات التالية.</span><span class="sxs-lookup"><span data-stu-id="95b62-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="95b62-107">انتقل إلى **التدبير والتوريد‬ \> الإعداد \> معلمات التدبير والتوريد**.</span><span class="sxs-lookup"><span data-stu-id="95b62-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="95b62-108">في علامة التبويب **عام**، حدد الارتباط **تحديث بنود الأمر**.</span><span class="sxs-lookup"><span data-stu-id="95b62-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="95b62-109">يسرد مربع الحوار **تحديث بنود الأمر** الحقول في البيانات الرئيسية للأمر والتي يمكنها أيضا تطبيق تحديثات تلقائية علي الحقول المرتبطة في بنود الأمر.</span><span class="sxs-lookup"><span data-stu-id="95b62-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="95b62-110">قم بتعيين كل حقل في القائمة إلى إحدى القيم التالية:</span><span class="sxs-lookup"><span data-stu-id="95b62-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="95b62-111">**دائمًا** – يجب تحديث بنود الأوامر تلقائياً عند تحديث البيانات الرئيسية للأمر.</span><span class="sxs-lookup"><span data-stu-id="95b62-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="95b62-112">**أبدًا** – يجب ألا يتم تحديث بنود الأوامر عند تحديث البيانات الرئيسية للأمر.</span><span class="sxs-lookup"><span data-stu-id="95b62-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="95b62-113">**المطالبة** – ستتم مطالبة المستخدم بتحديد ما إذا كان يجب تحديث بنود الأمر أو لا.</span><span class="sxs-lookup"><span data-stu-id="95b62-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
