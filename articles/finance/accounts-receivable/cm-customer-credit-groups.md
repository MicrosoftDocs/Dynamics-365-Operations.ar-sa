---
title: مجموعات ائتمان العملاء
description: يوفر هذا الموضوع معلومات حول مجموعات ائتمان العملاء.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f7121b78f3318bae9f82b2f0f951bc7bfe6c4358
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015101"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="ae33e-103">مجموعات ائتمان العملاء</span><span class="sxs-lookup"><span data-stu-id="ae33e-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="ae33e-104">يمكنك تحديد مجموعات من العملاء لديهم الحد الائتماني نفسه.</span><span class="sxs-lookup"><span data-stu-id="ae33e-104">You can define groups of customers who have the same credit limit.</span></span> <span data-ttu-id="ae33e-105">وتتم أيضًا مراعاة الحد الائتماني الفردي المحدد في حساب فاتورة العميل.</span><span class="sxs-lookup"><span data-stu-id="ae33e-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="ae33e-106">يمكن تحديد أعضاء مجموعة ائتمان العملاء من كيانات قانونية مختلفة.</span><span class="sxs-lookup"><span data-stu-id="ae33e-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="ae33e-107">عند إضافة عميل إلى قائمة العملاء في مجموعة ائتمان العملاء، يتغير تاريخ انتهاء صلاحية الحد الائتماني لكل عميل إلى تاريخ انتهاء الصلاحية المعين للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="ae33e-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="ae33e-108">يمكنك إعداد مجموعات ائتمان العملاء في صفحة **مجموعات ائتمان العملاء** (**إدارة الائتمان \> مجموعات ائتمان العملاء \> مجموعات ائتمان العملاء**).</span><span class="sxs-lookup"><span data-stu-id="ae33e-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="ae33e-109">في الحقلين‏‎ **رقم المجموعة** و**الوصف**، أدخل معرفًا ووصفًا للمجموعة.</span><span class="sxs-lookup"><span data-stu-id="ae33e-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="ae33e-110">في الحقلين‏‎ **الحد الائتماني** و**العملة**، أدخل الحد الائتماني‏‎ والعملة التي ينبغي استخدامها عندما يتحقق النظام من الحد الائتماني لأي عضو في المجموعة.</span><span class="sxs-lookup"><span data-stu-id="ae33e-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="ae33e-111">في الحقل **حد ائتماني حتى تاريخ**، أدخل التاريخ الذي تنتهي فيه صلاحية الحد الائتماني.</span><span class="sxs-lookup"><span data-stu-id="ae33e-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="ae33e-112">يجب تعيين تاريخ انتهاء صلاحية لمجموعات ائتمان العملاء.</span><span class="sxs-lookup"><span data-stu-id="ae33e-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="ae33e-113">بعد الانتهاء من إعداد مجموعة ائتمان العملاء، يمكنك إضافة العملاء إليها عن طريق تحديد كيانهم القانوني ومعرف حساب العميل الخاص بكل واحد منهم.</span><span class="sxs-lookup"><span data-stu-id="ae33e-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="ae33e-114">عند إضافة عميل جديد إلى مجموعة ائتمان العملاء، يبحث النظام عن العميل نفسه عبر جميع الكيانات القانونية ويطالبك بإضافته إلى مجموعة ائتمان العملاء.</span><span class="sxs-lookup"><span data-stu-id="ae33e-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="ae33e-115">استخدم قائمة **الأرصدة القديمة‬** لعرض تفاصيل رصيد قديم لجميع فواتير العملاء في مجموعة ائتمان العملاء.</span><span class="sxs-lookup"><span data-stu-id="ae33e-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="ae33e-116">تعرض صفحة‏‎ **رصيد التقادم** ملخصًا للأرصدة القديمة الخاصة بحسابات عملاء الفواتير.</span><span class="sxs-lookup"><span data-stu-id="ae33e-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>
